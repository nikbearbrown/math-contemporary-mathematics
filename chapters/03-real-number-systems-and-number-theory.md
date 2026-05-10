# Chapter 3 — Real Numbers and Number Theory

## Suggested titles

- **Prime Numbers and the Structure of Integers**
- **Building the Numbers: From Natural to Rational**
- **What Numbers Are Made Of**

---

## TL;DR

Every integer above 1 is either prime or builds uniquely from primes. Extending numbers to negatives and fractions preserves the rules of arithmetic—nothing breaks. The machinery of number theory powers encryption, scheduling, and every fraction you handle.

---

## Cold Open

A cryptographer in 2021 sits down to design a new security system for a banking app. She needs a number so large—so incomprehensibly large—that even the fastest computers on Earth would take 300 trillion years to break it down into its prime factors. She reaches for two primes with hundreds of digits each, multiplies them together, and that product becomes the lock. No one on the planet can reverse the process in reasonable time. Yet the two primes *must exist*, and they must be unique. She doesn't build this system from abstract theory. She builds it on a fact about numbers that a student in ancient Greece figured out: every integer is either prime or builds from primes in exactly one way.

That fact is not a curiosity. It is load-bearing.

This chapter teaches you to see inside numbers—how they factor, how they combine, how they fail to combine. It shows you why negative numbers don't break the rules. It shows you fractions the way a baker or a chemist sees them: as precise ratios between quantities. And it prepares you for the rest of this book, which runs on these gears.

### Learning objectives

By the end of this chapter you will be able to:

- **Identify** prime and composite numbers and apply divisibility tests to classify them.
- **Find** the prime factorization of any composite number and recognize that factorization is unique.
- **Calculate** the greatest common divisor (GCD) and least common multiple (LCM) and apply them to real scheduling and packing problems.
- **Interpret** negative numbers as directions on a number line and perform arithmetic with integers.
- **Distinguish** rational numbers (fractions) from other real numbers and simplify them to lowest terms.
- **Perform** addition, subtraction, multiplication, and division with fractions, with and without a calculator.
- **Solve** real-world problems involving unit conversion, percentages, and proportional reasoning.

### Prerequisites

You know how to divide. You know that 24 ÷ 3 = 8 and that when you have a remainder, division doesn't come out even. You're comfortable with the idea of zero and comfortable enough with negative numbers to know that a bank account can be overdrawn. You've handled fractions in cooking or splitting a bill.

### Why this chapter matters

Number theory isn't abstract algebra floating in textbooks. Prime factorization secures every encrypted transaction. GCD and LCM solve real problems: how to cut fabric without waste, how to schedule teams fairly when people work different numbers of hours. Rational numbers (fractions) are how you compare rates (miles per gallon, cups per person), convert units, understand percentages, and read nutrition labels. This chapter is where you learn to see the structure inside the numbers you use every day.

---

## Concept 1: Prime Numbers, Factorization, and the Structure of Integers

You open a file on your computer and it encrypts instantly—a process that relies on factorization. You look at a nutrition label and see "serving size 2/3 cup"—a fraction from divisibility. You organize a shift schedule so three people work every 6 days and they overlap fairly—an application of multiples. Each one rests on the same machinery: what numbers divide evenly into other numbers, and what prime pieces those numbers break into.

A **natural number** (or counting number) is any of {1, 2, 3, 4, 5, ...}. The **integers** extend that to include zero and negatives: {..., −3, −2, −1, 0, 1, 2, 3, ...}. The Greeks called them *mathemata*—things that could be counted or measured. We call them the natural numbers, from Latin *naturalis*, meaning "by nature." For this section we focus on natural numbers and their structure.

Divisibility is the core idea. A natural number $n$ is **divisible** by a number $m$ if we can express $n$ as $m$ times another natural number with no remainder. Written algebraically: $n$ is divisible by $m$ if $n = m \times k$ for some integer $k$. We also say "$m$ divides $n$" or "$m$ is a divisor of $n$."

