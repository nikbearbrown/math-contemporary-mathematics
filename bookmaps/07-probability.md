# Source map — Chapter 7: Probability

## Overview

The OpenStax Contemporary Mathematics Chapter 7 spans 12 source modules, covering counting principles, basic probability, conditional probability, and expected value. The rewritten chapter selects three core concepts and defers five others to maintain clarity and math density over word count.

---

## Twelve source modules and their content

1. **m00034** (intro): Casinos and the motivation for counting. Lays out the problem: with 2,598,960 possible 5-card hands, how do you analyze probabilities without listing every one?

2. **m00085** (Multiplication Rule for Counting): Foundational. Three examples: cupcakes, cards in a deck, license plates. Introduces the multiplication rule as a shortcut when listing fails.

3. **m00086** (Permutations): Factorials, permutation formula, Olympic swimming example (8 swimmers, top 3 finishers). Emphasizes that order matters in a permutation.

4. **m00087** (Combinations): Contrasts with permutations. Poker hands, Clue cards, lottery. Formula $C(n,r) = n! / (r!(n-r)!)$ and why dividing by $r!$ removes the ordering.

5. **m00088** (Sample Spaces and Outcomes): Tables and tree diagrams for listing all outcomes in multistage experiments. Covers independence vs. dependence. Includes Punnett squares (genetics example).

6. **m00089** (Basic Probability Concepts): Three methods: theoretical probability (equally likely outcomes), empirical probability (observed frequency), subjective probability (guess). Complement rule. Gerolamo Cardano history.

7. **m00090** (Probability with Permutations and Combinations): Applies counting tools to probability. Royal flush example, Scrabble tiles, Palmetto Cash 5 lottery.

8. **m00091** (Odds): Ratio of favorable to unfavorable outcomes. Relationship between odds and probability. Converting odds to probability and vice versa.

9. **m00092** (Addition Rule for Probability): Mutually exclusive events and the formula $P(E \text{ or } F) = P(E) + P(F)$ when no overlap. Inclusion-Exclusion Principle for overlapping events.

10. **m00093** (Conditional Probability and Multiplication Rule): Probability updates when new information arrives. Conditional probability $P(E|F)$. Multiplication rule for sequential events. Birthday problem and Monty Hall problem.

11. **m00094** (Binomial Distribution): Binomial experiments, binomial formula, probability density and cumulative distribution functions. Abraham de Moivre history.

12. **m00097** (Expected Value): Mean of outcomes weighted by probability. Interpretation as long-run average. Applications to roulette, Keno, football fourth-down decisions. Pascal's Wager and Pierre de Fermat.

---

## Three concepts chosen for the rewrite

### Concept 1: Counting Principles (from m00085, m00086, m00087)
- **Why selected:** Foundational. Without the ability to count, you cannot assign probabilities to rare events. The multiplication rule, permutations, and combinations are the tools that make probability calculations tractable.
- **Coverage:** All three are compressed into one concept section, emphasizing permutations vs. combinations distinction and the trade-off between order mattering and not mattering.
- **Depth:** The rewrite covers the formulas, the relationship between them, and worked examples; defers the most elaborate examples (e.g., very large factorials demonstrating combinatorial explosion, though 52! is mentioned for flavor).

### Concept 2: Basic Probability (from m00088, m00089)
- **Why selected:** The core definition. Once you know how to count, you need to know how to assign meaning to counts. Theoretical, empirical, and subjective probability are the three methods used in practice.
- **Coverage:** Sample spaces and events (inheriting vocabulary from Chapter 1). The complement rule is emphasized as a practical shortcut; the addition rule is deferred.
- **Depth:** Worked examples include card draws, die rolls, and weather forecasts. The historical note on Cardano is omitted; the emphasis is on *how and when to use each method*, not on history.

### Concept 3: Expected Value (from m00097, m00091)
- **Why selected:** The payoff concept. After defining probability, students must understand why it matters: expected value predicts long-run outcomes and drives real decisions (casino profit, insurance pricing, lottery design). This is the bridge from abstract probability to application.
- **Coverage:** Formula, interpretation as a long-run average (Law of Large Numbers), and a detailed worked example of a roulette bet at the casino level.
- **Depth:** The rewrite connects expected value to decision-making (which game to play, whether a lottery is worth buying a ticket). It emphasizes the scale shift from a single bet (variance dominates) to thousands of bets (expected value dominates).

---

