# NOTES — the Haitian Creole rendering (ht.v1)

*The fifty-fourth chair. The first French-lexifier creole at the table.*

## The trail

- **Relay burn**: lit 2026-09-02 11:15, closed 18:16 — 23,213 verses in ~7 hours
  (glm tier ladder, one z.ai lane). Burn froze at 23,165; a 48-verse stubborn
  press (parallel, per-verse catch) closed the store. The 48 were the usual
  relay chunk-seam pairs.
- **Census/gleaning rounds**: 467 flagged → 45 → ~12 sticky → 0 (sealed).
  Round-1 classes: bracket-English 192, xml/ascii brackets 140, Hebrew leak 68,
  non-Latin bleed 47, Cyrillic 19, rails rejections seyè 16 + letènèl 1,
  editorial arrows 14, malformed markers 14. Rounds 1–2 pressed through the
  rails; the sticky tail went to hand.
- **Hand repairs** (model `fable-5-hand`, 16 verses): ⟨is⟩→⟨se⟩ or dropped
  (Ps 147:5, SoS 5:13); ⟨the⟩ dropped (Josh 21:11); editorial arrows cut
  (Eccl 2:22, 2 Kgs 3:21, 2 Kgs 21:20 ⟨HaElohim→Yawe⟩); ASCII brackets
  (Mic 6:14, Ps 136:25 — refrain rebuilt to the 136:1 house style
  "hesed ⟨li⟩ genyen"); Josh 15:51 garbled number phrase rebuilt ("onz site");
  1 Kgs 22:2 token-less twice → rebuilt by hand (Yehochafat, not the press's
  "Yehochoua-Chofat"); Jer 29:23 token-less with a CJK leak (手) → rebuilt on
  the en token spine (22 tokens, kethib הו/ידע split preserved).

## Lessons

- **The Ofèl false positive**: Java's default `\b` is ASCII — è breaks the
  word, so `(?i)\b(of)\b` matched inside **Ofèl** (Neh 3:26, 11:21) and would
  have gleaned two clean verses forever. Census + gleaning English regexes now
  carry `(?iU)`. On accented-Latin chairs, every bare-word stoplist regex
  needs Unicode word boundaries.
- **Accent-dropped rejection variants earn their keep**: the (?iU)
  seyè/letènèl regexes with è/e alternates caught 17 rails-rejection verses
  the plain forms would have missed.

## Tekoa review (Bondye survey)

24 verses carried *Bondye*. Verdict: **22 lawful** — parenthetical
Name-explanations with the transliteration held ("El Chadday (Bondye ki gen
tout pouvwa)", "El Olam (Bondye ki pou tout tan)") and common-noun seats
(Job 20:5 "moun san bondye" for חנף; Deut 23:18 cult-service idiom).
**2 class-A fixed**: Ps 30:5 (חסידיו mis-glossed "kavalye ⟨li⟩ Bondye a" —
rebuilt "moun ki fè byen devan ⟨li⟩ yo"); Exod 13:19 (Bondye at an אלהים
seat → Elohim; also a corrupted token surface יפקod → יפקד).
Sealing census: bondye-review = 22, all lawful.

## Aleph-tav audit

Round 1: 56 defective — 54 spurious markers stripped, 21 sentence edits,
39 misaligned gleaned + re-pressed, 3 unresolved to hand:
- Dan 3:12 — Aramaic יתהון is a suffixed pronoun ("yo"), not a bare marker.
- Ezek 36:13 — kethib אתי is the archaic 2fs pronoun ("ou menm"); kethib the ground.
- Isa 11:4 — **phantom את surface** where the record reads the second ארץ;
  the verse has no את at all. Surface restored, both TR markers cut.
Round 2: 1 misaligned survivor (Jer 29:23, re-pressed token-less → hand).
Round 3: **0 / 0 / 0 — clean.**

## The seal (2026-09-02 ~19:00)

files=23213 · empty=0 · no-tokens=0 · all leak classes 0 · seyè/letènèl/
granmèt/jewova/lanfè-at-שאול 0 · **Yawe 5,800 · Elohim 1,847** · ⟨את⟩ verses
7,482 · aleph-tav audit clean.

Open for Scott: the **ch-for-ש** orthography ruling (Cheol / Moche / Machiya —
kreyòl "ch" = /ʃ/, the biggest orthographic break in the chair lineage) and
the rails' 10 lighting flags.

— the shovel, with the assayer's checks in the groove
