---
name: doc-nav-factory
description: Documentation Navigator skill factory. Analyzes any documentation folder and generates a complete Documentation Navigator skill. Creates skills that enable surgical, context-efficient documentation access. Supports nested folder structures, auto-detects domains, and section markers. CRITICAL FEATURE - Content-based outlier detection using heading structure analysis, NOT filename patterns. Detects guides, configuration docs, troubleshooting docs, and other non-standard content even when filenames match standard patterns.
allowed-tools: Read, Grep, Glob, Bash, Write, AskUserQuestion
---

# Documentation Navigator Factory

This skill analyzes a documentation folder and generates a complete Documentation Navigator skill following the agentskills.io specification.

**Key capability:** Content-based outlier detection. Files are classified as outliers based on their **heading structure**, not their filenames. A file like `s3-as-pulumi-backend.md` will be correctly identified as a configuration guide (outlier) even though its filename matches the `<service>-<resource>.md` pattern.

---

## Input

The user provides a path to a documentation folder. This folder:
- May contain nested subdirectories
- Contains text files (`.md`, `.txt`)
- Can be any size (warning issued if > 100MB)

---

## Process Overview

Execute these phases in order:

### Phase 1: Structural Analysis
### Phase 2: Content Analysis (Tiered Sampling)
### Phase 3: Pattern Detection & Outlier Identification
### Phase 4: Strategy Selection
### Phase 5: Name Suggestion + User Confirmation
### Phase 6: Generate SKILL.md (Two-Tier Architecture)
### Phase 7: Generate file-index.md (if needed)
### Phase 8: Copy Documentation

---

## Phase 1: Structural Analysis

Gather structural metadata about the documentation folder.

### 1.1 Count Files and Calculate Size

```bash
# Count documentation files
find "<source_folder>" -type f \( -name "*.md" -o -name "*.txt" \) | wc -l

# Calculate total size
du -sh "<source_folder>"

# List folder structure (top 2 levels)
find "<source_folder>" -type d -maxdepth 2
```

### 1.2 Map Folder Hierarchy

Identify:
- Top-level folders (potential domains)
- Nesting depth
- File distribution across folders

### 1.3 Check Size Threshold

If total size > 100MB:
- **Continue with the work** (do not stop)
- **Print warning** to user with this message:

```
WARNING: Documentation exceeds 100MB

This is a large documentation set. Potential issues:
1. The generated skill folder will be large (affects version control)
2. Full analysis will take longer
3. The navigator may need to be more pattern-based than explicit

Suggestions:
- Consider splitting documentation into separate domain-specific skills
- Remove generated/duplicate content before processing
- Archive old/deprecated documentation separately
- If this is API reference, consider keeping only current version

Proceeding with analysis...
```

---

## Phase 2: Content Analysis (Tiered Sampling)

Perform content analysis using a tiered approach based on file count. **Priority: accuracy over speed.**

### 2.1 Extract ALL Headings (Cheap - Do For Every File)

This is a low-cost operation that reveals structure across the entire doc set:

```bash
# Extract all ## headings with file names
grep -rh "^## " "<source_folder>" --include="*.md" | sort | uniq -c | sort -rn > /tmp/heading-patterns.txt

# Extract all ### headings
grep -rh "^### " "<source_folder>" --include="*.md" | sort | uniq -c | sort -rn > /tmp/subheading-patterns.txt
```

### 2.2 Tiered File Sampling

Based on file count, determine sampling strategy:

| File Count | Sampling Strategy |
|------------|-------------------|
| < 30 files | Read first 40 lines of ALL files (use parallel Read calls) |
| 30-100 files | Read first 30 lines of ALL files in batches of 15 |
| > 100 files | Read first 30 lines of 30 representative samples + rely on headings |

**Parallel Read Pattern** (for efficiency):
- Issue multiple Read tool calls in a single message
- Example: Read 10-15 files simultaneously, then next batch

### 2.3 Extract Per-File Metadata

For each sampled file, extract:
- **Title**: Usually line 1-3 (first `#` heading)
- **Description**: First paragraph after title
- **Key Topics**: From `##` and `###` headings
- **Keywords**: Technical terms, product names, action verbs

Store in working memory for later phases.

### 2.4 Identify Domains

Domains are determined by:
- Top-level folders in the documentation
- Distinct topic clusters detected from headings
- Separate product areas