## Five concepts deferred and why

### Concept 4: Odds (m00091)
- **Coverage in source:** Converting between probability and odds; odds as a ratio of favorability vs. unfavorability.
- **Why deferred:** Odds are used in gambling and betting terminology but are not essential to understanding probability. Once students know probability, odds can be learned as an alternative notation. The chapter tests understanding of probability, not facility with odds conversion formulas.
- **Note:** A single worked example in the rewrite shows odds as a comparison of favorable to unfavorable outcomes (e.g., "3:1 against rolling a 7"), but the formulas for converting probability to odds are omitted.

### Concept 5: Addition Rule and Inclusion-Exclusion (m00092)
- **Coverage in source:** Formula $P(E \text{ or } F) = P(E) + P(F)$ for mutually exclusive events; Inclusion-Exclusion Principle for overlapping events.
- **Why deferred:** These rules are important but can be understood once students solidify the definition of probability and the complement rule. The chapter already stacks three major concepts; adding a fourth (compound events and union rules) would exceed the recommended density. This is a natural next topic after completing the chapter.
- **Note:** The term "mutually exclusive" is introduced in passing (to contrast with the complement rule), but the formal union formulas are not taught here.

### Concept 6: Conditional Probability and Multiplication Rule (m00093)
- **Coverage in source:** Probability updates when new information arrives; $P(E|F)$ notation; the formula $P(E \text{ and } F) = P(E) \times P(F|E)$ for sequential events.
- **Why deferred:** Conditional probability is a deep and important concept, but it is logically downstream of basic probability. A student must first understand unconditional probability before grappling with how probabilities change. The rewrite mentions conditional probability in the context of independence (e.g., drawing without replacement), but does not make it a focal point.
- **Note:** This concept is essential for Chapter 8 (Statistics) and is a natural bridge once Chapter 7 is complete. The source includes beautiful examples (Abraham Wald's World War II analysis of bomber armor placement, the Monty Hall problem), which will be powerful when revisited in the next chapter.

### Concept 7: Binomial Distribution (m00094)
- **Coverage in source:** Binomial experiments, the binomial formula, probability density functions (PDFs), and cumulative distribution functions (CDFs).
- **Why deferred:** The binomial distribution is a specific application of probability to repeated independent trials with two outcomes. It is important and will be used in Chapter 8 (Statistics), but including it here would push the chapter over its recommended word count and mathematical density. The Chapter 1 vocabulary of subsets ($2^n$ subsets of an $n$-element set) connects to binomial experiments (each trial is a binary choice: success or failure), but the binomial formula itself is not needed to understand expected value.
- **Note:** The chapter mentions binomial reasoning only in passing (Challenge Exercise 7.11), with a hint to compute the complement. The full binomial distribution is reserved for a follow-up unit.

---

## Deferred material summary table

| Module | Topic | Reason for Deferral | Where It Fits Next |
|--------|-------|---------------------|-------------------|
| m00091 | Odds conversion | Alternative notation; learnable after probability | Review section after Chapter 7 |
| m00092 | Addition Rule & Inclusion-Exclusion | Stacks too many concepts; essential after Concept 2 | Early in Chapter 8 or as a mid-unit skill-builder |
| m00093 | Conditional probability | Logically downstream; essential for inference | Chapter 8 (Statistics), Concept 1 |
| m00094 | Binomial distribution | Specific application; needed for statistical inference | Chapter 8 (Statistics), Concept 2 |

---

## Source-level notes

### m00085 (Multiplication Rule)
- **Preserved:** Cupcake example, card deck example, license plate example.
- **Omitted:** "Check Your Understanding" questions (these become exercises); detailed discussion of ordered vs. unordered (saved for permutations/combinations).

### m00086 (Permutations)
- **Preserved:** Factorial definition, permutation formula, Olympic swimming example, permutation-as-ordered-arrangement concept.
- **Omitted:** "Very Big Permutations" sidebar (52! discussed more briefly in the context of example, not as an extended sidebar).

### m00087 (Combinations)
- **Preserved:** Distinction between permutations and combinations, the color-coding table showing why $P(n,r) = C(n,r) \times r!$, combination formula, multiple examples.
- **Omitted:** Historical note on Pingala and Eastern mathematicians; the "Early Eastern Mathematicians" sidebar is too long for this rewrite's scope.

### m00088 (Sample Spaces)
- **Preserved:** Definition of sample space, independence vs. dependence, tables for two-stage experiments, tree diagrams for multistage experiments.
- **Omitted:** Punnett squares (genetics example) — while valuable, it is a domain-specific application that distracts from the core message about sample spaces. The same concepts apply to any table or tree structure.

### m00089 (Basic Probability Concepts)
- **Preserved:** Three methods (theoretical, empirical, subjective), complement rule, the Monopoly cold-open example, the definition of certain and impossible events.
- **Omitted:** Gerolamo Cardano history (important to probability history but not essential to learning the concepts); "Benford's Law" sidebar (too specialized); extensive "Buffon's Needle" project (valuable but peripheral).

### m00090 (Probability with Permutations and Combinations)
- **Preserved:** The logic of applying counting tools to find sample space size and event size, then computing probability. Royal flush and lottery examples.
- **Omitted:** Scrabble hand (consonant-only draws) — overly complex for this chapter's scope; the same lesson (using combinations to count favorable outcomes) is conveyed with simpler examples.

### m00091 (Odds)
- **Status:** Mostly deferred. A brief mention in passing (e.g., "the odds are 1:3 against rolling a 7") appears in the Concept 1 worked examples, but conversion formulas and detailed odds examples are not included.

### m00092 (Addition Rule)
- **Status:** Deferred. The concept of mutually exclusive events is mentioned in passing (in Concept 2, when introducing independence). The formal Addition Rule and Inclusion-Exclusion Principle are reserved for a follow-up unit.

### m00093 (Conditional Probability)
- **Status:** Mostly deferred. The term "conditional probability" and the concept of how probability changes when new information arrives appear in Concept 2 (in discussion of dependence). The formal notation $P(E|F)$ and the Multiplication Rule $P(E \text{ and } F) = P(E) \times P(F|E)$ are not taught in the chapter but will be essential in Chapter 8. The Monty Hall problem and Abraham Wald's bomber analysis are held for that chapter.

### m00094 (Binomial Distribution)
- **Status:** Heavily deferred. Only one challenge exercise hints at binomial reasoning. The binomial formula, PDF, CDF, and de Moivre history are omitted from this chapter and will be covered in Chapter 8 (Statistics).

### m00097 (Expected Value)
- **Preserved:** Definition, formula, interpretation as long-run average, worked examples (die roll, two dice, Rummy card values), connection to decision-making, applications (roulette, Keno).
- **Omitted:** "Pascal's Wager" (theological application; too far afield); "Expected Values in Football" (interesting but domain-specific); "Pierre de Fermat and Blaise Pascal" history (valuable but not essential to learning expected value); elaborate Keno examples are simplified.

---

## Integration with Chapter 1 (Sets)

The rewrite explicitly connects probability to Chapter 1 vocabulary:

- A **sample space** is a **universal set** in the context of probability.
- An **event** is a **subset** of the sample space.
- The **complement** of an event is **$E'$** (complement notation from Chapter 1).
- **Cardinality** $n(S)$ uses the same notation from Chapter 1.
- The **multiplication rule for counting** connects to the principle behind counting subsets ($2^n$ subsets of an $n$-element set from Chapter 1).

This continuity helps students see probability as an extension of set theory, not a separate domain.

---

## Concept frequency in chapter structure

| Concept | Chapter Section | Word Count | Source Module(s) |
|---------|-----------------|-----------|------------------|
| Counting (mult. rule, perm., comb.) | Concept 1 | ~1,800 | m00085, m00086, m00087 |
| Basic Probability (sample space, events, three methods, complement) | Concept 2 | ~1,600 | m00088, m00089 |
| Expected Value (definition, interpretation, decision-making) | Concept 3 | ~1,200 | m00097 |
| Integration (casino example) | Integration | ~500 | m00089, m00097 |
| Exercises (warm-up, application, synthesis, challenge) | Exercises | ~800 | All modules |
| Summary & Connections | Conclusion | ~600 | All modules |

**Total:** ~6,500 words (target: 5,000–8,000 words)

---

## Why these three concepts scale well

1. **Counting principles** are prerequisite to understanding probability. No count, no probability assignment.
2. **Basic probability** is the core concept. Everything in the chapter rests on it.
3. **Expected value** is the application and the payoff. It shows *why* probability matters to real decisions.

This sequence is natural, scaffolded, and complete for a first exposure to probability. It sets up conditionally probability and the binomial distribution as natural next steps, which appear in Chapter 8 (Statistics).
