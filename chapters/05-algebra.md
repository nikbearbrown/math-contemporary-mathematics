# Chapter 5 — Algebra

## Suggested titles

- **Algebra: When You Don't Know the Number (Yet)**
- **How to Solve for X, and Why You'd Want To**
- **Variables, Functions, and the Machinery of Constraint**

---

## TL;DR

Algebra is the language you speak when you need to find a number you don't yet know, or track how one quantity changes when another one does. We'll build three ideas that unlock almost everything: how to isolate an unknown value by reversing operations (solving equations), how to name and visualize relationships between quantities (functions and graphs), and how to solve real problems that hinge on multiple constraints at once (systems of equations).

---

## Part 1: Cold Open

You walk into a coffee shop and order a pastry. The barista rings it up: $3.85. You hand over a $10 bill. Before they hand back your change, your brain has already done the arithmetic: $10 − $3.85 = $6.15. You didn't think about it. You just flipped the operation—subtraction to find the missing part.

But now imagine a different scenario. A small business uses wool to make scarves and sweaters. A scarf needs three bags of wool and sells for $8 profit. A sweater needs four bags of wool and sells for $10 profit. The business has exactly 27 bags of wool to spend this week, and they can make at most 8 items. They want to maximize profit. How many scarves and how many sweaters should they make?

You can't just do this in your head. You need to set up the problem, write down the constraints, and find the answer systematically. This is where algebra becomes more than arithmetic—it becomes a tool for reasoning through complexity.

In this chapter, we're going to build three interlocking skills. First: solving for unknown values when you have an equation (finding the missing number). Second: naming relationships between quantities and visualizing them on a graph (functions). Third: handling situations where multiple equations and constraints must all be satisfied at once (systems).

The payoff is this: you'll be able to take a word problem—any word problem—translate it into mathematical language, and then solve it mechanically. You won't have to guess or test values. You'll have a method.

### Learning objectives

By the end of this chapter you will be able to:

- **Solve** a linear equation in one variable using properties of equality, and **construct** an equation from a word problem.
- **Distinguish** between an equation and a function; **evaluate** a function using function notation.
- **Graph** a linear function using points, intercepts, or slope; **interpret** a graph to answer real-world questions.
- **Solve** a system of two linear equations in two variables using substitution or elimination.
- **Model** a real-world constraint problem using a system of equations and **verify** your solution.

### Prerequisites

You should be comfortable with arithmetic: adding, subtracting, multiplying, dividing whole numbers, fractions, and decimals. You should understand that when you do the same thing to both sides of an equation, the equation stays balanced. You should be able to read and use a simple coordinate plane (Chapter 4 touched on this).

### Why this chapter matters

Algebra is the language in which the rest of mathematics speaks. Logic (Chapter 2) uses algebraic reasoning. Money management (Chapter 6) relies on equations to calculate interest and loan payments. Probability and statistics (Chapters 7–8) use functions to describe distributions and predict outcomes. Geometry (Chapter 10) uses equations to describe lines, circles, and shapes. Every field that uses mathematics—engineering, medicine, agriculture, economics, social science—starts with the ability to set up and solve equations. And every equation, at root, is a puzzle: *find the number that makes this statement true*.

---

## Concept 1: Solving Linear Equations — Finding the Unknown Value

A **linear equation in one variable** is a statement that two expressions are equal, and your job is to find the number that makes it true. That number is called the **solution**.

Here's the cold open for this section: You're buying a used car. The dealer offers you a deal: $5 per hour above minimum wage. You work 40 hours a week. If your weekly paycheck is $360, what is the hourly rate? Let $x$ be the hourly rate. You earn $5x$ from 40 hours of work. So:

$$40x = 360$$

To find $x$, you need to *undo* the multiplication by 40. You divide both sides by 40:

$$\frac{40x}{40} = \frac{360}{40}$$

$$x = 9$$

Your hourly rate is $9 per hour. You just solved a linear equation.

### The properties of equations

When you solve an equation, you use one fundamental principle: **what you do to one side, you must do to the other**. This keeps the equation balanced.

The four operations work like this:

**Addition Property:** If $a = b$, then $a + c = b + c$. 

**Subtraction Property:** If $a = b$, then $a − c = b − c$.

**Multiplication Property:** If $a = b$, then $ac = bc$.

**Division Property:** If $a = b$ and $c \neq 0$, then $\frac{a}{c} = \frac{b}{c}$.

### A worked example: Solving a multi-step equation

Solve: $3x + 5 = 20$.

*Step 1: Subtract 5 from both sides to isolate the $x$ term:*

$$3x + 5 - 5 = 20 - 5$$
$$3x = 15$$

*Step 2: Divide both sides by 3:*

$$\frac{3x}{3} = \frac{15}{3}$$
$$x = 5$$

*Step 3: Check. Substitute $x = 5$ back into the original:*

$$3(5) + 5 = 15 + 5 = 20$$ ✓

The solution is $x = 5$.

### Another worked example: Equations with variables on both sides

Solve: $5y - 3 = 2y + 9$.

This equation has $y$ on both sides. Don't panic. You still follow the same principle: get all variable terms on one side, all constants on the other.

*Step 1: Subtract $2y$ from both sides (to collect variables on the left):*

$$5y - 2y - 3 = 2y - 2y + 9$$
$$3y - 3 = 9$$

*Step 2: Add 3 to both sides (to isolate the variable term):*

$$3y - 3 + 3 = 9 + 3$$
$$3y = 12$$

*Step 3: Divide both sides by 3:*

$$y = 4$$

*Step 4: Check. Substitute $y = 4$ into both sides of the original:*

Left side: $5(4) - 3 = 20 - 3 = 17$

Right side: $2(4) + 9 = 8 + 9 = 17$

Both sides equal 17. ✓

The solution is $y = 4$.

### Trade-off: Exactness vs. trial-and-error

When you have an equation like $3x + 5 = 20$, you could solve it by guessing. Try $x = 6$: $3(6) + 5 = 23$. Too big. Try $x = 4$: $3(4) + 5 = 17$. Too small. Eventually you'd land on $x = 5$. 

But this only works for small integers. If the answer is $x = 7.3$ or $x = -\frac{2}{5}$, guessing becomes impractical. The algebraic method—applying properties of equations step by step—gives you an exact answer every time, in any case, without trying values. That's the trade-off: equations demand more careful thinking up front, but they reward you with certainty and speed.

### Common misconceptions

**You must do the same operation to both sides, completely.** If you have $\frac{x+2}{3} = 5$, you multiply both sides by 3 to get $x + 2 = 15$, not $x + 2 = 5 \cdot 3$. The 3 multiplies the entire left side and the entire right side.

**Negative numbers don't break the rules.** When you subtract a negative, it becomes addition: $5 − (−3) = 5 + 3 = 8$. This is not a special case; it's the same principle applied.

**An equation with no solution and an equation with infinitely many solutions are both valid answers.** For $x + 3 = x + 5$, no value of $x$ works (the variable cancels, leaving $3 = 5$, which is false). For $2(x + 1) = 2x + 2$, every value of $x$ works (both sides are identical). Both are legitimate outcomes.

### Applications: Translating words to equations

The hardest part is usually not solving the equation—it's writing it down from a word problem.

**Example:** Your gym membership costs $10 per month, plus $5 per class you attend. Your budget is $75 per month. How many classes can you take?

*Translation:*
- Let $c$ = number of classes
- Monthly cost = $10 + 5c$
- Budget = $75$
- Equation: $10 + 5c = 75$

*Solution:*
$$5c = 75 - 10 = 65$$
$$c = 13$$

You can take 13 classes on a $75 budget.

---

## Concept 2: Functions — Naming and Visualizing Relationships

A **function** is a relationship where each input has exactly one output. Think of it as a machine: you put a number in, the machine does something to it, and exactly one number comes out.

Cold open: A pizza restaurant charges $12 for a large pizza plus $1.50 per topping. If you order with $t$ toppings, the cost is $12 + 1.5t$. 

