# Chapter 1 — Sets

## Cold open

The Red Cross van is parked outside a community center in a Boston suburb on a Saturday morning, and you are sitting in a folding chair with a cuff on your arm and a tube full of your own blood working its way out of you. The phlebotomist tapes a label to the bag. The label reads *AB negative*. She glances at the cooler beside her, where the bags from earlier donors have been sorted into compartments — *O+*, *A+*, *B+*, *O−*, *A−*, *B−*, *AB+*, *AB−* — eight little cells.

She is not just labeling bags. She is, without thinking about it, performing one of the oldest moves in mathematics. She is dividing the universe of donors at this drive into groups. The groups are exhaustive — every donor lands somewhere — and they are mutually exclusive — no donor lands in two cells at once. Then she counts: forty-six donors today carried the A factor in their blood. Sixteen carried no Rh+ at all. Seven were O−, the universal donor type, which is the bag the trauma-team doctors will reach for first when they don't know who they're trying to save.

A *set* is a collection of things treated as a single object. The donors with type A blood form a set. The donors with the Rh+ factor form another set. The donors with both — type A *and* Rh+ — form a third set, which is the *intersection* of the first two. The donors with either A *or* Rh+ form the *union*. The whole drive — every donor in the cooler — is the *universal set* for the day. The complement of "type A donors" is everyone else.

You can run an entire blood bank on this vocabulary. Hospitals do. The Major League Soccer general manager picking eleven starters from a thirty-player roster does too — the starters are a *subset* of the roster. So does the relational database under the application that processes your tax return, the Venn diagram on the kitchen wall where your kids sort dinosaurs by armor and diet, and the social-media advertising algorithm deciding whether to show you a running shoe based on your search history.

This chapter teaches you the vocabulary. It is short, careful vocabulary. Most of it is older than algebra. All of it is doing real work right now in places you can touch.

### Learning objectives

By the end of this chapter you will be able to:

- **Represent** a set in roster, set-builder, and Venn-diagram form, and translate between the three.
- **Compute** the cardinality of finite sets and recognize the cardinality of basic infinite sets.
- **Distinguish** equal sets from equivalent sets and explain why the distinction matters.
- **List** all subsets of a finite set and **calculate** the number of subsets without listing them, using the formula $2^{n(A)}$.
- **Determine** the union, intersection, and complement of sets and apply the cardinality formula $n(A \cup B) = n(A) + n(B) - n(A \cap B)$.
- **Construct** Venn diagrams with two and three sets and use them to read off cardinalities from real-world data.

### Prerequisites

Arithmetic with whole numbers. The ability to read $2^3 = 2 \cdot 2 \cdot 2 = 8$ without flinching. Comfort with the idea that $0$ is a number, not a placeholder for nothing.

### Why this chapter matters

Every chapter that follows uses set vocabulary. Logic is sets of propositions joined by AND and OR. Probability is the ratio of one set to another. Statistics groups data into sets and asks how those sets behave. Graph theory builds networks out of sets of vertices. Voting theory begins with the set of voters and the set of candidates. The reason this is Chapter 1 is that it is the alphabet — every later chapter spells things with it.

---

## Concept 1 — What a set is, and how to write one down

You opened your kitchen drawer this morning to get a fork. The drawer is a *collection* of objects: forks, spoons, butter knives, the meat thermometer your mother-in-law bought you, a can opener with a chipped handle. The drawer is, if you squint at it sideways, a set. The forks and the spoons and the can opener are *elements* of that set.

Mathematicians like to write things down compactly. The kitchen drawer, written down, looks like this:

$$F = \{\text{fork}, \text{spoon}, \text{knife}, \text{meat thermometer}, \text{can opener}\}$$

Capital letter for the set. Curly braces around the elements. Commas between the elements. This is called the *roster method* or *listing method*. It is the simplest way to write a set, and it works whenever you can list everything that's in there.

### Well-defined sets, and what's not one

For a collection to be a set in the mathematical sense, membership has to be decidable. Either an item is in or it isn't, and any two people looking at the same item should agree.

The collection of all U.S. vice presidents in history is a set. Either someone was the U.S. vice president or they wasn't. Joe Biden, yes. Britney Spears, no. There is no ambiguity.

The collection of *old cats* is not a set. "Old" is a fuzzy word. A friend of mine thinks her seven-year-old tabby is old. My grandmother's cat is fourteen and she calls it middle-aged. The membership criterion does not give the same answer to two reasonable observers. A collection that fails this test is not yet a set; it's a notion that needs sharpening before mathematics can touch it.

This will come up again in Chapter 2 when we look at logic. Vague terms cannot be reasoned with. Math earns its rigor here, in the first sentence of the first chapter, by refusing to work with definitions that wobble.

### The empty set

