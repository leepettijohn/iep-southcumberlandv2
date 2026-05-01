# South Cumberland Community Atlas — Preview Bundle

**Status:** Refinement playground export · 2026-05-01 · NOT production-ready

## What's in this zip

- `community-home.html` — South Cumberland community home page (the index.html for /south-cumberland/)
- `beersheba-atlas.html` — Beersheba Springs - Altamont Atlas containing all 3 personas (Resident, Director, Practitioner) in a single file with a top-of-page persona switcher

## Known limitations

This bundle is a design preview, not a deploy-ready release.

- **Most links from the community home page 404.** The home page links to other area Atlases (Tracy City, Sewanee-Monteagle-Pelham, Gruetli) and an Overall report — none of which have been built yet. Only the Beersheba link has a target, and even that target is the single-file artifact, not the multi-page URL structure described in the brief.
- **The Director gate is client-side only.** The password "admin" is visible in the HTML source. This is a soft gate for preview purposes. Production deploys need server-side auth (Netlify URL token validation per the brief).
- **The Practitioner persona is unrefined.** Only the Resident and Director views have been iterated on in the refinement chat. The Practitioner view is in its initial state.
- **Several charts use placeholder or partial data.**
  - The "Coming next iteration" cards on the Resident charts tab haven't been built (none currently — both deferred YoY charts were built last iteration).
  - 3 demographic cards on the Resident charts tab show "Data not yet available" labels: School % Free/Reduced Lunch, Foundation Annual $$, Foundation Compound $$.
  - The 7 respondent demographic charts on the "Who Participated" tab are still placeholders.
- **The strategic recommendations on the Director view are derived placeholders**, not analyst-produced strategic recommendations. The card layout is what's being previewed.
- **Sewanee data quality flag.** The 2026 survey has 2 responses under "Sewanee - Monteagle" and 61 under "Sewanee - Monteagle - Pelham" — these should be reconciled in the survey form.

## To deploy this for real, the following work remains

1. Split `beersheba-atlas.html` into a multi-page structure matching the URL spec: `/beersheba-springs-altamont/2026/persona1/index.html` etc.
2. Build the missing area Atlases (Tracy City, Sewanee, Gruetli) and the Overall report.
3. Build per-area landing pages (`/beersheba-springs-altamont/index.html`) and per-year landings (`/beersheba-springs-altamont/2026/index.html`).
4. Replace the soft Director gate with server-side auth.
5. Wire up real data pipelines so Action Cards reflect analyst-produced strategic recommendations, not derived placeholders.
6. Add the missing demographic data (Tennessee state baseline, school free/reduced lunch, foundation finances).
7. Refine the Practitioner persona.
8. Build the respondent demographic charts on the Who Participated tab.

## Powered by

Innovation Economy Partners · IEP Community Atlas template
