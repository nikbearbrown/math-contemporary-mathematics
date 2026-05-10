# Source map — Chapter 2: Logic

## Source files processed

| File | Source module | Contribution |
|---|---|---|
| 01-m00016.md | Chapter intro + statements & quantifiers | Cold open (logic in law) + learning objectives + definition of logical statement + introduction to symbolization |
| 02-m00017.md | Statements & quantifiers (cont.) | Identification of logical statements, symbolic representation (p, q, r), negation in words and symbols, quantified statements (all/some/none), negation of quantified statements |
| 03-m00018.md | Compound statements & connectives | Logical connectives (∧, ∨, ~, →, ↔), translation to/from symbolic form, dominance of connectives (order of operations) |
| 04-m00019.md | Truth tables (negation, AND, OR) | Interpretation of negation/AND/OR truth values, construction of truth tables for 2-3 statement combinations, validity of statements using truth tables |
| 05-m00020.md | Conditional & biconditional truth tables | Conditional statement truth table, biconditional truth table, validity determination using truth tables |
| 06-m00021.md | Logical equivalence, converse/inverse/contrapositive | Logical equivalence via truth tables, converse/inverse/contrapositive definitions, truth tables for each form, contrapositive as logically equivalent to conditional |
| 07-m00022.md | De Morgan's Laws, negation of conditionals | De Morgan's Laws (both forms), negation of conditional as p∧~q, logical properties table (commutative, associative, distributive), application to negate complex statements |
| 08-m00023.md | Valid arguments (detachment, denying consequent, chain rule) | Law of detachment (modus ponens), law of denying consequent (modus tollens), chain rule (hypothetical syllogism), validity vs. soundness, fallacy definition, deductive vs. inductive arguments |

## Concept coverage

| Concept | Primary source | Supplementary sources | Role in chapter |
|---|---|---|---|
| **Propositions, symbolic representation, negation** | 02-m00017 (statements & negation) | 01-m00016 (definition) | Concept 1: Foundation. Defines what a logical statement is, how to represent it symbolically, how to negate it (simple and quantified). |
| **Compound statements and truth tables** | 03-m00018 + 04-m00019 (connectives and truth tables) | 05-m00020 (conditional) | Concept 2: Core mechanics. Introduces AND, OR, NOT; builds truth tables systematically; shows how truth values combine. |
| **Valid logical arguments** | 08-m00023 (detachment, denying consequent, chain rule) | 06-m00021 (contrapositive, equivalence) | Concept 3: Payoff. Shows how the machinery (propositions, truth tables) is used to validate arguments; introduces three key valid forms. |
| **De Morgan's Laws** | 07-m00022 (negation of conjunctions/disjunctions) | — | Distributed: mentioned in Concept 3 as a tool for clarifying statements; worked example 2.7; Challenge exercise 2.11. |
| **Logical equivalence & contrapositive** | 06-m00021 (equivalence, contrapositive) | 07-m00022 (De Morgan's as equivalence) | Distributed: contrapositive mentioned as logically equivalent to conditional (law of denying consequent); full treatment deferred to Challenge exercise 2.10. |
| **Quantified statements** | 02-m00017 (all/some/none) | — | Integrated into Concept 1, worked example, and Warm-up exercises. |

## Deferred material

| Topic | Source file | Reason deferred |
|---|---|---|
| **Full treatment of converse/inverse/contrapositive** | 06-m00021 | The rewrite prioritizes the three valid argument forms (detachment, denying consequent, chain rule) over exhaustive coverage of all four conditional forms. Contrapositive equivalence is essential; the converse and inverse are mentioned but not deeply explored. Challenge exercise 2.10 offers deeper practice. |
| **Exclusive OR (XOR)** | (not in source, but mentioned in Chapter Review projects) | Out of scope for this chapter. The source uses inclusive OR throughout, which is standard in formal logic. The project on "Logic Gates" (in source module 08) explores XOR but is an extended project, not chapter content. |
| **Boolean logic and digital circuits** | 07-m00022 (note on Boole) + 08-m00023 (projects) | Out of scope. The chapter mentions George Boole's contribution to logic and Boolean algebra, but detailed coverage of logic gates is reserved for the optional projects at the end of the chapter. |
| **Fallacies (hasty generalization, affirming consequent, etc.)** | 08-m00023 (definitions, projects) | Mentioned in narrative (affirming consequent as invalid form), but not systematically taught. Source includes a project on logical fallacies; this chapter focuses on valid forms, allowing the fallacy project to be an extension. |
| **Soundness vs. validity (deep treatment)** | 08-m00023 (definitions) | The chapter distinguishes the two (Exercise 2.12 touches on this), but does not deeply explore the philosophical or practical implications. Integration section uses Marshall's case to show the difference, but full epistemology is deferred. |

## Source-level notes

1. **Inconsistency in notation:** Source uses both $\sim$ and "not" interchangeably; rewrite standardizes on $\sim$ for symbolic form and "not" for English.

2. **Complexity of quantified statements:** Source module 02-m00017 has detailed tables on negating all/some/none statements. Rewrite simplifies this into a memorable rule: "All → Some...not; Some → None; None → Some." Challenge exercises allow for deeper practice.

3. **Dominance of connectives:** Source module 03-m00018 teaches order of operations for logical connectives (parentheses → negation → AND/OR → conditional → biconditional). Rewrite mentions this briefly when needed (Concept 2) but does not make it a standalone topic, relying instead on worked examples and exercises to build fluency.

4. **Truth tables for three variables:** Source module 04-m00019 includes examples with three propositions (p, q, r), requiring 8 rows. Rewrite includes one such example (Challenge exercise 2.9) but keeps most examples at 2-variable level for clarity.

5. **Projects on logic gates and fallacies:** Source modules include optional projects on logic gates (Boolean circuits) and fallacies. These are noted in the chapter but are treated as optional extensions. A separate section in the chapter (or in supplementary materials) can expand on these.

6. **Venn diagrams for argument validation:** Source modules 08-m00023 uses Venn diagrams to verify deductive arguments (e.g., law of detachment). Rewrite relies primarily on truth tables, with a note that Venn diagrams are an alternative visualization.

7. **Distinction between inductive and deductive arguments:** Source 08-m00023 defines both but focuses on deductive (which lends itself to formal logic). Rewrite mentions this distinction briefly (note in Concept 3) but does not deeply explore inductive reasoning, as it relies on empirical evidence rather than logical form.

---

## Coverage summary

**All essential content from source is retained:**
- Logical statements and non-statements ✓
- Symbolic representation (p, q, r) ✓
- Negation (simple and quantified) ✓
- Compound statements (AND, OR, NOT) ✓
- Truth tables for all connectives ✓
- Conditional and biconditional ✓
- Validity determination ✓
- Law of detachment ✓
- Law of denying consequent ✓
- Chain rule ✓
- De Morgan's Laws ✓
- Logical equivalence ✓
- Contrapositive ✓

**Prioritized content (emphasized in rewrite):**
- Three core concepts: propositions → truth tables → valid arguments
- Concrete, grounded examples (café, store, Marshall's courtroom)
- Mechanical process (truth tables as tools)
- Real-world stakes (law, persuasion, democracy)

**Secondary content (mentioned but not deeply developed):**
- Converse and inverse (mentioned, not deeply explored)
- Soundness vs. validity (mentioned, briefly explained)
- Fallacies (mentioned as invalid forms, not systematically named)
- Boolean logic and circuits (reserved for projects)
- Inductive reasoning (mentioned, not developed)
