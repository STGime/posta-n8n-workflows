# Posta n8n Workflows

Ready-to-import [n8n](https://n8n.io) workflow templates for automating social media with **[Posta](https://getposta.app)** — create, schedule, and publish to **8 networks** (LinkedIn, TikTok, Instagram, YouTube, Pinterest, Facebook, Bluesky, Threads) from your automations.

All templates use the verified [`n8n-nodes-posta`](https://www.npmjs.com/package/n8n-nodes-posta) community node.

## Workflows

| Workflow | What it does | Requires | Import |
|----------|--------------|----------|--------|
| **Blog post → social media** | Reads your blog RSS feed and schedules a social post (with the article image) across your connected accounts. | Posta | [JSON](workflows/blog-to-social-media.json) · [Guide](https://getposta.app/workflows/blog-to-social-media) |
| **Blog post → LinkedIn carousel** | Summarizes a new blog post into a 5-slide LinkedIn carousel PDF — AI text (DeepSeek) over AI backgrounds (fal.ai), assembled by Posta. | Posta (Professional), DeepSeek, fal.ai | [JSON](workflows/blog-to-linkedin-carousel.json) · [Guide](https://getposta.app/workflows/blog-to-linkedin-carousel) |
| **5-day product launch campaign** | Turns a product into a 5-day, multi-platform launch campaign with per-network captions written by AI. | Posta, DeepSeek | [JSON](workflows/product-launch-campaign.json) · [Guide](https://getposta.app/workflows/product-launch-campaign) |
| **YouTube video → social media** | Reads your YouTube feed, grabs the latest video and thumbnail, and drafts AI promo posts for every platform. | Posta, DeepSeek | [JSON](workflows/youtube-to-social-media.json) · [Guide](https://getposta.app/workflows/youtube-to-social-media) |

## How to import

**Option A — Import from URL (fastest):** in n8n, open the **⋯ menu → Import from URL** and paste the raw JSON link, e.g.

```
https://raw.githubusercontent.com/STGime/posta-n8n-workflows/main/workflows/blog-to-social-media.json
```

**Option B — Import from File:** download a `.json` from [`workflows/`](workflows/) and use **⋯ menu → Import from File**.

After importing, connect your credentials (see the table) and update the trigger / feed URL as needed. Each workflow is documented in-canvas with sticky notes.

## Setup

1. **Install the node** — in n8n: **Settings → Community Nodes → Install** `n8n-nodes-posta`.
2. **Get a Posta API token** — sign up at [getposta.app](https://www.getposta.app) (14-day free trial, no credit card) → **Settings → API Tokens**.
3. **Add credentials** — open any Posta node, create a credential with your token (Base URL `https://api.getposta.app/v1`). Add DeepSeek / fal.ai credentials for the AI workflows.

## Notes

- These templates contain **no credentials or secrets** — n8n will prompt you to select your own on import.
- More guides and a browsable gallery: **[getposta.app/workflows](https://getposta.app/workflows)**.
- Want agents to drive Posta directly (MCP, Claude Code, REST)? See **[getposta.app/agents](https://getposta.app/agents)**.

## License

[MIT](LICENSE) — free to use, modify, and share.
