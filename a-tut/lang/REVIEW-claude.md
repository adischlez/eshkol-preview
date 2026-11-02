# Claude a-tut/lang review (local draft — not published)

Base: origin/main `85953ae`. Branch: `claude-atut` at `/tmp/ep-claude`.
Commits: `78ba3d0` (Claude bundle), `d5aee0e` (panel micro-fixes).
Nothing pushed.

## Security / privacy
- No new external hosts. Only existing `mipui-eshkol.goatcounter.com` + `gc.zgo.at`.
- GoatCounter core (URL, path, events `a-tut/new-device|returning-device|visit-n/*|open/*`, device key `atut_anon_v1`) byte-identical to origin/main in all 3 files.
- No new localStorage/sessionStorage/cookies/IndexedDB keys. No new fetch targets.
- No child/teacher names. Footer unchanged (`A-TUT-LANG-01` / per-page footers, `נבנה ע״י אשכול-בוט`, no טיוטה / צוות טלפון).

## Adi rules
- Train dormant, not in menu; `למשחק הבא` → firstletter/words pages; test hook still works; one empty wagon → one-tap place.
- Words: level 1 one-gap + single tap place; auto-advance, no כפתור הבא.
- Script toggle + `?script=` across hub/pages; choice is URL-only (no storage).
- Tap targets ≥44px on header/help/שוב/lv buttons (verified Playwright iPhone+iPad).
- Existing human recordings only; LN map now includes finals ךםןףץ → existing ln_* files.
- Plene Hebrew OK.

## Expert panel (brief)
1. **Grade-1 teacher** — approve: L1 4 choices / L2 6; word spoken every round; finals distractor.  
2. **Literacy pedagogue** — approve: listening prompt in nameletter; final-letter name on 2nd wrong via LN.  
3. **Child psychologist** — approve with note: soft single vibrate; 6 progress stars (not level count on end); confirm before leave/level switch; confetti respects reduce-motion.  
4. **Speech/literacy** — approve: existing audio only.  
5. **Special ed** — approve: fewer choices early; larger taps; progress bar/dots.  
6. **UX** — approve with note: split toggle + toast clear; ← on "לרמה הבאה" matches existing hub "למשחק הבא ←" (RTL forward). Confetti can briefly overlap header but `pointer-events:none`.  
7. **Parent** — approve: help text updated for split toggle.  
8. **Privacy** — approve: analytics unchanged.

### Fixed by panel (commit d5aee0e)
- Confirm default copy: `לצאת מהמשחק…` (was `לצאת למשחק`).
- `askHome()` now calls `askConfirm` with a real yes-handler (was a dead dialog if ever called).

## Playwright (block goatcounter; venv `/workspace/eshkol/share/v9/pwvenv`)
iPhone 13 + iPad Pro 11: menu/train/script/toast/taps/mute-help recover/findall end/nameletter flow/hub+level confirms/words L1=4 L2=6 tiles/deeplink/no console errors — pass.
End-screen auto-advance needs real (or mocked) Audio `onended`; with Audio mock, end UI + 6 stars + next-level button verified. Screenshots: `/workspace/eshkol/share/claude-atut-review/S0*.png`.

## Judgment calls for Adi
1. Keep Claude’s split script toggle + toast, or revert to the simpler single button?
2. Words L1=4 / L2=6 choices (vs always 8)?
3. Speak the word at the start of every words round (more audio)?
4. Soft single vibrate only on wrong (vs longer pattern)?
5. Mid-game ☰ / level-tag confirm dialogs?
6. Confetti + six-star end screen?
7. Keep `←` on "לרמה הבאה" (same as hub) or flip the arrow?

## Verdict
**Safe / OK to show Adi.** Local draft only; do not push until Adi approves.
