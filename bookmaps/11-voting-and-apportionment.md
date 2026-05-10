# Bookmap — Chapter 11: Voting and Apportionment

Analysis of the OpenStax *Contemporary Mathematics* source modules for voting and apportionment (m00024–m00029), mined for writing strategies, conceptual moves, and reusable structures.

---

## Source overview

Six OpenStax modules make up Chapter 11 in the source:
1. **m00024:** Introduction and chapter framing
2. **m00025:** Voting methods (plurality, runoff, ranked-choice, Borda, pairwise, approval)
3. **m00026:** Fairness criteria and Arrow's Impossibility Theorem
4. **m00027:** Apportionment problem, standard divisor, standard quota
5. **m00028:** Apportionment methods (Hamilton, Jefferson, Adams, Webster)
6. **m00029:** Apportionment paradoxes (Alabama, population, new-states)

**Total source size:** ~16,000 words across six modules.

**Rewritten chapter:** ~6,500 words. Compression achieved by integrating concepts rather than enumerating them, and by choosing three key voting methods (plurality, ranked-choice, Borda, pairwise, approval) rather than six separate subsections.

---

## Structural insights from source

### The frame: Imaginaria

**What the source does:** Opens with a premise—students are "founders" designing a new democracy and must choose voting and apportionment methods.

**Why it works:** This contextualizes the choice as political and consequential. "Let's choose the best method" is meaningless until we define what "best" means. Imaginaria asks: best for *whom*?

**How the rewritten chapter adapts it:** The rewrite drops the explicit Imaginaria framing in the chapter body but preserves the underlying principle: you must choose, and the choice reflects your values. The cold open (the town of 100 voters with spoiler effects) grounds the choice immediately in a real scenario (the 2000 election) rather than a fictional country.

### Enumeration vs. synthesis

**What the source does:** Lists voting methods separately (plurality §1, runoff §2, ranked-choice §3, Borda §4, pairwise §5, approval §6). Each method gets a dedicated section with "Steps to Determine Winner" plus examples.

**Trade-off:** Comprehensive. Every method gets thorough treatment. But the comparison is implicit—readers must synthesize across sections.

**How the rewritten chapter adapts it:** Concept 1 presents six methods as variations on a single question: "What does winning mean when no candidate has a majority?" This structure lets readers compare on the fly. Trade-offs (spoilers, monotonicity, Condorcet fairness) are named as each method is introduced.

### The fairness criteria structure

**What the source does:** Each criterion gets a worked example showing which voting methods pass and which fail. E.g., the majority criterion is tested on plurality, ranked-choice, pairwise, and Borda, with a table summarizing results.

**What works:** The table format makes comparison easy. Readers can see at a glance which methods fail which criteria.

**What the rewrite preserves:** The summary table (in Concept 2). The worked example showing that Borda can violate majority even when one candidate has 51% first-place votes.

### Arrow's theorem as culmination

**What the source does:** States the theorem, explains it applies to rank-based systems, notes that cardinal systems (rating, not ranking) might avoid some problems.

**Conceptual move:** Arrow's theorem is presented as a surprising impossibility result, not an algorithmic problem. This is correct and important.

**How the rewrite adapts it:** The theorem appears halfway through Concept 2, after the four fairness criteria are defined. This preserves the "shock" of the impossibility while ensuring readers understand what is impossible (all four criteria simultaneously).

### Apportionment method pedagogy

**What the source does:** 

- Defines standard divisor and standard quota clearly.
- Shows Hamilton's method with a detailed step-by-step (give lower quotas, identify largest fractional parts, award remaining seats one at a time).
- Shows Jefferson, Adams, and Webster methods with similar detail.
- Includes a worked example comparing all four methods on the same data.

**What works:** The step-by-step structure makes each method learnable. The comparison example shows that methods give different answers and asks students to consider trade-offs.

**What the rewrite preserves:** The algorithms (all four methods explained). The comparison example (Hawaii apportionment). The note that Jefferson favors large states, Adams favors small states, Webster balances.

### Paradox presentation

**What the source does:** 

1. **Alabama paradox:** Explains the 1880 historical case, then gives a simplified three-state example (A=6, B=6, C=2, apportion 10 then 11 seats).
2. **Population paradox:** Defines growth rate as a percentage. Gives a hospital respirator example (state B grows faster but loses a respirator).
3. **New-states paradox:** Explains Oklahoma 1907 as the historical case, then gives fictional examples (San Lorenzo, Gulliversia).

