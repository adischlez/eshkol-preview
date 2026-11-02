# Expert panel · א׳ תות subject menu + math addsub (2026-11-02)

Artifact reviewed: `/a-tut/` subjects, `/a-tut/math/` menu, `/a-tut/math/addsub/` (Claude חיבור וחיסור). Screenshots in `/workspace/eshkol/share/atut-subjects/`. Playwright QA passed (goatcounter blocked).

## 1. Homeroom teacher (א׳)
**Approve with changes (applied).** Subject split matches class reality (שפה / מתמטיקה). Addsub levels 1→4 match grade-1 ten-frame progression (subitize → friends of 10 → ±/sub to 10 → crossing ten to 20). Ped-note on subjects tightened to “שפה — … · מתמטיקה — …”.

## 2. Math didactics
**Approve.** Level 1 five-colouring (blue 5 + orange remainder) teaches five-structure; level 4 fill-ten then continue is correct crossing-ten scaffolding. Wrong-answer hint after 2 misses (blue five) is pedagogically sound. Device TTS is OK for classroom; optional local clips not required.

## 3. Child psychologist
**Approve.** Non-shaming feedback (“נסו שוב 🙂 אפשר להציץ”), peek tool, mute, hub escape with confirm. No scores/leaderboards. Run size 8 is age-appropriate.

## 4. Speech / literacy
**Approve with note.** Default path is device `speechSynthesis` he-IL (variable quality by phone). Script toggle present for Hebrew UI. Numbers stay LTR in tiles/eq. Open question: whether Adi wants Phonikud clips generated later (script not published).

## 5. Special education
**Approve.** Large tiles (≥44px), one prompt at a time, peek + hear-again, high contrast navy/cream. Cursive optional. ADHD-friendly short rounds.

## 6. Child UX
**Approve with fixes applied.** Matching graphic language (navy header, gbtn cards, green primary). Script toggle href now refreshes on math menu. Overflow check clean (aside intentional off-screen hapticLab). iPhone / iPad / desktop shots OK. Lang ⌂ returns to subjects; addsub ☰ to math menu.

## 7. Parent
**Approve.** Plain start → levels → play. Privacy line visible. No account.

## 8. Privacy & safety
**Approve.** Only GoatCounter `mipui-eshkol` + `atut_anon_v1` (UUID never sent). No cookies beyond that key, no child PII, no ads. `fetch(audio/manifest.json)` is same-origin optional. Stripped `tools/gen_voice.py` and comments that pointed at publishing it. Paths: `a-tut/open/addsub`, page `/a-tut/math/addsub/`.

## Fixed this pass
- Subject page + math menu; Claude game at `math/addsub/` (not under `lang/`)
- Analytics paths + product id A-TUT-MATH-01
- Math menu script-toggle updates game link
- Lang hub ⌂ → subjects; legacy `a-tut-lang`→lang, `a-tut-math`→math
- Old draft math hub moved to `math/_draft-topics/` (unlinked)

## Open questions for Adi
1. Generate Phonikud clips later, or stay on device TTS?
2. Keep `_draft-topics` offline, or delete from repo?
