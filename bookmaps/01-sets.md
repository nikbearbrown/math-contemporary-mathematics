# Source map — Chapter 1: Sets

## Source files

- `01-m00010.md` — Chapter intro (kitchen-drawer / flatware analogy, brief framing of sets in statistical studies). Contributed: chapter cold-open kitchen-drawer reference; Concept 1 opening anchor.
- `02-m00011.md` — Sets and ways to represent them (roster, set-builder, ellipsis, well-defined sets, empty set, cardinality, finite/infinite, equal vs. equivalent, Cantor biographical note). Contributed: full Concept 1 — primary source for notation, cardinality, equal/equivalent distinction, and the Cantor reference for $\aleph_0$.
- `03-m00012.md` — Subsets and proper subsets, exponential notation, equivalent subsets (Galileo, MLS roster, NBA scorers, fast-food deal). Contributed: full Concept 2 — primary source for subset definition, $2^n$ formula, Galileo's pairing of naturals with squares.
- `04-m00013.md` — Universal set, Venn diagrams (single-subset case), complement of a set. Contributed: Concept 3 — primary source for universal set, Venn diagram conventions, complement operation.
- `05-m00014.md` — Intersection and union of two sets, cardinality formula $n(A \cup B) = n(A) + n(B) - n(A \cap B)$, AND/OR set operations, Venn diagrams with two sets, John Venn / Euler / Lewis Carroll history note. Contributed: Concept 3 — union, intersection, the cardinality formula, the cake-and-ice-cream worked example.
- `06-m00015.md` — Three-set Venn diagrams, three-set operations, blood-types example, study-survey example, De Morgan's law for complement over union, projects on the continuum hypothesis and set notation. Contributed: Concept 3 three-set examples — three-set Venn construction, blood-bank integration, study-survey worked example, De Morgan's laws.

## Concept coverage

- **Concept 1 — What a set is, and how to write one down.** Primary source: m00011. Supplementary: m00010 (chapter intro framing).
- **Concept 2 — Subsets and how to count them.** Primary source: m00012.
- **Concept 3 — Set operations and Venn diagrams.** Primary sources: m00013 (universal set, complement, single-subset Venn), m00014 (two-set operations and cardinality formula), m00015 (three-set diagrams, De Morgan).

## Deferred material

Material in source not used (or only briefly referenced) in the rewritten chapter:

- **Set difference operator $A - B$** — referenced in m00014 and m00015 (within app-promotional notes for "Sets Challenge" and "Venn Diagram" smartphone apps); not introduced in the chapter because the source itself notes this operation is not formally covered. Would belong in a fuller treatment of set algebra. Reason deferred: the chapter is already at adequate length without it, and the source signals it's outside scope.
- **Smartphone-app promotional sections** — m00014 and m00015 each include "Tech Check" notes recommending a "Sets Challenge" Android/iOS app and a "Venn Diagram" Android app. Reason deferred: app-promo content doesn't belong in a textbook chapter; tools come and go, the math endures.
- **The Continuum Hypothesis project** — m00015 ends with a research project on Cantor, Cohen, and the continuum hypothesis. Reason deferred: out of scope for a liberal-arts survey chapter; the seed is mentioned in passing (countable vs. uncountable) and a more thorough treatment would belong in a dedicated infinity chapter or an appendix.
- **Set Notation project (alternative complement, set-difference, symmetric-difference notations)** — m00015. Reason deferred: out of scope for a vocabulary chapter; alternative notations are best introduced when a course needs them.
- **History of the real number system project** — m00015. Reason deferred: belongs in Chapter 3 (Real Numbers and Number Theory).
- **Some "exam" examples** — the source contains a large number of worked examples, and the rewrite consolidates them: every distinct concept gets at least one anchored worked example, but redundant examples (e.g., multiple cardinality drills with substituted nouns) collapse into single representative examples in the rewrite. The pedagogical content is preserved; the duplication isn't.

## Source-level notes

- The source uses inconsistent notation in a few places (the complement is written as $A'$ in the main text, but the embedded app-promo notes mention $A^c$ as an alternative; the source explicitly flags this). The rewrite uses $A'$ throughout, consistent with the source's main-text convention.
- The source flags that the smartphone app "Sets Challenge" uses set-difference notation $A - B$ that isn't covered in the chapter. This was preserved as a deferred item rather than introduced.
- The source's Galileo passage (m00012) attributes to him the conjecture that the concepts of less-than, greater-than, and equal-to don't apply to infinite sets. The rewrite preserves this, with the additional note that Cantor's later work showed the situation is more interesting (different sizes of infinity exist). This is a straight expansion, not an invention; the Cantor mention is sourced from m00011.
- The source includes a generic "Employment Opportunities" career-promo note in m00012 about relational-database design. This is omitted from the rewrite — it's career-info adjacent rather than mathematical content. The relational-database analogy itself (one-to-one correspondence between primary key and associated rows) is deferred; if it returns it should be in a chapter explicitly about applications.
- The source includes a cluster of unfilled `<figure id="fig-XXXXX">` placeholders. These are real figure references in the original textbook that don't render in the markdown export. The rewrite preserves the *content* of the figure references via prose plus the `[FIGURE: ...]` placeholders that point at the briefs in `images/01-sets.md`.
- The source uses Cantor's quote *"A set is a Many that allows itself to be thought of as a One"* — this is attributed to Cantor in the source and is retained in the chapter cold open / chapter summary; the attribution is from secondary sources within the original textbook and is widely repeated. `[verify]` flag is not strictly necessary but production should source it to Cantor's *Beiträge zur Begründung der transfiniten Mengenlehre* (1895–1897) if a primary citation is needed.
