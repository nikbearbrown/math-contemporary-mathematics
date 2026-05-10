# Source Map — Chapter 5: Algebra

## Overview

The OpenStax *Prealgebra* Chapter 5 (Algebra) consists of 12 source modules covering approximately 80 pages of material. The rewritten chapter focuses on three core concepts sufficient for liberal-arts civic mathematics, and defers the rest to later specialized courses or to a detailed bookmap for instructors.

---

## Source files and coverage

| File | Topic | Lines | Status in Rewrite |
|------|-------|-------|-------------------|
| 01-m00032 | Intro: variables and algebra motivation | 33 | Integrated into cold open |
| 02-m00098 | Algebraic expressions and evaluation | 1,579 | Partially; focus moved to functions |
| 03-m00099 | Linear equations in one variable | 554 | **PRIMARY: Concept 1** |
| 04-m00100 | Linear inequalities in one variable | 803 | Deferred |
| 05-m00101 | Ratios and proportions | 591 | Deferred |
| 06-m00102 | Polynomials, binomials, quadratics | 1,100+ | Deferred |
| 07-m00103 | Relations and functions | 600+ | **PRIMARY: Concept 2** |
| 08-m00104 | Graphing points and equations | 1,200+ | **PRIMARY: Concept 2** (graphing) |
| 09-m00105 | Slope, intercepts, graphing functions | 800+ | **PRIMARY: Concept 2** (slope) |
| 10-m00106 | Systems of linear equations | 700+ | **PRIMARY: Concept 3** |
| 11-m00107 | Systems of linear inequalities | 600+ | Deferred |
| 12-m00108 | Linear programming | 700+ | Deferred |

**Concepts selected for primary focus:**

1. **Linear Equations & Solving (m00099):** The foundational skill. Every reader must be able to isolate an unknown and check the solution. Real-world applications: pricing, budgeting, dosing.

2. **Functions & Graphing (m00103 + m00104 + m00105 combined):** How to name relationships between quantities and visualize them. Domain, range, function notation, slope, intercepts, and the three main methods to graph (points, intercepts, slope-intercept form).

3. **Systems of Equations (m00106):** Modeling situations with multiple constraints. Substitution and elimination methods. No solution and infinitely many solutions as valid outcomes.

**Concepts deferred:**

- Ratios and proportions (m00101): Important, but Chapter 6 (Money Management) uses these extensively; better scaffolded there first.
- Polynomials, factoring, and quadratics (m00102): Specialized skill for those pursuing math/science. Present chapter gives enough algebraic reasoning; quadratics are optional depth.
- Linear inequalities in one variable (m00100): Single-variable inequalities are less commonly used in civic mathematics than equations and functions. Systems of inequalities (m00107) are deferred with them.
- Linear programming (m00108): Optimization is advanced. The structure (objective function + constraints) appears in systems of equations; full linear programming is elective.

---

## Concept coverage in rewrite

### Concept 1: Solving Linear Equations

**Source:** Primarily m00099 (550+ lines).

**Preserved material:**
- Definition of linear equation: $ax + b = 0$.
- Four properties of equality (addition, subtraction, multiplication, division).
- Worked example: 7-step process (simplify, collect variables, collect constants, isolate variable, check).
- Applications: gym membership, snowblower rental, paycheck.
- Special cases: no solution, infinitely many solutions.

**Reorganized or condensed:**
- Removed abstract motivation; replaced with immediate practical cold open (used-car wage example).
- Consolidated 4–5 detailed examples into 1–2 core worked examples + summary of common errors.
- Deferred: solving formulas for a given variable (m00099 section), card tricks (interesting but not essential).

**Not included:**
- Long motivational preambles ("the jump from arithmetic to algebra is difficult...").
- Excessive repetition of the same property across multiple examples.

### Concept 2: Functions & Graphing

**Sources:** m00103 (600 lines), m00104 (1200 lines), m00105 (800 lines).

**From m00103 (Relations and Functions):**
- Definition of relation and function.
- Domain and range (needed for context).
- Function notation: $f(x)$ vs. $y = ...$
- Evaluation: $f(3)$ means substitute 3, compute the output.

**From m00104 (Plotting Points):**
- Coordinate plane: x-axis, y-axis, origin, quadrants.
- Ordered pairs: $(x, y)$.
- Plotting points on a grid.

**From m00105 (Graphing Functions):**
- Intercepts: x-intercept (set $y = 0$), y-intercept (set $x = 0$).
- Slope: $m = \frac{\text{rise}}{\text{run}} = \frac{\Delta y}{\Delta x}$.
- Slope-intercept form: $y = mx + b$.
- Graphing using slope and a point.

