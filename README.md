# print-GHC

A standalone, single-file HTML microsite presenting the **Envision Print** managed print program proposal, built for **Genesis Health Clubs** — a multi-location operator headquartered in Wichita, Kansas.

## Contents

- `Envision Print for Genesis - Standalone.html` — the entire site bundled into one file (~13 MB). All images, fonts, and other assets are base64-encoded and gzip-compressed inside the HTML and unpacked into Blob URLs by the page on load.
- `README.md` — this file.

## What's in the page

The microsite walks a prospective client through Envision Print's offering for multi-location brands. Sections include:

- **Hero** — "Built for Multi-Location Operators. Engineered for Brand Integrity."
- **Headline metrics** — first-run approval rate, faster delivery through integration, reduction in creative review, inventory obsolescence.
- **From File Intake to Final Delivery** — template-based storefronts, integrated fulfillment, brand control without bottlenecks.
- **Genesis Print Hub walkthrough** — embedded interactive preview.
- **Operating Principles** — Permissions, Logistics, Integration, and Accountability layers.
- **Full-stack capabilities** — web-to-print storefronts, digital and offset production, finishing, kitting, wide-format, warehousing, pick-pack-ship fulfillment, and KPI dashboards.
- **Catalog shaped for Genesis Health Clubs** — welcome kits, membership cards, business cards, class schedules, club signage, reactivation mailers, event programs, pro shop materials.
- **Network rollout / acquisition-day readiness** and a closing **Start the Conversation** CTA.

## Viewing it

Because every asset is embedded, no build step or web server is required.

- **Local:** open the `.html` file directly in any modern browser (Chrome, Edge, Safari, Firefox). JavaScript must be enabled — the page uses `DecompressionStream` to unpack gzipped assets at runtime, so a recent browser version is recommended.
- **Hosted:** drop the file onto any static host (GitHub Pages, S3, Netlify, etc.) and link to it directly.

On load you will briefly see an "Unpacking…" indicator while the bundled assets are decoded into Blob URLs.

## Editing

The file is a self-contained bundle produced by an external tool — the live markup is stored as a JSON template inside a `<script type="__bundler/template">` block and assets live in a `<script type="__bundler/manifest">` block. Hand-editing the rendered content is impractical; regenerate the standalone file from the original source when changes are needed.
