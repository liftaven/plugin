# Liftaven plugin

[Website](https://liftaven.com) · [MCP setup](https://liftaven.com/agents/) · [Privacy](https://liftaven.com/privacy/) · [Support](https://github.com/liftaven/plugin/issues)

Investigate your website with evidence from connected Google Search Console, Google Analytics 4 and Bing Webmaster Tools. This package pairs Liftaven’s remote OAuth MCP server with a skill for choosing the right reports, comparing dates and metrics, and preparing website improvements for review.

## What you can do

- Discover the websites and reporting accounts you have authorized.
- Compare search clicks, impressions, CTR and query/page performance.
- Examine organic landing-page engagement and configured key events in GA4.
- Inspect available Bing search, crawl and sitemap reports.
- Read connected website content and prepare exact edit proposals, with a review link to Liftaven Actions.
- Submit a sitemap after an explicit request. Submission does not guarantee indexing.

Example requests: “Which high-impression pages have low CTR?”, “Compare organic landing-page engagement over the last 28 days”, or “Read this page and prepare a title improvement using its search data.”

## Connect

Install this plugin in a compatible client, then complete browser OAuth for the bundled endpoint:

```text
https://mcp.liftaven.com/mcp
```

Connect or repair providers in your Liftaven account. Only data available through your authorized connections can be retrieved. For Claude Code, authenticate the Liftaven server through `/mcp` when prompted. This repository contains `.claude-plugin/plugin.json`, `.codex-plugin/plugin.json`, `.mcp.json` and `skills/liftaven/SKILL.md`. It has no install hooks or bundled executables.

For clients that require stdio, see [liftaven-mcp on npm](https://www.npmjs.com/package/liftaven-mcp) and the [MCP server repository](https://github.com/liftaven/mcp-server). The standalone [agent skill](https://github.com/liftaven/agent-skill) is also available.

## Permissions and limits

Analytics and advertising tools are read-only. Search tools also support explicit sitemap submission. Website edits remain proposals until you review and apply them in Liftaven; GitHub changes create a pull request and never merge automatically. Missing connections return connection guidance, not fabricated reports. Provider reports can be delayed, sampled or incomplete, and different metrics and attribution windows must not be added together.

Your client receives the report and content data requested through the tools. Provider credentials stay on the server. Revoke access in Liftaven and remove the connection from your client when no longer needed. Read the [privacy policy](https://liftaven.com/privacy/) and [terms](https://liftaven.com/terms/) for data handling and service conditions.

## Development

Public snapshots are published by GitHub Actions from an allowlisted source directory, without exporting private application history. Report connection or packaging issues through [GitHub Issues](https://github.com/liftaven/plugin/issues); never include tokens, login codes or private report data.

MIT licensed. Directory submission does not imply listing, endorsement or approval by a client provider.
