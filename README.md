[README.md](https://github.com/user-attachments/files/28044346/README.md)
# Search Labs prototype

A self-contained HTML prototype of the Elastic Search Labs site, built from Figma designs (Sunny's Blog file).

## What's in here

- `index.html` — the entire site in a single file (HTML, CSS, and JS inlined). No build step, no dependencies.

## Pages

The prototype is a single-file SPA. Routing is handled by toggling `[hidden]` on page sections.

- **Homepage** (`data-page="main"`) — "New and popular on Search Labs" with featured + latest articles, plus Tutorials, Examples, Integrations, and CTA sections
- **Blog list / Title: Tag topics** (`data-page="blogs"`) — 2-column grid of blog cards with filterable category sidenav. Reachable from "View all" and "View more articles" buttons, or by clicking the "Agentic AI" chip on the article page
- **Article page** (`data-page="article"`) — the long-form article ("Top Vulnerabilities and Attack Vectors in Agentic AI Systems"). Grey hero with multi-author avatar stack
- **Tutorial page** (`data-page="tutorial"`) — "Install Elasticsearch"
- **Example page** (`data-page="example"`) — Prompt Library
- **Observability Lab** (`data-page="obs"`) — featured post + Latest articles (9 in a 3×3 grid)
- **Security Lab** (`data-page="sec"`) — featured post + 4 named sections (Threat Command, Product Updates, Reports, Enablement)

## Navigation features

- **Top nav** with announcement bar, slides up on scroll-down, back on scroll-up
- **Secondary lab nav** (sticky pill row) with per-lab hover colors:
  - Elasticsearch Lab → yellow `#FFDE7D`
  - Observability Lab → peach `#FF9B85`
  - Security Lab → magenta `#F04E98`
- **Left sidenav** with `/ GO TO PAGE` eyebrow, contents change per page
- **Smooth scroll** to section anchors on Security Lab and Observability Lab pages

## Local viewing

Just open `index.html` in a browser. No server required.

```bash
open index.html
```

## Notes

- Display font is Manrope (fallback for Mier B which is the spec font but isn't licensed for this repo)
- Body font is Inter, mono is IBM Plex Mono
- Article hero styling for the MCP-style article is wrapped in a revertible CSS block; see comments in `index.html` marked `ARTICLE-HERO-V2`
- Yellow accent tokens from the Figma spec are intentionally not implemented
