# Images for Chapter 12 — Graph Theory

## Figure descriptions and placements

### Opening scene: Königsberg bridges and graph representation

**[FIGURE: Map of Königsberg with four regions and seven bridges]**
- Left: Historical map showing the Pregel River splitting the city into four regions connected by seven bridges.
- Placement: Early in "Opening — Königsberg, 1736" section.
- Purpose: Grounds the reader in the historical puzzle before abstracting to graph form.

**[FIGURE: Graph representation of Königsberg]**
- Four vertices (dots) labeled with region names or letters A, B, C, D.
- Seven edges (lines) connecting them, showing which regions are bridged.
- Note the multi-edge: two bridges connect the same pair of regions.
- Placement: Immediately after the Königsberg map.
- Purpose: Shows the abstraction from geography to structure.

---

### Concept 1: Vertices, edges, and degree

**[FIGURE: Airport network with five vertices and six edges]**
- Five cities: Denver, Chicago, Atlanta, Phoenix, Miami (or simplified as letters).
- Edges represent direct flights.
- Placement: In "Picture an airport during morning departures" section.
- Purpose: Grounded, relatable example of a graph.

**[FIGURE: A graph with vertices labeled and degrees marked]**
- Show a small graph (5-6 vertices) where each vertex is labeled with a letter or name and annotated with its degree.
- Example: vertex A has degree 2, vertex B has degree 3, etc.
- Placement: After "Count the edges that meet at one vertex" in Concept 1.
- Purpose: Clarifies degree calculation.

**[FIGURE: The conference room problem graph]**
- Five vertices representing Alice, Bob, Carol, Dan, Eve.
- Edges representing previous collaborations as described in the example.
- Show the graph as a pentagon with two interior edges.
- Placement: In the "Example: The conference room problem" section.
- Purpose: Concrete, named-person example.

**[FIGURE: Complete graph K₅]**
- Five vertices, all pairs connected.
- Annotate each vertex with degree 4.
- Placement: Near Sum of Degrees Theorem discussion.
- Purpose: Shows a highly connected structure and validates the theorem: sum of degrees = 2 × 10 = 20.

---

### Concept 2: Euler circuits and routes

**[FIGURE: A connected graph with all even-degree vertices]**
- Example: Four vertices arranged in a square, with edges forming the square and diagonals (or similar structure ensuring all degrees are even).
- Placement: In "When does an Euler circuit exist?" section.
- Purpose: Shows a graph where Euler circuit exists.

**[FIGURE: A connected graph with some odd-degree vertices]**
- Same square or similar structure, but with one or more edges removed so some vertices have odd degree.
- Placement: Right after the previous figure for contrast.
- Purpose: Demonstrates that Euler circuit does not exist.

**[FIGURE: 2×2 grid of streets (4 intersections, 6 streets)]**
- Four intersections as vertices.
- Six streets as edges (the four edges forming the square perimeter plus two diagonals or cross-streets).
- Annotate degrees: corners have degree 3, center has degree 4 (if applicable).
- Placement: In "Example: Does the delivery route exist?" section.
- Purpose: Realistic urban delivery scenario.

**[FIGURE: 3×3 grid of streets]**
- Nine intersections as vertices in a grid layout.
- Streets as edges connecting adjacent intersections.
- Annotate that interior vertices have degree 4, edge vertices have degree 3, corner vertices have degree 2... Actually, reconsider. In a 3×3 grid, edges are the streets between intersections, so each intersection connects to 2, 3, or 4 others. This creates even degrees for a proper grid. Annotate accordingly.
- Placement: Following the 2×2 example.
- Purpose: Shows a scenario where Euler circuit is possible.

**[FIGURE: Königsberg graph with odd degrees marked]**
- Redraw the Königsberg graph with degree annotations: (3, 3, 3, 3) for all four regions.
- Highlight that all are odd.
- Placement: In "Integration — From Königsberg to Your Neighborhood" section.
- Purpose: Reinforces the historical example with modern notation.

**[FIGURE: Königsberg graph after Eulerization]**
- Same graph but with one edge duplicated (drawn in a different color or dashed line).
- Show that after duplication, the degrees become (4, 3, 4, 3) or similar—all even.
- Placement: Immediately after the previous figure.
- Purpose: Shows the solution: repeat a street to enable an Euler circuit.

