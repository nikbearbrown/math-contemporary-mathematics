# Source map — Chapter 3: Real Numbers and Number Theory

## Source files processed

- **01-m00030.md**: Encryption context (prime factorization, 300 trillion years). Hook material.
- **02-m00041.md**: Divisibility rules, prime and composite numbers, prime factorization, factor trees, GCD, LCM and their applications. Core concepts 1 + skill foundation.
- **03-m00042.md**: Integers, number line, integer comparison, absolute value, addition/subtraction/multiplication/division with integers, applications (net worth). Core concept 2.
- **04-m00043.md**: Order of operations (EMDAS/PEMDAS). Included for context; minimal incorporation (mentioned in fractions section).
- **05-m00044.md**: Rational numbers (definition, perfect squares, terminating/repeating decimals), reducing fractions, adding/subtracting fractions, converting between improper fractions and mixed numbers, decimal-to-fraction conversion, multiplying/dividing fractions, percent, density property. Core concept 3 + applications.
- **06-m00045.md**: Irrational numbers (square roots, pi, simplification, arithmetic with irrationals, rationalizing denominators). **Deferred** — complexity beyond gen-ed scope.
- **07-m00046.md**: Real numbers (subsets: ℕ, ℤ, ℚ, irrationals, ℝ), properties of real numbers (distributive, commutative, associative, identities, inverses). **Partially deferred** — real numbers defined, properties included as reference for later; full treatment deferred.
- **08-m00047.md**: Clock arithmetic (modulo 12, modulo 7). **Deferred** — specialized application, not foundational to number structure.
- **09-m00048.md**: Exponent rules. **Deferred** — belongs in Chapter 4 (number representation).
- **10-m00049.md**: Scientific notation. **Deferred** — belongs in Chapter 4.
- **11-m00050.md**: Arithmetic sequences. **Deferred** — specialized pattern, not core number theory.
- **12-m00051.md**: Geometric sequences. **Deferred** — specialized pattern, not core number theory.

## Concept coverage in rewritten chapter

### Concept 1: Prime Numbers and Factorization
**Primary sources**: 02-m00041.md (divisibility rules, primes, composites, prime factorization, factor trees, GCD, LCM)
- Divisibility definition and rules (by 2, 3, 5, 10)
- Prime vs. composite classification
- Prime factorization algorithm and Fundamental Theorem of Arithmetic
- Factor trees as visual aids
- GCD: definition, application to packing/sharing problems
- LCM: definition, application to scheduling problems
- All worked examples grounded in accessible numbers (140, 247, 12 & 18)

### Concept 2: Integers and Operations
**Primary source**: 03-m00042.md (integers, number line, operations, net worth)
- Integer definition and number line visualization
- Absolute value
- Addition/subtraction with sign rules
- Multiplication/division with sign rules
- Worked example: net wealth with positive and negative assets/debts
- Integration: bank accounts, directed quantities

### Concept 3: Rational Numbers and Arithmetic
**Primary sources**: 05-m00044.md (rational definition, fractions, reduction, arithmetic, percents)
- Rational number definition (ratio of integers)
- Fractions vs. terminating decimals vs. repeating decimals
- Reducing fractions to lowest terms using GCD
- Addition/subtraction with common denominators and LCM
- Multiplication/division without common denominators
- Mixed numbers and improper fractions (reference only, not central)
- Percent as rational number (n/100)
- Worked examples: recipe scaling, banking scenarios, percentage problems
- Density property (brief mention that between any two rationals is another)

## Deferred material and reasons

### Irrational Numbers (06-m00045.md)
**Reason deferred**: Requires understanding of perfect squares, square root simplification, and rationalizing denominators. These are specialized skills. Gen-ed students encounter irrationals primarily in:
- Geometry (side of square with area 2 = $\sqrt{2}$)
- Statistics (normal distribution, where π appears)
- More advanced courses
However, for an introductory chapter on "real numbers and number theory," the focus is on what can be counted, divided, and represented as ratios. Irrationals don't fit that pattern and require separate treatment.

**How to reintegrate**: A follow-up section (Chapter 3, Part 2) or later module would cover:
- What makes a number irrational
- Simplifying square roots
- Arithmetic with radicals
- Rationalizing denominators
- Brief mention that real numbers = rationals ∪ irrationals

### Real Numbers and Properties (07-m00046.md)
**Reason partially deferred**: The chapter briefly defines real numbers as "all possible physical lengths and their negatives." Full treatment (including properties like commutativity, associativity, distributivity) is deferred because:
- Properties are demonstrated through examples but not formalized
- Gen-ed students apply the properties intuitively (e.g., 2×50×13 is easier as 100×13)
- Formal proof of properties belongs in algebra or proof-based courses