- 0 toppings: $12 + 1.5(0) = 12$
- 1 topping: $12 + 1.5(1) = 13.50$
- 2 toppings: $12 + 1.5(2) = 15$
- 3 toppings: $12 + 1.5(3) = 16.50$

Each number of toppings gives exactly one price. This is a function.

### Function notation

Instead of writing $y = 12 + 1.5t$, we can write:

$$f(t) = 12 + 1.5t$$

Read "$f$ of $t$" or "the value of $f$ at $t$." The parentheses do not mean multiplication. They mean "input this value."

If you want to know the cost of a pizza with 4 toppings:

$$f(4) = 12 + 1.5(4) = 12 + 6 = 18$$

So $f(4) = 18$: a 4-topping pizza costs $18.

### Domain and range

The **domain** (from Latin *dominium*, "territory") is the set of all possible inputs—all the values you're allowed to put in. For a pizza with toppings, the domain might be 0, 1, 2, 3, 4, 5 (whole numbers, since you can't order half a topping). 

The **range** is the set of all possible outputs—all the values that come out. For our pizza function with domain 0 through 5:

$$\text{Range: } \{12, 13.50, 15, 16.50, 18, 19.50\}$$

The domain and range depend on the real-world context. If you're graphing the function $y = x^2$ in pure math, the domain is all real numbers. If you're modeling height as a function of age for a human, the domain is ages 0 to about 100, and the range is heights 0 to about 8 feet.

### Another worked example: Evaluating and interpreting a function

A phone company charges \$50 per month (base fee) plus \$0.10 per text message. Write a function for monthly cost, and find the cost if you send 300 texts.

Let $t$ = number of texts, and $C(t)$ = monthly cost.

$$C(t) = 50 + 0.10t$$

To find the cost for 300 texts:

$$C(300) = 50 + 0.10(300) = 50 + 30 = 80$$

If you send 300 texts, your monthly bill is \$80.

