# Revision Notes

Track what you've added, removed, or rewritten here.

## 2026-05-07 — book.md created

Drafted `book.md` for the bundle. Audience: liberal-arts gen-ed students completing a quantitative-reasoning requirement. Scope: 13 chapters from Sets through "Math and …" Voice notes specify grounded examples for all math/physics, plain-English glosses for notation, and math density over word count.

## 2026-05-07 — Attenborough × Feynman v1.1 conversion: Chapter 1 (pilot)

Pilot run for contemporary-mathematics. Voice calibration draft. Source folder NOT deleted; held pending Bear's sign-off on the math voice landing for the liberal-arts audience.

- 01-sets — 6,963 words — PASSED self-verification (3,500-word floor; all 14 Combined Test items; no forbidden phrases). Source preserved at `chapters/01-sets/` until review.

Companion files generated:
- `pantry/01-sets.md`
- `images/01-sets.md`
- `bookmaps/01-sets.md`

### Voice notes for this bundle

- Cold open earned: a Saturday-morning Red Cross blood drive in a Boston suburb. The blood-type Venn diagram is in the source; the scene around it is added to ground the chapter. Returns at the integration section as a populated three-set diagram.
- Concept-section openings: kitchen drawer (Concept 1, anchored to source), MLS roster (Concept 2, anchored to source), three-set high-school study survey (Concept 3, anchored to source). Each opens in a concrete situation before the math arrives.
- Math density approach: equations in LaTeX (`$inline$` and `$$display$$`), notation glossed in plain English on first use ("the vertical bar means *such that*"; "$\cup$ is shaped like a cup; you can pour both sets into it").
- Grounded examples throughout: kitchen drawer for cardinality, NBA scorers for $2^n$, fifty-state scale for combinatorial growth, cake-and-ice-cream party for the union formula, study survey for three-set construction, blood bank for the integration.
- Cantor mention preserved from source (m00011); aleph-null introduced; the difference between countable and uncountable infinity flagged but not developed (deferred — could earn its own chapter or appendix).
- Galileo's pairing of naturals with squares preserved from source (m00012); used to motivate equivalent infinite subsets.

### Source-structure note

The source uses smartphone-app promo blocks ("Tech Check: Sets Challenge", "Venn Diagram for Android"), career-info notes ("Employment Opportunities in relational database design"), and unfilled `<figure id="fig-XXXXX">` placeholders. App-promo and career-info content was omitted from the rewrite as out-of-scope for the textbook chapter; figure placeholders were replaced with `[FIGURE: ...]` briefs that point at `images/01-sets.md`.

### Source folder preservation

Per the chapter-1-then-stop pattern Bear approved for previous math bundles, the source subfolder `chapters/01-sets/` remains in place until Bear has reviewed the math voice for the liberal-arts audience. `_toc.md` left unchanged for now; will be rewritten in bulk when chapters 2–13 run after voice sign-off.

## 2026-05-07 — Attenborough × Feynman v1.1 conversion run: Chapters 2–13

Bear authorized the bulk run after pilot. 12 chapters dispatched to parallel subagents; each read book.md and chapter 01-sets.md as the voice anchor before drafting. Source folders for all 12 deleted after Combined Test passed and ≥ 3,500-word floor cleared. `_toc.md` rewritten to flat structure.

| Chapter | Slug | Words | Status | Notes |
|---|---|---:|---|---|
| 02 | logic | 4,458 | OK | 8 source modules → 3 concepts (propositions, compound + truth tables, valid arguments). Forbidden-phrase fix: removed "Obviously true once you think about it" → trace-through-cases phrasing. |
| 03 | real-number-systems-and-number-theory | 3,946 | OK | 12 source modules → 3 concepts (prime factorization & GCD/LCM, integers & operations, rationals & fractions). Irrationals, exponents, sequences deferred. |
| 04 | number-representation-and-calculation | 5,153 | OK | 6 source modules → 3 concepts (numerals & place value, ancient systems trade-offs, generalized base conversion). Arithmetic-in-other-bases tables deferred. |
| 05 | algebra | 5,120 | OK | 12 source modules → 3 concepts (linear equations, functions & graphing, systems). Polynomials, quadratics, inequalities, linear programming all deferred — bookmap names where each fits. |
| 06 | money-management | 4,838 | OK | 14 source modules → 3 concepts (simple interest, compound interest, loans & amortization). 11 deferred (budgeting, investments, mortgages, taxes, etc.). Civic stakes named (predatory lending, credit-card trap). |
| 07 | probability | 4,648 | OK | 12 source modules → 3 concepts (counting, basic probability, expected value). Conditional probability, addition rule, binomial distribution deferred. |
| 08 | statistics | 5,346 | OK | 9 source modules → 3 concepts (sampling, center & spread, normal distribution & inference). Visualization technique and regression deferred. |
| 09 | metric-measurement | 4,947 | OK | 6 source modules → 4 concepts (prefixes, length/area, volume, weight/mass). Forbidden-phrase fix: "I find it remarkable" → direct statement about Mars Climate Orbiter. |
| 10 | geometry | 3,911 | OK | 9 source modules → 3 concepts (lines/angles, polygons & area, Pythagorean theorem). Tessellations, 3D solids, trigonometry deferred. Forbidden-phrase fix: "obviously useful" → "directly useful." |
| 11 | voting-and-apportionment | 6,565 | OK | 6 source modules → 4 concepts (voting methods, fairness criteria & Arrow, divisor/quota, paradoxes & Balinski-Young). Civic stakes named (2000 Florida, Alabama paradox, electoral college). |
| 12 | graph-theory | 5,118 | OK | 11 source modules → 3 concepts (vertices/edges/degree, Euler circuits, Hamilton & TSP). Trees, planarity, isomorphism, Four-Color deferred. |
| 13 | math-and | 5,642 | OK | 6 source modules → 3 concepts (golden ratio & Fibonacci, music & harmony, proportion & architecture). Math-and-environment, math-and-medicine, math-and-sports deferred to pantry. Closer carries the book's coda. Forbidden-phrase fix: "name clearly" → "name directly." |

**Totals.** 12 chapters, 60,692 words. 39 companion files (13 each in `pantry/`, `images/`, `bookmaps/`). All 12 chapters ≥ 3,500-word floor. All 14 Combined Test items pass on each. Forbidden-phrase audit: zero hits across all 12 after fixes.

**Source folders.** All 12 source subfolders (chapters/02–13) deleted after verification. `chapters/01-sets/` (pilot) preserved per the prior decision; can be removed manually once Bear is done comparing the pilot to the rewrite.

**Voice consistency.** Each subagent was given `01-sets.md` as the voice anchor. Light variation across chapters (Ch 6 leans into civic weight, Ch 11 names spoilers and apportionment paradoxes by historical case, Ch 13 closes reflectively). The four voice rules — cold open mid-scene, concept-section cold opens, every term glossed on first use, named trade-offs — hold across all 12.

**TOC.** Rewritten to flat structure pointing at the 13 chapter files.

**Known follow-ups.**
- Chapter 3 came in at 3,946 words — within floor but lower than the ≥ 5,000 target. Source for number theory was modular and many topics were deferred for scaffolding reasons. Consider whether to expand or accept lean length.
- Chapter 10 (Geometry) at 3,911 words — same situation.
- All deferred topics across all chapters are catalogued in their respective bookmap files. A "deferred topic" pass could fill an appendix volume.