Example: 36 is divisible by 4 because $36 = 4 \times 9$. No remainder. The number 37 is not divisible by 4 because $37 = 4 \times 9 + 1$. There is a remainder.

Rather than test divisibility by long division every time, mathematicians use **divisibility rules** — quick tests for common divisors.

| Divisor | Rule |
|---------|------|
| 2 | Last digit is even |
| 3 | Sum of all digits is divisible by 3 |
| 5 | Last digit is 0 or 5 |
| 10 | Last digit is 0 |

Example: Is 318 divisible by 3? Sum the digits: $3 + 1 + 8 = 12$. Is 12 divisible by 3? Yes (it equals $3 \times 4$). So 318 is divisible by 3. We can verify: $318 = 3 \times 106$.

Now to the core structure.

A **prime number** is a natural number greater than 1 that has exactly two divisors: 1 and itself. The first primes are {2, 3, 5, 7, 11, 13, 17, 19, 23, 29, ...}.

A **composite number** is a natural number greater than 1 that has at least one divisor other than 1 and itself. The number 12 is composite because it is divisible by 2, 3, 4, and 6 in addition to 1 and 12.

The number 1 is special—neither prime nor composite. It has only one divisor (itself). We exclude it from both categories.

The **Fundamental Theorem of Arithmetic** states: every integer greater than 1 can be expressed as a product of primes in exactly one way, apart from the order in which the primes appear.

This is not obvious. It is profound. It means 18 can be factored as $2 \times 3 \times 3$ but no other combination of primes will produce 18. That uniqueness is what makes prime factorization a lock that cannot be unpicked.

To find the **prime factorization** of a composite number, we repeatedly divide by small primes until only 1 remains. 

Example: Factor 140.
- 140 is even, so divide by 2: $140 = 2 \times 70$
- 70 is even, so divide by 2 again: $70 = 2 \times 35$, so $140 = 2 \times 2 \times 35 = 2^2 \times 35$
- 35 ends in 5, so it's divisible by 5: $35 = 5 \times 7$
- 7 is prime. Stop.
- Prime factorization of 140: $2^2 \times 5 \times 7$

Check: $2 \times 2 \times 5 \times 7 = 4 \times 5 \times 7 = 20 \times 7 = 140$. ✓

A useful visual tool is the **factor tree**. Write the number at the top. Draw branches down to two factors. If either factor is composite, branch again. Stop when all leaves are prime.

```
        140
       /   \
      2     70
           /  \
          2    35
              /  \
             5    7
```

Reading the leaves: $140 = 2 \times 2 \times 5 \times 7$. Same answer, visual path.

### Trade-off: uniqueness vs. computational difficulty

The Fundamental Theorem guarantees uniqueness—a number has exactly one prime factorization. But here is the trade-off: while factoring small numbers is easy, factoring very large numbers is computationally hard. A 2048-bit number (about 617 digits in decimal) is impossible to factor on current hardware, even with weeks of computation. This asymmetry—uniqueness is guaranteed, but breaking the factorization is hard—is why it powers encryption.

### Worked example: Is 247 prime or composite?

We don't know yet. To determine this, we check if any prime up to $\sqrt{247}$ divides it.

$\sqrt{247} \approx 15.7$, so we check primes up to 15: {2, 3, 5, 7, 11, 13}.

- 247 is odd, so not divisible by 2.
- Sum of digits: $2 + 4 + 7 = 13$. 13 is not divisible by 3, so neither is 247.
- 247 doesn't end in 0 or 5, so not divisible by 5.
- Divide: $247 \div 7 = 35$ remainder 2. Not divisible.
- Divide: $247 \div 11 = 22$ remainder 5. Not divisible.
- Divide: $247 \div 13 = 19$ with no remainder. Divisible!

