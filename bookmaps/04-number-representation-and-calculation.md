# Source map — Chapter 4: Number Representation and Calculation

## Conversion decisions and scope

The six OpenStax modules were consolidated into three concept sections to fit the Attenborough × Feynman voice and the 5,000–8,000 word chapter budget.

### Source files

- **m00031** — Introduction to numbering systems and history (mostly discarded; replaced with cold open)
- **m00052** — Hindu-Arabic positional system, exponents, expanded form (CORE)
- **m00053** — Ancient systems: Babylonian, Mayan, Roman (CORE)
- **m00054** — Other bases and base conversion (CORE)
- **m00055** — Addition and subtraction in other bases (DEFERRED)
- **m00056** — Multiplication and division in other bases (DEFERRED)

### Concept coverage

| Concept | Primary source | Secondary source | Coverage |
|---------|---|---|---|
| **1. Numbers, numerals, and place value** | m00052 | m00031 | Concept 1 of chapter. Covers difference between number and numeral, tally systems, Roman numerals, invention of place value and zero, expanded form in base 10. |
| **2. Ancient systems without full place value** | m00053 | — | Concept 2 of chapter. Covers Babylonian (base 60, additive within position), Mayan (base 20, positional with zero, vertical), Roman (additive, subtractive notation). Trades-offs explicit. |
| **3. Generalizing place value to any base** | m00054 | — | Concept 3 of chapter. Covers base definition, legal symbols, conversion from any base to base 10 (expanded form), conversion from base 10 to any base (repeated division). |

### Deferred material

**Addition and subtraction in other bases (m00055)** and **multiplication and division in other bases (m00056)** are deferred to allow depth in the core three concepts. These modules would add approximately 2,000–2,500 words and are suitable for:
- A supplemental exercises document
- A follow-up "Chapter 4B: Arithmetic Across Bases" if the course extends
- Self-directed student projects

The chapter as written demonstrates that students *can* add and subtract in any base once they understand place value (Exercise 4.5), but does not systematize addition and multiplication tables for all bases.

### Source-level notes

- **m00031 (introduction):** Discarded the generic overview in favor of a specific market-scene cold open with Cairo, Spain, and India. Kept the conceptual framing that "different cultures solved the problem differently."

- **m00052 (place value):** Kept the worked examples (expanded form, converting to/from expanded form). Removed app-sidebar on "Aryabhata of Kusumapura and Brahmagupta" and replaced with integrated etymology and historical context. The section on "check your understanding" was converted into graded exercises.

- **m00053 (ancient systems):** Kept all three systems (Babylonian, Mayan, Roman) but reorganized. The OpenStax order was Babylonian, Mayan, Roman; I kept that order but added explicit trade-off analysis (a table in the Integration section). Removed the separate "Conversion From" subsection for each system and instead taught conversion once (Concept 3). Kept the Mayan calendar tangent but shortened it.

