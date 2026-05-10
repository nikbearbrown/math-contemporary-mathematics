# Chapter 10 — Geometry

## Suggested Titles

- **How We Measure the World**: From the Egyptian Rope to GPS Satellites
- **Geometry: The Machinery of Shape and Space**
- **Lines, Angles, and the Pythagorean Theorem: What Builders and Surveyors Know**

---

## TL;DR

Geometry is the mathematics of shape and space. This chapter teaches three core machineries: how lines and angles form the skeleton of the spatial world, how perimeter and area let us measure the boundaries and interiors of shapes, and how the Pythagorean theorem connects the sides of right triangles—a relationship so fundamental it powers everything from construction to GPS.

---

## Cold Open

A surveyor stands at the corner of a plot of land, holding a transit and a measuring tape. The client wants to know the exact distance across the property to the far corner, but there is a pond in the way. The surveyor cannot simply wade through and measure. Instead, she plants a stake at the client's position, walks perpendicular to the direction of the far corner, plants another stake, measures that distance, records the angle back to the far corner, and writes three numbers in her notebook. From those three numbers—using machinery that Pythagoras figured out 2,500 years ago—she calculates the distance across the pond without getting her boots wet.

This is geometry at work. Not the geometry of theorem-proving for theorem-proving's sake, but geometry as an instrument. It is the mathematics of space and shape, born from the need to re-measure Egyptian fields after the Nile flooded them, and still doing the same work today when an engineer needs to know if a beam is truly perpendicular or a contractor needs to know how much concrete fills a foundation.

The word *geometry* comes from Greek: *geo* (earth) and *metron* (measure)—literally, "earth-measuring." That honest etymology is the whole discipline in miniature.

### Learning Objectives

By the end of this chapter you will be able to:

- **Specify** the properties of lines, rays, line segments, angles, and planes; use notation correctly.
- **Distinguish** angle types by measure and relationships (complementary, supplementary, vertical angles); solve for unknown angle measures.
- **Classify** triangles and polygons; compute perimeter and area from dimensions.
- **Apply** the Pythagorean theorem to find unknown sides of right triangles; use it to solve real-world distance problems.
- **Recognize** when similar figures have proportional sides; use that scaling to estimate heights and distances.

### Prerequisites

Comfortable with arithmetic. Ability to solve simple algebraic equations ($ax = b$, $a + bx = c$). Willingness to think visually.

### Why This Chapter Matters

Geometry answers the question "how do we measure space?" It is the foundation for everything that requires knowing distances, angles, areas, or volumes. Construction, surveying, navigation, engineering, physics, computer graphics—all rest on the geometric machinery you will learn here. Unlike logic or probability, which are more abstract, geometry is directly anchored to the world you can touch and see. That makes it the most directly useful mathematics most students encounter.

---

## Concept 1 — Lines, Rays, and Angles: The Language of Direction

You are standing in a city grid. A street runs north-south in front of you. Another runs east-west. Where they meet is a corner—what a geometer calls a *point*. The street itself, running infinitely in both directions, is a *line*. The block you are standing on—the street from this corner to the next corner—is a *line segment*: a line with two endpoints.

In about 300 BCE, Euclid, the Greek mathematician who compiled all geometric knowledge into his *Elements*, did not try to define these objects rigorously. A point was "that which has no part"—it has no width, no length, no dimension, just location. A line was "length without breadth." These descriptions are not proofs; they are *primitives*—concepts so basic that trying to define them in terms of other things would be circular. You can understand the description without needing a formal definition, just as you understand "dog" without needing to construct dogs from smaller concepts.

Here is what we write:

- A point $A$ is named with a capital letter.
- A line segment from point $A$ to point $B$ is written $\overline{AB}$ (a bar over the two letters).
- A ray starting at $A$ and passing through $B$ is written $\overrightarrow{AB}$ (an arrow in one direction).
- A line passing through both $A$ and $B$ is written $\overleftrightarrow{AB}$ (arrows in both directions).

Here is what matters: two distinct points determine exactly one line. One point and a direction determine exactly one ray. A line segment has a definite length; a ray goes on forever in one direction; a line goes on forever in both directions.