For each domain, note:
- Folder path
- File count
- Key topics
- Relationship to other domains

---

## Phase 3: Content-Based Outlier Detection

**This phase is critical for ensuring no files are missed. Outlier detection MUST be content-based, not filename-based.**

A file is an outlier if its **content structure** differs from the dominant document type, regardless of whether its filename matches a pattern. For example, `s3-as-pulumi-backend.md` might look like a resource doc by filename, but its content (configuration guide) makes it an outlier.

### 3.1 Detect Filename Patterns (Secondary Signal Only)

Analyze filenames to understand naming conventions, but **do not use this for outlier detection**:

```bash
# List all file names for pattern analysis
find "<source_folder>" -type f -name "*.md" -exec basename {} \; | sort > /tmp/filenames.txt
```

Document the pattern for the generated skill's "File Naming Convention" section, but proceed to content-based analysis for outlier detection.

### 3.2 Build Heading Vocabulary (All Files)

Extract ALL headings from ALL files to build a complete vocabulary:

```bash
# Extract all H2 headings with their source files
grep -rn "^## " "<source_folder>" --include="*.md" > /tmp/h2-by-file.txt

# Count H2 heading frequencies
grep -rh "^## " "<source_folder>" --include="*.md" | sed 's/^## //' | sort | uniq -c | sort -rn > /tmp/h2-frequency.txt

# Extract all H3 headings with frequencies
grep -rh "^### " "<source_folder>" --include="*.md" | sed 's/^### //' | sort | uniq -c | sort -rn > /tmp/h3-frequency.txt
```

### 3.3 Identify Dominant Content Profile

From the heading frequency analysis, identify the **dominant heading set** - headings that appear in >15% of files. These represent the "standard" document structure.

**Example dominant heading set (API reference docs):**
```
## Example Usage         (appears in 95% of files)
## Import                (appears in 90% of files)
## Inputs                (appears in 85% of files)
## Outputs               (appears in 85% of files)
## Supporting Types      (appears in 70% of files)
## Constructor syntax    (appears in 65% of files)
```

**Build a content profile by identifying:**
1. **Dominant H2 headings**: Headings appearing in >15% of files
2. **Dominant H3 headings**: Headings appearing in >10% of files
3. **Dominant first-paragraph patterns**: Common opening phrases ("This resource...", "The X function...")

### 3.4 Calculate Content Similarity Score

For EACH file, calculate how similar its content structure is to the dominant profile:

**Heading Overlap Score Formula:**
```
score = (file_headings ∩ dominant_headings) / file_headings_count
```

**Scoring process:**
1. Extract all H2 headings from the file
2. Count how many match the dominant heading set
3. Calculate percentage overlap

**Example calculations:**
```
ec2-instance.md:
  Headings: "Example Usage", "Import", "Inputs", "Outputs", "Supporting Types"
  Matches: 5/5 = 100% overlap → STANDARD FILE

s3-as-pulumi-backend.md:
  Headings: "Why Use S3 as Backend?", "S3 Bucket Setup", "Project Configuration",
            "Stack Naming Convention", "PULUMI_CONFIG_PASSPHRASE Requirement",
            "Stack References", "Package.json Scripts Pattern", "Backend Migration",
            "Troubleshooting", "Quick Reference"
  Matches: 0/10 = 0% overlap → OUTLIER

installation-guide.md:
  Headings: "Prerequisites", "Installation", "Configuration", "Verification", "Next Steps"
  Matches: 0/5 = 0% overlap → OUTLIER
```

### 3.5 Flag Content Outliers

**A file is a content outlier if its heading overlap score is <50%.**

This threshold catches:
- Files with completely different structure (0-20% overlap)
- Files with mixed content (20-50% overlap)

While allowing:
- Standard files with minor variations (50-100% overlap)

**Generate outlier list:**
```bash
# For each file, you'll need to programmatically:
# 1. Extract its headings
# 2. Compare against dominant heading set
# 3. Calculate overlap percentage
# 4. Flag if < 50%
```

### 3.6 Document Archetype Classification

Classify each outlier by its **document archetype** based on heading patterns and content signals:

| Archetype | Heading Signals | Content Signals |
|-----------|-----------------|-----------------|
| **Guide** | "Getting Started", "Prerequisites", "Step N", "How to", "Setup" | Numbered steps, sequential instructions |
| **Configuration** | "Configuration", "Settings", "Options", "Environment Variables", any `*_PASSPHRASE`, `*_CONFIG` | Key-value pairs, env vars, config files |
| **Troubleshooting** | "Troubleshooting", "Common Issues", "FAQ", "Errors", "Problems" | Error messages, solutions, Q&A format |
| **Migration** | "Migration", "Upgrade", "Moving from", "Breaking Changes" | Version comparisons, before/after |
| **Tutorial** | "Tutorial", "Walkthrough", "Building", "Creating" | Extended example, learning-focused |
| **Conceptual** | "Overview", "Introduction", "What is", "Why", "Architecture" | Explanatory, no code-heavy sections |
| **Reference (non-standard)** | "API", "Reference", "Methods", "Properties" but different structure | Tables, signatures, but different layout |
| **Index** | "Index", "Contents", "All", "List of" | Links, tables of contents |
| **Changelog** | "Changelog", "Release Notes", "Version", "What's New" | Dated entries, version numbers |

**For each outlier, assign the best-matching archetype based on:**
1. Presence of archetype-specific headings
2. First paragraph content analysis
3. Overall document structure

### 3.7 Deep Analysis of ALL Outliers

**For every identified outlier, read the first 50 lines regardless of total file count.**

Outliers are typically <5% of files, making this affordable. Extract:
- **Full title**: First H1 heading
- **Description**: First paragraph after title (2-3 sentences)
- **All H2 headings**: Complete list for the skill documentation
- **Keywords**: Technical terms, product names, configuration keys
- **Archetype**: From classification above

**Store outlier data in this format:**
```
File: s3-as-pulumi-backend.md
Archetype: Configuration/Guide
Title: Pulumi S3 Backend Configuration Guide
Description: Documents configuration details, naming conventions, and gotchas
             when using AWS S3 as a Pulumi backend instead of Pulumi Cloud.
Headings: Why Use S3 as Backend?, S3 Bucket Setup, Project Configuration,
          Stack Naming Convention, PULUMI_CONFIG_PASSPHRASE Requirement,
          Stack References, Backend Migration, Troubleshooting
Keywords: S3 backend, Pulumi state, PULUMI_CONFIG_PASSPHRASE, stack naming,
          cross-account access, backend migration, pulumi login
```

### 3.8 Validate No Outliers Missed

**Final validation step - check for edge cases:**

1. **Single-occurrence headings check:**
   ```bash
   # Find headings that appear only once - these files might be outliers
   grep -rh "^## " "<source_folder>" --include="*.md" | sort | uniq -c | grep "^\s*1 "
   ```
   Review files containing these unique headings.

2. **First paragraph anomaly check:**
   ```bash
   # Sample first paragraphs looking for non-standard openings
   # Standard: "This resource...", "The aws.X.Y function..."
   # Outlier: "This guide...", "Learn how to...", "When using..."
   ```

3. **File size anomaly check:**
   - Files significantly larger than average may be comprehensive guides
   - Files significantly smaller may be stubs or indexes

4. **Cross-reference with filename patterns:**
   - If a file has standard content but unusual filename → document in naming convention notes
   - If a file has unusual content but standard filename → **THIS IS THE CRITICAL CASE** - ensure it's in outlier list

### 3.9 Outlier Summary Output

After completing content analysis, produce a summary:

```
Content Analysis Complete
=========================
Total files analyzed: 687
Dominant content type: API Reference (resource documentation)
Dominant headings: Example Usage, Import, Inputs, Outputs, Supporting Types

Content Outliers Detected: 12 files (1.7%)

By Archetype:
- Configuration/Guide: 3 files
  • s3-as-pulumi-backend.md - Pulumi S3 backend configuration
  • docker-installation-configuration.md - Docker provider setup
  • aws-credentials-setup.md - AWS authentication guide

- Troubleshooting: 2 files
  • common-errors.md - Error resolution guide
  • debugging-guide.md - Debugging strategies

- Index: 4 files
  • ec2.md - EC2 service index
  • s3.md - S3 service index
  • iam.md - IAM service index
  • lambda.md - Lambda service index

- Migration: 1 file
  • terraform-migration.md - Migrating from Terraform

- Conceptual: 2 files
  • pulumi-concepts.md - Core Pulumi concepts
  • state-management.md - Understanding Pulumi state

All outliers will be explicitly listed in SKILL.md with full descriptions.
```

