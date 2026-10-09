# Checklist for Jira for Cursor

Cursor plugin for [Checklist for Jira](https://marketplace.atlassian.com/apps/2797342217/checklists-for-jira) by RMK Labs. It connects Cursor to Checklist for Jira over MCP.

The tools are the same checklist actions the Checklist agent uses in Jira. Each call runs as the person who signed in, on the site they selected.

## Before you connect

Install Checklist for Jira on the Jira site. A Jira admin then turns on **Expose tools to MCP-compatible apps** once for that site. Follow [Enable MCP tools exposure in Jira](https://rmk-labs.atlassian.net/wiki/spaces/CFJWRAA/pages/260177941/Enable+MCP+tools+exposure+in+Jira).

## Install

[![Add Checklist for Jira to Cursor](https://cursor.com/deeplink/mcp-install-dark.svg)](https://cursor.com/install-mcp?name=checklist-for-jira&config=eyJ0eXBlIjoiaHR0cCIsInVybCI6Imh0dHBzOi8vY2hlY2tsaXN0LWZvci1qaXJhLW1jcC5ybWstbGFicy5jby8ifQ%3D%3D)

That opens the install dialog with the name `checklist-for-jira` and the server URL already filled in.

Or add the server in `mcp.json`:

```json
{
  "mcpServers": {
    "checklist-for-jira": {
      "type": "http",
      "url": "https://checklist-for-jira-mcp.rmk-labs.co/"
    }
  }
}
```

The plugin is listed on the [Cursor Directory](https://cursor.directory/plugins/checklist-for-jira). That listing's one-click button names the server `server`. Use the button above, or change Name to `checklist-for-jira` before you install.

To load this repository locally:

1. Copy this directory to `~/.cursor/plugins/local/checklist-for-jira`.
2. Reload the window.
3. Open Customize and confirm the Checklist MCP server is present.

On Enterprise, an admin turns on **Allow Local Plugin Imports** under Dashboard → Settings → Security & Identity → Marketplace and Plugins before a local copy loads.

## Team marketplace

A team admin on a Teams or Enterprise plan imports this repository from Dashboard → Plugins & MCPs → Team Marketplaces → Add Marketplace → Import from Repo:

`https://github.com/RMK-Labs/checklist-for-jira-cursor`

`.cursor-plugin/marketplace.json` lists the Checklist for Jira plugin. Each person installs it from Customize and signs in to Jira. This does not register the server for Cloud Agents. Add the same HTTP server under Dashboard → Plugins & MCPs for that.

## Sign in

After you finish setting up the connector, Cursor asks you to sign in to Jira. Follow the instructions and select your site.

Setup steps for customers are on the [Cursor MCP connector](https://rmk-labs.atlassian.net/wiki/spaces/CFJWRAA/pages/260112407/Cursor+MCP+connector) page.

## Support

- Documentation: [MCP Server](https://rmk-labs.atlassian.net/wiki/spaces/CFJWRAA/pages/258211841/MCP+Server)
- Privacy policy: [Privacy Policy](https://rmk-labs.atlassian.net/wiki/spaces/CFJWRAA/pages/29065256/Privacy+Policy)
- Email: support@rmk-labs.com

<!-- Smoke test: cloud agent can open a pull request against checklist-for-jira-cursor. Safe to close without merging. -->