Now we introduce direction. When two rays share a starting point (called the *vertex*), they form an *angle*. The angle is measured by the amount of rotation from one ray to the other, typically in degrees. A *straight angle* measures 180°. A *right angle* measures 90° (and is often drawn with a small square at the vertex to indicate it). An *acute angle* measures less than 90°. An *obtuse angle* measures between 90° and 180°.

#### Scale Shift: From the Corner to the Earth

Here is where geometry becomes powerful. The same machinery that measures a corner lot also measures the curvature of the Earth. A surveyor wants to know if two roads are parallel. They check: do the roads maintain a constant distance apart as they extend? By Euclid's definition, two lines in the same plane are *parallel* if they never intersect, no matter how far they extend. In practice, the surveyor uses the fact that parallel lines make equal *corresponding angles* with a third line (called a *transversal*) that crosses them both. If the angles are equal, the lines are parallel. If they are not, one road is drifting toward the other.

When two lines intersect at a right angle—90°—they are *perpendicular*, written $\ell_1 \perp \ell_2$. A perpendicular line is the shortest path from a point to a line.

#### Worked Example: Finding Unknown Angles Using Supplementary Angle Relationships

A surveyor measures the angle between a property line and a new fence to be 47°. The fence runs the full length of the property, which is a straight line (180°). What is the angle on the other side of the fence?

*Given:* One angle measures 47°. The two angles form a straight line (are *supplementary*—sum to 180°).

*Solution:* 
$$180° - 47° = 133°$$

The angle on the other side is 133°.

*Check:* $47° + 133° = 180°$. ✓

*General principle:* Two angles that share a side and together form a straight line are *supplementary*; they always sum to 180°. Two angles that sum to 90° are *complementary*. If you know one, you can always find the other.

#### Common Misconceptions

**Parallel lines are the same as perpendicular lines.** They are opposites. Parallel lines never meet. Perpendicular lines meet at exactly a 90° angle.

**An angle is defined by its shape, not its measure.** A 45° angle and a 47° angle look similar but are different. The degree measure is the entire definition.

**The sum of angles in any configuration is always 180°.** Only for triangles. For a quadrilateral (four-sided shape), the sum is 360°. For a five-sided shape, 540°. The rule is $(n - 2) \times 180°$ for an $n$-sided polygon.

---

## Concept 2 — Polygons, Perimeter, and Area: Measuring Boundaries and Interiors

You are designing a kitchen. The floor is rectangular, measuring 12 feet long and 9 feet wide. You need to:

1. Order enough trim (the wood border along the edges) to go around the room.
2. Order enough tile to cover the floor.

The first is a *perimeter* problem: the sum of the lengths of all the edges. The second is an *area* problem: the total square footage inside the boundary.

A *polygon* is a closed, flat shape made of straight line segments. The line segments are called *sides*; the corners where sides meet are *vertices* (plural of vertex). Polygons are named by the number of sides: a triangle has 3, a quadrilateral has 4, a pentagon has 5, a hexagon has 6, and so on.

#### Perimeter: The Boundary

For your rectangular kitchen:
$$\text{Perimeter} = 2 \times \text{length} + 2 \times \text{width} = 2(12) + 2(9) = 24 + 18 = 42 \text{ feet}$$

You order 42 feet of trim.

For any *regular polygon* (all sides equal, all angles equal), the perimeter is simply:
$$P = n \times s$$
where $n$ is the number of sides and $s$ is the length of one side.

A regular pentagon with sides of 8 cm has perimeter $P = 5 \times 8 = 40$ cm.

For a *circle*—the only polygon-like shape without sides—the perimeter is called the *circumference*. It is related to the radius (distance from center to edge) by:
$$C = 2\pi r \quad \text{or} \quad C = \pi d$$
where $d$ is the diameter (twice the radius) and $\pi \approx 3.14159$.

#### Area: The Interior

Area is measured in square units—square feet, square meters, square inches. Think of it this way: if the floor were tiled with one-foot-square tiles, how many tiles would you need?

For the rectangular kitchen:
$$\text{Area} = \text{length} \times \text{width} = 12 \times 9 = 108 \text{ square feet}$$

For a *triangle*, the area is half of base times height:
$$A = \frac{1}{2} b h$$

The *height* is measured perpendicular (at a 90° angle) to the base. This matters: if the base is 10 cm and you drop a perpendicular from the opposite vertex to that base, and the perpendicular measures 6 cm, then:
$$A = \frac{1}{2} (10)(6) = 30 \text{ square cm}$$

