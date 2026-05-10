# Chapter 12 — Graph Theory

## Three title options

1. **Networks of Dots and Lines: What Graphs Actually Count**
2. **The Shape of Connection: How Maps Become Mathematics**
3. **Routing Reality: From Euler's Bridges to Your Delivery Driver**

---

## TL;DR

A graph is a set of dots (vertices) and lines (edges) that encodes relationships and connections. The degree of a vertex—how many edges meet there—determines whether you can visit every edge exactly once, or visit every location exactly once, and these distinctions unlock the mathematics of routing, scheduling, and network design.

---

## Opening — Königsberg, 1736

In 1736, the mathematician Leonhard Euler received a puzzle from the city of Königsberg, in what is now Russia. The city sat on the Pregel River, and the river split the land into four regions connected by seven bridges. The question was deceptively simple: is there a route that crosses each bridge exactly once and returns to the starting point?

For a long time, nobody had found one. People tried. They failed. They gave up. Euler didn't give up. Instead, he did something radically economical: he threw away the map.

He replaced each of the four regions with a single dot, a *vertex*. Each bridge became a single line, an *edge*, connecting two dots. He drew a picture that looked nothing like the actual city—it didn't preserve distance, or the shape of the banks, or the size of the regions. What it *did* preserve was the single fact that mattered: which regions were connected to which by bridges.

The resulting picture was a *graph*. Not a graph-of-a-function (the $xy$ coordinate plane). A graph in the sense modern mathematicians mean: a collection of vertices connected by edges, stripped of all information except connectivity.

Euler looked at that picture for five minutes and proved it was impossible. Not impossible for that particular arrangement, but impossible in principle, given the way the vertices connected. He did this by asking one question: how many bridges meet at each region?

That one question—what we now call the *degree* of a vertex—contained all the architecture of the problem. It still does. In this chapter you will learn to see the world as Euler saw Königsberg: as a network of points and connections, where the degree of a vertex tells you what kinds of routes are possible.

### Learning objectives

By the end of this chapter you will be able to:

- **Represent** connections as vertices and edges and construct simple graphs from real-world scenarios (airports, social networks, road systems).
- **Calculate** the degree of vertices and apply the Sum of Degrees Theorem to find the number of edges.
- **Determine** whether an Euler circuit or Euler trail exists using the degree sequence.
- **Identify** Hamilton cycles and paths, and apply the Traveling Salesperson Problem to route-optimization contexts.
- **Distinguish** between Euler and Hamilton routes: one visits every edge once, the other visits every vertex once.
- **Solve** real-world routing and scheduling problems using graph-theoretic reasoning.

### Prerequisites

Arithmetic with whole numbers and fractions. Ability to read a simple network diagram. Comfort with the idea that a map is just information—you can throw away the parts that don't matter.

### Why this chapter matters

Graph theory has moved from a curiosity about bridges into one of the most useful mathematical structures in the world. Google's PageRank algorithm, which made Google a search engine and not just a browser, is graph theory: webpages are vertices, hyperlinks are edges. Uber's routing engine is graph theory: intersections are vertices, streets are edges. The internet itself is a graph: computers are vertices, cables are edges. When you schedule a school bus route, deliver packages, plan a network of relationships in a social system, or design a circuit board, you are solving a graph-theory problem. This chapter teaches you to see the problem and the structure of its solution.

---

## Concept 1 — Vertices, Edges, and Degree: The Vocabulary of Connection

