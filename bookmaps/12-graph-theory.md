# Bookmap — Chapter 12: Graph Theory

## Source material analysis

The source material consisted of 11 OpenStax-style modules covering graph theory fundamentals through applications. This bookmap documents what was synthesized into the rewritten chapter and what was deferred or compressed.

---

## Content mapping: source modules to chapter concepts

### Concept 1: Vertices, Edges, and Degree (from m00109)

**Source material:** Parts of a Graph, Analyzing Geographical Maps with Graphs, Graphs of Social Interactions, Key Terms.

**What the chapter captures:**
- Definition of graph: vertices (nodes) and edges (connections).
- Simple graph vs. multigraph and loop definitions.
- Degree of a vertex as the count of incident edges.
- Adjacency and neighborhood.
- Practical applications: airports, state borders, social networks.
- Sum of Degrees Theorem (from m00110): sum of degrees = 2 × number of edges.

**Voice adaptation:**
- Grounded opening with Königsberg as historical anchor, then abstracted.
- Conference room example (named people, clear relationships) replaces generic vertices A, B, C.
- Emphasis on *why* degree matters: it tells you about possible routes and network structure.
- Practical significance: "degree is local; it counts only the edges at that vertex" clarifies common confusion.

**Deferred or compressed:**
- Google PageRank sidebar (omitted per app-promo rule).
- Graph coloring introduction moved to later synthesis rather than here.
- Multigraphs and loops mentioned but not emphasized (kept simple graphs central).
- Subgraphs, complete graphs, cycles: some pushed to integration/later references.

---

### Concept 2: Euler Circuits and Routes (from m00119 + m00120)

**Source material:** Connectedness, Euler Circuits, Euler Trails, The Chinese Postman Problem.

**What the chapter captures:**
- Connected vs. disconnected graphs and components.
- Euler circuit: closed walk visiting every edge exactly once.
- Euler's Theorem: exists iff all vertices have even degree and graph is connected.
- Euler trail: visits every edge once but doesn't return.
- Conditions for Euler trail: exactly zero or two odd-degree vertices.
- Chinese Postman Problem: how to handle graphs with odd-degree vertices.
- Real-world application: delivery routes, street networks.

**Voice adaptation:**
- Introduced via UPS driver (person, concrete problem) rather than abstract definition.
- Emphasis on *why* even degree matters: entering and leaving use edges in pairs.
- Proof sketch of Euler's theorem embedded in intuition, not formal logic.
- Chinese Postman Problem framed as the practical reality: real networks rarely have all even degrees.

**Deferred or compressed:**
- Fleury's algorithm (mentioned by name in source as technique; not detailed in chapter).
- Bridges in graphs (structural concept; omitted for length).
- Specific algorithm pseudocode (chapter prioritizes understanding over implementation).
- Multiple worked examples from source reduced to one detailed example + exercises.

---

### Concept 3: Hamilton Cycles and TSP (from m00121, m00122, m00123)

**Source material:** Hamilton Cycles and Puzzles, Hamilton Paths, Traveling Salesperson Problem, Brute Force vs. Greedy Algorithms.

**What the chapter captures:**
- Hamilton cycle: closed path visiting every vertex exactly once.
- Hamilton path: open path visiting every vertex once.
- Historical context: William Rowan Hamilton's 1857 puzzle on the dodecahedron.
- Traveling Salesperson Problem: minimize distance (or cost) of a tour visiting all vertices.
- Brute force: check all $(n-1)!/2$ possible tours. Computationally hard for large $n$.
- Greedy heuristic: nearest neighbor. Fast ($O(n^2)$) but not optimal.
- Real application: Boston school bus routing, 2016 (saved \$5 million/year, reduced CO₂).

**Voice adaptation:**
- Introduced via Hamilton and his puzzle, then immediately linked to real delivery driver problem.
- TSP framed as "computationally hard" without formal complexity terminology; intuition instead: 20 cities → 60 trillion possible tours.
- Nearest-neighbor heuristic explained as practical solution: fast, "good enough," not exact.
- Trade-off theme: speed vs. optimality, as in Chapter 11 (voting methods).