---

## Phase 4: Strategy Selection

Based on content analysis, select the navigation strategy.

### Decision Matrix

| File Count | Content Homogeneity | Outliers | Strategy |
|------------|---------------------|----------|----------|
| < 30 | Any | Any | Full explicit listing |
| 30-100 | High (>80% match dominant profile) | Few (<10) | Pattern + explicit outliers |
| 30-100 | Low (<80% match) | Many (>10) | Categorized explicit listing |
| > 100 | High (>85% match dominant profile) | Few (<20) | Pattern + explicit outliers + file-index |
| > 100 | Low (<85% match) | Many (>20) | Domain grouping + file-index |

**Content Homogeneity** = percentage of files whose heading structure matches the dominant content profile (from Phase 3.4).

### Strategy Descriptions

**Full Explicit Listing**
- Every file listed in SKILL.md with description
- No separate file-index needed
- Best for small doc sets

**Pattern + Explicit Outliers**
- Pattern-based navigation for standard files (those matching dominant profile)
- **ALL content outliers listed explicitly in SKILL.md "Non-Standard Documentation" section**
- Outliers grouped by archetype (Configuration, Troubleshooting, Migration, etc.)
- Outlier keywords added to skill description for semantic matching
- Optional file-index for large sets

**Categorized Explicit Listing**
- Files grouped by detected content categories/domains
- Each category listed in SKILL.md
- No pattern assumptions - all files treated as potentially unique

**Domain Grouping + File-Index**
- SKILL.md contains domain overview + ALL outliers explicitly listed
- file-index.md contains full catalog of standard files
- Required for > 100 files with diverse content types

### Critical Rule for ALL Strategies

**Regardless of strategy chosen, ALL content outliers MUST be:**
1. Explicitly listed in the "Non-Standard Documentation" section of SKILL.md
2. Grouped by archetype (Configuration, Troubleshooting, Migration, Conceptual, Index)
3. Include description and key topics/keywords
4. Have their keywords included in the skill's description field

---

## Phase 5: Name Suggestion + User Confirmation

### 5.1 Generate Name Suggestion

Based on content analysis, suggest a skill name that:
- Reflects the documentation subject matter
- Is concise (1-3 words, kebab-case)
- Is descriptive enough for semantic matching

Examples:
- AWS SDK documentation -> `aws-sdk-docs`
- React component library -> `react-components`
- Internal API reference -> `api-reference`
- Kubernetes guides -> `k8s-guides`

### 5.2 Ask User for Confirmation

Use `AskUserQuestion` with options:
- Accept suggested name
- Provide custom name

**Question format:**
```
Based on analyzing the documentation content, I suggest naming this skill:

  "<suggested-name>"

This name will be used for:
- The skill folder: .claude/skills/<name>/
- The skill identifier in SKILL.md
- Semantic matching when Claude auto-loads skills

Do you want to use this name or provide a different one?
```

---

## Phase 6: Generate SKILL.md (Two-Tier Architecture)

Create a **lean** SKILL.md that stays under ~150-200 lines.

### 6.1 Skill Location

```
.claude/skills/<skill-name>/
├── SKILL.md           # Lean navigator (~150 lines)
├── file-index.md      # Full catalog (if > 100 files)
└── references/
    └── [documentation files]
```

### 6.2 SKILL.md Size Guidelines

| Doc Set Size | SKILL.md Target | Content |
|--------------|-----------------|---------|
| < 30 files | ~100 lines | List all files |
| 30-100 files | ~150 lines | Top 30 + all outliers + patterns |
| > 100 files | ~150 lines | Top 20 + all outliers + patterns + file-index reference |

### 6.3 SKILL.md Template

