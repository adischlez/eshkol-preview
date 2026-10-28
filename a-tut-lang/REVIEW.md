# Expert panel — A-TUT-LANG-01 (מצאו את האות + mipui)

Date: 2026-10-28 · Grade א׳ · Preview only

## Verdicts

| Expert | Verdict | Notes |
|--------|---------|-------|
| Homeroom teacher | approve with changes | מצאו את האות moved to end of menu so letter topics come first; תרגול זריז starts with ד׳ not a 22-letter game. |
| Pedagogue / literacy | approve | Random order of letter names; grey-out on correct; soft re-say; highlight after 2 misses; no finals (סופיות) — correct for recognition of base forms. |
| Child psychologist | approve | Feedback "נסו שוב 🙂" / "הקשיבו שוב 🙂"; celebration + עוד סיבוב; no timer, no scores stored. |
| Speech / early literacy | approve with changes | Letter clips are «הָאוֹת {name}» @ tempo 0.75 (Deepdub Meditation Guide). ASR noisy on טית/קוף shorts — audible; keep. No mic yet (awaiting Adi). |
| Special ed / a11y | approve | Tap targets ≥44px on 375/390; high contrast navy/ink; mute available; one prompt at a time. |
| Child UX | approve with changes | SE menu with 6 topics overflowed ~19px → compacted @media max-400 (padding/qk/tbtn). Findall grid fits 390×844 and 375×667 without scroll. |
| Parent | approve | Help text plain; progress «N מתוך 22»; שוב replay obvious. |
| Privacy | approve | No localStorage / cookies / analytics / child identifiers. |

## Fixes applied this pass
1. Menu SE overflow: tighter @media(max-width:400px) + body padding-bottom 8px.
2. מצאו את האות placed last in TOPICS (scaffolding + quick practice).
3. layout_qa.mjs: azgrid path + minH/count/overflow checks; 0 fails.
4. Weak ln_tet / ln_qof re-recorded @0.75.

## Open questions for Adi
1. Microphone input for letter names — wait for decision (not built).
2. Should «תרגול זריז» include מצאו את האות as the last station, or skip it? (currently included as last of 6.)

## Voice update 2026-10-28 (letter names)
- Tempo letter clips (`ln_*`, `name_*`): **0.65** (instr stays 0.85)
- Classroom names: הֵיי (not הא), צַדִּיק (not צדק), פֵּיי, וָב (TTS respelling → vav not wou), כַּף
- Phrase shape: `הָאוֹת, {name}` (comma pause)
- Samples: `/workspace/eshkol/share/v7/{hey,tsadik,vav,all_letters}.mp3`