For a *circle*, area is:
$$A = \pi r^2$$

A circle with radius 5 inches has area:
$$A = \pi (5)^2 = 25\pi \approx 78.5 \text{ square inches}$$

#### Worked Example: Calculating Area and Cost for a Real Renovation

You are installing vinyl tile in a rectangular basement measuring 20 feet by 15 feet. Each box of tiles covers 25 square feet and costs $40. How many boxes do you need, and what will you spend?

*Given:*
- Basement dimensions: 20 ft by 15 ft
- Coverage per box: 25 sq ft
- Cost per box: $40

*Solution:*

Step 1. Find the total area of the basement:
$$A = 20 \times 15 = 300 \text{ square feet}$$

Step 2. Divide by the coverage per box to find how many boxes are needed:
$$\text{Boxes needed} = \frac{300}{25} = 12 \text{ boxes}$$

Step 3. Multiply by the cost per box:
$$\text{Total cost} = 12 \times 40 = \$480$$

*Check:* $12 \times 25 = 300$. ✓

*General lesson:* Always break real-world area problems into clear steps: measure, compute total area, divide by unit coverage, multiply by unit cost. The algebra is simple; the care is in getting the dimensions right.

#### Common Misconceptions

**Perimeter and area are the same thing.** They are completely different. Perimeter measures the distance around the boundary (in linear units like feet). Area measures the space inside (in square units like square feet). A shape can have a large perimeter and small area, or vice versa.

**The area formula for a triangle is $A = bh$.** It is $A = \frac{1}{2}bh$. The factor of $\frac{1}{2}$ comes from the fact that a triangle is half of a rectangle with the same base and height.

**The circumference of a circle equals its radius.** Circumference is $2\pi r$, which is about 6.28 times the radius, not equal to it.

---

## Concept 3 — The Pythagorean Theorem: The Most Famous Relationship in Geometry

Right triangles are triangles with one angle measuring exactly 90°. They are the most useful triangles in practice because they appear everywhere: a ladder leaning against a wall, a ramp into a building, the diagonal of a rectangular plot of land. And they obey a rule so elegant and powerful that it has been known for at least 2,500 years.

The *Pythagorean theorem* states:

$$a^2 + b^2 = c^2$$

where $a$ and $b$ are the lengths of the two sides that form the right angle (the *legs*), and $c$ is the length of the side opposite the right angle (the *hypotenuse*—the longest side).

This is not a theorem because it is useful. It is useful because it is a theorem—it follows with mathematical certainty from the axioms Euclid laid down.

#### The Machinery Behind It

Imagine a right triangle with legs of length 3 and 4. Construct a square on each side of the triangle:

- The square on the leg of length 3 has area $3^2 = 9$ square units.
- The square on the leg of length 4 has area $4^2 = 16$ square units.
- The sum is $9 + 16 = 25$ square units.

Now construct a square on the hypotenuse. The Pythagorean theorem says its area will be exactly 25 square units—which means the hypotenuse has length $\sqrt{25} = 5$.

Indeed: $3^2 + 4^2 = 9 + 16 = 25 = 5^2$.

The triple $(3, 4, 5)$ is one of the most ancient *Pythagorean triples*—sets of three whole numbers that satisfy the theorem. Others include $(5, 12, 13)$, $(8, 15, 17)$, and $(7, 24, 25)$. The ancient Babylonians (around 1800 BCE, long before Pythagoras) knew these triples and used them in surveying.

#### Worked Example: Finding the Distance Across a Pond

A surveyor stands at point $A$ on one side of a pond. The point she wants to reach is $B$ on the opposite side. She measures off a perpendicular line from $A$ toward the far shore, marking a point $C$ 60 meters away. From $C$, she turns 90° and measures the distance to $B$, which is 80 meters.

What is the distance directly across the pond from $A$ to $B$?

*Given:*
- $AC = 60$ meters (perpendicular to the direction of $B$)
- $CB = 80$ meters (at a right angle to $AC$)
- Angle $ACB = 90°$

*Solution:* The path $A \to C \to B$ forms a right triangle. The direct distance $AB$ is the hypotenuse.