So $247 = 13 \times 19$. Both 13 and 19 are prime. Thus 247 is composite, and its factorization is $13 \times 19$.

### Common misconception: "Prime means odd"

False. 2 is the only even prime. All other primes are odd (because any other even number is divisible by 2). But odd does not mean prime—9, 15, 21 are odd and composite.

---

## Concept 2: Integers and Operations with Signed Numbers

The ancient mathematicians had a problem. They could add and multiply positive numbers. But what happens if you owe money? What if you measure a position relative to a reference point—above or below sea level, north or south of the equator? How do you do arithmetic with "anti-magnitude," with quantities that point in opposite directions?

The solution: extend the natural numbers to include zero and negative numbers. These form the **integers**: {..., −3, −2, −1, 0, 1, 2, 3, ...}.

An integer has two parts: a **magnitude** (size, absolute value) and a **direction** (positive, negative, or zero).

On a **number line**, zero sits in the middle. Positive integers point right. Negative integers point left. The **absolute value** of a number is its distance from zero, always non-negative. We write it with vertical bars: $|5| = 5$ and $|-5| = 5$.

Example: Your bank account starts at \$0. A deposit of \$50 moves it to +50. A withdrawal of \$30 moves it to +20. An overdraft of \$25 moves it to −25. Each transaction is addition or subtraction with direction. The absolute values are 50, 30, 25. The directions are clear: deposits are positive, withdrawals are negative.

Adding integers follows a visual rule. **Start at the first number. Move right if you're adding a positive number, left if you're adding a negative.**

$3 + 5 = 8$ (start at 3, move right 5 steps, land at 8)

$3 + (-5) = -2$ (start at 3, move left 5 steps, land at −2)

$(-3) + (-5) = -8$ (start at −3, move left 5 steps, land at −8)

Subtraction reverses direction: **$a - b$ means start at $a$ and move left $b$ steps.**

$7 - 3 = 4$ (start at 7, move left 3 steps, land at 4)

$3 - 7 = -4$ (start at 3, move left 7 steps, land at −4)

A useful rule: **Subtracting a negative is the same as adding a positive.** $7 - (-3) = 7 + 3 = 10$.

Multiplication has a sign rule. **Same signs give positive. Opposite signs give negative.**

- $(3) \times (4) = 12$ (both positive, result is positive)
- $(-3) \times (-4) = 12$ (both negative, result is positive)
- $(3) \times (-4) = -12$ (different signs, result is negative)

Division follows the same sign rule. $12 \div 3 = 4$ and $(-12) \div (-3) = 4$, but $(12) \div (-3) = -4$.

### Trade-off: generality vs. loss of intuition

By adding negative numbers, we lose the physical intuition that magnitude is always positive. But we gain the ability to solve any linear equation. Consider $3 + x = 2$. With only positive integers, this has no solution. With integers (including negatives), $x = -1$. Negative numbers are the price we pay for generality.

### Worked example: Net wealth

Emma has assets worth \$15,000 (savings and a car) and debts of \$8,000 (student loans and credit cards). What is her net wealth?

Net wealth = Assets − Debts = $15,000 − 8,000 = 7,000$.

Emma has a net wealth of +\$7,000.

Now suppose Marcus has assets of \$12,000 but debts of \$18,000. His net wealth is $12,000 − 18,000 = -6,000$. Negative net wealth means he owes more than he owns.

This is not an abstraction. Credit agencies compute this every day. Negative numbers model reality.

### Common misconception: "Minus times minus should give minus"

False. The sign rule is: **same signs → positive, different signs → negative.** $(-3) \times (-4) = +12$. Think of it as a reversal: negating a negative direction flips it back to positive. Or think of it algebraically: the number line itself reverses direction under multiplication by a negative, and reversing a reversal leaves you where you started.

---

## Concept 3: Rational Numbers and Arithmetic with Fractions

