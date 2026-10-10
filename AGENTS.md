# Agent rules for the REKA brand kit

This repository is the **source of truth for the REKA brand**. `brand-guidelines.html` is the master; `ai-docs/` are its exports; `tokens/` transcribes its values; `guide/` covers what it does not and records where later decisions differ. AntaraX has its own kit (`haziqfaris/AntaraX-brand-kit`).

## Before any REKA work, in any repository

- Read `ai-docs/REKA_UNIVERSAL_BRIEF.md`, plus the brief for the task (colours, design language, typography, UI components, voice, product families, landing page, stripe).
- Read `guide/01-reconciliation.md` before stating anything about products, divisions, proof points or colours: it says where the October 2026 decisions override the June guidelines.
- Follow the hard copy rules: no em dashes; no currency figures; flag illustrative figures "(illustrative)"; "Malaysia's first", never "Southeast Asia's first"; "Founder", never CEO; no fabricated metrics, deployments or partnerships.
- Use only the official assets in `assets/`. Never redraw, recolour, rotate, stretch or add effects to the mark.

## When changing this repository

- **Edit `brand-guidelines.html` first**, then re-export or update the matching file in `ai-docs/`, then `tokens/`. Never edit an ai-doc so that it disagrees with the guidelines.
- Do not change `brand-guidelines.html` content without an owner decision. Log every decision in `guide/06-decisions-log.md` with its date; put unresolved items in `guide/07-open-questions.md`; when a conflict in `guide/01-reconciliation.md` is settled, remove its row.
- Keep `tokens/tokens.json` and `tokens/tokens.css` in step.
- Do not edit `reference/` to match the guide.