$$AB^2 = AC^2 + CB^2 = 60^2 + 80^2 = 3,600 + 6,400 = 10,000$$

$$AB = \sqrt{10,000} = 100 \text{ meters}$$

*Check:* This is a scaled version of the $(3, 4, 5)$ Pythagorean triple: $(60, 80, 100) = 20 \times (3, 4, 5)$. ✓

*General lesson:* Whenever you have two perpendicular measurements and need to find the diagonal distance between two points, the Pythagorean theorem is your tool. It turns a measurement problem that would otherwise require walking into a calculation problem.

#### The Scaling Insight: Similar Triangles

Here is a powerful observation. If you take a right triangle with sides 3, 4, and 5, and you scale every dimension by the same factor—say, multiply by 10—you get a right triangle with sides 30, 40, and 50. The angles are exactly the same. The shapes are *similar*: same angles, proportional sides.

This means: if you know the angles of a right triangle, you can figure out the proportions of the sides without measuring them. A ladder leaning against a building at a 30° angle to the ground will always rise in proportion to its length, regardless of whether the ladder is 10 feet or 40 feet long. This is why architects and builders can scale drawings up and down without losing accuracy.

#### Common Misconceptions

**The Pythagorean theorem applies to all triangles.** It applies only to right triangles. For other triangles, you need different tools.

**The hypotenuse is always the longest side.** It is—by definition. The hypotenuse is opposite the right angle, and the right angle is the largest angle in a right triangle, so the side opposite it must be longest.

**You must always get a whole number for the hypotenuse.** Many right triangles have irrational hypotenuses. For example, a right triangle with legs of 1 and 1 has hypotenuse $\sqrt{1^2 + 1^2} = \sqrt{2} \approx 1.414$. Pythagoras himself proved that $\sqrt{2}$ cannot be written as a fraction, which shocked the ancient Greek world.

---

## Integration: The Building Site, Complete

Return to the surveyor with her transit and her three measurements. She has determined three distances using the machinery of geometry:

- From her starting point to a perpendicular reference line: 60 meters.
- From that reference point to the far corner (measured at a right angle): 80 meters.
- Using the Pythagorean theorem, the direct distance to the far corner: 100 meters.

But there is more. The client wants a fence around the perimeter of the property. The property is a rectangle with one side 100 meters (the distance across the pond) and an adjacent side that she measures to be 150 meters.

*Perimeter:* $P = 2(100) + 2(150) = 200 + 300 = 500$ meters of fencing needed.

*Area:* $A = 100 \times 150 = 15,000$ square meters.

The client also needs to know if the fence will meet code. Local code requires posts every 10 meters. $500 \div 10 = 50$ posts.

The surveyor writes the numbers in her report: 500 meters perimeter, 15,000 square meters area, 50 fence posts. The client nods, orders the fencing, and the work begins.

This is geometry doing the work it was invented to do. Not abstract. Not divorced from consequence. The three core ideas—how to measure directions and angles, how to compute perimeters and areas, how to use the Pythagorean theorem to find distances without walking them—are three separate tools. But they work together. The angles tell you the shape. The perimeter tells you the boundary cost. The area tells you the interior cost. The Pythagorean theorem lets you skip the walking and measure with mathematics instead.

---

## Exercises

### Warm-up

**Exercise 10.1** *(LO: angles and notation.)* In a right angle, two rays meet at a vertex. One ray points due north. The other ray points 37° east of north. What angle do the two rays form?

**Exercise 10.2** *(LO: perimeter of a rectangle.)* A rectangular garden measures 18 feet by 12 feet. How much fencing is needed to enclose it?

**Exercise 10.3** *(LO: area of a triangle.)* A triangular plot of land has a base of 24 meters and a height of 10 meters (perpendicular to the base). What is its area in square meters?

### Application

**Exercise 10.4** *(LO: Pythagorean theorem.)* A ladder leans against a wall. The base of the ladder is 6 feet from the wall. The ladder is 10 feet long. How high up the wall does the ladder reach?

**Exercise 10.5** *(LO: perimeter and area combined.)* You are tiling a square bathroom floor with tiles that measure 1 foot by 1 foot. The bathroom is 9 feet on each side. (a) How many tiles do you need? (b) If you run a decorative border tile along the entire perimeter, how many border tiles do you need?