You walk into a bakery and the baker tells you she needs $\frac{2}{3}$ cup of sugar for one batch of cookies and $\frac{1}{4}$ cup of butter. But you're making three batches. How much sugar? How much butter? How do you combine these quantities?

A **rational number** is a number that can be expressed as a fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \neq 0$. The word "rational" comes from Latin *ratio*, meaning "relation" or "proportion" — a fraction expresses one quantity compared to another.

Every integer is rational. Write 5 as $\frac{5}{1}$. Write −3 as $\frac{-3}{1}$. But rational numbers extend beyond integers to all proper and improper fractions, terminating decimals (like 0.5 or 3.14), and repeating decimals (like 0.333... or 0.142857142857...).

The key property: **two fractions are equal if they represent the same portion.** $\frac{2}{4}$ and $\frac{1}{2}$ both represent "half." To reduce a fraction to lowest terms, we divide both numerator and denominator by their **greatest common divisor (GCD)**.

The GCD of two integers is the largest positive integer that divides both. Example: the divisors of 12 are {1, 2, 3, 4, 6, 12}. The divisors of 18 are {1, 2, 3, 6, 9, 18}. The common divisors are {1, 2, 3, 6}. The greatest is 6. So GCD(12, 18) = 6.

To reduce $\frac{12}{18}$: divide top and bottom by the GCD, 6. $\frac{12}{18} = \frac{12 \div 6}{18 \div 6} = \frac{2}{3}$. Now 2 and 3 share no common divisors except 1, so $\frac{2}{3}$ is in lowest terms.

Adding and subtracting fractions requires a **common denominator**—a number both denominators divide into. The **least common multiple (LCM)** is the smallest positive integer divisible by both.

Example: $\frac{1}{4} + \frac{1}{6}$. 

The LCM of 4 and 6 is 12 (since $4 = 2^2$, $6 = 2 \times 3$, and LCM = $2^2 \times 3 = 12$).

Convert each fraction:
- $\frac{1}{4} = \frac{1 \times 3}{4 \times 3} = \frac{3}{12}$
- $\frac{1}{6} = \frac{1 \times 2}{6 \times 2} = \frac{2}{12}$

Now add: $\frac{3}{12} + \frac{2}{12} = \frac{5}{12}$.

Multiplication is simpler—no common denominator needed. **Multiply numerators together and denominators together**: $\frac{a}{b} \times \frac{c}{d} = \frac{a \times c}{b \times d}$.

Example: $\frac{2}{3} \times \frac{3}{4} = \frac{6}{12} = \frac{1}{2}$.

Division uses the **reciprocal**: $\frac{a}{b} \div \frac{c}{d} = \frac{a}{b} \times \frac{d}{c} = \frac{ad}{bc}$.

Example: $\frac{2}{3} \div \frac{1}{4} = \frac{2}{3} \times \frac{4}{1} = \frac{8}{3}$.

**Percent** is a specific rational number: $n\%$ means $\frac{n}{100}$. To find 30% of 200, multiply: $\frac{30}{100} \times 200 = 0.30 \times 200 = 60$. Percentages let you compare proportions across different bases (e.g., "60% of voters approve" and "45% of voters approve" are directly comparable even if one group has 1,000 voters and the other has 2,500).

### Trade-off: exactness vs. termination

Rational numbers let us express any ratio exactly. But some ratios produce infinite decimals. $\frac{1}{3} = 0.333...$. We accept this because the pattern repeats. But this trade-off means we can't represent *all* real numbers as fractions—numbers like $\sqrt{2}$ (the side of a square with area 2) cannot be written as $\frac{p}{q}$ for any integers $p$ and $q$. These are **irrational numbers**, deferred to Chapter 3, part 2.

### Worked example: A recipe scales.

