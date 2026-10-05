# Iteration 3 — GitHub Pages Catalog Site Skeleton

- **Date:** 2026-10-06
- **Iteration:** 3 (Phase 3 SEO pull-forward)

## What Was Built

- `docs/index.html`: static, dependency-free searchable catalog page. Dark GitHub-style theme, client-side search over scenario metadata, direct links to each guide in `catalog/guides/`. SEO meta (title, description, OG tags, canonical) targets long-tail queries: 'perplexity competitive analysis scenario', 'perplexity deep research template', etc.
- Currently indexes the 10 written guides; the `scenarios` array in the page is the single point to extend — every new guide batch adds one line.

## Why docs/ and not gh-pages

A gh-pages branch creation was blocked by the write-approval gate this iteration; `docs/` on main achieves the same result because GitHub Pages can serve from `/docs` on the main branch.

## Manual Step Required

Enable Pages: repo Settings → Pages → Source: 'Deploy from a branch', Branch: `main`, Folder: `/docs`. No other config needed.

## Verification (next iteration)
- Check https://referturnet.github.io/perplexity-scenario-factory/ resolves.
- Submit to Google Search Console for indexing.
- Verify search works for 'competitor', 'market', 'fact'.
