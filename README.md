# Google Ads Transparency Scraper — MCP Server

Scrape any advertiser's Google ads from the Ads Transparency Center from your AI agent or MCP client — creative ID, format, first-shown and last-shown dates, how many days the ad was shown and the ad creative itself — as clean structured records. Run it once for an advertiser's current ad library, or attach a monitor store and schedule it: monitoring mode then delivers only the ads no earlier run has seen, becoming a quiet new-ad alert feed for your whole competitive set.

This repo is the MCP listing for the [Google Ads Transparency Scraper](https://apify.com/magnova/google-ads-transparency-monitor) Actor by Magnova on Apify. The server is hosted by Apify at the pinned endpoint below — there is nothing to install or run from this repository; you just point your MCP client at the URL.

## Tools

The pinned connection loads a focused tool set:

- **magnova--google-ads-transparency-monitor** — Scrape any advertiser's ads from Google's Ads Transparency Center, with an optional only-new monitoring mode. Returns structured records: creative ID, format, first/last shown dates, days shown, and the ad creative.
- **fetch-actor-details** — Fetch the Actor's full input schema, pricing, and documentation, so an agent can check parameters and cost before running it.
- **get-actor-run / get-dataset-items** — Run and storage helpers, loaded automatically, used to fetch the results a run produced.

## Connect

Pinned endpoint (Streamable HTTP):

```
https://mcp.apify.com?tools=fetch-actor-details,magnova/google-ads-transparency-monitor
```

On first connect, your client will ask you to sign in with your Apify account (OAuth). If your client cannot do OAuth, pass your Apify API token as an `Authorization: Bearer <YOUR_APIFY_TOKEN>` header instead.

### Cursor / VS Code / other Streamable HTTP clients

```json
{
  "mcpServers": {
    "google-ads-transparency-monitor": {
      "url": "https://mcp.apify.com?tools=fetch-actor-details,magnova/google-ads-transparency-monitor"
    }
  }
}
```

### Claude Desktop

Claude Desktop's config file only runs local commands, so use the `mcp-remote` bridge:

```json
{
  "mcpServers": {
    "google-ads-transparency-monitor": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com?tools=fetch-actor-details,magnova/google-ads-transparency-monitor"
      ]
    }
  }
}
```

The same pinned URL also lives in this repo's `.mcp.json`, and `server.json` is the listing for the Official MCP Registry, published as `io.github.memeanalyst/google-ads-transparency-monitor-mcp`.

## Pricing

Pay per event, billed to your own Apify account: **$0.01 per ad returned — $10 per 1,000 ads**. No start fee, no subscription, and you are only charged for records actually delivered.

## Links

- Actor on Apify Store: https://apify.com/magnova/google-ads-transparency-monitor
- MCP endpoint: https://mcp.apify.com?tools=fetch-actor-details,magnova/google-ads-transparency-monitor

*Ad records come from Google's public Ads Transparency Center.*