**Exercise 10.6** *(LO: area application — real-world cost.)* A room measures 16 feet by 20 feet. You want to install carpeting that costs $3.50 per square foot. What is the total cost?

### Synthesis

**Exercise 10.7** *(LO: Pythagorean theorem + perimeter.)* A right triangle has legs measuring 5 cm and 12 cm. (a) Find the length of the hypotenuse using the Pythagorean theorem. (b) Find the perimeter of the triangle.

**Exercise 10.8** *(LO: similar triangles and proportions.)* Two similar right triangles have corresponding legs in the ratio 2:5. The smaller triangle has legs of 6 cm and 8 cm. Find the lengths of the legs of the larger triangle.

**Exercise 10.9** *(LO: complementary and supplementary angles.)* Two angles are supplementary (sum to 180°). One angle measures $4x + 10$ degrees, and the other measures $3x - 5$ degrees. Find the measure of each angle.

**Exercise 10.10** *(LO: circumference and area of a circle.)* A circular garden has a diameter of 14 meters. (a) Find the circumference. (b) Find the area. Use $\pi \approx 3.14$.

### Challenge

**Exercise 10.11** *(LO: Pythagorean triples and scaling.)* The Pythagorean triple $(3, 4, 5)$ is scaled by a factor of $k$ to produce $(3k, 4k, 5k)$. (a) Verify that $(3k)^2 + (4k)^2 = (5k)^2$ algebraically. (b) If $k = 7$, what is the new triple? (c) What is the perimeter of the right triangle with sides $3k$, $4k$, and $5k$? (d) What is the area?

**Exercise 10.12** *(LO: modeling a real situation.)* You live in a house with a rectangular roof. The roof measures 30 meters by 20 meters. During a heavy rainstorm, water flows off the roof. (a) What is the total area of the roof? (b) If 1 cubic meter of water falls as rain per square meter of roof, how much water (in cubic meters) falls on your roof? (c) If gutters can handle 0.5 cubic meters per hour, can the gutters handle a 1-hour rainstorm? Why or why not?

---

## Chapter Summary

You can now do five things with geometry that you likely could not an hour ago.

You can read a building blueprint and understand what the lines, angles, and measurements mean. You know that a right angle is 90°, that parallel lines never meet, and that perpendicular lines meet at exactly that angle.

You can calculate the perimeter of any polygon (the distance around the edge) and the area of any common shape (the square footage inside). This means you can figure out how much fencing, trim, carpeting, or paint you need for a real project.

You can apply the Pythagorean theorem to find unknown distances in right triangles without measuring them directly. This is the tool surveyors, carpenters, and navigators use when they cannot walk the path they need to measure.

You understand that similar shapes scale: if two triangles have the same angles, their sides are proportional, which means you can estimate heights and distances using proportions.

And you have seen how three separate ideas—angles and directions, measurements of boundaries and interiors, and the Pythagorean relationship—fit together into a coherent toolkit for making sense of space.

The thing to watch for, going forward, is *what you are actually measuring*. Perimeter is a linear measurement (units like feet or meters). Area is a square measurement (square feet or square meters). Volume (which appears in the next chapter) is a cubic measurement (cubic feet or cubic meters). Keep the units straight, and the rest is bookkeeping.

What you should now be able to teach a friend who asks: what is the Pythagorean theorem, why the 3-4-5 triangle is special, and why perimeter and area are completely different things.

---

## Connections Forward

Chapter 11 extends geometry into the third dimension: volume and surface area of prisms and cylinders. The Pythagorean theorem reappears there in calculating diagonal distances through three-dimensional space.

Probability (Chapter 7) uses area to visualize sample spaces. A circular dartboard region divided by lines creates geometric shapes whose areas represent the likelihood of different outcomes.

The similarity and scaling you learned here is the foundation for trigonometry, which uses the proportions of sides in special right triangles to find angles and unknown distances. You will encounter this in any physics or engineering course.

And here is a hidden connection: the algebraic idea of solving for an unknown ($x$) is exactly what you do with the Pythagorean theorem when you know two sides and solve for the third. Geometry and algebra are not separate languages; they are two ways of saying the same thing.

---

## Tags

#geometry #pythagorean-theorem #perimeter-area #angles #polygons #surveying #measurement #euclidean-geometry #right-triangles #similarity

