# Expert panel review — במה מתחילה המילה?

**Artifact (local, not pushed):** `a-tut/lang/firstletter/` in `adischlez/eshkol-preview`  
**Hub:** `a-tut/lang/` (4th menu game, separate; does not replace others)  
**Reviewed:** 2026-10-30 (Asia/Jerusalem) · iPhone 390×844 + iPad 820×1180  
**Screenshots / QA:** `/workspace/eshkol/share/firstletter1/`

## Word bank (speech / phonology lock)

### KEEP — 24 words (unambiguous first letter for age 6)
| Word | First | Note |
|------|-------|------|
| דג | ד | clear stop |
| לב | ל | continuous |
| יד | י | clear |
| פרח | פ (פּ) | clear |
| פיל | פ | clear |
| ספר | ס | clear; never same-round with ש/צ |
| מים | מ | clear; Whisper may show מיים (known quirk) |
| שמש | ש (שׁ) | shin only; never same-round with ס |
| ירח | י | clear |
| דלת | ד | clear |
| דב | ד | clear first; Whisper sometimes drops final ב → «דו» |
| חתול | ח | OK; כ/ק never in pool / same round |
| צהוב | צ | clear; never same-round with ס |
| ירוק | י | clear |
| פרפר | פ | clear |
| נחש | נ | continuous |
| רגל | ר | continuous |
| גמל | ג | clear |
| סוס | ס | clear; never with ש/צ |
| לימון | ל | continuous |
| זבוב | ז | clear |
| מטוס | מ | first מ clear; Whisper sometimes מתוס (medial ט/ת) — not first-letter risk |
| גזר | ג | clear (re-TTS + Whisper OK) |
| חלב | ח | OK; never with כ/ק |

### EXCLUDED (with reasons)
| Word | Reason |
|------|--------|
| עץ | starts with **ע** (ambiguous with א) |
| עוגה | starts with **ע** |
| כלב | starts with **כ** (כ/ק/ח cluster) |
| כחול | starts with **כ** |
| כובע | starts with **כ** |
| כוכב | starts with **כ** |
| בית | starts with **ב** (ב/ו) |
| בלון | starts with **ב** |
| אבא | starts with **א** (א/ע/ה) |
| אמא | starts with **א** |
| אדום | starts with **א** |
| תפוח | starts with **ת** (ט/ת) |
| **צב** | starts with צ but TTS/Whisper often → «סב» (צ/ס); dropped after speech check — **צהוב** covers צ |

Also excluded by policy as starters (none in bank anyway): **ה כ ק ט ת ב ו שׂ**.

### Same-round bans (all levels)
א/ע(/ה) · כ/ק/ח · ט/ת · ס/ש(ׂ risk) · ב/ו · צ/ס  
Distractor pool = מ ל נ ר ש ס ז ד ג פ צ י ח only. 2600 random builds: 0 sound clashes.

## Levels
1. 3 far options · 2. 4 options · 3. 4 + one shape-near · 4. 6 + shape-near  
Sound bans always on. No «הבא»; wrong → «נסו שוב» + replay **word** (never wrong letter name); 🔊 תשמיעו לי; hub/home confirm on home; celebration; anonymous; credit אשכול-בוט.

## Panel verdicts

| Expert | Verdict |
|--------|---------|
| 1. Homeroom (א׳) | **Approve** — PA initial consonant; plain title; 6-word run; levels match class warm-up. |
| 2. Pedagogue / early literacy | **Approve** — continuous-first preference; confuse pairs never co-present; L1 far shapes. |
| 3. Child psychologist | **Approve** — soft wrong feedback, hint blink after 3, celebration, exit confirm, no comparison. |
| 4. Speech / phonology | **Approve with changes (applied)** — dropped ע/כ/ב/א/ת starters; dropped **צב** after ASR סב; kept מטוס (first מ clear); ח only without כ/ק. |
| 5. Special ed | **Approve** — large tiles (64–84px), high contrast, one tap, optional replay, reduced-motion. |
| 6. Child UX | **Approve** — matches hub shell; 3/2×2/3×2 grids; fits 390px; menu shows 4th game. |
| 7. Parent | **Approve** — no parent guide needed; listen/look/tap; privacy line clear. |
| 8. Privacy / safety | **Approve** — no storage/cookies/names; noindex; no ads. |

**Overall:** Approve after applied fixes.

## Fixes applied
1. Phonology filter: only clear starters; excluded list above.  
2. Regenerated + Whisper-verified מטוס / גזר (nikud, −10%); dropped צב.  
3. Hub `GAMES` entry `href:"firstletter/"`.  
4. SOUND_GROUPS + distractor pool enforced on L1–L4.

## Open questions for Adi
Optional later: re-add צב only with human/Deepdub clip that clearly separates צ from ס.

## QA (Playwright)
- Hub shows 4 games; navigates to firstletter.  
- iPhone + iPad, L1–L4 full runs; option counts 3/4/4/6; 0 sound clashes; all 24 webp + audio 200; wrong → נסו שוב; celebration; home confirm.  
- Evidence: `hub_iphone.png`, `*_L{1-4}.png`, `round_iphone.png`, `round_ipad.png`, `qa_results.json`.