Some sets have no elements at all. The set of women who served as U.S. vice president before January 20, 2021, is empty. (Kamala Harris was sworn in on that day; before then, none.) The set of prime numbers less than two is empty. (A prime is a whole number greater than one that is divisible only by itself and one. The smallest prime is two. There aren't any below it.) The set of birds that are also mammals is empty.

The empty set has its own symbol: $\emptyset$. You can also write it $\{\}$. They mean the same thing — a set with nothing in it.

A common pitfall: $\{0\}$ is **not** the empty set. It is a set containing one element, which happens to be the number zero. Symbolically, $\{0\} \neq \{\}$. The set is the box; the elements are what's in the box. A box containing a small "0" is not the same as an empty box.

### Ellipses for patterns and infinity

What about big sets you can't comfortably list? The lowercase English alphabet has twenty-six letters. You could write all of them:

$$A = \{a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z\}$$

But it's faster to write:

$$A = \{a, b, c, \ldots, z\}$$

The three dots — the *ellipsis* — say *and so on, in the obvious pattern, until*. You list the first three to establish the pattern, drop in the dots, and (for a finite set) end with the last element.

For infinite sets you don't end. The natural numbers, also called the counting numbers — the numbers you'd use to count cookies or chairs — have no largest member. There is always one more.

$$\mathbb{N} = \{1, 2, 3, \ldots\}$$

The blackboard-bold $\mathbb{N}$ is reserved for this set; whenever you see it, it means the natural numbers. The ellipsis has nothing after it because there's nothing after it: the set runs forever.

The integers — natural numbers, their negatives, and zero — also run forever, but in both directions:

$$\mathbb{Z} = \{\ldots, -2, -1, 0, 1, 2, \ldots\}$$

The $\mathbb{Z}$ comes from *Zahlen*, the German word for "numbers."

### Set-builder notation

Sometimes the elements are easier to describe than to list. The set of all rational numbers — fractions — is hard to roster. You can't sensibly write the first three and then dot-dot-dot. Instead you describe the membership rule:

$$\mathbb{Q} = \left\{ \frac{p}{q} \;\middle|\; p \text{ and } q \text{ are integers and } q \neq 0 \right\}$$

Read it aloud: "The set of all $p$ over $q$ such that $p$ and $q$ are integers and $q$ is not zero." The vertical bar means *such that*. Everything before the bar is what the elements look like; everything after is the rule for membership. This is *set-builder notation*. It's the best tool when listing fails.

### Cardinality — counting elements

For a finite set, its *cardinality* is the number of elements in it. We write the cardinality of $F$ as $n(F)$.

The kitchen drawer has five things in it, so $n(F) = 5$. The empty set has nothing in it, so $n(\emptyset) = 0$.

For an infinite set, "how many" gets stranger. Georg Cantor — a nineteenth-century Russian-born German mathematician who basically invented set theory single-handed and once defined a set as "a Many that allows itself to be thought of as a One" — proved that not all infinities are the same size. The natural numbers $\mathbb{N}$ are *countably infinite*; their cardinality is written $\aleph_0$, pronounced "aleph-null." Any set that can be put in one-to-one correspondence with $\mathbb{N}$ is also countably infinite, even when it intuitively feels bigger. The integers, the rationals, the even numbers, the squares — all $\aleph_0$. The real numbers — every point on the number line — are *uncountably infinite*, a strictly larger size of infinity. We won't prove this here, but the result is one of the most beautiful in mathematics, and it is older than your great-grandparents.

### Equal versus equivalent

In everyday English we use the words *equal* and *equivalent* loosely. In set theory they mean different things, and the difference matters.

Two sets are **equal** if they have exactly the same elements. The set of letters in the word *happy* is $\{h, a, p, y\}$. Notice that $p$ appears only once even though it appears twice in the word — when listing a set, repeated elements collapse to a single listing. The set $\{h, a, p, y\}$ equals the set $\{y, p, a, h\}$ because order doesn't matter inside the curly braces. We write $A = B$.

Two sets are **equivalent** if they have the same number of elements — the same cardinality — even if the elements themselves are different. The kitchen drawer $F = \{\text{fork}, \text{spoon}, \text{knife}, \text{meat thermometer}, \text{can opener}\}$ and the set of even numbers from 2 to 10, $E = \{2, 4, 6, 8, 10\}$, both have five elements. They are equivalent: $F \sim E$. They are not equal — a fork is not the number two.

The trade-off here is precision versus generality. *Equal* is the strict, picky relation: same elements, same set. *Equivalent* is the looser, more general relation: same size. *Equal* implies *equivalent* (if two sets have exactly the same elements, they certainly have the same number of elements), but not the other way around. Mathematicians needed both relations because they answer different questions. Are these two collections the same thing? — that's equality. Can I match them up one for one? — that's equivalence. The Toyota dealership with 10 RAV4s, 8 Priuses, 7 Highlanders, and 12 Camrys has a one-to-one correspondence between the set of vehicle types and the set of vehicle counts: $\{\text{RAV4}, \text{Prius}, \text{Highlander}, \text{Camry}\} \sim \{10, 8, 7, 12\}$. Equivalent, four to four. Equal, no — a Camry is not the number twelve.

### Worked example — different ways to write the same set

Write the set of even natural numbers from 2 through 100 in (a) roster notation with an ellipsis and (b) set-builder notation.

*Given:* the even natural numbers from 2 through 100.

*Roster with ellipsis:* establish the pattern with the first three, dot-dot-dot, then close with the last:

$$E = \{2, 4, 6, \ldots, 100\}$$

*Set-builder:* describe the membership rule:

$$E = \{n \mid n = 2k \text{ where } k \in \mathbb{N} \text{ and } 1 \leq k \leq 50\}$$

Both descriptions pick out the same fifty numbers. Cardinality: $n(E) = 50$.

*Check against intuition:* the evens between 2 and 100 are every other natural number. There are 100 natural numbers from 1 to 100, half of them are even, so 50. Matches.

*General lesson:* you should be able to translate between roster and set-builder, choosing whichever is shorter for the situation. A small finite set wants roster. A described pattern wants set-builder. An ellipsis bridges the two when the pattern is obvious.

### Common misconceptions

**Order doesn't matter.** $\{1, 2, 3\}$ and $\{3, 2, 1\}$ are the same set. If order mattered, mathematicians would have used parentheses; they reserved curly braces specifically for unordered collections.

**Repetition doesn't add anything.** $\{a, a, b\}$ and $\{a, b\}$ are the same set. An element is either in the set or it isn't; there's no "in twice."

**Equal and equivalent are not interchangeable.** Many students lose points on the first quiz of a set theory unit by saying two sets are equal when they only mean the same size. Use the picky word when you mean the picky thing.

---

## Concept 2 — Subsets and how to count them

A Major League Soccer team can carry up to thirty players on its roster. On game day, only eighteen suit up. Of those eighteen, eleven start the match. Each smaller group is a *subset* of the larger one. The eleven starters are a subset of the eighteen on the bench-and-field. The eighteen are a subset of the thirty. Choosing well at each level is what general managers and coaches get paid for.

A set $A$ is a **subset** of a set $B$, written $A \subseteq B$, if every member of $A$ is also a member of $B$. The starting eleven are a subset of the game-day eighteen. The kitchen-drawer subset $D = \{\text{fork}, \text{knife}\}$ is a subset of the full drawer $F = \{\text{fork}, \text{spoon}, \text{knife}, \text{meat thermometer}, \text{can opener}\}$ because every element of $D$ is also in $F$.

A subset is a **proper subset**, written $A \subset B$, if it's a subset *and* it's not the whole thing — that is, $B$ has at least one element not in $A$. The kitchen-drawer pair $D \subset F$ is proper because $F$ has the spoon and the meat thermometer and the can opener, none of which are in $D$.

Two edge cases worth memorizing:

1. **Every set is a subset of itself.** $B \subseteq B$ always. The starting eleven from a five-a-side team where everyone plays is still a subset of the team. But $B$ is not a *proper* subset of itself, because there's nothing outside it within itself.

2. **The empty set is a proper subset of every set except itself.** If $B$ is any non-empty set, $\emptyset \subset B$. This sometimes feels weird. Here's why it works: a subset relation $A \subseteq B$ requires that every element of $A$ also be in $B$. The empty set has no elements at all. There's no element that fails the test, so the test is vacuously satisfied. Mathematicians call this kind of statement *vacuously true*.

### Listing all the subsets of a finite set

Suppose you walk into an airport newsstand and the rack has three things on it: a newspaper, a magazine, and a paperback book. Call this set $L = \{\text{newspaper}, \text{magazine}, \text{book}\}$. How many ways can you walk out — including walking out empty-handed?

You can leave with all three. You can leave with two of them, and there are three ways to choose which two. You can leave with one of them, and there are three ways to choose which one. You can leave with none.

Here are all eight:

- Three items: $\{\text{newspaper}, \text{magazine}, \text{book}\}$
- Two items: $\{\text{newspaper}, \text{magazine}\}$, $\{\text{newspaper}, \text{book}\}$, $\{\text{magazine}, \text{book}\}$
- One item: $\{\text{newspaper}\}$, $\{\text{magazine}\}$, $\{\text{book}\}$
- Zero items: $\{\,\}$ — the empty set

That's $1 + 3 + 3 + 1 = 8$ subsets.

A two-element set, like a coin you might flip, $\{H, T\}$, has $1 + 2 + 1 = 4$ subsets: $\{H, T\}, \{H\}, \{T\}, \{\,\}$.

A one-element set has 2 subsets: itself and the empty set.

The empty set has 1 subset: itself.

### The 2-to-the-n trick

Look at the count: 1 subset of $\emptyset$, 2 subsets of a one-element set, 4 subsets of a two-element set, 8 subsets of a three-element set. Each time you add an element, the number of subsets *doubles*.

That's not a coincidence. Here's why. To build a subset of $\{a, b, c\}$, you have to make three independent yes-or-no decisions. Is $a$ in or out? Is $b$ in or out? Is $c$ in or out? Each decision has two options. The total number of combinations is $2 \cdot 2 \cdot 2 = 2^3 = 8$.

In general, if a set $A$ has $n(A)$ elements, the number of subsets of $A$ is

$$\text{Number of subsets of } A = 2^{n(A)}$$

This works for any size, including the empty set: $2^0 = 1$, and the empty set does have one subset (itself).

### Worked example — counting without listing

How many subsets does the set of the top five all-time NBA scorers have? The set is $S = \{\text{LeBron James}, \text{Kareem Abdul-Jabbar}, \text{Karl Malone}, \text{Kobe Bryant}, \text{Michael Jordan}\}$.

*Given:* $n(S) = 5$.

*Apply formula:* $2^{n(S)} = 2^5 = 32$.

*Sanity check:* could you list them? Yes, but it would take a while. There would be one subset with all five names, $\binom{5}{4} = 5$ subsets with four names, $\binom{5}{3} = 10$ with three, $\binom{5}{2} = 10$ with two, $\binom{5}{1} = 5$ with one, and $\binom{5}{0} = 1$ with none. Total: $1 + 5 + 10 + 10 + 5 + 1 = 32$. Matches. (The $\binom{n}{k}$ notation is read "$n$ choose $k$." We'll meet it properly in Chapter 7.)

*General lesson:* doubling per element gets very large very fast. A ten-person team has $2^{10} = 1{,}024$ subsets. A standard fifty-state country has $2^{50}$, which is more than a quadrillion. This is why combinatorial problems explode. Chapter 7 will lean on this fact.

### Equivalent subsets of an infinite set — a small Galileo wonder

Here's a thing that bothered Galileo Galilei in the early seventeenth century. The set of natural numbers $\mathbb{N} = \{1, 2, 3, 4, 5, \ldots\}$ contains the set of perfect squares $\{1, 4, 9, 16, 25, \ldots\}$ as a subset. The squares are, in any common-sense reckoning, a "smaller" portion of the naturals — they get rarer as you go up — and yet you can pair them off:

$$1 \leftrightarrow 1, \quad 2 \leftrightarrow 4, \quad 3 \leftrightarrow 9, \quad 4 \leftrightarrow 16, \quad 5 \leftrightarrow 25, \quad \ldots$$

Every natural number has a unique square. Every square has a unique natural-number root. The two sets are *equivalent*: same cardinality. Galileo, sensibly, concluded that the words *less than*, *greater than*, and *equal to* don't apply to infinite sets the same way they apply to finite ones. He stopped there.

Two and a half centuries later, Cantor showed that the situation is more interesting than Galileo realized, but Galileo's instinct was right: a part can be the same size as the whole when both are infinite. The set of even numbers is equivalent to all the natural numbers. The set of multiples of three, $\{3, 6, 9, \ldots\}$, is equivalent to all the natural numbers. In set-builder notation:

$$\{m \mid m = 3n \text{ where } n \in \mathbb{N}\}$$

The pairing $n \leftrightarrow 3n$ matches them one to one.

### Common misconceptions

**The empty set is its own kind of subset.** Students sometimes leave it out when listing subsets. Don't. It always appears. A four-element set has $2^4 = 16$ subsets, and one of them is $\{\,\}$.

**The set itself counts as a subset.** When the problem says "list all subsets," that includes the whole set. It does not include the whole set if the problem says "list all *proper* subsets" — there the whole set is excluded.

**Doubling, not adding.** Every additional element doubles the subset count, doesn't add to it. Five elements is $32$, not $10$.

---

## Concept 3 — Set operations and Venn diagrams

A high-school teacher walks her class through what they did to study for the last test. Forty-three students answered. Twenty-four made flash cards. Fourteen reviewed their notes. Twenty-seven completed the practice review. Some did multiple things — twelve did the review and made flash cards, nine did review-plus-notes, seven did flash-cards-plus-notes — and five overachieving souls did all three. A handful did nothing.

The teacher wants a picture. She draws three overlapping circles, one per study technique, inside a rectangle representing the whole class. Then she fills in the regions where the circles overlap. The picture is called a *Venn diagram*, and it lets her read off the answer to questions like *how many students studied with only flash cards?* without doing extra arithmetic in her head. The picture does the bookkeeping.

### The vocabulary of combination

Sets can be combined with three operations.

The **union** of two sets is everything in either one — $A \cup B = \{x \mid x \in A \text{ or } x \in B\}$. The symbol $\cup$ is shaped like a cup; you can pour both sets into it. The little ∈ symbol means *is an element of*; ∉ means *is not an element of*. Read $\cup$ as *or*. To be in the union, an element has to be in at least one of the sets — possibly both.

The **intersection** of two sets is what they have in common — $A \cap B = \{x \mid x \in A \text{ and } x \in B\}$. The symbol $\cap$ is shaped like a hat; both sets have to wear it for an element to qualify. Read $\cap$ as *and*.

The **complement** of a set is everything that's *not* in it, within some understood universal set — $A' = \{x \in U \mid x \notin A\}$. The prime mark says *not in here*. The complement requires you to specify the universe — complement of what, against what?

### Why the universal set matters

Consider the set $A = \{2, 4, 6, 8\}$. What is $A'$?

You can't answer that without knowing the universe. If $U = \{1, 2, 3, 4, 5, 6, 7, 8, 9, 10\}$, then $A' = \{1, 3, 5, 7, 9, 10\}$. If $U$ is the natural numbers, $A' = \mathbb{N} \setminus \{2, 4, 6, 8\}$, which is everything from 1 except those four numbers — an infinite set. If $U$ is the even numbers, $A'$ is the even numbers other than 2, 4, 6, 8 — an infinite set of even numbers.

This is the trade-off of the complement operation. Complement is a fast way to flip a set, but it carries a hidden dependency on what universe you've agreed on. In Chapter 7 (Probability) this becomes important: $P(\text{not } A) = 1 - P(A)$ assumes you've nailed down what the sample space is.

### Venn diagrams

A *Venn diagram* is a picture for sets. Named after John Venn, an English logician who formalized them in 1881 — though circles for set relationships were used by Leonhard Euler more than a century earlier. (The "Venn" name stuck because Venn made the diagrams systematic; he added shading conventions and the enclosing universal-set rectangle. C. L. Dodgson, better known as Lewis Carroll, refined them further.)

The convention: draw the universal set as a rectangle. Draw each subset as a circle inside the rectangle. If two subsets share elements, their circles overlap. If they share none — they are *disjoint* — the circles don't touch.

[FIGURE: Two-set Venn diagram. Rectangle labeled "U". Inside, two overlapping circles labeled "A" and "B". The overlapping lens region is where the elements common to both sets sit. The student should notice four regions: only-A, only-B, both, and neither.]

[FIGURE: Three-set Venn diagram. Rectangle labeled "U". Inside, three overlapping circles labeled "A", "B", and "C", arranged so that all three pairs overlap and there's a central region where all three meet. The student should notice eight regions, including the four at every two-way intersection plus the central three-way intersection plus the three "only-one" regions plus the "outside-all" region.]

Two intersecting circles partition the rectangle into four regions: in $A$ but not $B$; in $B$ but not $A$; in both; in neither. Three intersecting circles partition it into eight regions. Each additional set roughly doubles the diagram's complexity, which is why Venn diagrams stop being convenient past three or four sets — though the math doesn't stop. It just outgrows the picture.

### The cardinality formula for unions

If you want to know how many elements are in $A \cup B$, you might be tempted to add $n(A) + n(B)$. That's wrong when the sets overlap. You'd be double-counting everyone who's in both.

Subtract the double-count once and you've got it right:

$$n(A \cup B) = n(A) + n(B) - n(A \cap B)$$

If the sets are disjoint, $n(A \cap B) = 0$ and the formula collapses to $n(A) + n(B)$. If they overlap, the subtraction undoes the double-count.

### Worked example — the cake-and-ice-cream party

Don Woods is hosting a Juneteenth celebration for fifty-four people. Thirty guests took cake. Twenty took ice cream. Twelve took neither. How many took both?

*Given:*
- Universe $U$: 54 guests.
- Set $C$: cake-takers, $n(C) = 30$.
- Set $I$: ice-cream-takers, $n(I) = 20$.
- Neither: 12 guests, which means $n((C \cup I)') = 12$.

*Asked:* $n(C \cap I)$ — how many took both.

*Reasoning:*

Step 1. Find how many had cake or ice cream (the union):

$$n(C \cup I) = n(U) - n((C \cup I)') = 54 - 12 = 42$$

Step 2. Apply the union cardinality formula:

$$n(C \cup I) = n(C) + n(I) - n(C \cap I)$$

$$42 = 30 + 20 - n(C \cap I)$$

$$42 = 50 - n(C \cap I)$$

$$n(C \cap I) = 50 - 42 = 8$$

*Check:* eight people had both. The thirty cake-takers consist of 8 who also had ice cream and 22 who had only cake. The twenty ice-cream-takers consist of 8 who also had cake and 12 who had only ice cream. Cake-only plus ice-cream-only plus both plus neither: $22 + 12 + 8 + 12 = 54$. Matches the guest count.

*General lesson:* the union formula plus a Venn diagram converts word-problem chaos into bookkeeping. The trick is always to start from the inside out — innermost overlap first, then two-way overlaps, then single-set-only regions, then the "outside everything" region.

### Worked example — the three-set study survey

Forty-three students surveyed. Twenty-four made flash cards. Fourteen studied notes. Twenty-seven completed the review. Twelve did review-and-flash-cards. Nine did review-and-notes. Seven did flash-cards-and-notes. Five did all three. How many did none of the three?

*Strategy: build the Venn diagram inside out.*

Step 1. The center — all three. Five students.

Step 2. The two-way overlaps. Each "exactly two" region equals (the count for that two-way) minus (the all-three count), because the all-three center is contained in each two-way overlap.

- Review-and-flash-cards-but-not-notes: $12 - 5 = 7$
- Review-and-notes-but-not-flash-cards: $9 - 5 = 4$
- Flash-cards-and-notes-but-not-review: $7 - 5 = 2$

Step 3. The single-set-only regions. Each "only this one" region equals (the total for that set) minus (everything already accounted for inside that set).

- Flash cards only: $24 - 7 - 5 - 2 = 10$
- Notes only: $14 - 4 - 5 - 2 = 3$
- Review only: $27 - 7 - 5 - 4 = 11$

Step 4. Add up everything inside the three circles: $5 + 7 + 4 + 2 + 10 + 3 + 11 = 42$.

Step 5. The remaining region — outside all three circles — is the universe minus the inside-circles total: $43 - 42 = 1$.

*Answer:* one student didn't do any of the three.

*Check:* Let's verify the flash-cards count. Flash-cards-only (10) + flash-cards-and-review-only (7) + flash-cards-and-notes-only (2) + all-three (5) = $24$. Matches the given $n(\text{flash cards}) = 24$. The diagram is internally consistent.

*General lesson:* three-set Venn diagrams look intimidating until you discipline yourself to fill them in from the deepest overlap outward. Each region, once you have it, can be cross-checked against any single-set total it sits inside.

### De Morgan's laws — and why complements flip ANDs and ORs

Augustus De Morgan, a nineteenth-century English mathematician and a contemporary of John Venn, proved a pair of identities that sound abstract but capture a deep structural fact about sets:

$$(A \cup B)' = A' \cap B'$$

$$(A \cap B)' = A' \cup B'$$

Read the first one in English: "Things that are not in (A or B) are exactly the things that are not in A *and* not in B." That is, to be outside the union of two sets, you have to be outside *both*. Conversely, to be in the union, you only have to be in at least one.

The second: "Things that are not in (A and B) are exactly the things that are not in A *or* not in B." To miss the intersection, you only have to miss *one* of the sets.

Notice what's happening. Complement flips union into intersection and intersection into union. There's a duality.

### Worked example — verifying De Morgan with a small universe

Let $U = \{1, 2, 3, 4, 5, 6, 7\}$, $A = \{2, 3, 4\}$, $B = \{3, 4, 5, 6\}$. Verify $(A \cup B)' = A' \cap B'$.

*Left side:*
- $A \cup B = \{2, 3, 4, 5, 6\}$
- $(A \cup B)' = \{1, 7\}$ (the elements of $U$ not in the union)

*Right side:*
- $A' = \{1, 5, 6, 7\}$ (the elements of $U$ not in $A$)
- $B' = \{1, 2, 7\}$ (the elements of $U$ not in $B$)
- $A' \cap B' = \{1, 7\}$ (the elements both complements share)

Both sides equal $\{1, 7\}$. ✓

*General lesson:* checking with a specific small example is not a proof — the identity could hold by coincidence for that universe. For a real proof you'd shade two Venn diagrams (one for each side) and confirm the regions match. We'll return to this kind of structural argument in Chapter 2 on logic, where the same duality shows up between AND and OR in propositions.

### Common misconceptions

**Union does not mean "add."** $n(A \cup B) \neq n(A) + n(B)$ unless the sets are disjoint. The intersection has to be subtracted to avoid double-counting.

**Disjoint vs. complement.** $A$ and $A'$ are always disjoint (they share nothing) and their union is always $U$. But two arbitrary sets can be disjoint without being complements. Lions and tigers are disjoint subsets of cats, but neither is the complement of the other within cats — there are also leopards, jaguars, ocelots, house cats.

**The complement depends on the universe.** Always specify $U$ before computing $A'$.

---

## Integration — the blood bank, finished

Return to the Saturday-morning blood drive from the cold open. The cooler holds 100 donor bags from the day. We can describe what's in it with three sets: $A$ for donors with the type-A factor, $B$ for the type-B factor, and $\text{Rh}^+$ for the Rh-positive factor. Each donor lands in one of eight cells based on which combination of factors they carry, and a Venn diagram with three intersecting circles is a natural picture for the cooler.

[FIGURE: Three-set Venn diagram showing blood-type donor counts. Circles labeled A, B, and Rh+. Each region populated with a count: O− (outside all three) = 7; A− = 6; A+ = 36; B− = 2; B+ = 33; AB− = 1; AB+ = 3; O+ = 12. The student should notice that adding any single circle's regions gives the cardinality of that blood factor, and that the universe of 100 is the sum of all eight regions.]

Suppose the totals come out:

| Region | Blood type | Count |
|---|---|---|
| Outside all three | O− | 7 |
| Only A | A− | 6 |
| Only B | B− | 2 |
| Only Rh+ | O+ | 12 |
| A and Rh+ only | A+ | 36 |
| B and Rh+ only | B+ | 33 |
| A and B only | AB− | 1 |
| All three | AB+ | 3 |

Sum: $7 + 6 + 2 + 12 + 36 + 33 + 1 + 3 = 100$. ✓

Now read the cooler.

How many donors carry the A factor? Sum the four regions inside circle $A$: $A^- + A^+ + AB^- + AB^+ = 6 + 36 + 1 + 3 = 46$.

How many donors are Rh+? Sum the four regions inside circle $\text{Rh}^+$: $O^+ + A^+ + B^+ + AB^+ = 12 + 36 + 33 + 3 = 84$.

How many donors are Rh−? By the complement formula, $n(U) - n(\text{Rh}^+) = 100 - 84 = 16$. Or sum directly: $O^- + A^- + B^- + AB^- = 7 + 6 + 2 + 1 = 16$. Both methods agree.

Julio has type B+. He needs surgery and his hospital says he can accept any blood without a type-A factor. How many of today's bags can his transfusion team use? That's the complement of $A$ — everything outside the A circle: $7 + 2 + 12 + 33 = 54$ bags. Equivalently, $100 - n(A) = 100 - 46 = 54$.

This is set theory doing the work. The phlebotomist sorted 100 strangers into eight cells. The hospital's protocol then asks the cells a question, and the cells answer in numbers.

The pattern repeats every time you sort and count, in fields that look very different from blood banks. A web analytics dashboard sorts visitors into cells by which two ads they clicked and which three pages they viewed. A relational database sorts customers into cells by which products they've purchased. A presidential primary sorts voters into cells by which candidates they ranked and which they didn't. The mathematics is the same: a universe, some subsets, the operations of union, intersection, and complement, and a discipline of counting.

That's why this is Chapter 1.

---

## Exercises

### Warm-up

**Exercise 1.1** *(LO: represent and compute.)* Let $K = \{a, e, i, o, u\}$. (a) Compute $n(K)$. (b) Write $K$ in set-builder notation. (c) Determine whether $\{a, i\} \subset K$, and explain in one sentence.

**Exercise 1.2** *(LO: represent.)* Write each of the following sets in roster notation, using an ellipsis where helpful.

(a) The set of months whose names begin with the letter J.
(b) The set of natural numbers that are perfect squares less than 100.
(c) The set of integers between $-3$ and $4$ inclusive.

**Exercise 1.3** *(LO: equal vs. equivalent.)* For each pair of sets, state whether they are equal, equivalent but not equal, or neither.

(a) The set of letters in *listen* and the set of letters in *silent*.
(b) The set of even natural numbers $\leq 10$ and the set of odd natural numbers $\leq 10$.
(c) $\{2, 4, 6, 8\}$ and $\{8, 6, 4, 2\}$.

### Application

**Exercise 1.4** *(LO: subset counting.)* You have five bills in your wallet: a $1, a $5, a $10, a $20, and a $50. (a) How many distinct combinations of these bills can you take out, including taking nothing? (b) Of those combinations, how many give you exactly $25? List them.

**Exercise 1.5** *(LO: union/intersection cardinality.)* A music festival sold 800 tickets. 540 attendees said they came mainly for the indie-rock acts; 320 said they came mainly for the hip-hop acts; 90 said both equally. How many came mainly for one of the genres but not both? How many for neither?

**Exercise 1.6** *(LO: complement.)* Given $U = \{1, 2, 3, \ldots, 12\}$ and $P = \{2, 3, 5, 7, 11\}$ (the primes in $U$), find $P'$. What set is $P'$ in plain English?

**Exercise 1.7** *(LO: Venn diagram interpretation.)* From a survey of 200 commuters: 110 use the subway, 80 ride a bike at least sometimes, 30 do both. Draw a two-set Venn diagram and use it to answer: how many use the subway only? How many neither bike nor subway?

### Synthesis

**Exercise 1.8** *(LO: synthesis — three-set diagram.)* A college canteen surveyed 200 students about coffee, tea, and energy drinks during finals week. 110 drank coffee. 60 drank tea. 80 drank energy drinks. 30 drank coffee and tea. 40 drank coffee and energy drinks. 20 drank tea and energy drinks. 10 drank all three. (a) How many drank none of the three? (b) How many drank exactly one? (c) How many drank exactly two?

**Exercise 1.9** *(LO: De Morgan + computation.)* Let $U = \{1, 2, 3, \ldots, 10\}$, $A = \{1, 2, 3, 4, 5\}$, $B = \{4, 5, 6, 7\}$.

(a) Compute $A \cup B$, $A \cap B$, $A'$, $B'$.
(b) Verify $(A \cup B)' = A' \cap B'$ by computing both sides.
(c) Verify $(A \cap B)' = A' \cup B'$ by computing both sides.

**Exercise 1.10** *(LO: subsets of a roster.)* List all the subsets of the set $T = \{\text{red}, \text{blue}, \text{yellow}\}$. Confirm the count matches $2^3$.

### Challenge

**Exercise 1.11** *(LO: open-ended, points forward.)* Cantor showed that the natural numbers and the positive even numbers have the same cardinality. (a) Construct an explicit one-to-one correspondence between $\mathbb{N}$ and the positive even numbers. (b) Construct one between $\mathbb{N}$ and the integers $\mathbb{Z}$. (Hint: alternate signs.) (c) Why doesn't the same trick work for $\mathbb{N}$ and the real numbers? (You don't need to prove it; describe the obstacle in your own words. We won't formally answer this until much later, if at all.)

**Exercise 1.12** *(LO: model a real situation.)* You're hosting a party with 25 guests. You're tracking three things: who RSVP'd yes, who has a dietary restriction, and who has young children coming. You need: a count of the people you need to call to confirm; a count of guests who'll need a vegetarian option; a count of how many car seats to expect; and a count of how many guests are *only* in the "RSVP'd yes" set with no other complications. Choose plausible cardinalities for each set and overlap, draw a three-set Venn diagram, and answer all four questions. State your assumptions about the cardinalities so that someone reviewing your work can re-do the arithmetic.

---

## Chapter summary

You can now do five things you probably could not do an hour ago.

You can take a vague description of a collection — *the items in my kitchen drawer*, *the donors at today's blood drive*, *the students who studied for the test* — and decide whether it counts as a well-defined set. If it does, you can write it down in three different notations and compute its size.

You can count the number of subsets of a finite collection without listing them, using $2^n$. This will reappear in probability, in genetics, in computer science, anywhere choices proliferate.

You can combine two or more sets with union, intersection, and complement, and you can do the bookkeeping with the formula $n(A \cup B) = n(A) + n(B) - n(A \cap B)$ instead of trying to hold all the overlaps in your head.

You can read and build Venn diagrams with up to three sets and use them to answer real questions about real overlapping populations.

And you have met a small piece of one of the most beautiful results in mathematics: that infinite sets can be the same size as proper parts of themselves, and that — beyond that — there are different sizes of infinity. We won't prove that here. But it is in the room.

The thing to watch for, going forward, is the **universal set**. Almost every common set-theory mistake — and almost every common probability mistake — comes from being sloppy about what universe we're working in. State the universe first. State it explicitly. Everything else is bookkeeping.

What you should now be able to teach a friend who asks: how to count subsets without listing them, why $\{0\}$ isn't the same as $\{\,\}$, and why doubling is the right rule and addition isn't.

---

## Connections forward

Chapter 2 is about logic. You will learn that the AND of intersection and the OR of union are the same AND and OR that govern propositions in logical reasoning. The duality you saw in De Morgan's laws — that complement flips intersection and union — appears again as the rule that *not (P and Q)* is equivalent to *not P or not Q*. The vocabulary of sets and the vocabulary of logic turn out to be, as Cantor would have liked, a Many that can be thought of as a One.

Then in Chapter 7 you will see that probability is built on top of sets. Every probability question begins with a *sample space*, which is a universal set, and an *event*, which is a subset of that sample space. Every probability identity — including the long-misunderstood birthday-problem result — is an application of the union and complement formulas you learned today, dressed up in fractions instead of counts.

The drawer, the blood bank, the study survey, the cake-and-ice-cream party. Same picture every time. The picture is sets.
