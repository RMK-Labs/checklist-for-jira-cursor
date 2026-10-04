# Checklist for Jira for Cursor

Cursor plugin for [Checklist for Jira](https://marketplace.atlassian.com/apps/2797342217/checklists-for-jira) by RMK Labs. It connects Cursor to Checklist for Jira over MCP.

The tools are the same checklist actions the Checklist agent uses in Jira. Each call runs as the person who signed in, on the site they selected.

## Before you connect

Install Checklist for Jira on the Jira site. A Jira admin then turns on **Expose tools to MCP-compatible apps** once for that site. Follow [Enable MCP tools exposure in Jira](https://rmk-labs.atlassian.net/wiki/spaces/CFJWRAA/pages/260177941/Enable+MCP+tools+exposure+in+Jira).

## Install

[Add Checklist for Jira to Cursor](https://cursor.directory/plugins/checklist-for-jira).

You can also add the server in `mcp.json`:

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

To load this repository locally:

1. Copy this directory to `~/.cursor/plugins/local/checklist-for-jira`.
2. Reload the window.
3. Open Customize and confirm the Checklist MCP server is present.

## Sign in

After you finish setting up the connector, Cursor asks you to sign in to Jira. Follow the instructions and select your site.

Setup steps for customers are on the [Cursor MCP connector](https://rmk-labs.atlassian.net/wiki/spaces/CFJWRAA/pages/260112407/Cursor+MCP+connector) page.

## Support

- Documentation: [MCP Server](https://rmk-labs.atlassian.net/wiki/spaces/CFJWRAA/pages/258211841/MCP+Server)
- Privacy policy: [Privacy Policy](https://rmk-labs.atlassian.net/wiki/spaces/CFJWRAA/pages/29065256/Privacy+Policy)
- Email: support@rmk-labs.com