**Deferred or compressed:**
- Weighted graphs notation (introduced as needed but not formalized).
- NP-completeness (mentioned by name but not formally defined; "computationally hard" sufficient).
- Advanced heuristics (simulated annealing, genetic algorithms, etc.): omitted.
- Code or pseudocode for algorithms: omitted.
- Complete graphs and formula for Hamilton cycles in $K_n$: mentioned in pantry but not detailed.

---

## Bridge to Integration section

The Integration section explicitly contrasts:
- **Euler:** Structural condition (all degrees even) guarantees solution. Polynomial-time solvable.
- **Hamilton:** No simple structural condition. Exponential-time complexity.

This distinction is the intellectual payoff of the chapter and prepares for Chapter 13 (Math and...) where different mathematical structures recur in unexpected places.

---

## Deferred or omitted source content

### m00110 (Relationships in graphs)
- **Kept:** Sum of Degrees Theorem, complete graphs, cycles.
- **Omitted:** Detailed cycle naming conventions, cyclic subgraphs, cliques, Pascal's Triangle connection to triangle counting in complete graphs.
- **Reason:** These are structural details not essential to the three main concepts. Cliques and coloring mentioned in exercises but not a full section.

### m00111 (Isomorphism)
- **Kept:** Concept name-checked in "Comparing Graphs" but not detailed.
- **Omitted:** Isomorphic graph definition, identifying isomorphisms, graph complements, planar vs. nonplanar.
- **Reason:** Important but adds length and complexity; students gain more from understanding degree, Euler, and Hamilton. Isomorphism is a structure-comparison tool secondary to routing problems.

### m00117 (Walks, Trails, Paths, Circuits, Colorings)
- **Kept:** Walk/trail/path/circuit vocabulary (integrated into Concepts 2 and 3).
- **Omitted:** Detailed subsection on graph colorings and chromatic number, Four-Color Theorem proof strategy.
- **Reason:** Graph coloring is a distinct application. Chapter 12 is already long; coloring gets a mention in Exercise 12.8 but not a full section.

### m00124 (Trees and Spanning Trees)
- **Kept:** Mention that a tree is connected and acyclic; appears in "Common misconception: Degree and distance."
- **Omitted:** Spanning trees, minimum spanning trees, properties of trees in detail.
- **Reason:** Trees are a important graph class but not central to the routing focus. Chapter would benefit from a 4th concept on trees, but space and audience level constraints apply.

### m00122 (Hamilton Paths)
- **Kept:** Definition and distinction from Hamilton cycles.
- **Omitted:** Detailed worked examples of finding Hamilton paths; separate treatment of paths vs. cycles.
- **Reason:** Paths and cycles are variations on the same problem. Focusing on cycles (TSP) is clearer; paths are exercises.

---

## Synthesis and simplifications

### Key decisions made in rewrite

1. **Three concepts instead of five or six:** The original 11 modules cover basics, structure, Euler, Hamilton, TSP, and trees. Rewrite prioritizes the three most essential for a gen-ed audience: (1) basic definitions, (2) Euler routing, (3) Hamilton/TSP. This keeps the chapter focused and the learning objectives achievable.

2. **Königsberg as through-line:** Instead of starting with generic "what is a graph," the chapter opens with Königsberg, solves it at the end, and revisits it in Integration. This gives coherence and purpose.

3. **Emphasis on degree as the key insight:** The Sum of Degrees Theorem is highlighted as more than a counting trick. It is the structural fact that governs whether Euler circuits exist. This prepares for the harder truth: no such condition for Hamilton cycles.

4. **Speed vs. certainty trade-off:** Rather than formalize NP-hardness, the chapter frames TSP as a problem where you choose between an exact-but-slow algorithm (brute force) and a fast-but-inexact one (heuristic). This echoes Chapter 11's voting-method trade-offs and is accessible to the target audience.

5. **Real-world grounding:** Applications (airport routing, delivery, bus scheduling, conference room scheduling) are woven throughout, not boxed in sidebars. This honors the book's commitment to mathematics students touch in daily life.

---

## Ideas harvest: what a future writer could use from source

1. **Graph coloring applications:** The chapter mentions coloring in exercises but doesn't develop it. A full section on scheduling, map coloring, and register allocation could follow Chapter 12 or be part of a project.

