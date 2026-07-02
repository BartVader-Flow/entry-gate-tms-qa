# QA Entry Gate Concept

Static slide decks on branch **`gh-pages`**.

## Decks

| Version | File | Live URL |
|---------|------|----------|
| **v1** — target-state concept | [`index.html`](index.html) | https://bartvader-flow.github.io/entry-gate-tms-qa/ |
| **v2** — rollout + QA leads session | [`index-v2.html`](index-v2.html) | https://bartvader-flow.github.io/entry-gate-tms-qa/index-v2.html |
| **v2 preview** (always latest from branch) | [`preview-v2.html`](preview-v2.html) | https://bartvader-flow.github.io/entry-gate-tms-qa/preview-v2.html |

Navigate with arrow keys (← →).

### v1 (unchanged)

Cover + **9 content slides:** lifecycle · responsibility shift (5 comics) · Entry Gate · QA workflow · quality layers.

Meta `deploy-version`: **20260701-6** · counter on last slide: **10 / 10** (cover included).

### v2 (second foliensatz)

Cover + **12 content slides:** slides **1–6** same as v1 · **7** four pillars & strategy hub · **8** Entry Gate · **9** tandem QA capacity plan (from Excel) · **10** QA workflow (internal) · **11** module onboarding + dual-track transition (CargoBeamer & RCG) · **12** quality layers + enforcement.

Meta `deploy-version`: **20260701-v2-14** · green badge **LIVE** bottom-right; orange **STALE** = Pages CDN behind GitHub.

### Deploy / “not updated” troubleshooting

| Check | What it means |
|-------|----------------|
| Badge **`… · LIVE`** | This URL matches `version.json` on `gh-pages`. |
| Badge **`… · STALE`** + orange banner | GitHub branch is newer; **Pages has not redeployed** (not your browser). |

**Always-current HTML preview (renders as slides, not raw source):**  
https://htmlpreview.github.io/?https://raw.githubusercontent.com/BartVader-Flow/entry-gate-tms-qa/gh-pages/index-v2.html

Or open [`preview-v2.html`](preview-v2.html) on Pages for the same link.

**Do not use** `cdn.jsdelivr.net/gh/.../index-v2.html` — jsDelivr serves HTML as plain text.

**Fix stuck Pages:** Repo **Settings → Pages → Build and deployment** → re-select branch **`gh-pages`** / **`/ (root)`** → **Save** (forces a new build).
