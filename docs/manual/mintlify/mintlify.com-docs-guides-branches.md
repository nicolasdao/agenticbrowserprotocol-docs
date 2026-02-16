---
url: https://mintlify.com/docs/guides/branches
canonical: https://www.mintlify.com/docs/guides/branches
title: "Work with branches - Mintlify"
description: "Create branches to preview changes and collaborate before publishing."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Git

Work with branches

Search...

⌘K

##### Overview

- [Guides](https://www.mintlify.com/docs/guides)

##### AI

- [Automate documentation updates](https://www.mintlify.com/docs/guides/automate-agent)
- [Build an in-app assistant](https://www.mintlify.com/docs/guides/assistant-embed)
- [Claude Code](https://www.mintlify.com/docs/guides/claude-code)
- [Cursor](https://www.mintlify.com/docs/guides/cursor)
- [GEO](https://www.mintlify.com/docs/guides/geo)
- [Windsurf](https://www.mintlify.com/docs/guides/windsurf)

##### API docs

- [Migrate from MDX to OAS](https://www.mintlify.com/docs/guides/migrating-from-mdx)

##### Best practices

- [Accessibility](https://www.mintlify.com/docs/guides/accessibility)
- [Content types](https://www.mintlify.com/docs/guides/content-types)
- [Content templates](https://www.mintlify.com/docs/guides/content-templates)
- [Improve your docs](https://www.mintlify.com/docs/guides/improving-docs)
- [Internationalization](https://www.mintlify.com/docs/guides/internationalization)
- [Linking](https://www.mintlify.com/docs/guides/linking)
- [Maintenance](https://www.mintlify.com/docs/guides/maintenance)
- [Media](https://www.mintlify.com/docs/guides/media)
- [Organize navigation](https://www.mintlify.com/docs/guides/navigation)
- [SEO](https://www.mintlify.com/docs/guides/seo)
- [Style and tone](https://www.mintlify.com/docs/guides/style-and-tone)
- [Understand your audience](https://www.mintlify.com/docs/guides/understand-your-audience)

##### Git

- [Git concepts for documentation](https://www.mintlify.com/docs/guides/git-concepts)
- [Work with branches](https://www.mintlify.com/docs/guides/branches)

##### Use cases

- [Developer documentation](https://www.mintlify.com/docs/guides/developer-documentation)
- [Knowledge base](https://www.mintlify.com/docs/guides/knowledge-base)
- [Support center](https://www.mintlify.com/docs/guides/support-center)

![US](https://d3gk2c5xim1je2.cloudfront.net/flags/US.svg)

English

Branches are a feature of version control that point to specific commits in your repository. Your deployment branch, usually called `main`, represents the content used to build your live documentation site. All other branches are independent of your live docs unless you choose to merge them into your deployment branch. Branches let you create separate instances of your documentation to make changes, get reviews, and try new approaches before publishing. Your team can work on branches to update different parts of your documentation simultaneously without affecting what users see on your live site. The following diagram shows an example of a branch workflow where a feature branch is created, changes are made, and then the feature branch is merged into the main branch.

mainfeature-branchInitial commitBranch createdAdd ChangesAdd more changesAdd reviewer feedbackMerge into mainLive docs

We recommend always working from branches when updating documentation to keep your live site stable and enable review workflows.

##

[​](#branch-naming-conventions)

Branch naming conventions

Use clear, descriptive names that explain the purpose of a branch. **Use**:

- `fix-broken-links`
- `add-webhooks-guide`
- `reorganize-getting-started`
- `ticket-123-oauth-guide`

**Avoid**:

- `temp`
- `my-branch`
- `updates`
- `branch1`

##

[​](#create-a-branch)

Create a branch

- Using web editor

- Using local development


1.  Click the branch name in the editor.
2.  Click **New Branch**.
3.  Enter a descriptive name.
4.  Click **Create Branch**.

1

[](#)

Create a branch from your terminal
```
git checkout -b branch-name
```
This creates the branch and switches to it in one command.

2

[](#)

Push the branch to GitHub
```
git push -u origin branch-name
```
The `-u` flag sets up tracking so future pushes just need `git push`.

##

[​](#save-changes-on-a-branch)

Save changes on a branch

- Using web editor

- Using local development


Select the **Save as commit** button in the top-right of the editor toolbar. This creates a commit and pushes your work to your branch automatically.

Stage, commit, and push your changes.
```
git add .
git commit -m "Describe your changes"
git push
```

##

[​](#switch-branches)

Switch branches

- Using web editor

- Using local development


1.  Select the branch name in the editor toolbar.
2.  Select the branch you want to switch to from the dropdown menu.

Unsaved changes are lost when switching branches. Save your work first.

Switch to an existing branch:
```
git checkout branch-name
```
Or create and switch in one command:
```
git checkout -b new-branch-name
```

##

[​](#merge-branches)

Merge branches

Once your changes are ready to publish, create a pull request to merge your branch into the deployment branch.

Was this page helpful?

YesNo

[Git concepts for documentationPrevious](https://www.mintlify.com/docs/guides/git-concepts)[Create developer documentationNext](https://www.mintlify.com/docs/guides/developer-documentation)

⌘I