```yaml
---
name: <skill-name>
description: "<Primary subject>. <Main domains/services>. <Standard content types>. ALSO: <outlier topic 1>, <outlier topic 2>, <outlier keywords...>."
allowed-tools: Read, Grep, Glob
---

# <Skill Name> Documentation Navigator

Documentation location: `.claude/skills/<skill-name>/references/`

---

## ⚠️ IMPORTANT: Non-Standard Documentation (Outliers)

**CHECK THIS SECTION FIRST** for questions about:
- Configuration, setup, installation
- Troubleshooting, errors, debugging
- Migration, upgrades, breaking changes
- Concepts, architecture, "how does X work"
- Getting started, tutorials, walkthroughs

These files have **different content structure** than the standard reference docs and won't be found by pattern-based navigation.

### Configuration & Setup Guides

| File | Description | Key Topics |
|------|-------------|------------|
| <file>.md | <description> | <topic1>, <topic2>, <topic3> |

### Troubleshooting & Debugging

| File | Description | Key Topics |
|------|-------------|------------|
| <file>.md | <description> | <topic1>, <topic2>, <topic3> |

### Migration & Upgrade Guides

| File | Description | Key Topics |
|------|-------------|------------|
| <file>.md | <description> | <topic1>, <topic2>, <topic3> |

### Conceptual & Architecture Docs

| File | Description | Key Topics |
|------|-------------|------------|
| <file>.md | <description> | <topic1>, <topic2>, <topic3> |

### Service Index Files

| File | Description |
|------|-------------|
| <service>.md | Lists all <service> resources and functions |

[Include only non-empty archetype sections. Remove sections with no files.]

---

## Quick Reference

[For pattern-based docs: Service/domain summary table]
[For pattern-less docs: Category summary]

| Domain/Service | Files | Description |
|----------------|-------|-------------|
| ... | ... | ... |

---

## File Naming Convention

[Document the detected pattern, if any]

**Pattern:** `<pattern-description>`

**Examples:**
- `<example-1>` - <what it contains>
- `<example-2>` - <what it contains>

**⚠️ Exception:** Files in the "Non-Standard Documentation" section above don't follow this pattern. Always check that section first for guides, configuration, and troubleshooting topics.

---

## Section Markers

[Document consistent section headings found in STANDARD files only]

| Section | Marker | Content |
|---------|--------|---------|
| ... | `## ...` | ... |

Note: Outlier files have different section structures. Read their headings directly.

---

## How to Find Files

### 1. Check outliers first
If the question involves configuration, setup, troubleshooting, migration, or concepts, **check the "Non-Standard Documentation" section first**.

### 2. By keyword search
```
Grep pattern="<keyword>" path=".claude/skills/<skill-name>/references/" output_mode="files_with_matches"
```

### 3. By pattern (for standard files)
```
Glob pattern=".claude/skills/<skill-name>/references/<service>-*.md"
```

### 4. From full index (for large doc sets)
```
Read file_path=".claude/skills/<skill-name>/file-index.md"
```

---

## Common Files Quick Access

[List top 15-20 most commonly needed STANDARD files]

| File | Description |
|------|-------------|
| ... | ... |

---

## Protocol

1. **ALWAYS check "Non-Standard Documentation" section first** if question involves:
   - Configuration, setup, environment variables
   - Errors, troubleshooting, debugging
   - Migration, upgrades, version changes
   - Concepts, "why", "how does X work"
   - Getting started, tutorials

2. **For standard resource/API questions:** Identify domain and construct path using pattern

3. **Search for section marker:** `Grep pattern="<marker>" path="<file>" -A 5`

4. **Read surgically:** `Read file_path="<file>" offset=<line-5> limit=50`

---

## Constraints

- Maximum read: 50-100 lines at a time
- Always use offset/limit parameters
- Search for section markers before reading
- Never read entire files
- Check file-index.md when unsure which file to consult
```

### 6.4 Description Generation

**CRITICAL: The `description` value MUST be wrapped in double quotes.** Unquoted descriptions containing parentheses `()`, colons `:`, or other YAML special characters will cause the skill parser to silently truncate the description. This results in the skill registering with a tiny token count and failing to appear in the system prompt. Always use `description: "..."` format.

**YAML double-quote safety rules:**
- **Escape inner double quotes** as `\"` — e.g., `"Covers the \"Enterprise\" tier"`
- **Escape backslashes** as `\\` — e.g., `"Paths like C:\\Users\\docs"`
- **Never include literal newlines** inside the quoted string — keep it as one line
- When in doubt, **avoid double quotes and backslashes in the description text entirely** by rephrasing (e.g., use `Enterprise tier` instead of `"Enterprise" tier`)

The description MUST include:
- Primary subject matter
- Key domains/services covered
- Standard content types (resources, functions, etc.)
- **ALL outlier topics and keywords** (critical for skill invocation)

**Example:**
```yaml
description: "Pulumi AWS provider documentation. AWS services (EC2, S3, IAM, RDS, Lambda, ECS). Resources, functions, inputs, outputs, examples, import syntax. ALSO: S3 backend configuration, Pulumi state management, stack naming conventions, PULUMI_CONFIG_PASSPHRASE, cross-account access, migration from Terraform."
```

The "ALSO:" section ensures outlier topics trigger skill invocation.

---

## Phase 7: Generate file-index.md (If Needed)

For doc sets > 100 files, generate a comprehensive index.

### 7.1 When to Generate

- File count > 100
- OR file count > 50 AND no clear naming pattern

### 7.2 file-index.md Template

```markdown
# <Skill Name> - Complete File Index