**What works:** Mixing real history with fictional examples anchors the paradoxes in something students care about (real consequences) while the fictional examples let students manipulate numbers.

**What the rewrite does differently:** Consolidates the explanation of each paradox into a single definition, then refers to the source material's examples. This saves space while preserving the conceptual content. A rewritten chapter on voting is not primarily about paradoxes; it is about the structural impossibility of fairness. Paradoxes are evidence of that impossibility, not the point itself.

### Balinski-Young theorem

**What the source does:** States it as the parallel to Arrow's theorem for apportionment. Notes that some methods satisfy the quota rule (Hamilton), while others avoid paradoxes (Jefferson, Adams, Webster), but none satisfy both.

**Conceptual move:** This is the "punchline" of apportionment—the realization that there is no best method, only trade-offs.

**How the rewrite adapts it:** Concept 4 opens with Balinski-Young as the frame for the three paradoxes, not as a separate topic. This reinforces that paradoxes are not bugs; they are symptoms of an underlying impossibility.

---

## Strategies extracted for reuse

### 1. Cold open with concrete example, then generalize

**From source:** Opening to voting methods discusses the 2000 U.S. election (Al Gore had a plurality but not a majority; Nader's votes from Gore voters; spoiler effect).

**Generalization:** Don't open with "What is plurality voting?" Open with "In an election with three candidates, someone can win with 35% of votes while 65% prefer someone else. This happened in 2000 in Florida."

**Application in rewrite:** Chapter opens with the town of 100 voters, Alice 40, Bob 37, Carol 23. Plurality voting makes Alice the winner, but majority would prefer Bob. Then adds Dorothy (write-in), showing spoiler effect. Then names the 2000 election. This moves from abstract to concrete to historical to structural.

### 2. Fairness as a defined concept that can fail

**From source:** The source defines four fairness criteria as precise conditions (majority criterion: "if a candidate has >50% first-place votes, they should win"). Then tests whether methods satisfy them.

**Generalization:** Don't say "this method is fair or unfair." Define what fairness means (specific criteria), test methods against it, and report the results.

**Application in rewrite:** Concept 2 defines each criterion in a single sentence, then shows a worked example where Borda violates majority (a candidate with 51% first-place votes can lose). This is clearer than abstract explanation.

### 3. Teach the impossibility theorem as a logical structure, not a single result

**From source:** Arrow's theorem is stated, then the source shows examples of voting methods violating different criteria, then concludes that no method satisfies all four.

**Generalization:** Impossibility is not a flaw or a surprise once you understand the structure. If you have N criteria and fewer than N mutually-satisfying methods, impossibility is inevitable.

**Application in rewrite:** The chapter shows the four criteria, then states Arrow's theorem, then shows that each major voting method violates at least one. The pattern is clear: if you want criteria A, B, and C but not D, pick method X. Trade-offs, not failure.

### 4. Use comparison tables to summarize trade-offs

**From source:** Every section on voting methods ends with a table like:

| Method | Majority | Condorcet | Monotonicity | IIA |
|--------|----------|-----------|--------------|-----|
| Plurality | ✓ | ✗ | ✓ | ✗ |
| Ranked-choice | ✓ | ✗ | ✗ | ✗ |
| ... | ... | ... | ... | ... |

**Generalization:** Use these tables as reference, not exposition. Tell the story in prose; the table confirms it at a glance.

**Application in rewrite:** Concept 2 uses a table but embeds it within the discussion of each criterion, rather than deferring it to the end.

### 5. Apportionment as a concrete arithmetic problem that reveals deeper structure

**From source:** The source teaches algorithms (Hamilton, Jefferson, etc.) with detailed steps. But it also contextualizes them: "These methods give different answers. Which method does your country prefer?"

**Generalization:** Algorithms are not neutral. Different algorithms encode different political values. Teaching the algorithm is teaching the political choice.

**Application in rewrite:** Concept 3 teaches the standard divisor and standard quota as foundational (all methods use these), then Concept 4 shows that methods diverge in how they handle fractional parts. This builds the intuition that the "choice" happens at the rounding stage—where humans must decide what "fair" means.

### 6. Paradoxes as evidence of impossibility, not anomalies

**From source:** Paradoxes are presented with historical examples, then mathematical proofs of when they occur.

**Generalization:** Don't treat paradoxes as curiosities. They are proof of a theorem: no method avoids all three. This reframes them from "surprising bugs" to "expected trade-offs."

**Application in rewrite:** Concept 4 begins with Balinski-Young, then shows the three paradoxes as evidence. This is a different order from the source (source teaches paradoxes first, proves impossibility after). The rewrite's order emphasizes the impossibility theorem as the main result.

### 7. Civic stakes must accumulate, not be announced

**From source:** The source mentions gerrymandering in a sidebar (note-00021, "Gerrymandering: A Subtle Way to Impact Apportionment"). It mentions the Electoral College as an example of a voting system that divorces the popular vote from the outcome. But these are asides.

**Generalization:** Don't say "this chapter has civic stakes." Let the stakes emerge from the mathematics. Spoilers changed an election. Apportionment paradoxes mean some states lose representation. Arrow's theorem means democracy is constrained.

**Application in rewrite:** The rewrite opens with 2000 Florida and the spoiler effect. It ends with the observation that apportionment paradoxes occur because "you cannot avoid paradoxes without violating the quota rule." The civic weight accumulates through examples and results, not through assertions.

---

## Deferred or condensed material

**From source but not in rewrite (or condensed):**

1. **Runoff voting as a distinct method:** Source Section 3 (m00025) teaches runoff voting separately. The rewrite mentions it briefly in Concept 1 as an alternative to plurality, but does not give it a full worked example. Rationale: Runoff voting is less commonly used than ranked-choice (which simulates runoffs), and space is limited.

2. **Two-round systems and the Hare Method distinctions:** Source m00025 distinguishes between runoff systems that eliminate only the bottom candidate (Hare Method) and runoff systems where the top two advance (two-round system). The rewrite treats ranked-choice voting generically as "instant runoff" without these subdivisions. Rationale: The distinction is technical; the core idea (eliminate and redistribute) is captured.

3. **Approval voting in detail:** Source m00025 Section 11 (Approval Voting) and a worked example (Rock, Paper, Scissors, Lizard, Spock) are condensed to a brief mention in the rewrite's Concept 1. Rationale: Approval voting is less emphasized in contemporary U.S. elections than the other five methods, so it receives less space.

4. **Detailed worked examples of Jefferson, Adams, Webster methods:** Source m00028 Section 7–9 give full worked examples for each method on the Hawaii school apportionment problem. The rewrite mentions these methods and their trade-offs but does not reproduce the full step-by-step calculations. Rationale: Instructors using the chapter have access to the pantry file, which contains detailed solutions.

5. **The Oklahoma 1907 historical case in full detail:** Source m00029 Section 6 gives the Oklahoma case completely. The rewrite mentions it as an example of the new-states paradox but does not walk through the exact numbers. Rationale: The principle is clear without the historical detail; the detail is preserved in the pantry.

6. **Electronic voting and voting machine security:** Source m00026 (note-00016) discusses electronic voting security concerns. The rewrite omits this. Rationale: It is important but tangential to the mathematical content. It could be added as a discussion prompt for instructors.

---

## Concepts reordered or restructured from source

1. **Arrow's theorem placement:** Source discusses all voting methods first (six sections), then fairness criteria (one section), then states Arrow's theorem as a conclusion. The rewrite integrates Arrow's theorem into Concept 2, midway through the discussion of voting methods. This allows fairness criteria to be applied immediately to the methods, rather than deferred.

2. **Apportionment paradoxes as evidence for Balinski-Young:** Source teaches paradoxes, then proves Balinski-Young. The rewrite states Balinski-Young first, then shows paradoxes as evidence. This emphasizes the impossibility theorem (parallel to Arrow) as the main result, with paradoxes as supporting examples.

3. **Integration section as synthesis, not summary:** Source chapters end with a "Key Concepts" summary section. The rewrite integrates the three apportionment methods on a single scenario (Hawaii counties), comparing outcomes and asking what the community values. This makes the trade-off explicit.

---

## Reusable language and phrases from source

**Effective definitions:**
- "Apportionment, from Old French *apportioner* meaning 'to divide into shares'"
- "Plurality, from Latin *plus*, meaning 'more'—the candidate with more votes than any other, even without a majority"

**Effective examples:**
- The cake-and-ice-cream party (Set theory, source Chapter 1; adapted in Chapter 11 as a general model for union/intersection thinking)
- The airline terminals allocation problem (source m00027, used to motivate proportionality in apportionment)
- The Ring Pops problem (source m00027; used to introduce the apportionment problem concretely)

**Effective framing questions:**
- "What does fairness mean?" (opens fairness criteria discussion)
- "Which method is best for Imaginaria?" (frames the chapter as a political choice)

---

## Opportunities for extension

**Not included in rewrite but worth pursuing:**

1. **Cardinal voting systems (rating, not ranking):** Source m00026 mentions that rating-based systems (five-star ratings, thumbs-up/down) might avoid Arrow's theorem's constraints. A deeper exploration could be a follow-up essay or extension.

2. **Voting power and the Banzhaf index:** Source does not mention this. It is an advanced topic but worth noting: in a parliament, not all votes have equal power (some coalitions are pivotal, others are not). This is another impossibility-style problem in voting theory.

3. **Gerrymandering as a graph problem:** Source mentions gerrymandering and cites Jonathan Mattingly's work on redistricting. This could be expanded into a full section: apportionment of geographic space, graph coloring, and algorithmic fairness.

4. **Approval voting in real elections:** Maine passed an approval-voting ballot measure (Question 5, 2020). A case study of this would be timely.

---

## Pedagogical notes for instructors

### On the 2000 election example:

Students respond well to this example because it is real, recent enough to research, and controversial enough that they care. Encourage them to look up:
- Florida's 2000 results (exact vote counts)
- Which states Nader "spoiled" (Florida, New Hampshire)
- Whether Gore would have won either state without Nader

This grounds the abstract notion of "spoiler effect" in something they can verify.

### On comparing voting methods:

Have students apply multiple methods to the same election data. E.g., use a class vote (favorite movie, best pizza toppings) and calculate:
1. Plurality winner
2. Ranked-choice winner
3. Borda count winner
4. Pairwise comparison winner

The methods will likely give different answers. Ask: "Which answer is 'right'?" This forces the discussion of fairness criteria.

### On apportionment methods:

The arithmetic of Hamilton's method is accessible to high-school-level students. Jefferson and Adams methods require more trial-and-error (guessing the modified divisor), which some find tedious. Webster's method is in between. Consider assigning different methods to different groups, then comparing results.

### On impossibility theorems:

Arrow's and Balinski-Young's theorems are intellectually mature results. Students often find them either obvious ("of course you can't have everything") or shocking ("there's no fair way to vote?"). Address both reactions:
- To the first: "You're right. The proof is the detail. The surprise is that no one saw this clearly until 1951."
- To the second: "No universal fair way that satisfies all criteria. But there are fair ways that satisfy some criteria. The choice is political."

---

## References to source for instructors

**For detailed worked examples beyond the chapter:**
- Source m00025 has full worked examples of all six voting methods on the same data. Use these for in-class practice.
- Source m00028 has detailed step-by-step walkthroughs of Hamilton, Jefferson, Adams, and Webster methods on Hawaii school apportionment. Use these for assignment solutions.
- Source m00029 has the historical Alabama paradox (1880 census data with exact vote counts). Use this to show students how real historical data exhibited the paradox.

**For historical context:**
- Source m00025 (note-00023) discusses the Marquis de Condorcet and his advocacy for pairwise comparison.
- Source m00026 (note-00005) quotes Robert Dahl on the tension between majority rule and minority rights.
- Source m00029 (notes-00021, 00022) discusses gerrymandering and Jonathan Mattingly's mathematical approach to detecting unfair districts.

---

## Assessment alignment

The rewritten chapter's structure aligns with these assessment goals:

**Knowledge:** Students can define fairness criteria (majority, Condorcet, monotonicity, IIA) and identify which voting methods satisfy which.

**Application:** Students can apply a voting method (plurality, ranked-choice, Borda, pairwise, approval) to real election data and predict the outcome.

**Analysis:** Students can compare two voting methods on the same data, identify which criteria each satisfies/violates, and explain the trade-offs.

**Synthesis:** Students can explain Arrow's Impossibility Theorem and Balinski-Young Impossibility Theorem as structural constraints on democratic choice, not failures of design.

**Reflection:** Students can argue for a voting or apportionment method for a specific community by naming which fairnesses they value and which they are willing to sacrifice.

All exercises in the chapter (Concept-end and chapter-end) target these goals. The pantry file provides solutions and extension problems.