A cookie recipe calls for $\frac{2}{3}$ cup of sugar, $\frac{3}{4}$ cup of flour, and $\frac{1}{4}$ cup of butter. You want to make 1.5 times the recipe (you're feeding a crowd). How much sugar?

Sugar needed: $1.5 \times \frac{2}{3}$ cups.

Rewrite 1.5 as a fraction: $1.5 = \frac{3}{2}$.

Multiply: $\frac{3}{2} \times \frac{2}{3} = \frac{6}{6} = 1$ cup.

For flour: $\frac{3}{2} \times \frac{3}{4} = \frac{9}{8} = 1\frac{1}{8}$ cups.

For butter: $\frac{3}{2} \times \frac{1}{4} = \frac{3}{8}$ cup.

This is not abstract. A baker or a chemist does this daily.

### Common misconception: "Fractions are for division; decimals are for real quantities"

False. Both fractions and decimals are rational numbers. Fractions are *exact* representations (no rounding). Decimals are *approximate* or *terminating*. A baker measures by fraction (a pinch, a cup). A car's fuel economy is given as a decimal (27.3 miles per gallon), which is the rational number $\frac{273}{10}$ written in decimal form.

---

## Integration: From Prime Structure to Practical Ratio

Return to the cold open. The cryptographer multiplies two primes with hundreds of digits. The product is sent to the bank. Every transaction is encrypted with that product as the lock.

Now zoom out. That encryption secures the transfer of money, which is measured in fractions of a dollar (cents). The customer withdraws $100.50 from an account—that's $\frac{10050}{100}$ cents, or $\frac{201}{2}$ dollars. The bank's server computes interest, which compounds monthly: $\text{New Balance} = \text{Old Balance} \times (1 + \frac{r}{12})$, where $r$ is the annual rate. A rate of 3.6% is $\frac{3.6}{100} = \frac{36}{1000} = \frac{9}{250}$. Monthly rate is $\frac{9}{250 \times 12} = \frac{3}{1000}$.

The GCD of 9 and 250 is 1, so $\frac{9}{250}$ is already lowest terms. The LCM of 250 and 12 is 1500. These are not abstract. They determine what you owe and what the bank earns.

The integration: **prime factorization secures the system. Rational arithmetic operates it. Both rest on the integers—the negative, zero, and positive whole numbers. And all three rest on the same truth: numbers have structure, and we can use that structure to build, compute, and understand.**

---

## Exercises

### Warm-up

**3.1** *(LO: divisibility and prime identification.)* Determine whether each number is prime or composite. For composite numbers, give the prime factorization.

(a) 23
(b) 51
(c) 100

**3.2** *(LO: GCD and LCM.)* Find the GCD and LCM of each pair.

(a) 12 and 18
(b) 20 and 35

**3.3** *(LO: integer operations.)* Compute:

(a) $(-5) + 8$
(b) $3 - (-7)$
(c) $(-4) \times (-6)$
(d) $(-20) \div 4$

**3.4** *(LO: rational operations.)* Simplify each to lowest terms.

(a) $\frac{24}{36}$
(b) $\frac{5}{7} + \frac{2}{3}$
(c) $\frac{3}{4} \times \frac{8}{9}$

### Application

**3.5** *(LO: GCD and real-world packing.)* A camp director has 48 sleeping bags and 64 tent stakes. She wants to make identical kits, each with the same number of sleeping bags and the same number of stakes, with no items left over. What is the maximum number of kits she can make, and how many sleeping bags and stakes go in each?

**3.6** *(LO: LCM and scheduling.)* Bus A arrives every 12 minutes. Bus B arrives every 18 minutes. Both just arrived. When is the next time both buses will arrive at the same time?

**3.7** *(LO: fraction operations and unit conversion.)* You have 2.5 liters of juice and want to pour it into bottles that hold $\frac{2}{5}$ liter each. How many full bottles can you fill? Do you have juice left over? If so, how much?

**3.8** *(LO: percent and real data.)* A college has 8,000 students. A survey finds that 62.5% have part-time jobs. How many students have part-time jobs?

### Synthesis

**3.9** *(LO: GCD, LCM, and optimization.)* A gardener has 60 feet of fencing and wants to create a rectangular garden where the length is a whole number of feet and the width divides the length evenly. What are the possible dimensions?

**3.10** *(LO: rational operations and recipe scaling.)* A soup recipe serves 4 and calls for $\frac{3}{2}$ cups of broth, $\frac{1}{4}$ cup of cream, and $\frac{5}{8}$ cup of vegetables. How much of each ingredient do you need to serve 10 people?

**3.11** *(LO: integer operations and financial reasoning.)* A company has quarterly profits of +\$250,000, −\$50,000 (a loss), +\$180,000, and −\$30,000. What is the total profit for the year? What is the average quarterly profit?

### Challenge

**3.12** *(LO: factorization and cryptography.)* Two primes multiply to give 143. Find both primes. (Hint: one prime is less than 15.)

**3.13** *(LO: rational synthesis and problem-solving.)* You are catering an event for 75 people. The recipe serves 12 and calls for $\frac{2}{3}$ cup sugar, $\frac{1}{2}$ cup butter. You have 6 cups sugar and 3 cups butter on hand. Do you have enough of each ingredient? Show your work.

---

## Chapter summary

You can now do six things.

You can identify prime and composite numbers, and you can break any composite number into its unique prime factors. This is load-bearing. It is how encryption works. It is how you recognize when two fractions are truly the same and when they are not.

You can work with negative integers—add them, subtract them, multiply them, divide them—following the sign rules. You understand that negative doesn't mean invalid. It means direction.

You can reduce fractions to lowest terms, add and subtract fractions using common denominators, and multiply and divide fractions without a common denominator. You see fractions as ratios—as precise ways to express parts of a whole, not as approximations.

You can find the GCD of two integers and use it to reduce fractions or to solve packing and sharing problems. You can find the LCM and use it to align repeating events or to add fractions with different denominators.

You can work with percents as rational numbers (fractions out of 100) and solve real problems: what percentage of the class scored above 85? If 40% of attendees are newcomers and there are 250 attendees, how many are newcomers?

And you understand, in your bones now, that numbers have structure. They factor. They combine. They follow rules. Those rules don't change when you extend them—from naturals to integers to rationals. That consistency is what allows you to build further, to trust the machinery, and to see into systems that depend on these gears.

The thing to remember: **every composite number is prime pieces, and those pieces are unique.** That uniqueness is what makes much of mathematics and much of modern security possible.

---

## Connections forward

Chapter 4 treats numbers not as abstract quantities but as *represented* in different ways—in base 10 (which you already know), in other bases (like base 2 for computers), and in the systems ancient cultures used. When you understand that the *same number* can be written in different bases, you see that base-10 itself is a choice, not a law.

Chapter 5, Algebra, takes the rules of arithmetic you've just learned and abstracts them further, replacing specific numbers with variables. But the rules of GCD, LCM, fraction operations, and sign arithmetic all remain. Algebra is just arithmetic with placeholders.

Chapter 6, Money Management, applies fractions and percents directly—interest, loans, tax, investment. Everything in this chapter is in motion there.

---

## What would change my mind

If a student found a composite number whose prime factorization was not unique, the Fundamental Theorem of Arithmetic would be wrong, and much of number theory would need rebuilding. This has not happened in recorded mathematics, and rigorous proofs show it cannot.

---

## Still puzzling

The distribution of primes—why they become rarer as numbers grow larger, and whether there is an exact formula that predicts where the next prime will appear—remains one of mathematics' deepest open questions. The Riemann Hypothesis, which addresses this, has been open since 1859 and carries a $1 million prize for its solution.

---

## Tags

prime-factorization, encryption, greatest-common-divisor, least-common-multiple, integers, negative-numbers, rational-numbers, fractions, percent, number-theory, fundamental-theorem-of-arithmetic

