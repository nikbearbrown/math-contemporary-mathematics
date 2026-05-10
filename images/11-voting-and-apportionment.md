# Images — Chapter 11: Voting and Apportionment

Manifest of figures referenced in the chapter. Original source files (OpenStax) have empty `<figure>` tags; this file documents what figures should be created or sourced for illustration.

---

## Figures by section

### Section: Voting methods (Concept 1)

**[FIGURE: Pairwise comparison matrix—restaurant example]**
- Description: A 3×3 matrix with candidates R (Rainbow China), D (Dough Boys), T (Taco City) on rows and columns. Entries show vote counts for each head-to-head matchup. Example: R vs D shows 70 votes for R, 30 for D.
- Type: Table/Matrix
- Purpose: Illustrate how pairwise comparison scores are recorded.
- Where used: Worked example, "comparing methods on a single election"

**[FIGURE: Approval voting ballot—restaurant example]**
- Description: A simple form with four restaurant names (Rainbow China, Dough Boys Pizza, Taco City, Caribbean Flavor). Each has a checkbox (✓ or ☐ ) for approval/disapproval.
- Type: Ballot mockup
- Purpose: Show how approval voting differs from ranking (no order, just yes/no).
- Where used: Discussion of approval voting method

**[FIGURE: Ranked-choice elimination rounds—restaurant example]**
- Description: A diagram showing three rounds of ranked-choice voting with vote tallies. Round 1: Taco City has fewest votes (0), is eliminated. Round 2 shows Taco City votes redistributed, Caribbean Flavor now has fewest, is eliminated. Round 3 shows final two candidates with majority count highlighted.
- Type: Flow diagram with tallies
- Purpose: Visualize the elimination and redistribution process in ranked-choice voting.
- Where used: Explanation of ranked-choice voting method

---

### Section: Fairness criteria and Arrow's theorem (Concept 2)

**[FIGURE: Fairness criteria summary table]**
- Description: A 2×5 table. Rows: "Criterion / Satisfied by / Violated by". Columns: Majority Criterion, Condorcet Criterion, Monotonicity Criterion, IIA Criterion. Each cell lists the voting methods.
- Type: Summary table
- Purpose: Quick reference for which voting methods satisfy which criteria.
- Where used: Summary of Concept 2