Notice: the domain here is $t \geq 0$ (you can't send a negative number of texts). The range is $C \geq 50$ (the minimum cost is \$50, even if you send no texts). These constraints come from the real-world context, not from the algebra itself.

### Graphing a function: Points and intercepts

To graph a function, you plot points and connect them. For $f(x) = 2x + 3$:

- When $x = 0$: $f(0) = 2(0) + 3 = 3$. Plot $(0, 3)$.
- When $x = 1$: $f(1) = 2(1) + 3 = 5$. Plot $(1, 5)$.
- When $x = 2$: $f(2) = 2(2) + 3 = 7$. Plot $(2, 7)$.
- When $x = -1$: $f(-1) = 2(-1) + 3 = 1$. Plot $(-1, 1)$.

Connect these points, and you see a straight line. That's why it's called a *linear* function.

Two special points make graphing easier:

- **x-intercept:** Where the line crosses the $x$-axis (where $y = 0$). Set $f(x) = 0$ and solve: $2x + 3 = 0 \Rightarrow x = -\frac{3}{2}$. Point: $(-\frac{3}{2}, 0)$.
- **y-intercept:** Where the line crosses the $y$-axis (where $x = 0$). This is just $f(0) = 3$. Point: $(0, 3)$.

With just these two points, you can draw the entire line.

### Slope: The rate of change

The **slope** of a line measures how steep it is. If you pick two points on the line, slope is:

$$m = \frac{\text{rise}}{\text{run}} = \frac{\Delta y}{\Delta x} = \frac{y_2 - y_1}{x_2 - x_1}$$

For the line $y = 2x + 3$, using points $(0, 3)$ and $(1, 5)$:

$$m = \frac{5 - 3}{1 - 0} = \frac{2}{1} = 2$$

Slope 2 means: for every 1 unit you move right, you move 2 units up. The slope is also the coefficient of $x$ in the equation.

**Slope in context:** If a car travels at 60 miles per hour, the function $d(t) = 60t$ has slope 60. The slope is the rate of change—miles per hour. A negative slope means the line goes downward as you move right. For example, if you have \$100 in your account and you spend \$5 per day, the function is $M(d) = 100 - 5d$ (money remaining after $d$ days). Slope is $-5$: you lose \$5 per day.

### Another worked example: Finding slope from two points

Find the slope of the line passing through $(2, 3)$ and $(5, 9)$.

$$m = \frac{9 - 3}{5 - 2} = \frac{6}{3} = 2$$

The slope is 2. This means: for every 1 unit you move right, you move 2 units up. Or equivalently, for every 3 units right, you move 6 units up.

**Note on order:** The order of the points doesn't matter. If you compute it as $\frac{3 - 9}{2 - 5} = \frac{-6}{-3} = 2$, you get the same answer. The key is to be consistent: if you subtract $y$-values in the numerator, subtract the corresponding $x$-values in the denominator.

### Trade-off: Slope-intercept form vs. point-slope form

A linear function can be written as:

**Slope-intercept form:** $y = mx + b$, where $m$ is slope and $b$ is the y-intercept. Easy to graph; shows the y-intercept at a glance.

**Point-slope form:** $y - y_1 = m(x - x_1)$, where $(x_1, y_1)$ is a point on the line. Useful when you know a point and the slope but not the y-intercept.

Both are correct; use whichever is more convenient for the problem.

### Common misconceptions

**The slope is not "rise divided by run" in units; it's a ratio.** If you move 3 units right and 6 units up, the slope is $\frac{6}{3} = 2$, not "6 units." Slope is unitless (or carries the units of the vertical axis divided by the horizontal axis).

**A horizontal line has slope 0; a vertical line has undefined slope.** Horizontal ($y = 5$) has $\Delta y = 0$, so slope is 0. Vertical ($x = 3$) has $\Delta x = 0$, so slope is $\frac{\Delta y}{0}$, which is undefined. These are not the same.

**Function notation is not multiplication.** $f(3)$ does not mean $f \times 3$. It means "the output of $f$ when the input is 3."

---

## Concept 3: Systems of Equations — Multiple Constraints

A **system of equations** is a set of two or more equations that you solve together. The solution is the values that make all equations true at once.

Cold open: You go to a restaurant with a friend. You order 2 tacos and 1 burrito; it costs $8.50. Your friend orders 1 taco and 2 burritos; it costs $9. How much does a taco cost? How much does a burrito cost?

Let $t$ = cost of a taco, $b$ = cost of a burrito.

$$\begin{cases}
2t + b = 8.50 \\
t + 2b = 9
\end{cases}$$

This is a system of two equations in two unknowns. You have two constraints: both your meal and your friend's meal have to cost the right amount.

### Solving by substitution

**Step 1: Solve one equation for one variable.**

From the second equation:
$$t + 2b = 9 \Rightarrow t = 9 - 2b$$

**Step 2: Substitute into the other equation.**

$$2(9 - 2b) + b = 8.50$$
$$18 - 4b + b = 8.50$$
$$18 - 3b = 8.50$$
$$-3b = -9.50$$
$$b = \frac{9.50}{3} \approx 3.17$$

A burrito costs about $3.17.

**Step 3: Find the other variable.**

$$t = 9 - 2(3.17) = 9 - 6.34 = 2.66$$

A taco costs about $2.66.

**Step 4: Check both equations.**

- Equation 1: $2(2.66) + 3.17 = 5.32 + 3.17 = 8.49 ≈ 8.50$ ✓
- Equation 2: $2.66 + 2(3.17) = 2.66 + 6.34 = 9$ ✓

The solution is approximately $(t, b) = (2.66, 3.17)$.

### Solving by elimination

Sometimes substitution is messy. **Elimination** is an alternative: multiply equations to make one variable cancel, then add or subtract.

Using the same system:

$$\begin{cases}
2t + b = 8.50 \\
t + 2b = 9
\end{cases}$$

**Step 1: Multiply the second equation by $-2$:**

$$-2(t + 2b) = -2(9)$$
$$-2t - 4b = -18$$

**Step 2: Add this to the first equation:**

$$\begin{align}
2t + b &= 8.50 \\
-2t - 4b &= -18 \\
\hline
-3b &= -9.50
\end{align}$$

**Step 3: Solve for $b$:**

$$b = \frac{9.50}{3} \approx 3.17$$

**Step 4: Substitute back to find $t$:**

$$2t + 3.17 = 8.50 \Rightarrow 2t = 5.33 \Rightarrow t = 2.66$$

Same answer, different path.

### Graphing a system

Each equation in a system is a line. The solution is the point where the lines intersect.

For our restaurant example:
- Line 1: $2t + b = 8.50 \Rightarrow b = 8.50 - 2t$ (y-intercept 8.50, slope -2)
- Line 2: $t + 2b = 9 \Rightarrow b = 4.50 - 0.5t$ (y-intercept 4.50, slope -0.5)

Plot both lines. They intersect at approximately $(2.66, 3.17)$. That's the solution.

The graphical method is useful for understanding what's happening: you're looking for the point where both constraints are satisfied simultaneously. But graphing by hand is imprecise. Unless the intersection is at integer coordinates (like $(2, 3)$), it's hard to read the exact values from a graph. This is why we use algebra: to find the precise answer.

### Verification: Why checking matters

Once you find a solution, always substitute it back into both original equations. Errors in algebra are common—a small slip can invalidate the entire solution. But if both equations check out, you know you have the right answer.

For our restaurant example with $t = 2.66$ and $b = 3.17$:
- Equation 1: $2(2.66) + 3.17 = 5.32 + 3.17 = 8.49 \approx 8.50$ ✓
- Equation 2: $2.66 + 2(3.17) = 2.66 + 6.34 = 9.00$ ✓

(The first equation is close but not exact because we rounded $2.66$ and $3.17$; if we use the exact values, both equations check perfectly.)

### Trade-off: Substitution vs. elimination vs. graphing

**Substitution** is good when one equation is already solved for a variable, or when solving for it is easy.

**Elimination** is good when coefficients line up nicely to cancel.

**Graphing** shows you visually where the solution is, but it's hard to read exact values unless the intersection is at integer coordinates.

In practice, you often use substitution or elimination. Graphing helps you see whether the system makes sense and whether your answer is reasonable.

### Special cases: No solution and infinitely many

**No solution:** Two parallel lines never intersect. For example:

$$\begin{cases}
y = 2x + 3 \\
y = 2x + 5
\end{cases}$$

Both lines have slope 2 but different y-intercepts (3 vs. 5). They never meet. The system has no solution.

**Infinitely many solutions:** Two equations represent the same line. For example:

$$\begin{cases}
2x + y = 5 \\
4x + 2y = 10
\end{cases}$$

The second equation is just the first multiplied by 2. They're the same line. Every point on the line is a solution.

### Common misconceptions

**You need two equations to solve two unknowns.** One equation in two unknowns has infinitely many solutions (it's a line). Two equations can narrow it to one point, or one line, or no solution.

**A solution to a system must satisfy all equations.** If a point works in one equation but not the other, it's not a solution to the system.

**Graphing is not guessing.** You can graph a system roughly to check your algebraic answer, but the algebra is what gives you the exact solution.

---

## Integration: The Restaurant Receipt

Return to the pizza and topping scenario. Now imagine a more realistic situation: a pizza shop offers two specialty pies.

- **Margherita:** \$12 base + \$1 per topping
- **Supreme:** \$16 base + \$0.50 per topping

You want a Margherita and a Supreme, with the same number of toppings on each. You spend $40 total. How many toppings does each pizza have?

Let $n$ = number of toppings on each.

$$12 + 1n + 16 + 0.5n = 40$$
$$28 + 1.5n = 40$$
$$1.5n = 12$$
$$n = 8$$

Each pizza has 8 toppings. Check: $(12 + 8) + (16 + 4) = 20 + 20 = 40$ ✓.

This is a single equation, but notice the structure: you translated a word problem into an equation, solved for the unknown, and verified the answer. This is the core of algebra.

### A more complex scenario: Different topping counts

Now add a complication: what if you want the Margherita to have 2 more toppings than the Supreme?

Let $m$ = toppings on Margherita, $s$ = toppings on Supreme.

$$\begin{cases}
12 + m + 16 + 0.5s = 40 \\
m = s + 2
\end{cases}$$

Substitute the second into the first:

$$12 + (s + 2) + 16 + 0.5s = 40$$
$$30 + s + 0.5s = 40$$
$$30 + 1.5s = 40$$
$$1.5s = 10$$
$$s = \frac{10}{1.5} = 6.67$$

The Supreme has about 6.67 toppings. The Margherita has about 8.67 toppings. Since you can't order a fractional topping, you'd round: perhaps 7 toppings on the Supreme and 9 on the Margherita. Let's check:

Cost = $(12 + 9) + (16 + 7 \times 0.5) = 21 + 19.5 = 40.50$.

That's \$0.50 over budget. Try 6 and 8 instead: $(12 + 8) + (16 + 6 \times 0.5) = 20 + 19 = 39$. That's \$1 under budget. In real life, you'd pick whichever is closest or ask the shop if they can adjust.

**The point:** as problems get more complex, you move from single equations (one unknown) to systems (multiple unknowns). Algebra gives you the toolkit to handle them. And real-world answers often require judgment—the math gets you close, but context matters for the final decision.

### Graphing the system

We could also solve this graphically. Write both equations in the form $s = ...$:

From Equation 1: $12 + m + 16 + 0.5s = 40 \Rightarrow m + 0.5s = 12 \Rightarrow s = 24 - 2m$

From Equation 2: $s = m - 2$

Plot both lines:
- Line 1: $s = 24 - 2m$ has y-intercept 24 and slope -2 (as $m$ increases by 1, $s$ decreases by 2).
- Line 2: $s = m - 2$ has y-intercept -2 and slope 1 (as $m$ increases by 1, $s$ increases by 1).

The intersection occurs at approximately $(m, s) = (8.67, 6.67)$. This confirms our algebraic answer. The graphical method shows visually that the two constraints narrow down the solution to a single point (or region, if we had inequalities instead of equalities).

---

## Exercises

### Warm-up

**5.1** Solve: $5x - 7 = 18$. Check your answer.

**5.2** Solve: $2y + 3 = y + 8$ (note: $y$ appears on both sides).

**5.3** Write an equation for this situation, then solve: "You earn \$15 per hour. After working, you have \$180. How many hours did you work?"

**5.4** For the function $f(x) = 3x - 2$, find (a) $f(0)$, (b) $f(4)$, and (c) $f(-1)$.

**5.5** Graph the line $y = -2x + 5$ by plotting at least three points. Identify the y-intercept and the slope.

### Application

**5.6** A car rental costs \$50 per day plus \$0.25 per mile. You rent for 3 days and drive 150 miles. What is your total cost?

**5.7** Find the slope of the line passing through $(1, 2)$ and $(4, 8)$. Interpret what the slope tells you in real-world terms if these coordinates represent (hours, distance in miles).

**5.8** A gym charges a flat monthly fee of \$30 plus \$2 per class. Write a function $C(c)$ for the monthly cost as a function of number of classes attended. If you attend 12 classes in a month, what is your cost?

**5.9** Solve the system using substitution: 
$$\begin{cases}
x + 2y = 7 \\
2x - y = 4
\end{cases}$$

**5.10** You have \$20. Apples cost \$2 each and oranges cost \$3 each. Write an equation showing the combinations of apples and oranges you can buy with exactly \$20. Find one solution (a specific number of apples and oranges) that works.

### Synthesis

**5.11** A gym charges a \$50 membership fee plus \$5 per class. A yoga studio charges \$10 per class with no membership fee. 

(a) Write a function $G(c)$ for the gym's total cost after $c$ classes, and a function $Y(c)$ for the yoga studio's total cost after $c$ classes.

(b) After how many classes does the gym become the cheaper option? (Hint: set $G(c) = Y(c)$ and solve.)

**5.12** Graph both $f(x) = 2x + 1$ and $g(x) = -x + 4$ on the same coordinate plane. Find their intersection point algebraically (by solving the system), then verify it on your graph.

**5.13** A bakery sells cupcakes for \$3 each and cookies for \$2 each. They want to sell 25 items total and make exactly \$60 in revenue. Set up a system of equations and solve for the number of cupcakes and cookies they must sell.

### Challenge

**5.14** Three friends split a restaurant bill. Alex ate twice as much as Chris. Blake ate \$2 more than Chris. The total bill is \$50. 

(a) Set up a system of equations (let $c$ = Chris's share, $a$ = Alex's share, $b$ = Blake's share).

(b) Solve for each person's share.

(c) Check that the three shares add up to \$50.

**5.15** A line passes through the points $(2, 5)$ and $(4, 11)$.

(a) Find the slope.

(b) Use the slope-intercept form $y = mx + b$ to find $b$ (the y-intercept).

(c) Write the equation of the line.

**5.16** You need to deliver packages to a town 120 miles away. You drive at 60 mph for the first part of the journey, then the weather worsens and you drive at 40 mph for the rest. The entire trip takes 2.5 hours. How many miles did you drive at each speed?

(Hint: Let $t_1$ = time at 60 mph and $t_2$ = time at 40 mph. Set up: $t_1 + t_2 = 2.5$ and $60t_1 + 40t_2 = 120$.)

---

## Chapter Summary

You can now do five things you probably could not do an hour ago.

You can **translate a word problem into an equation** and **solve it using properties of equality**—adding, subtracting, multiplying, or dividing both sides—to find the value of an unknown. This is the core skill of algebra.

You can **name a relationship between two quantities using function notation** and **evaluate it** to find outputs for given inputs. You understand that a function is a machine: one input, one output.

You can **graph a linear function** using points, intercepts, or slope, and read the graph to answer questions like "when does the function equal zero?" or "what is the rate of change?"

You can **set up and solve a system of two linear equations** using substitution or elimination, finding the point (or points) where both equations are true at once. This is how you handle problems with multiple constraints.

And you understand the **trade-offs** in each method: equations are exact but require symbol-manipulation; graphs are visual but hard to read precisely; systems with no solution or infinitely many solutions are valid outcomes, not errors.

The thing to watch for, going forward, is **clarity of translation**. Most algebra mistakes don't happen in the solving; they happen when you write down the equation. Read the problem twice. Identify what you're solving for. Label your variable. Translate carefully from words to symbols. Once the equation is right, the algebra is just mechanical.

What you should now be able to teach a friend who asks: how to solve $2x + 3 = 11$ without guessing, why a function is different from an equation, how to graph a line using slope and a point, and what it means for a system to have no solution.

---

## Connections Forward

**Chapter 6: Money Management** builds entirely on your ability to set up and solve equations. Loan payments, compound interest, retirement savings—all are equations. You'll use the same algebraic thinking here.

**Chapter 7: Probability** asks "what's the expected value?" The answer is a weighted average: an equation. You'll set up probabilities (functions of outcomes) and solve for unknowns.

**Chapter 8: Statistics** uses linear regression, which is a system of equations that fits a line to data. You're doing the same algebra, but now with purpose: understanding real data.

**Chapter 10: Geometry** describes lines, circles, and shapes with equations. A line is described by $y = mx + b$; a circle is described by $(x - h)^2 + (y - k)^2 = r^2$. You'll recognize these forms and use them to reason about space.

**Chapter 11: Voting and Apportionment** and **Chapter 12: Graph Theory** both use constraints and optimization (linear programming, from the deferred material in this chapter). The algebra of systems is how you model fair voting methods and efficient networks.

You've now learned the **alphabet** of mathematics. Everything that follows is **spelling with it**.

---

## What would change my mind

If a student showed me that linear equations, functions, and systems of equations are not actually sufficient to model the constraint problems that citizens and professionals face—that more exotic machinery is needed at the outset—I would revise the scope. But every example I know (pricing, scheduling, medical dosing, elections, infrastructure) starts here. I'm confident in the choice.

## Still puzzling

I'm still not entirely satisfied with the integration section. It works, but it could be richer. A three-variable system (three pizzas, three constraints) might be more compelling, but it also exceeds the scope of this chapter. I've left this as a note for the next draft.

---

## Tags

`algebra` `equations` `functions` `systems` `variables` `constraint-modeling` `Descartes` `real-world-application`