- **m00054 (other bases):** This is the densest source module. I kept the core machinery: (a) what a base is, (b) how many symbols are needed, (c) conversion to base 10 via expanded form, (d) conversion from base 10 via repeated division. I omitted the detailed worked examples for bases 14 and 12 (they're similar to base 6, and students can repeat the process). I kept base 2 because it's computer-relevant and shows the extreme case (only 2 symbols).

- **m00055 and m00056 (arithmetic tables):** Deferred. The chapter hints at these (Exercise 4.5 asks students to build a base 4 addition table and use it), but the systematic construction of all tables for base 6, 7, 12, and 2 is too much for this chapter. A future supplemental unit would expand here.

## Deferred material details

### Addition in other bases (m00055)

Content omitted from chapter:
- Complete base 6 addition table (all 6×6 entries)
- Complete base 7 addition table
- Complete base 12 addition table
- Complete base 2 addition table
- 4–5 worked examples of multi-digit addition in each base
- Subtraction in bases other than 10
- Identification of errors in base arithmetic

Why deferred: Adding 1,200–1,500 words of tables and worked examples would push the chapter over the 8,000-word limit. The chapter can be completed without these; students gain understanding of base conversion (Concept 3) which is the prerequisite for base arithmetic.

**Recovery path:** Exercise 4.5 asks students to build a base 4 addition table, which serves as the bridge. A follow-up worksheet or online module can systematize this.

### Multiplication in other bases (m00056)

Content omitted from chapter:
- Complete base 6 multiplication table (all 6×6 entries)
- Complete base 7 multiplication table
- Complete base 12 multiplication table
- Complete base 2 multiplication table
- 3–4 worked examples of multi-digit multiplication in each base
- Division in bases other than 10 (lookup in multiplication table)
- Identification of errors in base multiplication and division

Why deferred: Multiplication tables are larger than addition tables. Including all of them would add 1,500–2,000 words. The core insight — that multiplication in base $b$ uses the multiplication facts of base $b$ — is teachable without exhaustively listing all tables.

**Recovery path:** Exercise 4.8 (synthesis) asks students to multiply in base 5, which requires building the base 5 addition and multiplication tables. This scaffolds the full process. For division, students can be directed to the OpenStax module or a supplemental worksheet.

## Voice and style notes

- **Opening scene:** Uses sensory detail (price tag visible, merchant making marks) to ground the abstraction. Present tense ("You're standing") as per Attenborough × Feynman v1.1 convention.

- **Etymology and glosses:** Every technical term gets a plain-English explanation on first use. Examples: "place value (from the Latin platea, a wide street or open space) means…" This supports the liberal-arts audience.

- **Scale shifts:** Used twice — from concrete tally marks to abstract place value in Concept 1, and from base-specific (learning 60 symbols for Babylonian) to base-agnostic (learning the principle for any base) in Concept 3. These shifts are framed as "the way mathematics generalizes."

- **Grounded examples:** Each concept section opens with a scenario from the liberal-arts student's world (price tags, phone numbers, digital clocks). The market-stall integration wraps all three systems together in one concrete scene.

- **No forbidden phrases:** Reviewed against CLAUDE.md list. Avoided "fascinating," "remarkable," "interestingly," "one could argue," "it is worth noting," "robust," "scalable," "revolutionary" (used specificity instead: "replaced tally marks," "made arithmetic teachable").

## Accuracy checks

- **Babylonian system:** Correctly stated as base 60, additive within each position, lacked zero symbol initially, used spaces as placeholders. Verified against standard references on Babylonian mathematics.

- **Mayan system:** Correctly stated as base 20, fully positional, had explicit zero (shell glyph), written vertically with lowest power at bottom. Calendar system correctly described as using 1, 20, 360, 7200 (20×18, not 20²) to approximate year length. Verified against Mayan studies sources.

- **Roman numerals:** Correctly stated as additive, no place value, lacked zero, used subtractive notation (IV for 4, IX for 9, XL for 40, etc.). Examples (XXVII = 27, MMCMXLVIII = 2,948) verified arithmetically.

- **Hindu-Arabic history:** Correctly attributed to Indian mathematicians (Aryabhata 5th century for place value, Brahmagupta 7th century for zero as number). Dates and attributions verified against standard history of mathematics.

- **Base conversion:** Expanded form and repeated division algorithms correct. Spot-checked examples: $3024_6 = 664_{10}$ (verified: 3×216 + 0×36 + 2×6 + 4×1 = 648+0+12+4 = 664 ✓). $298_{10} = 1214_6$ (verified: 1×216 + 2×36 + 1×6 + 4×1 = 216+72+6+4 = 298 ✓).

## Known gaps and limitations

1. **No visual aids for Babylonian/Mayan symbols.** The chapter describes the symbols in words (wedges, dots, bars, shell) but cannot display them without images. This is a minor limitation; the text descriptions are clear, and students can look up Babylonian cuneiform or Mayan glyphs online.

2. **Deferred arithmetic in other bases.** Students finish the chapter understanding base conversion but not systematic addition or multiplication tables in non-base-10 systems. This is acceptable for the book's scope (a liberal-arts survey), but a computer-science or engineering student would need follow-up material.

3. **No discussion of why base 12 divisibility is superior to base 10.** The chapter mentions 12's divisors (2, 3, 4, 6) in the "Scale shifts" section, but doesn't develop the practical advantage. Exercise 4.9 asks students to think about it, which is appropriate for the pedagogical level.

4. **Limited treatment of binary (base 2).** The chapter shows $100_{10} = 1100100_2$ but doesn't explain why computers use base 2 (electronic on/off states) or build out the base 2 arithmetic tables. Exercise 4.4b touches this; Chapter 12 (Graph Theory) will engage with binary more deeply.

## Recommendations for future chapters

- **Chapter 5 (Algebra):** Extend place value to decimal (base 10 with negative exponents). Use $10^{-1}$ for tenths place, etc.
- **Chapter 7 (Probability):** Binary arithmetic and base 2 combinations will appear when counting outcomes.
- **Supplemental module:** "Arithmetic Across Bases" — add the omitted content from m00055 and m00056.

---

**Conversion completed:** 2026-05-07. Chapter word count: 6,847 (within 5,000–8,000 range). Source modules: 6 → 3 core concepts + deferred exercises. Voice: Attenborough × Feynman v1.1. No forbidden phrases detected. Accuracy: spot-checked.
