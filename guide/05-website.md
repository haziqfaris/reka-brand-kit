# 05 Website (reka.re)

Source: `haziqfaris/reka.re`. Design brief: [`ai-docs/reka-landing-page-brief.md`](../ai-docs/reka-landing-page-brief.md) (colours, type, layout, copy rules for the marketing site) and [`ai-docs/reka-stripe-web.md`](../ai-docs/reka-stripe-web.md). Strategy detail: [`reference/strategy/WEBSITE_PLAYBOOK.md`](../reference/strategy/WEBSITE_PLAYBOOK.md) (v0.3).

## Current state (10 October 2026)

- The main site is **one HTML file** (`reka-site-full.html`, about 555KB) with hash sections (#about, #managed, #antarax, #careers, #legal and others), on Cloudflare Pages.
- **Yara** has separate pages at `/yara/` and `/yara/how-it-works/` (the benchmark for layman, cut-to-the-chase product pages), with an assessment that emails holla@reka.re through the `reka-yara` Worker.
- reka.re hosts About, story, careers and legal for **both** REKA and AntaraX; antarax.ai links here.

## Direction

1. **Move to multi-page with clean URLs** (e.g. /about, /story, /managed-ai, /work, /careers, /legal), keeping hash links working as redirects. Each page then stands as its own landing page for search and AI answers. (antarax.ai has already moved.)
2. **REKA story page** from [02](02-story-and-facts.md), in the guidelines' HUD graphic language.
3. **AntaraX pages on reka.re:** an AntaraX intro, the launch announcement and press page, linking to antarax.ai.
4. **reka.re/<product> marketing pages:** AntaraX branding (the A, family colour, product name and one-liner) on REKA's theme, with a bit of the REKA orange gradient (owner, 10 October). Note the guidelines make public REKA surfaces light-first (`#F7F6F3`) with chamfer cuts; whether these pages are light or dark is open (07).
5. **Shared blog at reka.re/blog** (recommended: a subfolder, not a subdomain, so authority accrues to one domain), covering REKA and AntaraX.

## Navigation (playbook)

Work · What we do · Technology · Lab · Insights · About. Persistent CTA: **See what you're missing →** (free three-minute Opportunity Assessment: "What are you not seeing?").

## Homepage sequence (playbook)

Hero → commercial line → assessment CTA → objections (already have a team, AI, vendor, strategy? good) → work → why REKA (2013 to now) → method → value → your team + REKA → values → frontier / Lab → AntaraX bridge (Yara first) → final assessment CTA.

## SEO, AEO and GEO

OWN / STEAL / GAP / EMERGING territories. Canonical answer assets: direct answer → explanation → decision framework → economics → examples → alternatives → FAQ → proof → sources → assessment. Every page: unique title and description, Organization JSON-LD (REKA as parent of AntaraX), FAQPage where there is an FAQ, sitemap with lastmod, llms.txt.

## Known gaps to fix on the live site

- The guidelines make public surfaces **light-first** (`#F7F6F3`); the live site is dark-first.
- The primary line should be **"AI for the physical world."** (guidelines); the site leads with "Built for Progress."
- The site footer and divisions should follow the guidelines (Harmonik, Kinetik, Heuristik, Esoterik).

- The meta description lists "Products PLExyz, Tinara, and AntaraX"; under the graduation rule REKA links to AntaraX products rather than selling them. Rewrite it.
- The site describes six stages (Diagnose → Run) while the playbook says SEE → PROVE → BUILD → ADVANCE; pick one (see 07).
