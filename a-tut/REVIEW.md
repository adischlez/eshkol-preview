# Expert panel · A-TUT-01 (א׳ תות · חשבון ושפה) · 28.10.2026 Asia/Jerusalem

Artifacts reviewed: hub `a-tut/`, lang games (findall / fish / train), math shell (unchanged exercises), parent guides, layout_qa phone/tablet/desktop, letter-name audio samples.

## Panel

| Expert | Verdict | Findings → fixes |
|---|---|---|
| Homeroom (א׳) | approve with changes | Letter topics ד/ח/ס/כ removed; three games match classroom letter-name practice. Math still worksheet-like — **open Q** (proposal for Adi). |
| Pedagogue / literacy | approve with changes | Fish similar-distractors on «מומלץ»; train consecutive RTL run. Prompt clarified to «תפסו את הדג עם האות ששמעתם». Train toot + voice-read after fill. |
| Child psychologist | approve | Feedback non-shaming («הדג ברח — נסו שוב», «נסו אות אחרת»). Mute + menu exit always available. ~10 fish rounds / ~8 train segments — short enough. |
| Speech / early literacy | approve | Letter names @0.65 (fix2: Alef / stretched בית / Vav / Tav). Instr @0.85. catch_letter «תִּפְסוּ אֶת הָאוֹת,» + ln_*. Plene+nikud in voice maps. |
| Spec-ed / differentiation | approve | Easy/rec (fish) and easy/hard (train). Tap ≥56px fish/cards. `prefers-reduced-motion` disables swim. Large serif letters. |
| Child UX | approve | Hub חשבון/שפה fits one SE screen. layout_qa **0 fails** (se/iphone/ipad/desk). Credit «נבנה ע״י אשכול-בוט» on every screen. |
| Parent rep | approve | Guide lists 3 games + tip for similar letters. Hub privacy line. |
| Privacy / safety | approve | No localStorage / cookies / mic / analytics / child identifiers. noindex. |

## Applied this pass
- Body game classes `g-fish`/`g-train` (avoid `.fish` matching body).
- Fish prompt wording; softer miss copy.
- Train toot (WebAudio) before letter-name read-back.
- layout_qa: reducedMotion + force taps on animated fish.

## Open questions for Adi
1. **חשבון games** — choose from `MATH_GAMES_PROPOSAL.md` (5 one-liners); not built yet.
2. Mic / speech recognition later? (explicitly out of scope for this preview).