**[FIGURE: Arrow's Impossibility Theorem—conceptual diagram]**
- Description: A 4-circle Venn-diagram-like illustration with circles labeled "Majority," "Condorcet," "Monotonicity," "IIA." Arrows point to show that every voting method lands in the intersection of 3 circles but not all 4. A text box states: "Arrow's theorem: No voting system satisfies all four criteria."
- Type: Conceptual diagram
- Purpose: Visualize the constraint imposed by Arrow's theorem.
- Where used: Discussion of Arrow's Impossibility Theorem

---

### Section: Apportionment and distributing resources (Concept 3)

**[FIGURE: Standard divisor and standard quota example—schools]**
- Description: A table with columns: School, Student Enrollment, Standard Quota (enrollment ÷ standard divisor), Lower Quota, Upper Quota. Rows: A (30, 6.15, 6, 7), B (25, 5.12, 5, 6), C (28, 5.74, 5, 6), D (32, 6.56, 6, 7), E (24, 4.92, 4, 5), F (27, 5.53, 5, 6). Standard divisor = 4.88.
- Type: Table
- Purpose: Show how to calculate standard quota and identify lower/upper quotas.
- Where used: Discussion of standard divisor and quota; Concept 3

**[FIGURE: Hamilton's method step-by-step—schools]**
- Description: A flowchart showing (1) Calculate standard divisor and quotas. (2) Assign lower quotas to all schools. (3) Sum lower quotas (34, falls 1 short of 35 laptops). (4) Identify largest fractional part (Room D, 0.56). (5) Award remaining laptop to D. (6) Final count: sum = 35.
- Type: Step-by-step flowchart
- Purpose: Illustrate Hamilton's method algorithm.
- Where used: Explanation of Hamilton's method

---

### Section: Apportionment paradoxes (Concept 4)

**[FIGURE: Alabama paradox—state seat counts]**
- Description: Side-by-side comparison. Left: House size 299, state seats shown (Alabama gets 8). Right: House size 300, state seats shown (Alabama gets 7). Arrow from left to right with "?" indicating the paradox.
- Type: Comparison diagram
- Purpose: Visualize that adding seats caused Alabama to lose representation.
- Where used: Explanation of Alabama paradox

**[FIGURE: Population paradox—growth rates and seat changes]**
- Description: A three-row table. Rows: State A, State B, State C. Columns: 2020 Population, 2021 Population, Growth Rate (%), Seats in 2020, Seats in 2021, Change in Seats. Highlighted: State B has higher growth rate than State C, yet State C gains a seat and B loses one.
- Type: Annotated data table
- Purpose: Show the paradox clearly via numbers.
- Where used: Explanation of population paradox

**[FIGURE: New-states paradox—before and after]**
- Description: Two apportionment diagrams. Top: Two states (Clara, Velasco) get (39, 51) seats. Bottom: Three states (Clara, Velasco, Oscuridad) get (40, 50, 8) seats. Highlighted: Velasco lost a seat despite no population change.
- Type: Before/after comparison
- Purpose: Illustrate how adding a state causes an existing state to lose a seat.
- Where used: Explanation of new-states paradox

---

### Section: Integration (applying concepts)

**[FIGURE: Decision tree—choosing a voting method]**
- Description: A flowchart starting with "What matters most to your community?" Branches to: (1) Majority rule → Plurality, Ranked-choice. (2) Head-to-head fairness → Pairwise comparison. (3) Compromise candidates → Borda count. (4) Simplicity → Plurality, Approval voting. Each leaf includes trade-offs.
- Type: Decision flowchart
- Purpose: Guide readers toward choosing a voting method based on community values.
- Where used: Integration section

**[FIGURE: Decision tree—choosing an apportionment method]**
- Description: Similar flowchart. "What matters most?" branches to: (1) No paradoxes → Jefferson, Adams, Webster. (2) Quota rule → Hamilton. (3) Balance between large/small states → Webster. (4) Avoid bias → Hamilton. Each leaf notes caveats.
- Type: Decision flowchart
- Purpose: Guide readers toward choosing an apportionment method.
- Where used: Integration section

---

## Notes on source material

The OpenStax *Contemporary Mathematics* source modules (m00024–m00029) contained `<figure id="fig-XXXXX">` tags with empty content. In the rewritten chapter, these have been replaced with narrative descriptions and worked examples that do not depend on external figures. The manifested figures above represent educational visualizations that should be created to support student understanding.

For instructors creating slides or handouts: Each figure listed above can be created using:
- Tables: Use spreadsheet or markdown table syntax
- Diagrams: Use diagramming software (OmniGraffle, Lucidchart, Draw.io)
- Flowcharts: Use flowchart tools or simple text-based ASCII diagrams
- Mockups: Use design tools or simple form templates

All figures should prioritize clarity and accessibility over decoration. Numbers should be readable, labels should be precise, and the figure's purpose should be immediately obvious.

---

## Specific recommendations for visual creation

### For figures on voting methods:
- Use consistent color coding across figures (e.g., red for plurality winner, blue for ranked-choice winner, green for Borda winner). This helps readers track which candidate wins under which method.
- Include a small legend showing candidate colors or symbols if using more than 2 candidates.

### For figures on apportionment:
- Show state/district names and populations on the left; seat allocations in columns. This mimics the table format used in the source and chapter.
- For paradoxes: Use side-by-side comparisons or before/after layouts so the contradiction is visually obvious.

### For decision flowcharts:
- Keep branches to 2-3 options per node (not 5+), or the flowchart becomes cluttered.
- Include decision questions at each node in plain language ("Does your community value majority rule or Condorcet fairness?").

---

## Assessment via visuals

Instructors may ask students to:
1. **Recreate a pairwise comparison matrix** given preference ballots.
2. **Draw a flowchart** for Hamilton's method applied to a specific apportionment problem.
3. **Construct a before/after visualization** of an apportionment paradox.

These visual exercises reinforce understanding of the algorithms and trade-offs.