This index contains descriptions for all documentation files.
Use Ctrl+F or Grep to search for topics.

---

## Index by Domain/Category

### <Domain 1>

| File | Description | Keywords |
|------|-------------|----------|
| file1.md | Description | keyword1, keyword2 |
| file2.md | Description | keyword1, keyword3 |
...

### <Domain 2>

| File | Description | Keywords |
|------|-------------|----------|
...

---

## Alphabetical Index

| File | Domain | Description |
|------|--------|-------------|
| a-file.md | domain1 | ... |
| b-file.md | domain2 | ... |
...
```

### 7.3 Generating Descriptions at Scale

For > 100 files where full sampling isn't practical:

**Option A: Heading-based descriptions**
- Use extracted headings to generate descriptions
- Format: "Covers: <heading1>, <heading2>, <heading3>"

**Option B: Title + first line**
- Extract title (first `#` heading)
- Use as description directly

**Option C: Parallel batch processing**
- For very large sets (500+), consider headless fan-out pattern
- But this is rarely needed for documentation

---

## Phase 8: Copy Documentation

### 8.1 Create Skill Folder Structure

```bash
mkdir -p ".claude/skills/<skill-name>/references"
```

### 8.2 Copy Documentation Preserving Structure

```bash
# macOS compatible (use rsync)
rsync -av --include="*/" --include="*.md" --include="*.txt" --exclude="*" \
  "<source_folder>/" ".claude/skills/<skill-name>/references/"
```

### 8.3 Verify Copy

```bash
# Verify file count matches
find ".claude/skills/<skill-name>/references" -type f | wc -l
```

---

## Output

After completion, report to user:

```
Documentation Navigator skill created successfully!

Skill location: .claude/skills/<skill-name>/
- SKILL.md: Navigator file (<X> lines)
- file-index.md: Full catalog (<Y> files indexed) [if applicable]
- references/: <N> documentation files (<SIZE>)

Strategy used: <strategy-name>
Domains detected: <list>
Outliers identified: <count> (all explicitly listed in SKILL.md)

The skill is ready to use. Claude will auto-load it when questions match
the description keywords, or you can invoke it with /<skill-name>.
```

---

## Error Handling

### No Documentation Files Found
```
Error: No documentation files found in "<path>"

Looked for: .md, .txt files
Found: 0 files

Please verify:
1. The path is correct
2. Documentation uses .md or .txt extensions
3. The folder is not empty
```

### Permission Errors
```
Error: Cannot read "<path>"

This may be a permissions issue. Please verify you have read access to the folder.
```

### Skill Already Exists
```
Warning: Skill ".claude/skills/<name>" already exists.

This factory always recreates from scratch. The existing skill will be replaced.

Proceed? (The old skill folder will be deleted)
```

Use `AskUserQuestion` to confirm before overwriting.

---

## Efficiency Guidelines

### Parallel Tool Calls

When reading multiple files, issue parallel Read calls:
- Batch 10-15 files per message
- Don't wait for one file before reading the next
- Example: "Read files A, B, C, D, E simultaneously"

### Minimize Context Usage

- Extract headings with grep (cheap) before reading files
- Read only first 30-40 lines per file
- For outliers, read more (first 50 lines) since they're few

### When NOT to Use Subagents

For typical doc sets (< 500 files):
- Parallel Read calls are sufficient
- Subagent overhead not justified
- Keep everything in main context

For very large doc sets (> 500 files):
- Consider headless fan-out pattern
- But this is rare for documentation
