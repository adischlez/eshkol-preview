# Expert panel · A-TUT-01 (א׳ תות) · 28.10.2026 evening (Asia/Jerusalem)

Pass: findall-only menu + slower TTS + י=יוּד. Artifacts: hub/lang/math, layout_qa se/iphone/ipad/desktop, Whisper ASR on all ln_*, sample_slow.mp3.

## Panel (brief)

| Expert | Verdict | Findings |
|---|---|---|
| Homeroom (א׳) | approve | Language = מצאו את האות only (Adi request). Math unchanged; games still open Q. |
| Pedagogue / literacy | approve | Find-the-letter practices all 22 letter names; no letter-week drill. |
| Child psychologist | approve | Non-shaming feedback, mute, menu exit. Shorter language surface = less choice overload. |
| Speech / early literacy | approve with note | Tempos: letter names **0.55**, letter sounds 0.65 (unused — no snd_* in remaining games), instructions **0.75**. י spelling `הָאוֹת, יוּד.` → ASR «האות יוד». critical_fail []. Whisper flaky on samekh→«שמך», pe→«פי» (ear OK). |
| Spec-ed | approve | Large taps, credit footer, reduced-motion CSS still present for dormant fish. |
| Child UX | approve | layout_qa **0 issues** (overflow/credit/fish-train-hidden). Credit on hub/lang/math. |
| Parent | approve | One language game — simpler to explain. |
| Privacy | approve | No storage/cookies/mic/analytics/child IDs. noindex. |

## Applied this pass
- Hub + lang menu: only «מצאו את האות»; fish/train removed from navigation (code left dormant).
- Re-recorded all remaining lang+math narration via Deepdub dd-etts-3.4 Meditation Guide at slower tempos.
- י → יוּד (verified Whisper).
- Credit «נבנה ע״י אשכול-בוט» on every screen.

## Open questions for Adi
1. Math game picks from MATH_GAMES_PROPOSAL.md (unchanged).
2. Publish permanent link? (preview only until approved).


---

## Pass · 28.10.2026 evening · start-button + haptics (Asia/Jerusalem)

**Root cause of dead «בואו נתחיל»:** commit bee404f truncated `lang/index.html` after the TOPICS array (333 lines of JS removed) — no `btnQuick` handler / `startTopic` / `startFindAll`. Restored from 3e69cc0; kept findall-only TOPICS.

**Fixes**
- Restored full game JS; start unlocks AudioContext on tap.
- Correct tap: WebAudio success arpeggio + `navigator.vibrate([12,40,18])` (Android) / iOS switch-checkbox haptic fallback.
- Wrong tap: soft error tone + longer vibrate pattern; narrate **tapped** letter name (`ln_*` @0.55) then `try_again` («נַסּוּ שׁוּב.» Deepdub @0.75, ASR «נסו שוב.»); `inputLocked` while speaking.
- QA assert: `#btnQuick` → `#sc-ex` + 22 `.azcell` + prompt; deep-link `?topic=findall`; math quick + all 4 topics start. Chromium iPhone UA. WebKit MiniBrowser blocked on host (missing libevent) — Chromium+Safari UA used instead.


## Pass · hub letters-only (same evening)

Hub `a-tut/index.html` now redirects straight to `lang/?topic=findall`. Math section removed from hub navigation; `a-tut/math/` kept on disk (dormant). Credit retained on hub fallback + lang screens.
