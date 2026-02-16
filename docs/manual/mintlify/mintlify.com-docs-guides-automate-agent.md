---
url: https://mintlify.com/docs/guides/automate-agent
canonical: https://www.mintlify.com/docs/guides/automate-agent
title: "Tutorial: Auto-update documentation when code is changed - Mintlify"
description: "Use the agent API to automatically update your documentation."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

AI

Tutorial: Auto-update documentation when code is changed

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

##

[​](#what-you-will-build)

What you will build

An automation that updates your documentation when code is pushed to your main branch. The workflow can be built on multiple platforms, including GitHub Actions and n8n. It watches your code repository and then calls the agent API to update your documentation in a separate documentation repository. This workflow connects two separate repositories:

- **Code repository**: Where you store application code. You’ll set up the automation trigger on this repository. Examples include a backend API, frontend app, SDK, or CLI tool.
- **Documentation repository**: Where you store your documentation and connect to your Mintlify project. The agent creates pull requests with documentation updates in this repository.

This tutorial assumes your documentation is in a separate repository from your application code. If you have a monorepo, modify the workflow to target the directory where you store your documentation.

###

[​](#workflow-overview)

Workflow overview

1.  Someone pushes code to your main branch.
2.  The workflow triggers.
3.  The workflow calls the agent API to update your documentation.
4.  The agent creates a pull request with documentation updates in your documentation repository.

##

[​](#choose-your-platform)

Choose your platform

- GitHub Actions

- n8n


GitHub Actions is the simplest option if your code is already on GitHub. No additional services required.

##

[​](#prerequisites)

Prerequisites

- GitHub Actions enabled on your code and documentation repositories
- [Mintlify GitHub App](https://www.mintlify.com/docs/deploy/github) installed in both your code and documentation repositories
- [Mintlify admin API key](https://dashboard.mintlify.com/settings/organization/api-keys)
- [Mintlify project ID](https://dashboard.mintlify.com/settings/organization/api-keys)
- [Mintlify Enterprise plan](https://mintlify.com/pricing)
- Admin access to the GitHub repositories for your code and documentation

###

[​](#install-the-mintlify-app-on-your-code-repository)

Install the Mintlify app on your code repository

The Mintlify app must be installed on your code repository so the agent can fetch context from your codebase. To add the app to new repositories:

1.  Open the agent panel in your Mintlify dashboard.

    ![The agent panel in light mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-light.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=56ee8c375606ca4a50b9b889474fc769)![The agent panel in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-dark.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=ad82516ec69eb247ac0475fd3397c338)

2.  Click the **Settings** button.

    ![The settings button in light mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-settings-light.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=ecb555eecfddf7480baaaf7d2fd6bce9)![The settings button in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-settings-dark.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=a3250fa23cac19e8914b7185ac24c6d0)

3.  Click **Add to New Organization**. This will take you to the app installation page on GitHub.
4.  Select the repositories you want to grant access to from the list.
5.  Save your changes.

###

[​](#get-your-admin-api-key)

Get your admin API key

1.  Navigate to the [API keys](https://dashboard.mintlify.com/settings/organization/api-keys) page in your dashboard.
2.  Select **Create Admin API Key**.
3.  Copy the key and save it securely.

##

[​](#build-the-workflow)

Build the workflow

###

[​](#create-the-workflow-file)

Create the workflow file

1.  In your code repository, create a new file: `.github/workflows/update-docs.yml`
2.  Add this workflow:

    ```
    name: Update Docs

    on:
      push:
        branches:
          - main

    jobs:
      update-docs:
        runs-on: ubuntu-latest
        steps:
          - uses: actions/github-script@v8
            env:
              MINTLIFY_API_KEY: ${{ secrets.MINTLIFY_API_KEY }}
              PROJECT_ID: ${{ secrets.MINTLIFY_PROJECT_ID }}
            with:
              script: |
                const { owner, repo } = context.repo;
                const projectId = process.env.PROJECT_ID;
                const apiKey = process.env.MINTLIFY_API_KEY;

                if (!projectId || !apiKey) {
                  core.setFailed('Missing MINTLIFY_PROJECT_ID or MINTLIFY_API_KEY secrets');
                  return;
                }

                const url = `https://api.mintlify.com/v1/agent/${projectId}/job`;
                const payload = {
                  branch: `mintlify/docs-update-${Date.now()}`,
                  messages: [
                    {
                      role: 'system',
                      content: 'You are an action runner that updates documentation based on code changes. You should never ask questions. If you are not able to access the repository, report the error and exit.'
                    },
                    {
                      role: 'user',
                      content: `Update the documentation for our recent pushes to main:\n\nRepository: ${owner}/${repo}`
                    }
                  ],
                  asDraft: false
                };

                try {
                  const response = await fetch(url, {
                    method: 'POST',
                    headers: {
                      'Authorization': `Bearer ${apiKey}`,
                      'Content-Type': 'application/json'
                    },
                    body: JSON.stringify(payload)
                  });

                  if (!response.ok) {
                    throw new Error(`API request failed with status ${response.status}: ${await response.text()}`);
                  }

                  const reader = response.body.getReader();
                  const decoder = new TextDecoder();
                  let buffer = '';

                  while (true) {
                    const { done, value } = await reader.read();
                    if (done) break;
                    buffer += decoder.decode(value, { stream: true });
                    const lines = buffer.split('\n');
                    buffer = lines.pop() || '';
                    for (const line of lines) {
                      if (line.trim()) {
                        console.log(line);
                      }
                    }
                  }
                  if (buffer.trim()) {
                    console.log(buffer);
                  }

                  core.notice(`Documentation update job triggered for ${owner}/${repo}`);
                } catch (error) {
                  core.setFailed(`Failed to create documentation update job: ${error.message}`);
                }
    ```


###

[​](#add-secrets)

Add secrets

1.  In your code repository, go to **Settings** → **Secrets and variables** → **Actions**.
2.  Click **New repository secret**.
3.  Add the following secrets:
    -   Name: `MINTLIFY_API_KEY`, Secret: Your Mintlify admin API key
    -   Name: `MINTLIFY_PROJECT_ID`, Secret: Your Mintlify project ID (found on the [API keys](https://dashboard.mintlify.com/settings/organization/api-keys) page of your dashboard)

For more information, see [Using secrets in GitHub Actions](https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/use-secrets) in the GitHub documentation.

##

[​](#test-the-automation)

Test the automation

1.  Make a small change in your code repository and push to main:

    ```
    git add .
    git commit -m "Test: trigger docs automation"
    git push origin main
    ```

2.  Check the **Actions** tab in your code repository to see the workflow running.
3.  After the workflow runs, check your documentation repository for a new branch and pull request with documentation updates.

##

[​](#troubleshooting)

Troubleshooting

###

[​](#workflow-not-running)

Workflow not running

- Verify GitHub Actions is enabled in your code repository.
- Check the **Actions** tab for error messages.
- Ensure the workflow file is in `.github/workflows/` with a `.yml` extension.

###

[​](#401-error-from-agent-api)

401 error from agent API

- Verify your API key starts with `mint_`.
- Check the Authorization header is formatted as `Bearer mint_yourkey`.
- Confirm the API key is for the correct Mintlify organization.

###

[​](#no-documentation-updates-appearing)

No documentation updates appearing

- Check that the documentation repository is connected to your Mintlify project.
- Verify the agent has write access to the documentation repository.
- Check the workflow logs for error messages from the agent.

n8n provides a visual workflow editor and can integrate with multiple services.

##

[​](#prerequisites-2)

Prerequisites

- n8n workspace
- [Mintlify Enterprise plan](https://mintlify.com/pricing)
- Mintlify app installed on your code repository
- Mintlify admin API key
- Admin access to the GitHub repositories for your code and documentation
- GitHub personal access token

###

[​](#install-the-mintlify-app-on-your-code-repository-2)

Install the Mintlify app on your code repository

The Mintlify app must be installed on your code repository so the agent can fetch context from your codebase. To add the app to new repositories:

1.  Open the agent panel in your Mintlify dashboard.

    ![The agent panel in light mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-light.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=56ee8c375606ca4a50b9b889474fc769)![The agent panel in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-dark.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=ad82516ec69eb247ac0475fd3397c338)

2.  Click the **Settings** button.

    ![The settings button in light mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-settings-light.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=ecb555eecfddf7480baaaf7d2fd6bce9)![The settings button in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-settings-dark.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=a3250fa23cac19e8914b7185ac24c6d0)

3.  Click **Add to New Organization**. This will take you to the app installation page on GitHub.
4.  Select the repositories you want to grant access to from the list.
5.  Save your changes.

###

[​](#get-your-admin-api-key-2)

Get your admin API key

1.  Navigate to the [API keys](https://dashboard.mintlify.com/settings/organization/api-keys) page in your dashboard.
2.  Select **Create Admin API Key**.
3.  Copy the key and save it securely.

###

[​](#get-your-github-personal-access-token)

Get your GitHub personal access token

1.  In GitHub, navigate to **Settings**.
2.  Click **Developer settings**.
3.  Click **Personal access tokens**.
4.  Click **Tokens (classic)**.
5.  Click **Generate new token (classic)**.
6.  Select these scopes:
    -   `repo` (full control of private repositories)
    -   `admin:repo_hook` (if you want n8n to create webhooks)
7.  Generate and save the token securely.

For more information, see [Creating a personal access token (classic)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens?versionId=free-pro-team%40latest&productId=account-and-profile#creating-a-personal-access-token-classic) in the GitHub documentation.

##

[​](#build-the-workflow-2)

Build the workflow

###

[​](#create-the-webhook-trigger)

Create the webhook trigger

1.  In n8n, create a new workflow.
2.  Add a webhook node.
3.  Configure the webhook:
    -   HTTP Method: `POST`
    -   Path: `auto-update-documentation` (or any unique path)
    -   Authentication: None
    -   Respond: Immediately
4.  Save the workflow.
5.  Copy the production webhook URL. It looks like: `https://your-n8n-instance.app.n8n.cloud/webhook/auto-update-documentation`

![Screenshot of the configurations for the webhook node.](https://mintcdn.com/mintlify/MUT1RZiseS3dwdrU/images/guides/n8n/webhook-node.png?fit=max&auto=format&n=MUT1RZiseS3dwdrU&q=85&s=165a57aed92aa90d90609c5d381d29b7)

###

[​](#set-up-the-github-webhook)

Set up the GitHub webhook

1.  Navigate to your code repository on GitHub.
2.  Click **Settings**.
3.  Click **Webhooks**.
4.  Click **Add webhook**.
5.  Configure the webhook:
    -   Payload URL: Paste your n8n webhook URL
    -   Content type: `application/json`
    -   Which events would you like to trigger this webhook?
        -   Select **Let me select individual events.**
        -   Select only **Push events**.
    -   Select **Active**
6.  Click **Add webhook**.

###

[​](#filter-for-main-branch-pushes)

Filter for main branch pushes

Add a code node after the webhook to filter for pushes to main and extract the relevant information.

1.  Add a code node.
2.  Name it “Filter main pushes.”
3.  Set mode to **Run Once for All Items**.
4.  Add this JavaScript:
```
const webhookData = $input.first().json.body;

// Only continue if this is a push to main
if (webhookData.ref !== "refs/heads/main") {
  return [];
}

// Extract information
const repository = webhookData.repository;
const pusher = webhookData.pusher;

// Build message for agent
const agentMessage = `Update documentation for changes pushed to main in ${repository.name}. Always edit files and create a pull request.`;

return {
  json: {
    codeRepoName: repository.full_name,
    codeRepoShortName: repository.name,
    agentMessage: agentMessage
  }
};
```
![Screenshot of the configurations for the filter main pushes node.](https://mintcdn.com/mintlify/MUT1RZiseS3dwdrU/images/guides/n8n/filter-merged-PRs-node.png?fit=max&auto=format&n=MUT1RZiseS3dwdrU&q=85&s=a7661a96b0a5c6272e8a284edb8eb8f5)

This code stops the workflow if the push wasn’t to main, extracts all relevant information from the GitHub webhook, and creates a message for the agent API.

###

[​](#call-the-agent-api)

Call the agent API

Add an HTTP request node to create a documentation job.

1.  Add an HTTP request node.
2.  Name it “Create agent job.”
3.  Configure the request:

    -   Method: `POST`
    -   URL: `https://api.mintlify.com/v1/agent/YOUR_PROJECT_ID/job` (replace `YOUR_PROJECT_ID` with your project ID from the [API keys](https://dashboard.mintlify.com/settings/organization/api-keys) page)
    -   Authentication: Generic Credential Type → Header Auth
        -   Create a new credential:
            -   Name: `Authorization`
            -   Value: `Bearer mint_YOUR_API_KEY` (replace with your API key)
    -   Send Body: On
    -   Body Content Type: JSON
    -   Specify Body: Using JSON
    -   Add this JSON:

    ```
    {
    "branch": "docs-update-from-{{ $json.codeRepoShortName }}-{{ $now.toISOString() }}",
    "messages": [
        {
        "role": "system",
        "content": "{{ $json.agentMessage }}"
        }
    ],
    "asDraft": false
    }
    ```


![Screenshot of the configurations for the create agent job node.](https://mintcdn.com/mintlify/jW5VvzJALf7BW1X_/images/guides/n8n/create-agent-job-node.png?fit=max&auto=format&n=jW5VvzJALf7BW1X_&q=85&s=2bbb162905564f80a30bb7d75c917815)

The agent creates a pull request in your documentation repository using a descriptive branch name that includes the source repository name and timestamp.

###

[​](#activate-the-workflow)

Activate the workflow

1.  Save your workflow.
2.  Set it to active.

Your workflow is now monitoring your code repository for pushes to main.

![Screenshot of the automation workflow in the n8n editor.](https://mintcdn.com/mintlify/MUT1RZiseS3dwdrU/images/guides/n8n/workflow.png?fit=max&auto=format&n=MUT1RZiseS3dwdrU&q=85&s=55120ad3ffc9b32d56aefe05c6431324)

##

[​](#test-the-automation-2)

Test the automation

1.  Create a test branch in your code repository:

    ```
    git checkout -b test-docs-automation
    ```

2.  Make a small change and commit it:

    ```
    git add .
    git commit -m "Test: trigger docs automation"
    git push origin test-docs-automation
    ```

3.  Open a pull request on GitHub.
4.  Merge the pull request.

###

[​](#verify-the-automation)

Verify the automation

You should see a new n8n execution with all nodes completed successfully, and a new branch and pull request in your documentation repository.

##

[​](#troubleshooting-2)

Troubleshooting

###

[​](#webhook-not-triggering)

Webhook not triggering

- Verify the workflow is active in n8n.
- Check GitHub repository Settings → Webhooks → Recent Deliveries for the response code.
- Confirm the webhook URL matches your n8n webhook URL exactly.

###

[​](#401-error-from-agent-api-2)

401 error from agent API

- Verify your API key starts with `mint_`.
- Check the Authorization header is formatted as `Bearer mint_yourkey`.
- Confirm the API key is for the correct Mintlify organization.

###

[​](#401-error-from-github)

401 error from GitHub

- Verify your token has the `repo` scope.
- Check that the token hasn’t expired.
- Confirm you included the `User-Agent` header in the GitHub request.

Was this page helpful?

YesNo

[GuidesPrevious](https://www.mintlify.com/docs/guides)[Tutorial: Build an in-app documentation assistantNext](https://www.mintlify.com/docs/guides/assistant-embed)

⌘I

![The agent panel in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-dark.png?w=1650&fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=50053641543ddeeeb18818da997132ea)

![The settings button in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-settings-dark.png?w=1650&fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=c1d8e1cd78e6a494852b809cbeb1a695)

![The agent panel in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-dark.png?w=1650&fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=50053641543ddeeeb18818da997132ea)

![The settings button in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-settings-dark.png?w=1650&fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=c1d8e1cd78e6a494852b809cbeb1a695)

![Screenshot of the configurations for the webhook node.](https://mintcdn.com/mintlify/MUT1RZiseS3dwdrU/images/guides/n8n/webhook-node.png?w=1650&fit=max&auto=format&n=MUT1RZiseS3dwdrU&q=85&s=5c7c0fb7641c8696213d039708f0b30c)

![Screenshot of the configurations for the filter main pushes node.](https://mintcdn.com/mintlify/MUT1RZiseS3dwdrU/images/guides/n8n/filter-merged-PRs-node.png?w=1650&fit=max&auto=format&n=MUT1RZiseS3dwdrU&q=85&s=9c9086087bcd6069b467a8e31ecb8af5)

![Screenshot of the configurations for the create agent job node.](https://mintcdn.com/mintlify/jW5VvzJALf7BW1X_/images/guides/n8n/create-agent-job-node.png?w=1650&fit=max&auto=format&n=jW5VvzJALf7BW1X_&q=85&s=5a2bd3ae4862208ea9aedd0f3a3ed8e0)

![Screenshot of the automation workflow in the n8n editor.](https://mintcdn.com/mintlify/MUT1RZiseS3dwdrU/images/guides/n8n/workflow.png?w=1650&fit=max&auto=format&n=MUT1RZiseS3dwdrU&q=85&s=ef500f88af7377097e4c7a21843cbe6a)