**Preserved:**
- All major definitions and formulas.
- Worked examples of finding intercepts, computing slope, graphing a line.
- Interpretation of slope as rate of change.

**Reorganized:**
- Combined three modules into a single coherent "Concept 2," emphasizing functions as relationships.
- Moved graphing from "how to plot points" to "how to see a function."
- Emphasized: a function is a machine (input → output), not just an equation.

**Not included:**
- Horizontal and vertical lines (edge cases; covered in the rewrite implicitly).
- Parallel and perpendicular lines (advanced; excluded to keep focus).
- Desmos activities and interactive tools (out of scope for a textbook chapter).

### Concept 3: Systems of Equations

**Source:** Primarily m00106 (700 lines).

**Preserved:**
- Definition of system of linear equations in two variables.
- Checking if an ordered pair is a solution.
- Solving by substitution.
- Solving by elimination (adding/subtracting equations).
- Solving by graphing (identifying the intersection).
- Special cases: no solution (parallel lines), infinitely many solutions (same line).
- Applications: restaurant meals, shopping, two-job scenarios.

**Reorganized:**
- Simplified the order: graphic first, then algebraic methods. The rewrite leads with the visual (two lines intersect), then shows algebra as a way to find that point precisely.
- Condensed repetitive examples; kept the strongest illustrative ones.

**Not included:**
- Three-variable systems (scope creep; beyond "liberal-arts essential").
- Matrices and determinants (m00106 does not cover these; avoided).

---

## Deferred material and rationale

### m00100: Linear Inequalities in One Variable

**Why deferred:**
- Single-variable inequalities ($x > 5$, $-3 \leq x < 10$) are less central to civic mathematics than equations.
- Graphing on a number line is a specialized skill; graphing on the coordinate plane (m00107, which is also deferred) is more useful.
- Systems of inequalities (the payoff of m00100) are advanced and deferred.

**Future home:** Chapter 6 (Money Management) may use constraints like "you can spend at most \$X" and "at least Y percent"; those are better integrated in context. Linear inequalities as a standalone topic could live in a supplementary algebra appendix.

### m00101: Ratios and Proportions

**Why deferred:**
- Ratios and proportions are essential for Chapter 6 (Money) and Chapter 8 (Statistics: percent, rates, unit conversions).
- Starting algebra in a vacuum, before the reader encounters real need, makes them feel abstract.
- Better to teach proportions in Chapter 6 (loan rates, credit card APR) or Chapter 8 (comparing distributions, scaling data).

**Future home:** Chapter 6 section on interest and rates; Chapter 8 section on comparing groups.

### m00102: Polynomials, Factoring, Quadratics

**Why deferred:**
- Scope: this chapter already covers three major concepts. Adding polynomials and quadratics would push it to 12,000+ words, making it unwieldy.
- Audience: liberal-arts students do not encounter quadratics in voting, geometry, probability, or statistics (Chapters 11, 10, 7, 8). They appear in physics and engineering—specialized fields.
- Scaffolding: the algebra foundation (equations, functions, systems) is sufficient for all remaining chapters except, possibly, a specialized chapter on optimization.

**Future home:** Optional Chapter 5B ("Quadratics and Optimization") for students pursuing math/science, or a post-textbook skill module.

### m00104b (Graphing Two-Variable Inequalities)

**Why deferred:**
- Deferred with m00107 (Systems of Linear Inequalities), which builds on it.
- Not strictly necessary for the core Concepts 1–3.

**Future home:** Chapter 11 (Voting) may benefit from visualizing constraints as regions; could be taught there as a case study, not as a separate topic.

### m00108: Linear Programming

**Why deferred:**
- Structure appears in Chapter 5 Concept 3 (systems of equations).
- Full linear programming (objective function + multiple inequality constraints + optimization) is advanced.
- Real-world applications (airline scheduling, manufacturing, supply chains) are valuable but specialized.

**Future home:** Elective Chapter 5C ("Optimization and Linear Programming") or a specialized course.

---

## Source-level notes and decisions

### Motivational material

The source modules contain substantial motivational text ("Why is algebra hard?", "The jump from arithmetic is difficult..."). The rewrite preserves motivation but grounds it in immediate, concrete examples (used-car wages, pizza cost, restaurant bill) rather than abstract exhortations. The reader sees algebra as a tool *before* being asked to care about it.

### Terminology

The source introduces many terms: coefficient, like terms, monomial, binomial, trinomial, polynomial, linear equation, standard form, etc. The rewrite uses only the essential ones: **variable, equation, solution, function, domain, range, slope, intercept, system**. Others are deferred or dropped as jargon.

### Worked examples

The source provides 20+ worked examples across the 12 files. The rewrite selects 8–10 strong ones, each illustrating a *different* principle or application. Repeated examples (five different ways to solve $2x + 3 = 11$) are consolidated to one, with a note that the method generalizes.