**How to reintegrate**: When teaching algebra (Chapter 5), properties are invoked and named. The mention here is sufficient grounding.

### Clock Arithmetic / Modular Arithmetic (08-m00047.md)
**Reason deferred**: Real application (credit card validation, scheduling with cycles), but:
- It's a specialized variant of arithmetic, not foundational to the number systems themselves
- Gen-ed students don't need modular arithmetic to understand integer structure
- Belongs in Chapter 4 (number representation) or as an optional application topic
- Requires separate conceptual framework (remainders, cycling)

**How to reintegrate**: If Chapter 4 treats place value deeply, modular arithmetic fits there as "arithmetic in different cycles."

### Exponent Rules (09-m00048.md)
**Reason deferred**: Exponential notation is about *representation* of numbers, not their structure:
- $2^3$ and $8$ are the same number written differently
- Exponent rules apply in all number systems (integers, rationals, reals)
- Proper home is Chapter 4 (number representation) or Chapter 5 (algebra)

**How to reintegrate**: Chapter 4 covers base-10 place value; other bases; exponent notation; scientific notation. All together.

### Scientific Notation (10-m00049.md)
**Reason deferred**: Like exponents, this is representation, not structure:
- $1.45 \times 10^3$ is a way of writing 1,450 for very large or very small numbers
- Useful in science and engineering, but not essential for gen-ed number theory
- Better integrated into Chapter 4 or Chapter 9 (metric measurement, where micro-, nano-, giga- appear)

**How to reintegrate**: Chapter 4 (place value and notation) or Chapter 9 (units and conversions, where metric prefixes are natural).

### Arithmetic Sequences (11-m00050.md)
**Reason deferred**: Pattern recognition rather than number structure:
- Arithmetic sequences are about fixed differences, not about what numbers *are*
- Not needed for GCD, LCM, fraction operations, or basic integer arithmetic
- Useful context for compound interest (Chapter 6) but not foundational
- Better home: Chapter 6 (Money Management, where they connect to loans/savings) or a dedicated chapter on sequences

**How to reintegrate**: Chapter 6 introduces them for financial applications (e.g., calculating compound interest as a geometric sequence).

### Geometric Sequences (12-m00051.md)
**Reason deferred**: Same as arithmetic sequences, but more specialized:
- Geometric sequences apply to exponential growth/decay
- Essential for compound interest and investment problems
- Better home: Chapter 6 (Money Management) or a dedicated sequences chapter

**How to reintegrate**: Chapter 6 uses geometric sequences for investment doubling time and compound interest calculations.

## Source-level observations

### Strengths of source material
1. **Concrete examples throughout**: Every concept is paired with worked examples (not just definitions).
2. **Progressive difficulty**: Starts with small numbers (36, 12), scales to larger ones (2,117).
3. **Multiple representations**: Factor trees, prime factorization notation, Venn diagrams for GCD/LCM.
4. **Real applications named**: Packing/optimization (GCD), scheduling (LCM), unit conversion (fractions), credit card validation (modular arithmetic).

### Gaps and issues
1. **Separation of concepts**: Each module treats a subtopic in isolation. Fractions section doesn't explicitly connect to GCD/LCM even though they're foundational.
2. **Order of operations (04-m00043.md)**: Taught separately but needed for fraction arithmetic. Mentioned in chapter but not deeply developed.
3. **Irrational numbers introduced late (06-m00045.md)**: Comes after rationals, good, but the pedagogical function (explaining why fractions don't represent *all* numbers) is weak.
4. **Properties of real numbers (07-m00046.md)**: Formalized but not connected to why they matter. "Commutative property of multiplication: 4×13×25 is easier if you compute 4×25=100 first." This intuition is the teaching moment.

### Pedagogical issues resolved in rewrite
1. **Integration**: Wove GCD/LCM into prime factorization section so students see how they follow from prime structure.
2. **Grounding**: Every worked example is a real scenario (bank account, recipe, crypto, camping kits).
3. **Voice alignment**: Used Attenborough × Feynman register consistently—present-tense cold opens, scene-setting, specification of terms before use, honest about what is deferred and why.
4. **Explicit trade-offs**: Named the trade-off (e.g., "gain generality by adding negatives; lose intuition that magnitude is always positive"). Shows why extensions exist.

## Source-level notes for later work

1. **Chapter 4 should open with**: Base-10 representation as a choice (not a law), leading to other bases, leading to exponents and scientific notation.
2. **Chapter 5 (Algebra) needs**: Brief review of properties (distributive, commutative, associative) as they apply to variables. Can reference this chapter.
3. **Chapter 6 (Money) should include**: Arithmetic and geometric sequences in the context of savings, loans, and compound interest.
4. **Optional module or appendix**: Clock/modular arithmetic, if the audience is interested in cryptography or scheduling theory.

