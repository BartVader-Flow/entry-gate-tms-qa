# QA Entry Gate Concept

Static slide decks on branch **`gh-pages`**.

## Decks

The primary URL (`index.html`) and the versioned URL (`index-v2.html`) now serve the **same, current deck** — the old v1 target-state-only deck has been retired and overwritten. Both files are kept in sync so existing bookmarks/links keep working.

| File | Live URL |
|------|----------|
| [`index.html`](index.html) — primary URL | https://bartvader-flow.github.io/entry-gate-tms-qa/ |
| [`index-v2.html`](index-v2.html) — versioned URL, identical content | https://bartvader-flow.github.io/entry-gate-tms-qa/index-v2.html |
| [`preview-v2.html`](preview-v2.html) — always latest from branch | https://bartvader-flow.github.io/entry-gate-tms-qa/preview-v2.html |

Navigate with arrow keys (← →).

### Current deck

Cover + **12 content slides**, in this order: **1** lifecycle & who owns what (RACI overview) · **2** four pillars & strategy hub · **3** quality layers + enforcement · **4–8** the five responsibility-shift comics · **9** Entry Gate · **10** QA workflow (internal) · **11** tandem QA capacity plan (from Excel) · **12** module onboarding + dual-track transition (CargoBeamer & RCG).

Meta `deploy-version`: **20260701-v2-17** · green badge **LIVE** bottom-right; orange **STALE** = Pages CDN behind GitHub.

### Visual design (v2-17)

The deck follows the visual language of Pablo's "Testing Framework" Confluence deck (QIT space): light mint background, a Rail-Flow wordmark + mini rail-track logo in every slide header, and a thin color-coded top border per slide category — green for process/strategy slides, blue for enforcement & QA-workflow slides, coral for responsibility-shift comics & the Entry Gate. The cover slide carries a corner logo and a subtle "R·F" watermark. This was a purely additive CSS/HTML re-skin — no slide content, order, or copy was changed.

**v2-17 hotfix:** v2-16 had a regression on the cover slide — the logo was placed inline at the top of the centered content stack (with `margin-bottom`), which made the already content-dense cover (title, subtitle, 2-column grid, nav) taller than the fixed slide height, clipping the bottom cards. Fixed by making the logo `position:absolute` in the top-left corner so it no longer affects the flex layout at all — cover spacing is back to its original, pre-redesign values. Also corrected the logo artwork itself (removed an inaccurate train-car icon; it's now wordmark + rail-tie line only, matching Pablo's reference) on the cover and all 12 mini headers.

> The retired v1 deck (9 content slides, `deploy-version 20260701-6`) is no longer published, but remains fully recoverable from the `gh-pages` git history if ever needed.

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