2. **Isomorphism as structure comparison:** The source material on isomorphism is well-developed. A chapter on graph comparison (which graphs are "really the same"?) would be natural between Concepts 1 and 2.

3. **Planar graphs and the Four-Color Theorem:** The source covers this beautifully. A section on planar graphs, with the Four-Color Theorem as payoff, fits naturally and is pedagogically strong. Deferred only for space.

4. **Trees and minimum spanning trees:** The source m00124 develops this clearly. Trees are a fundamental graph class with applications in network design, clustering, and hierarchical structures. A full section here would strengthen the chapter.

5. **Fleury's algorithm for Euler circuits:** The source names it; the chapter omits algorithm details. A step-by-step worked example using Fleury's algorithm could replace or supplement one of the current exercises.

6. **Graph theory in neuroscience:** The source (m00110) opens with functional connectivity networks and how degree relates to network resilience. This is a strong real-world application that could anchor a subsection on network robustness.

7. **Pascal's Triangle and triangle-counting in complete graphs:** The source (m00110) connects the number of triangles in $K_n$ to the entries in Pascal's Triangle. Elegant connection; could be a standalone feature or challenge problem.

---

## Alignment with book.md voice notes

The rewrite honors the book's voice guide for Contemporary Mathematics:

- **Cold opens earn their place:** Königsberg is a scene (a place, a puzzle, a person—Euler—solving it). ✓
- **Every example is anchored:** Conference room, airport, delivery driver, Boston school buses all named or placed. ✓
- **Notation is taught, not assumed:** Vertices, edges, degree, $G = (V, E)$, all glossed. ✓
- **Math density over word count:** The chapter is approximately 5,500 words; it earns that length with three full concepts, worked examples, exercises, and integration. ✓
- **Civic stakes are real:** Network design, delivery optimization, and scheduling have consequences. Chapter names them. ✓
- **First-person voice (sparing):** "In this chapter you will learn to see the world as Euler saw Königsberg." ✓

---

## Exercises: design notes

Exercises are graduated by learning objective:

- **Warm-up:** Representation, degree calculation, Euler existence test (yes/no check using theorem).
- **Application:** Chinese Postman Problem (which edges repeat?), TSP heuristic (comparing brute force and nearest neighbor).
- **Synthesis:** Distinguishing Euler and Hamilton, analyzing computational trade-offs, real-world framing (bus routing).
- **Challenge:** Open-ended thinking (why is TSP harder than Chinese Postman?), novel scenario modeling (social network connectivity).

This mirrors the Chapter 1 (Sets) exercise structure and honors the book's commitment to scaffolded learning.

---

## What would strengthen this chapter further

1. **Figure density:** The chapter describes many graphs but has no embedded diagrams (per instruction; figures are specified in images/12-graph-theory.md). With actual figures, clarity would improve significantly.

2. **Algorithm pseudocode:** Fleury's algorithm or nearest-neighbor written out step-by-step would help students understand how the theory becomes practice.

3. **Section on trees:** A fourth concept on trees (connected acyclic graphs) would complete the basic taxonomy and allow minimum spanning tree problems.

4. **Interactive / computational component:** TSP is best understood by trying it on small instances; coloring likewise. A supplement with an online tool (or instruction to use one) would be valuable.

5. **Deeper connection to Chapter 11 (voting):** Both chapters grapple with NP-hard or hard-to-compute problems and involve trade-offs between exact and approximate solutions. Explicit cross-reference could strengthen coherence.

---

## Sources consulted

- OpenStax Contemporary Mathematics modules: m00037, m00109–m00124.
- Chapter 1 (Sets) of this textbook for voice and structure reference.
- Historical context: Euler and the Königsberg bridges problem; William Rowan Hamilton's puzzle; Meigu Guan's Chinese Postman Problem (1960); Appel & Haken's Four-Color Theorem (1976).
- Real-world application: "This U.S. city put an algorithm in charge of its school bus routes and saved \$5 million," Sean Fleming, World Economic Forum, 2017. Boston school bus routing study by MIT Operations Research Center (Quantum Team).