### Real-world applications

The source excels at grounding each skill in a real scenario: taxi rentals, cell phone bills, gym memberships, snowblower rentals, restaurant meals, sports equipment. The rewrite keeps these authentic examples but uses them more sparingly, focusing on the method rather than accumulating dozens of near-identical problems.

### Exercises

The source's "Check Your Understanding" sections are extensive (often 8–10 problems per section). The rewrite provides graduated exercises (warm-up, application, synthesis, challenge) with 2–4 per level. The principle is *depth over breadth*: one well-solved problem teaches more than five skimmed ones.

---

## Structural decisions

### Why three concepts?

- **One concept per section is not enough.** A chapter on "equations only" leaves students unable to see relationships; a chapter on "functions only" is abstract without the ability to solve for unknowns.
- **Three concepts scaffold naturally:** (1) How to find an unknown (equations). (2) How to describe a relationship (functions). (3) How to handle multiple unknowns simultaneously (systems).
- **Four or more concepts overloads a single chapter.** The cognitive load of learning polynomials, quadratics, and systems in one chapter is high. Better to master three thoroughly.

### Why the order: equations, then functions, then systems?

- **Equations first:** Students need the foundational skill (solving) before abstracting to functions.
- **Functions second:** With equation-solving as a baseline, students can evaluate functions and graph them.
- **Systems third:** With both equations and functions in hand, students can see two equations as two lines and their solution as an intersection.
- **Alternative considered:** Functions first (more abstract, motivates equations as special cases). Rejected: students without foundational solving skills struggle to evaluate functions.

### Integration section

The integration section (The Restaurant Receipt) spirals back to the concrete pizza scenario from the introduction, showing how adding constraints pushes you from one equation to a system. This mirrors the pedagogical principle: concrete → abstract → back to concrete (application).

---

## Quality checks against source

1. **No mathematical errors:** All facts, formulas, and solutions are verified against the source materials. ✓
2. **Preservation of key examples:** The strong worked examples (linear equations, restaurant bill, intersection of lines) are retained and integrated. ✓
3. **Accessibility:** Technical jargon is defined on first use or avoided. ✓
4. **Scope boundaries:** The chapter does not overreach into quadratics, inequalities, or programming. ✓
5. **Rigor without pedantry:** Definitions are precise; proofs and derivations are sketched, not omitted. ✓

---

## Notes for future instructors

- **Chapter 5 is not the only place to teach these ideas.** Instructors using this book may reinforce equations and systems in Chapter 6 (loan equations) and Chapter 8 (regression, which is a system of equations).
- **Deferred topics can be integrated on-demand.** If a student encounters a problem requiring quadratics or proportions, those can be taught as mini-units at the point of use.
- **Graphing technology (Desmos, GeoGebra) is recommended** but not required. All examples can be graphed by hand; technology deepens understanding.
- **The exercises are scaffolded.** Warm-up exercises check basic skills; application exercises ask students to solve realistic problems; synthesis exercises connect multiple ideas; challenge exercises push deeper.

---

## Summary table: What's in, what's out

| Idea | In Chapter 5? | If out, where? | Rationale |
|------|---------------|----------------|-----------|
| Variables | ✓ (Concept 1) | — | Core to all algebra. |
| Linear equations | ✓ (Concept 1) | — | Essential skill. |
| Evaluating expressions | Partial | Not a focus | Covered via function evaluation. |
| Algebraic operations (add, subtract, multiply, divide expressions) | Brief | Chapter 6+ (as needed) | Assumes students can apply operations to numbers; focus here is on *solving*. |
| Ratios and proportions | — | Chapter 6 | Better motivated by money/interest. |
| Functions and function notation | ✓ (Concept 2) | — | Central to representing relationships. |
| Graphing functions | ✓ (Concept 2) | — | Visualizing relationships. |
| Slope and rate of change | ✓ (Concept 2) | — | Interpreting graphs. |
| Linear inequalities (1 variable) | — | Chapter 6+ or appendix | Less central than equations; can be added when needed. |
| Systems of linear equations | ✓ (Concept 3) | — | Modeling with constraints. |
| Systems of linear inequalities | — | Optional supplement | Advanced; rarely used in citizen-level math. |
| Polynomials, binomials, trinomials | Brief (nomenclature) | Appendix or 5B | Specialized; needed for quadratics. |
| Factoring trinomials | — | Appendix or 5B | Specialized skill; not central to this audience. |
| Quadratic equations | — | Appendix or 5B | Not used in Chapters 6–13. |
| Linear programming | — | Optional 5C or 11 | Advanced; can be taught as optimization in voting/apportionment. |

