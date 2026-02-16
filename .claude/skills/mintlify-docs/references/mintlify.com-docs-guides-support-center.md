---
url: https://mintlify.com/docs/guides/support-center
canonical: https://www.mintlify.com/docs/guides/support-center
title: "Create a support center - Mintlify"
description: "Build a self-service support center that helps customers find answers, reduces ticket volume, and improves customer satisfaction."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Use cases

Create a support center

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

A support center helps customers solve problems and find information about your product. When customers can find answers themselves, they get help faster and your support team can focus on complex issues that require their expertise. Mintlify provides infrastructure for support centers that scale with your customer base.

- **AI-powered search**: The [assistant](https://www.mintlify.com/docs/ai/assistant) answers customer questions using your support content, so people can find answers without knowing exactly where to look or specific terms to search for.
- **Feedback collection**: Built-in [feedback widgets](https://www.mintlify.com/docs/optimize/feedback) let customers rate articles and report issues so you can improve content.
- **Analytics**: Track which articles get views, what questions customers ask, and where they struggle.
- **Authentication**: Use [SSO or OAuth](https://www.mintlify.com/docs/deploy/authentication-setup) to show personalized content based on customer plans or account types.

##

[​](#prerequisites)

Prerequisites

If you haven’t created a Mintlify project yet, see the [Quickstart](https://www.mintlify.com/docs/quickstart) to deploy your site.

- Content for your most common support topics
- Admin access to your Mintlify organization
- Domain for hosting your support center

##

[​](#migrate-existing-content)

Migrate existing content

If you’re creating a support center from scratch, skip to [Plan your support center structure](#plan-your-support-center-structure).

###

[​](#audit-existing-content)

Audit existing content

Review your current support resources to understand what to migrate.

- **Help articles**: What topics do you address? Which articles get the most views?
- **FAQs**: Do you have frequently asked questions that should become articles?
- **Support tickets**: What questions do customers ask repeatedly? These should become self-service content.
- **Product documentation**: Is there overlap between support content and product docs?

###

[​](#export-your-existing-content)

Export your existing content

- Export to **Markdown** for the simplest migration to Mintlify.
- Export to **HTML** if Markdown isn’t available, then convert to Markdown.
- Export **ticket data** to identify common questions that need documentation.

##

[​](#plan-your-support-center-structure)

Plan your support center structure

Organize your support center around customer problems, not product features. Customers arrive with questions and goals, so structure content that aligns with how they think about your product and common tasks.

Review your support tickets to understand what customers actually ask about. This helps you prioritize content and structure navigation around real problems.
```
{
  "navigation": {
    "groups": [
      {
        "group": "Get Started",
        "pages": [
          "getting-started/quick-setup",
          "getting-started/first-steps"
        ]
      },
      {
        "group": "Account",
        "pages": [
          "account/billing",
          "account/plans",
          "account/team-management",
          "account/security"
        ]
      },
      {
        "group": "Using the Product",
        "pages": [
          "product/feature-one",
          "product/feature-two",
          "product/integrations"
        ]
      },
      {
        "group": "Troubleshooting",
        "pages": [
          "troubleshooting/common-errors",
          "troubleshooting/connectivity",
          "troubleshooting/performance"
        ]
      }
    ]
  }
}
```
See [Navigation](https://www.mintlify.com/docs/organize/navigation) for more configuration options.

##

[​](#write-effective-support-content)

Write effective support content

Support content should help customers solve problems quickly. Every article should answer one specific question or solve one specific problem. Organize related content into groups instead of creating overly long pages that have too much information.

###

[​](#structure-articles-for-scanning)

Structure articles for scanning

Customers scan support pages looking for their specific issue. Use clear headings and short paragraphs.

Example support page
```
---
title: "Fix login issues"
description: "Troubleshoot common problems signing in to your account"
---

## Reset your password

If you forgot your password, request a reset link from the login page.

1. Go to the login page.
2. Select **Forgot password**.
3. Enter your email address.
4. Check your inbox for the reset link.

## Clear browser cache

Old cached data can cause login problems. Clear your browser cache and try again.

## Check account status

If your account is suspended or deactivated, you'll see an error when logging in.
Contact support if you believe this is a mistake.
```

###

[​](#include-step-by-step-instructions)

Include step-by-step instructions

When explaining how to do something, use numbered steps.

1

[](#)

Go to Settings

Click the gear icon in the toolbar.

2

[](#)

Select Billing

Click **Billing** in the navigation menu.

3

[](#)

Update payment method

Click **Update** next to your current payment method and enter new details.

###

[​](#add-visual-aids)

Add visual aids

Screenshots and diagrams help customers confirm they’re in the right place.

Example screenshot
```
![Settings page with billing section highlighted](/images/billing-settings.png)
```

##

[​](#set-up-the-assistant)

Set up the assistant

The assistant answers customer questions using your support content. Configure it from your [dashboard](https://dashboard.mintlify.com/products/assistant/settings).

1

[](#)

Add sample questions

Add common questions customers ask, such as:

- “How do I cancel my subscription?”
- “Why was my payment declined?”
- “How do I add team members?”

Sample questions appear as quick-access buttons, helping customers get answers with one click.

2

[](#)

Set a deflection email

Configure a support email for questions the assistant can’t answer. This ensures customers can still reach your team when self-service isn’t enough.

3

[](#)

Review conversations

Check assistant conversations regularly to identify:

- Questions the assistant can’t answer (content gaps)
- Incorrect or incomplete answers (content to improve)
- Common question patterns (content to prioritize)

##

[​](#enable-feedback-collection)

Enable feedback collection

Feedback helps you understand which pages are helpful and which need improvement. Review [feedback](https://www.mintlify.com/docs/optimize/feedback) to see which pages customers find helpful and which need improvement. Read all comments and update pages based on valid feedback.

##

[​](#set-up-analytics)

Set up analytics

Monitor how customers use your support center to improve content over time.

- **Popular articles**: Which articles get the most views? Keep these accurate and well-maintained.
- **Search queries**: What do customers search for? Create content for common searches that return no results.
- **Assistant conversations**: What questions does the assistant receive? Use this to identify content gaps.

##

[​](#restrict-content-by-customer-segment)

Restrict content by customer segment

If you have different customer tiers or product plans, show relevant content to each segment using group-based access control.

1

[](#)

Set up authentication

Configure [authentication](https://www.mintlify.com/docs/deploy/authentication-setup) to identify customers when they visit your support center.

2

[](#)

Configure user groups

Return group information in your user data to define customer segments based on plan type, account status, or other attributes. See [User data format](https://www.mintlify.com/docs/deploy/authentication-setup#user-data-format) for details.

3

[](#)

Tag content by group

Use frontmatter to specify which groups can see each article.
```
---
title: "Enterprise SSO setup"
groups: ["enterprise"]
---
```

##

[​](#maintain-your-support-center)

Maintain your support center

Support content becomes outdated as your product changes. Establish processes to keep content accurate.

1

[](#)

Update with product releases

When you ship product changes, update affected support articles. Include documentation updates in your release process.

2

[](#)

Review feedback regularly

Check article ratings and customer feedback weekly. Address negative feedback promptly. It often indicates confusing or incorrect content.

3

[](#)

Monitor support tickets

If customers submit tickets for issues covered in your support center, investigate why self-service didn’t work. The article might be hard to find, unclear, or incomplete.

4

[](#)

Archive outdated content

Remove or archive articles about deprecated features. Outdated content confuses customers and reduces trust in your support center.

##

[​](#next-steps)

Next steps

Your support center is ready to launch. After deploying:

1.  Link to your support center from your product and website.
2.  Monitor assistant conversations and search queries to find content gaps.
3.  Review feedback ratings weekly and improve low-rated articles.
4.  Track ticket volume to measure self-service effectiveness.

A good support center reduces support costs while improving customer satisfaction. Invest in content that answers common questions effectively.

Was this page helpful?

YesNo

[Create a knowledge basePrevious](https://www.mintlify.com/docs/guides/knowledge-base)

⌘I
