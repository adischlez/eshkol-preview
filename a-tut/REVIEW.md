# Expert panel · A-TUT-01 · name-the-letter + menu · 29.10.2026 (Asia/Jerusalem)

Artifact: `a-tut/` hub → `lang/` data-driven menu; games `findall` + `nameletter`. Preview only.

## Panel

| Expert | Verdict | Findings |
|---|---|---|
| Homeroom (א׳) | approve | Both games practice letter **names** for א׳ תות; menu under same a-tut link; plene «קוראים». |
| Pedagogue / literacy | approve with changes | Reverse of findall is sound (see→name). **Applied:** option cards show 🔊+number only (no letter glyphs — would spoil). Early rounds avoid SIM look-alikes. |
| Child psychologist | approve with changes | Soft «נסו שוב 🙂», mute, ☰ exit. **Applied:** first tap = hear+select; second tap on same card **or** green «זה! ✓» confirms (clear for age 6). Praise every 4. |
| Speech / early literacy | approve with note | Reuses `q_which_letter`, `ln_*`, `try_again`, `ok*`, `find_done`, `help_letter`. No new TTS (Deepdub exhausted). `help_letter` wording is slightly sound-oriented («לחצו על האות») while UI is name-cards — help **text** is accurate; clip is closest available. |
| Spec-ed | approve with changes | **Applied:** large taps (cards ≥76px, menu ≥64px), equal-weight menu buttons (no green bias), high-contrast navy/cream. |
| Child UX | approve with changes | **Applied:** data-driven `GAMES` array; hub redirects to menu (not findall); deep-link `?topic=` still shows התחל. Big letter + 3-card row fits phone. |
| Parent | approve | Two clear Hebrew titles; sublines explain each game. |
| Privacy | approve | No storage/cookies/mic/child IDs; noindex; credit footer. |

## Applied this pass
1. Hub `a-tut/` → `lang/` (menu), not forced findall.
2. `GAMES` array drives menu; only listed games shown (future slots omitted).
3. New game «איך קוראים לאות?» — big letter, 3 audio options, select→confirm.
4. Same feedback as findall (SFX/haptics, praise every 4, `find_done` at end).
5. Wrong: tapped name → `try_again` → replay three options.
6. Equal menu button styling; early-round SIM distractor filter.

## Open questions for Adi
1. Permanent publish? (still preview until OK).
2. When Deepdub credits return: optional re-record of `help_letter` for name-game wording.