Picture an airport during morning departures. Not the building—the system. One airport is Denver. Another is Chicago. Another is Atlanta. Six major airlines operate routes among them. Two planes fly Denver to Chicago daily. One flies Denver to Atlanta. Two fly Chicago to Atlanta. None go the other direction on these specific routes (they do, but we don't draw both directions for a *simple graph*).

From the airport's operational perspective, none of that matters except one fact: which pairs of cities are directly connected? That is the only information a routing algorithm needs to decide if you can get from Denver to Atlanta on a single connection (you cannot—you must go through Chicago). That is the only information the network needs to know to decide if a single plane failure would disconnect the system.

Replace each city with a *vertex*, a dot. Replace each direct-flight route with an *edge*, a line. You get a network of five dots and lines. You have made a *graph* (from the Greek root meaning "to write" or "to draw").

Here is the formal definition with the ancient terminology attached:

A **graph** $G$ consists of a set of *vertices* (from the Latin for "highest point" or "crown"—the nodes where edges meet) and a set of *edges* connecting pairs of vertices. We write $G = (V, E)$ where $V$ is the set of vertices and $E$ is the set of edges.

In our airport example: $V = \{\text{Denver}, \text{Chicago}, \text{Atlanta}, \text{Phoenix}, \text{Miami}\}$ and $E$ consists of the six flight routes listed above.

### What makes a simple graph simple

Not all graphs are simple. A *loop* is an edge that connects a vertex to itself. A *multiple edge* (or *double edge*) is when two vertices are connected by more than one edge. A *simple graph* forbids both. It's the version we use when the question is purely about whether two things are connected, not how many ways or in what direction.

This matters because the structure of a simple graph—which pairs of vertices touch—is all that matters for routing and connectivity. We will work almost entirely with simple graphs.

### The degree of a vertex and what it reveals

Count the edges that meet at one vertex. That number is its *degree*. In a simple graph on five cities with six routes, if Denver has two routes, its degree is 2. Chicago, which has three routes (to Denver, Atlanta, and two of the other cities if they connect) might have degree 3.

The degree of a vertex is not just a number. It is a constraint. A vertex of degree 0 is *isolated*—it has no connections. A vertex of degree 1 is a *leaf* or *pendant vertex*—it is a dead end. A vertex of degree 2 is on a path but can keep going. High-degree vertices are the hubs. The degree distribution of a graph—what degrees the vertices have—determines what kinds of routes are possible.

### Example: The conference room problem

A conference room has five people: Alice, Bob, Carol, Dan, and Eve. Before the meeting, we want to know who has worked with whom before. We represent each person as a vertex. If two people have worked together, we draw an edge. 

From interviews, we learn:
- Alice has worked with Bob and Carol (degree 2).
- Bob has worked with Alice, Carol, and Dan (degree 3).
- Carol has worked with Alice, Bob, and Eve (degree 3).
- Dan has worked with Bob and Eve (degree 2).
- Eve has worked with Carol and Dan (degree 2).

The graph looks like a pentagon: all five people are connected in a loop, with two interior edges (Alice-Carol and Bob-Eve). The degree sequence is (2, 3, 3, 2, 2).

Now, a practical question: can we divide the room so that no two people in the same subgroup have worked together before? This is a *graph coloring* problem, which we will return to. For now, notice: the degree sequence tells us something about the structure. This graph has a cycle, so it is *not* a tree. The highest degree is 3, so it requires at least 3 colors to separate adjacent people.

### The Sum of Degrees Theorem

Add up all the degrees: $2 + 3 + 3 + 2 + 2 = 12$. Count the edges: 6. Notice that $12 = 2 \cdot 6$. This is not an accident.

**The Sum of Degrees Theorem** states:

$$\sum_{v \in V} \deg(v) = 2|E|$$

That is, the sum of all degrees equals twice the number of edges. Why? Because each edge has two endpoints. When you sum the degrees, you count each edge twice—once at each end. So if you know the degree sequence, you can find the number of edges by adding the degrees and dividing by 2.

### Example: Determining edge count from degree sequence

Suppose a graph has six vertices with degrees 3, 3, 2, 2, 2, 2. The sum is $3 + 3 + 2 + 2 + 2 + 2 = 14$. So the number of edges is $14 / 2 = 7$.

If someone claims the graph has 6 edges, you know they made an error—the degrees alone prove it impossible.

### Adjacency and neighborhood

Two vertices are *adjacent* (or *neighboring*) if an edge connects them. The *neighborhood* of a vertex $v$ is the set of all vertices adjacent to $v$. The degree of $v$ is the size of its neighborhood.

In the conference room, Alice's neighborhood is $\{\text{Bob}, \text{Carol}\}$. Bob's neighborhood is $\{\text{Alice}, \text{Carol}, \text{Dan}\}$.

### Common misconception: Degree and distance

The degree of a vertex is not how far away it is from other vertices. A leaf vertex (degree 1) might be very central if it's the only bridge to another large component. Degree is local: it counts only the edges *at* that vertex.

---

## Concept 2 — Euler Circuits and Routes: Visiting Every Edge Exactly Once

In the winter of 1962, a UPS delivery driver in Milwaukee faced a simple problem: he had a list of streets to cover. Some intersections he had to cross multiple times. Some streets he had to drive twice. His supervisor asked: could he plan a route that covered every street exactly once and ended where he started?

He didn't know it, but he was asking for an *Euler circuit*.

An **Euler circuit** is a closed walk that traverses every edge of a graph exactly once. It starts at a vertex, follows edges (never repeating any edge), and returns to the starting vertex.

### When does an Euler circuit exist?

Here is the beautiful answer: an Euler circuit exists if and only if every vertex has even degree and the graph is connected.

Why even degree? Imagine you are walking an Euler circuit. Every time you enter a vertex (except the start), you must leave it—that uses up two edges. When you return to the start, you must enter and leave once more—another two edges. So every vertex must have degree $2k$ for some integer $k$. Odd-degree vertices are dead ends: you get stuck.

Think about what happens if a vertex has degree 3 (odd). Suppose you walk in on edge 1, out on edge 2. Now one edge is still connected to that vertex—edge 3. If you return to that vertex later in your walk, you enter on one edge (that leaves you at the vertex with only edge 3 unused). You must exit on edge 3. But now all three edges from that vertex have been traversed, and you're outside the vertex. You can never return to it without repeating an edge. That's why odd-degree vertices are problems.

**Euler's Theorem (for circuits):** A connected graph has an Euler circuit if and only if every vertex has even degree.

This is a complete characterization: you can check it instantly by counting degrees. No need to search for the circuit first; the degree sequence tells you whether it exists.

### Example: Does the delivery route exist?

A delivery company serves a neighborhood with streets laid out in a grid. They represent the streets as a graph: intersections are vertices, streets are edges. They want a route starting from the depot that drives every street exactly once and returns to the depot.

Let's say the grid is $2 \times 2$ (four intersections arranged in a square). The edges are the six streets around and across the square. Each interior corner has degree 3 (three streets meet). Since 3 is odd, no Euler circuit exists. The driver must repeat at least one street.

By contrast, in a different neighborhood where each intersection has exactly four streets meeting (a $3 \times 3$ grid), every vertex has even degree (at least 2, at most 4). An Euler circuit exists.

### The Chinese Postman Problem

The real world rarely offers perfect Euler circuits. A delivery driver must serve a neighborhood where some streets are shorter than others, or where the street network doesn't have all even degrees. The question becomes: what is the shortest route that covers every street at least once?

This is the **Chinese Postman Problem**, named after Chinese mathematician Meigu Guan, who posed it in the 1960s. The solution is elegant: find all the odd-degree vertices. Add extra edges (repeat streets) to make them all even. Then find an Euler circuit in the augmented graph. This circuit is the shortest solution.

Why must the number of odd-degree vertices be even? By the Sum of Degrees Theorem, the sum of all degrees is even (it equals $2|E|$). If an odd number of vertices had odd degree, the sum would be odd. But the sum of an odd number of odd integers plus any number of even integers is odd, contradicting the theorem. Therefore, odd-degree vertices always come in pairs.

This fact is crucial to the postman problem. You must pair up all odd-degree vertices and add paths between them. The pairing that minimizes the total distance of added paths is the solution. Once you've added those shortest paths (repeating some streets), all vertices have even degree, and an Euler circuit exists.

In practice: if your street network has vertices of odd degree (most do—a typical intersection has degree 3 or 4 depending on the urban grid), you must repeat some streets. The postman problem finds which streets to repeat to minimize total distance. For a mail carrier serving 50 streets with 8 odd-degree intersections, the postman problem identifies the optimal set of streets to drive twice.

### Euler trails: When you don't need to return

Sometimes you don't need to end where you started. An **Euler trail** is a walk that traverses every edge exactly once but doesn't have to return to the starting vertex.

When does an Euler trail exist? When the graph is connected and has exactly zero or two vertices of odd degree.

- Zero odd vertices: an Euler circuit exists (which is also an Euler trail).
- Two odd vertices: an Euler trail exists, and it must start at one odd vertex and end at the other.
- Any other number of odd vertices: no Euler trail exists.

### Example: The Pony Express

Imagine a mail route from Sacramento, California to St. Joseph, Missouri. Each town is a vertex; each stage of the journey is an edge. The postmaster wants a path that covers every stage exactly once, starting in Sacramento and ending in St. Joseph (no return required).

If Sacramento has odd degree and St. Joseph has odd degree, and all other towns have even degree, an Euler trail exists, starting in Sacramento and ending in St. Joseph.

---

## Concept 3 — Hamilton Cycles and the Traveling Salesperson Problem: Visiting Every Vertex Exactly Once

In the 1850s, mathematician William Rowan Hamilton invented a puzzle involving a dodecahedron (a 12-sided solid with 20 vertices). The question: is there a path along the edges that visits every vertex exactly once and returns to the start?

Hamilton was asking for what we now call a **Hamilton cycle** (or **Hamiltonian circuit**): a closed path that visits every vertex exactly once and uses only the edges of the graph.

### Why this is harder than Euler

This seems like a small change from Euler circuits. Instead of visiting every *edge* once, visit every *vertex* once. But the difference is profound.

For Euler circuits, we have a complete characterization: they exist if and only if all degrees are even. We can check this in linear time (count the degree of each vertex). We can find the circuit using Fleury's algorithm: greedily traverse edges without getting stuck, removing traversed edges as you go. The algorithm is linear in the number of edges.

For Hamilton cycles, there is no known efficient characterization. No simple degree condition guarantees a Hamilton cycle. A graph might have high-degree vertices (which you'd think would provide lots of options) and still lack a Hamilton cycle. A graph might be highly connected (nearly complete) and still require exponential time to find one.

Moreover, we don't even have a fast algorithm to *check* if a Hamilton cycle exists (this is the famous P vs. NP problem). The best known methods are:
- **Brute force:** List all $(n-1)!/2$ possible cycles and check each. Time: factorial.
- **Backtracking:** Start at a vertex, try extending a path to unvisited vertices, backtrack if stuck. Time: still exponential in the worst case.
- **Heuristic:** Find a good solution quickly without guarantee of optimality. Time: polynomial, quality: unknown.

For large graphs, finding a Hamilton cycle is computationally hard—intractable, in the precise sense that the problem is NP-complete.

### The Traveling Salesperson Problem (TSP)

The practical version: a salesperson must visit $n$ cities, call on clients in each one, and return home. The cities are vertices; roads between them are edges. Each edge has a *weight*—the distance or cost of travel. The question: what is the shortest tour visiting every city exactly once?

This is **NP-hard**, which means no known algorithm solves it in time proportional to $n$ or $n^2$ or even $n^{100}$. As $n$ grows, the number of possible tours grows as $(n-1)!/2$. Here is the scaling:

- 10 cities: $(10-1)!/2 = 181{,}440$ tours.
- 15 cities: $(15-1)!/2 \approx 43{,}589{,}145{,}600$ tours (43 billion).
- 20 cities: $(20-1)!/2 \approx 60{,}949{,}324{,}566{,}400$ tours (60 trillion).

A computer checking one trillion tours per second (extraordinarily fast) would take:
- 10 cities: 0.18 milliseconds.
- 15 cities: 44 seconds.
- 20 cities: 61 seconds.
- 25 cities: ~100 million seconds (about 3 years).

This is why brute force becomes impractical above about 15 cities. For real-world problems with hundreds or thousands of cities, brute force is not an option.

### Two approaches: exact vs. fast

**Brute Force (exact):** Check every possible tour. For 10 cities, this is feasible. For 20, it starts to strain. For 100, it is impossible.

The number of distinct cycles in a complete graph with $n$ vertices is $(n-1)!/2$. For $n=10$: $9! / 2 = 181{,}440$ cycles. For $n=15$: $14! / 2 \approx 43.6$ billion.

**Nearest Neighbor (heuristic):** Start at a city. At each step, go to the nearest unvisited city. When all cities are visited, return home. This is fast—linear time—but it doesn't guarantee the shortest tour. It usually gets within 20-30% of optimal, sometimes much better.

### Example: TSP with four cities

Suppose a salesperson must visit Denver, Chicago, Atlanta, and Miami. The distances form a complete graph $K_4$ (every city is connected to every other). There are $(4-1)!/2 = 3$ distinct cycles:

1. Denver → Chicago → Atlanta → Miami → Denver: 600 + 720 + 1200 + 2100 = 4620 miles
2. Denver → Chicago → Miami → Atlanta → Denver: 600 + 2100 + 1200 + 720 = 4620 miles
3. Denver → Atlanta → Chicago → Miami → Denver: 720 + 720 + 2100 + 2100 = 5640 miles

(Distances are approximate.) The first two are equivalent (one is the reverse of the other) and both are shorter. Brute force checks all three and picks the best.

Nearest neighbor starting from Denver: Denver → Chicago (nearest, 600) → Atlanta (nearest unvisited, 720) → Miami (only one left, 1200) → Denver (return, 2100) = 4620 miles. In this case, it found the optimal.

### Why TSP matters

TSP is not just a puzzle. In 2016, MIT's Quantum Team used optimization techniques (related to but more sophisticated than TSP heuristics) to redesign Boston's school bus routes. The result: \$5 million in savings per year and a 9,000-kilogram-per-day reduction in CO2 emissions. A single problem, solved better.

### The trade-off: speed vs. certainty

This is a fundamental question in computer science: do you want a guaranteed optimal solution (slow) or a fast answer that is probably pretty good (fast)? 

For real-world routing, fast and good-enough wins. A delivery company serving 500 stops doesn't need the absolute shortest possible route; they need a competent route they can compute in minutes, not years. A heuristic that gets to within 10% of optimal is worth millions of dollars in savings.

For some high-stakes problems (chip design, satellite repositioning, genome sequencing), you might invest in sophisticated exact or near-exact methods—algorithms that use branch-and-bound, dynamic programming, or approximations. These can solve instances with 50-100 cities to proven optimality, given hours of computation.

The choice reflects the business trade-off:
- **Exact (brute force):** Cost: time. Benefit: guaranteed optimal. Used for: small instances where even a few percent savings justify the computation.
- **Heuristic (nearest neighbor):** Cost: no guarantee of optimality. Benefit: instant answer, usually 10-30% above optimal. Used for: large instances where speed and reasonable quality matter more than perfection.
- **Sophisticated algorithms:** Cost: development complexity, moderate computation time. Benefit: often finds near-optimal solutions for medium-sized instances. Used for: problems where both quality and speed matter (e.g., airline scheduling).

---

## Integration — From Königsberg to Your Neighborhood

Return to Euler's bridge problem. The Pregel River separated Königsberg into four regions. Seven bridges connected them. Euler proved no Euler circuit existed because the four regions had degrees 3, 3, 3, 3 (count the bridges at each shore). All odd. By Euler's theorem, an odd number of odd-degree vertices means no Euler circuit.

But Königsberg's citizens still needed to visit all the bridges. Euler's analysis showed the minimum: you must repeat at least one bridge. Eulerize the graph: duplicate one edge. Now all degrees are even. An Euler circuit exists.

This idea generalizes. In 1960, Mei-Ko Kwan generalized Euler's approach to the Chinese Postman Problem: given a connected graph where not all vertices have even degree, find the minimum total weight of edges to duplicate so that an Euler circuit exists.

The solution: identify all odd-degree vertices. Add edges between them to make all degrees even. The added edges should have minimum total weight. This is itself a challenging optimization problem (finding a minimum-weight perfect matching on the odd-degree vertices), but it is tractable. Once you have it, an Euler circuit exists, and you have your minimum-distance delivery route.

In contrast, the Traveling Salesperson Problem asks for a Hamilton cycle in a weighted complete graph—visit every vertex once with minimum total weight. This is harder because there is no structural guarantee about when a Hamilton cycle exists, and finding the optimal one is computationally intractable for large instances.

The mathematics makes a clear distinction:
- **Euler:** Visit every *edge* once. Condition: all degrees even. Solvable in polynomial time.
- **Hamilton:** Visit every *vertex* once. Condition: (none known). Solvable in exponential time (brute force) or heuristically fast.

This distinction—which quantities you must hit exactly once, and what structural conditions they satisfy—is the intellectual spine of routing and network design.

---

## Exercises

### Warm-up

**Exercise 12.1** *(LO: represent and compute degree.)* A social network has five users: Alice, Bob, Carol, Dan, and Eve. Edges represent "mutual friendship." The friendships are: Alice-Bob, Alice-Carol, Bob-Carol, Bob-Dan, Carol-Dan, and Dan-Eve. (a) Draw the graph. (b) Compute the degree of each vertex. (c) Apply the Sum of Degrees Theorem to find the number of edges.

**Exercise 12.2** *(LO: determine existence of Euler circuit.)* For each degree sequence below, determine whether an Euler circuit is possible. Explain using Euler's theorem.

(a) Degrees: 2, 2, 2, 2.

(b) Degrees: 3, 3, 2, 2, 2.

(c) Degrees: 4, 4, 4, 4, 4.

**Exercise 12.3** *(LO: Hamilton vs. Euler.)* A graph has five vertices arranged in a pentagon (a 5-cycle). (a) Is there an Euler circuit? Why or why not? (b) Is there a Hamilton cycle? (c) If you add an edge from the top vertex to the center vertex, does an Euler circuit exist? Does a Hamilton cycle exist?

### Application

**Exercise 12.4** *(LO: apply Chinese Postman Problem.)* A mail carrier must deliver to every street in a neighborhood with six intersections arranged as follows: a central hub with five streets radiating out to five surrounding intersections. Each surrounding intersection has one street back to the hub. (a) Draw this as a graph. (b) Compute the degree of each vertex. (c) Does an Euler circuit exist? (d) If not, which edges must be traversed twice to create a closed route covering all streets?

**Exercise 12.5** *(LO: apply TSP heuristic.)* A salesperson must visit four cities: A, B, C, D. The distances (in miles) are: A-B: 100, A-C: 300, A-D: 200, B-C: 250, B-D: 150, C-D: 200. (a) List all possible tours (cycles). (b) Calculate the distance of each. (c) Which is shortest? (d) Now apply the nearest-neighbor heuristic starting from A. What distance do you get? How does it compare to the optimal?

**Exercise 12.6** *(LO: model a real scenario.)* You are routing a garbage truck through a neighborhood. Every street must be driven at least once. The truck starts and ends at the depot. (a) Is this an Euler circuit problem or a Hamilton problem? (b) If some streets have odd-degree intersections, must the truck drive some streets twice? (c) How would you find which streets to repeat?

### Synthesis

**Exercise 12.7** *(LO: synthesize Euler and Hamilton.)* Consider a complete graph on $n$ vertices. (a) Does it have an Euler circuit for any $n \geq 2$? Explain. (b) Does it have a Hamilton cycle for any $n \geq 3$? Explain. (c) For which values of $n$ is every Euler circuit also a Hamilton circuit?

**Exercise 12.8** *(LO: analyze trade-offs.)* The Chinese Postman Problem is solvable in polynomial time. The Traveling Salesperson Problem is NP-hard. Suppose you have a real-world problem that could be framed either way. (a) When would you choose the postman formulation (visit edges)? (b) When would you choose the salesperson formulation (visit vertices)? (c) What are the computational and practical consequences of each choice?

### Challenge

**Exercise 12.9** *(LO: open-ended exploration.)* In Boston, the 2016 school bus routing problem was to visit every bus stop exactly once on each route, starting and ending at the depot. (a) Is this a Hamilton problem or an Euler problem? (b) Why is minimizing the number of routes (tours) also important? (c) Suppose you have 500 bus stops. Is a brute-force exact solution practical? What approach would you use, and why?

**Exercise 12.10** *(LO: model a novel scenario.)* You are designing a new social network feature: a "trust path" that shows users whether two accounts are connected through mutual friends. (a) Is this asking for existence of an Euler path, a Hamilton path, or neither? (b) What graph structure do you need to guarantee that every pair of accounts is connected? (c) If you want to minimize the "degrees of separation" (longest shortest path), is this an optimization problem analogous to TSP? Explain.

---

## Chapter summary

In this chapter, you have learned to see the world as a network of connections and to ask precise questions about what routes are possible.

**A graph** is a set of vertices (dots) and edges (lines). The degree of a vertex is the number of edges meeting there. By the Sum of Degrees Theorem, the sum of all degrees equals twice the number of edges.

**An Euler circuit** visits every edge exactly once and returns to the start. It exists if and only if all vertices have even degree and the graph is connected. The **Chinese Postman Problem** solves the practical case: given a real street network, which streets should you repeat to create a minimum-distance route covering every street?

**A Hamilton cycle** visits every vertex exactly once and returns to the start. Unlike Euler circuits, there is no simple degree condition for existence. The **Traveling Salesperson Problem** finds the shortest Hamilton cycle in a weighted graph. This is computationally hard, and most real solvers use heuristics like nearest-neighbor rather than brute force.

The distinction is fundamental: degree conditions (local, structural) govern Euler paths; no such condition governs Hamilton paths. This is why routing by edge (postman) is polynomial-time solvable, while routing by vertex (salesperson) is NP-hard.

What you should be able to teach a friend: why Königsberg's bridge problem had no solution, what the Chinese Postman Problem is and why it matters, why finding the shortest tour visiting all cities is computationally harder than finding a route covering all roads.

---

## Connections forward

In Chapter 13, we explore mathematics in art, music, and the built world. Graph theory shows up there too: the graph of a city's street network, encoded in how a composer writes variations on a theme, embedded in the structure of a musical scale.

More broadly, graph theory is the language of networks. Wherever you see systems (social, biological, computational, transportation, neural), you see a graph hiding underneath. The distinction between "visit every edge" and "visit every vertex"—between structural conditions (degrees) and algorithmic hard problems (optimization)—appears again and again across mathematics and computer science. You have learned to ask which kind of problem you are facing, and what tools apply. That discipline of asking is what carries forward.

---

## What would change my mind

I claim the Chinese Postman Problem is polynomial-time solvable while TSP is NP-hard. If someone showed me a polynomial-time algorithm for TSP (solving the P = NP problem), that would change this reading. More modestly, if evidence emerged that real TSP instances have structure that makes heuristics nearly optimal at scale beyond what is currently known, I would adjust the emphasis on why heuristics are necessary in practice.

## Still puzzling

I do not fully understand why degree conditions (sufficient and necessary for Euler circuits) have no analogue for Hamilton cycles. The intuition is clear—edges and vertices are different—but I would like a deeper structural explanation of why checking all degrees doesn't suffice for the Hamilton case. The answer may lie in deeper algebraic or combinatorial structures that this chapter does not expose.

---

## Tags

graph-theory, networks, routing, euler-circuits, hamilton-cycles, traveling-salesman-problem, degree-theorem, chinese-postman, optimization, computational-complexity, feynman-method