---

### Concept 3: Hamilton cycles and TSP

**[FIGURE: A dodecahedron wireframe]**
- The 3D polyhedron shown as a 2D projection or unfolding.
- Placement: Early in Concept 3 to ground the historical Hamilton puzzle.
- Purpose: Visual hook to the puzzle's origin.

**[FIGURE: A pentagon with a Hamilton cycle highlighted]**
- Five vertices arranged in a circle.
- Edges forming the cycle highlighted (perhaps in bold or color).
- Placement: Example of a graph that has both Euler trails (if degrees are right) and Hamilton cycles.
- Purpose: Shows a small graph where finding a Hamilton cycle is easy to visualize.

**[FIGURE: Complete graph K₄ (four cities)]**
- Four vertices (cities: Denver, Chicago, Atlanta, Miami).
- All pairs connected.
- Placement: In "Example: TSP with four cities" section.
- Purpose: Shows a small TSP instance.

**[FIGURE: Four possible tours in K₄ with distances annotated]**
- Draw or list the three distinct cycles (or six if showing direction separately).
- Annotate each with its total distance.
- Highlight the shortest.
- Placement: Immediately following the K₄ figure.
- Purpose: Demonstrates brute-force enumeration.

**[FIGURE: Nearest neighbor heuristic on K₄, step by step]**
- Multiple panels showing the nearest-neighbor algorithm's progression.
- Starting vertex, first nearest, second nearest, third, return.
- Annotate distances at each step.
- Final tour distance.
- Placement: Following the brute-force example.
- Purpose: Shows how a heuristic progresses versus exhaustive search.

---

### General structural figures

**[FIGURE: A disconnected graph with two components]**
- Component 1: three vertices, connected.
- Component 2: two vertices, connected, isolated from component 1.
- Placement: In any section discussing connectedness.
- Purpose: Clarifies the concept of components.

**[FIGURE: A tree (acyclic connected graph)]**
- 5-6 vertices with no cycles.
- Could be a family tree or generic tree structure.
- Placement: When trees are mentioned.
- Purpose: Shows what acyclic, connected structure looks like.

**[FIGURE: A graph with cycles and a highlighted cycle]**
- A more complex graph with multiple cycles.
- Highlight one cycle (perhaps a triangle or a larger cycle) in color.
- Placement: When discussing cycles.
- Purpose: Clarifies that cycles can exist within larger graphs.

---

### TSP heuristic visualization

**[FIGURE: Nearest neighbor heuristic on a larger map]**
- Several cities scattered on a region.
- Starting point marked.
- Lines showing the progression of nearest-neighbor choices.
- Final tour shown.
- Placement: In the TSP applications discussion.
- Purpose: Shows that the heuristic can produce reasonable-looking tours for realistic instances.

---

## Technical notes for figures

- **Vertex labels:** Use lowercase letters (a, b, c, ...) for generic graphs; use descriptive names (city names, person names) for applied examples.
- **Edge styles:** Simple lines for unweighted; labeled numbers for weighted edges (TSP distances).
- **Degree annotations:** Place degree labels near or inside vertices, e.g., "deg(a) = 2" or just "2" inside the vertex.
- **Color and emphasis:** Use color to highlight Euler circuits (if drawn), Hamilton cycles, odd-degree vertices, or duplicated edges. But keep primary diagrams in black/gray for accessibility.
- **Avoid clutter:** Keep graphs simple enough to read. Vertices should not overlap; edges should not cross unless necessary (planar drawings preferred).
- **Consistency:** Use consistent vertex sizes, edge thickness, and font sizes across all figures.

---

## Links to primary source figures from OpenStax

The original OpenStax chapter has numerous figures for:
- Maps of regions with shared borders (Four Corners, Midwest states)
- Social network examples (Roblox friends, triadic closure)
- Various graph configurations showing degree differences
- Examples of isomorphic and non-isomorphic graphs
- Floor plans converted to graphs
- Maze diagrams and their graph representations

**Status:** Original figures removed per instruction. Descriptions and references placed here to guide recreation if needed. New figures should be drawn to match Nik's voice: grounded in named places and people, clean and minimalist.

