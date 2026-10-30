# Expert panel review — כותבים מילים (images + tiles + replay label)

**Artifact (local, not pushed):** `a-tut/lang/words/` in `adischlez/eshkol-preview`  
**Hub:** `a-tut/` (3 games)  
**Reviewed:** 2026-10-30 (Asia/Jerusalem) · iPhone 390×844 + iPad 820×1180  
**Screenshots / contact sheet:** `/workspace/eshkol/share/words2/`

## Changes this round
1. Replaced 27 flat SVGs with soft 3D picture-book illustrations (512×512 WebP, EXIF stripped).
2. Replay button label: `🔊 שוב` → `🔊 תשמיעו לי` (+ aria-label).
3. Letter tray always **8 tiles in 2×4** on all levels (was up to 14 / 2×7); larger tiles and letters.

## Image source / license
- Generated with the bot’s `GenerateImage` tool for this product (original assets for אשכול דיגיטלי).
- Not third-party stock; no copyrighted characters.
- Format: WebP 512×512, quality ~90, no EXIF. PNG masters kept under `/workspace/eshkol/share/words2/final/`. Old SVGs backed up at `/workspace/eshkol/share/words2/svg_backup/`.

## Panel verdicts (images + tray + label)

| Expert | Verdict |
|--------|---------|
| 1. Homeroom teacher (א׳) | **Approve** — picturable first-grade words stay clear; 8 large tiles match class iPads/phones; label «תשמיעו לי» is plain Hebrew kids hear. |
| 2. Pedagogue / early literacy | **Approve** — paint-splat colors (אדום/כחול/צהוב/ירוק) cannot be mistaken for object words; sofit letters still come from the word pool; ban of confuse-pairs + given letters as distractors kept. |
| 3. Child psychologist | **Approve** — warmer pictures raise engagement; fewer tiles cut visual load/frustration; no shame change. |
| 4. Speech-language | **Approve** — audio unchanged; replay wording clearer for kids who need the word again. |
| 5. Special ed | **Approve** — 2×4, larger type (≈30px phone / 38px tablet), 44px+ targets, high-contrast navy letters on white. |
| 6. Child UX | **Approve with changes (applied)** — always `cols4`; wider tray; button `white-space:nowrap` + slightly smaller font so «תשמיעו לי» fits 390px. |
| 7. Parent | **Approve** — dad/mom are generic cartoons (not family photos); privacy footer unchanged. |
| 8. Privacy / safety | **Approve** — no child photos, no storage; generated illustrations only. |

**Overall:** Approve after applied fixes below.

## Fixes applied this round
1. Regenerated **צהוב** as yellow paint splat (first draft looked sun-like → clash with שמש).
2. Regenerated **כחול** without a face (match other color splats).
3. Regenerated **כובע** as plain blue baseball cap (wizard hat with star → clash with כוכב).
4. Regenerated **פרח** without a face (clearer “flower”, consistent with object style).
5. Tile count locked to 8; CSS enlarges tiles; replay label + aria updated.

## Open questions for Adi
None blocking. Optional later: if אבא/אמא feel “too realistic CGI”, can soften further; book cover has a tiny landscape (still clearly a book).

## QA (Playwright, local server)
- iPhone 390×844 + iPad 820×1180, levels 1–4.
- 8 tiles / `cols4` on every level; all 27 `.webp` load 512×512; no console/page errors; no broken images.
- Evidence: `round_iphone.png`, `round_ipad.png`, `qa_results.json`, `all_images.png`.
