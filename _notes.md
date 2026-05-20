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


---

## 2026-05-12 — Running Project Exercises generated (Audit a Real-World System)

Running-project LLM exercises added to all 13 chapters. Project: **Audit One Real-World System Through 13 Lenses** — student picks one specific system in Ch 1 (a transit network, streaming catalog, sports league, restaurant, hospital, election, university enrollment system, etc.), then analyzes it through every chapter's mathematics. Final deliverable: a 25-30 page integrated audit using all 13 mathematical lenses on a single target.

**Replaced 27 pre-existing chapter-specific verify-the-LLM exercises** across chapters 02, 03, 04, 07, 10, 13. The legacy format (5 short prompts per chapter, asking the student to ask an LLM something and check the answer) was pedagogically sound for the audience but did not connect chapters into a project. Per user direction, replaced with single running-project block per chapter that builds toward the integrated audit.

| Ch | Topic | Audit lens added |
|---|---|---|
| 01 | Sets | System spec + set-theoretic categorization (Venn diagram, cardinalities, De Morgan) |
| 02 | Logic | Logical audit — formalize 3 if-then rules, identify 1 invalid argument, De Morgan on system language |
| 03 | Real Numbers / Number Theory | Divisibility audit — cycles via LCM, shared structure via GCD, fraction reduction, irrational appearances |
| 04 | Number Representation | Encoding audit — 3 encoding schemes, base conversion, capacity calculation, design-decision insight |
| 05 | Algebra | Threshold audit — 3 thresholds, one solved with algebra, one system of equations |
| 06 | Money Management | Money audit — 3 financial flows, interest calc, 6-period amortization, credit-card-style dynamic |
| 07 | Probability | Probability audit — 3 events, complement trick, EV calc, identified "casino" feature |
| 08 | Statistics | Statistical audit — disaggregation, mean/median/spread, z-score, sampling problem |
| 09 | Metric Measurement | Units audit — inventory, conversion vulnerability, dimensional analysis, scaling factor, reasonableness check |
| 10 | Geometry | Spatial audit — Pythagorean distance + directness ratio, area calc, similar-triangle scaling, geometric inefficiency |
| 11 | Voting & Apportionment | Fairness audit — map system to voting method, run second method, fairness criteria check, Arrow trade-off named |
| 12 | Graph Theory | Structural audit — graph model, high-degree vertex, Euler check, shortest path, TSP/postman framing |
| 13 | "Math and..." + CLOSER | Pattern analysis (with honesty caveat) + **compiled 25-30 page integrated audit** (executive summary, 13 chapter audits, 3 connecting observations, recommendations, what-would-change-my-mind, 200-word coda) |

**Project shape:** Persistent Claude Project across all 13 chapters. The system spec drafted in Ch 1 carries forward; every chapter adds an analytical lens. Final deliverable in Ch 13 is the 25-30 page integrated audit organized in 6 sections.

**Calibration choices:**
- Ch 1 forces system specification — the prompt rejects systems "too vague to count things in" and requires a 200-word spec saved to the Project.
- Ch 13's PART A includes an explicit honesty caveat against over-applying golden-ratio reasoning — the chapter itself warns about this and the exercise enforces it.
- Ch 13's coda asks the student to reflect on what 13 lenses taught them about MATHEMATICS (not just about the system).
- Each chapter's exercise references prior-chapter findings so the project genuinely accumulates.

**Audience flag:** This project is more analytically demanding than Project 1 (Daily-Life Casebook) would have been. Some gen-ed students may find it stretched. The user picked it deliberately knowing this — the artifact is more impressive at the cost of accessibility.

**No follow-ups flagged.**
