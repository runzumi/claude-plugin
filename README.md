# Runzumi

Analyze your GitHub Actions runners on [Runzumi](https://runzumi.com) from Claude: job duration, queue time, success rate, compute costs and why a CI job failed.

The plugin is for analytics and investigation. It can't start, cancel or change CI jobs. Setup, billing and repository settings stay on the Runzumi website.

## Get started

1. [Create a Runzumi account](https://app.runzumi.com/onboarding), then create or join a workspace and connect GitHub.
2. Install this plugin and sign in with your Runzumi account when Claude asks.

## Install

In Claude Code 2.1.275 or later, run:

```
/plugin install runzumi --marketplace runzumi/claude-plugin
```

In earlier versions, add the marketplace first, then install the plugin:

```
/plugin marketplace add runzumi/claude-plugin
/plugin install runzumi@runzumi
```

From a terminal, use `claude plugin marketplace add runzumi/claude-plugin` and `claude plugin install runzumi@runzumi`.

## Skills

- [connect-runzumi](skills/connect-runzumi/SKILL.md): connect Runzumi, find your workspace and open the dashboard.
- [explain-ci-slowness](skills/explain-ci-slowness/SKILL.md): find out why CI is slow by comparing job duration, queue time and job attempts.
- [explain-compute-costs](skills/explain-compute-costs/SKILL.md): explain compute usage and costs for a workspace, a repository or a job.
- [investigate-failure](skills/investigate-failure/SKILL.md): find out why a GitHub Actions job failed from its details and logs.
- [choose-runner-size](skills/choose-runner-size/SKILL.md): choose a `runs-on` label and runner size, or check if a larger runner would help.

## Try asking

- Show job duration, queue time and success rate for my repository this week.
- Why did my GitHub Actions job fail? Use its details and logs.
- Show my workspace's compute usage and costs for the last 31 days.

## What the plugin connects to

The plugin connects to one remote MCP server, `https://mcp.runzumi.com/mcp`. You sign in with your Runzumi account through Claude's OAuth flow. The plugin never asks you for passwords or tokens.

The plugin ships instructions only. It runs no local code or scripts.

The server reads workspace, repository, job, usage and log data that your Runzumi account can access. It can save display preferences, such as a default workspace or repository. Log excerpts enter the conversation only when you ask for them. The plugin can't start, cancel or change CI jobs.

## Links

[Support](https://runzumi.com/support) · [Privacy](https://runzumi.com/privacy) · [Terms](https://runzumi.com/terms)
