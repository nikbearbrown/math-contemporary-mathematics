# Chapter 4 — Number Representation and Calculation

## Possible titles

1. How Numbers Get Written Down — What Changes and What Stays the Same
2. The Machinery of Place Value — Why Ten Fingers Built the World
3. Other Bases and Ancient Minds — The Architecture of Counting Systems

---

## TL;DR

Numbers and numerals are different things. A numeral is a written symbol; a number is an abstract idea. The Hindu-Arabic system works because of place value — the position of a digit determines its meaning, not just repetition of marks. Once you understand how place value works in base 10, you can use that same machinery in any other base, including base 2 (the language of computers). This chapter shows you why that machinery is the same, how other cultures built it differently, and what it means to do arithmetic when your symbols and grouping change.

---

## Chapter opening — A price tag and three counting systems

You're standing in a market in Cairo in the year 1100. The merchant is selling linen. You want to buy 27 cubits' worth. The merchant makes a mark on a piece of papyrus. One mark. Not 27 marks. One single symbol that means 27 to anyone who learned his writing. Sixteen hundred miles west, in what's now Spain, a Roman clerk records the same transaction using Roman numerals: XXVII — twenty, five, and two ones, written out symbol by symbol. One thousand miles east, in India, a different notation is emerging in a scholar's manuscript: the merchant there writes 27 using our modern digits, 2 and 7. Same quantity. Three different ways to say it.

The question is: which system forces your brain to work less? Which one could you teach to a child in an afternoon? Which one lets you multiply two prices together without losing your mind?

You probably know the answer. But the answer isn't obvious if you're the merchant in Cairo. It only becomes obvious once you understand the trick hiding inside the numerals.

### Learning objectives

By the end of this chapter you will be able to:

- **Distinguish** between a number (an abstract quantity) and a numeral (a way of writing it down), and explain why the difference matters.
- **Explain** what place value is, why it works, and how it makes our arithmetic faster.
- **Convert** between the Hindu-Arabic numeral system and expanded form using exponents.
- **Understand** how ancient systems (Babylonian, Mayan, Roman) solved the problem of representing large quantities without place value.
- **Identify** the base of a numeration system, name the legal symbols in that base, and convert between any base and base 10.
- **Perform** addition, subtraction, and multiplication in bases other than 10, using the appropriate place-value machinery.

### Prerequisites

Arithmetic with whole numbers. Familiarity with exponents as repeated multiplication ($2^3 = 2 \times 2 \times 2 = 8$). Comfort reading place value in base 10: the rightmost digit represents ones, the next left represents tens, the next represents hundreds, and so on.

### Why this chapter matters

This chapter is not about learning to use a computer (though computers run in base 2, and you're about to see why). It's about understanding that the way we write numbers is a *choice*, not a law of nature. Once you grasp that choice — once you watch how the same quantity looks in base 10, base 2, base 20, and base 60 — you'll never again think of arithmetic as a fixed system handed down from on high. You'll see it as a human invention, debugged and refined over thousands of years. That shift in perspective is the beginning of real mathematical thinking. You'll see the machinery underneath, not just the rules on top.

---

## Concept 1 — Numbers, numerals, and why place value was the innovation of the millennium

Open your eyes in a grocery store. You see a price tag on a carton of eggs: $3.99. That price tag is a numeral. It's written down using a specific system — the Hindu-Arabic system with its digits 0 through 9 and its rules about position. But the *amount of money* — the abstract idea of "almost four dollars" — that's the number.

A **numeral** is a symbol or a group of symbols used to write down a number. The number is the quantity itself. The word "four," the Roman numeral IV, the tally mark ⬜⬜⬜⬜, and the digit 4 are all different numerals for the same number: four.

This distinction seems small. It matters enormously for understanding why some systems of numerals work and others create chaos.

### The tally system and repetition

The oldest way to record quantity was to repeat a single mark — one mark for one sheep, two marks for two sheep, a line through every fifth mark to group them. This is an *additive system*, from the Latin *addere*, meaning to add. You add up the marks and you know the count. A tally of 27 would require 27 marks. Write them all out.

This system has advantages: a child can understand it immediately, and there's no way to get confused about what a mark means. But try to record the year 1492 in tally marks. You'd use 1,492 marks. A Roman census would require a library. An accountant would go mad.

### Roman numerals: still additive, but clever

The Romans invented a refinement: use different symbols for different quantities. I for one, V for five, X for ten, L for fifty, C for one hundred, D for five hundred, M for one thousand. Then add them together: XVI means ten plus five plus one, so sixteen. MCMLVII means one thousand plus (one thousand minus one hundred) plus fifty plus five plus two, so nineteen hundred fifty-seven.

This is still additive. You still add up the symbols. But now MCMLVII is manageable, because you're using seven symbols instead of 1,957 marks. The Roman system works reasonably well for modest numbers and readable dates. It fails catastrophically for multiplication. Try multiplying 37 by 24 using Roman numerals. You can do it (it's more like decoding a puzzle than arithmetic), but you'll understand why Roman accountants eventually retired.

The problem: Roman numerals don't use position. The M in MCMLVII means "one thousand" no matter where it sits. So you can't use the same symbol in different positions to mean different quantities. You need a new symbol for each order of magnitude. Once you run out of symbols, you're stuck.

### Place value: the idea that changed everything

Somewhere around the fifth century in India, a mathematician named Aryabhata wrote down a transformative thought: *the position of a digit determines what it represents*. In the numeral 27, the 2 is in the "tens place," so it means 2 tens, or 20. The 7 is in the "ones place," so it means 7 ones. The number 27 is 20 + 7.

More radically, Aryabhata realized you could write the same symbol in different positions and it would mean different things. In 222, the leftmost 2 means 2 hundreds (200), the middle 2 means 2 tens (20), and the rightmost 2 means 2 ones. Same symbol, three different values, because of position.

**Place value** — from the Latin *platea*, a wide street or open space — means the position of a digit in a numeral determines its meaning. Each position is a multiple of some base raised to a power. In base 10, the rightmost position is $10^0 = 1$ (the ones place), the next left is $10^1 = 10$ (the tens place), the next is $10^2 = 100$ (the hundreds place), and so on.

This is why the number $3,099 reads as three thousand ninety-nine: the 3 is in the thousands position ($10^3 = 1,000$), the 0 is in the hundreds position (meaning "skip the hundreds"), the 9 is in the tens position ($10^1 = 10$), and the 9 is in the ones position.

But place value needs something tally marks don't: a symbol for zero. If you want to write "one thousand and nine" (no hundreds, no tens), you need a way to say "nothing is here" in the hundreds and tens places. You need 0.

### Why zero was a hard invention

For most of human history, there was no zero. The concept made philosophers uncomfortable. Aristotle didn't believe in void or emptiness — how could nothing be something? But merchants and engineers kept running into the same problem: you need to *show* that a place is empty. The Babylonians, around 700 BCE, used a space. The Mayans, around 400 CE, drew a symbol that looks like a shell. The Indians, around 600 CE, wrote a dot and later a circle — the ancestor of our 0.

Brahmagupta, a mathematician in India in the seventh century, did something radical: he said 0 is a number. It has properties. You can do arithmetic with it. He made zero an object of study, not just a placeholder.

Once place value and zero arrived together, the system became unstoppable. Here's why: *you need only as many symbols as your base*. Base 10 needs 10 symbols (0–9). That's it. Any number, no matter how large, can be written using those 10 symbols arranged in different positions. Your position determines your magnitude. A child who learns 10 symbols can represent any quantity in the world.

### Worked example — unpacking a familiar numeral

The number $738$ looks simple. When you read it aloud, you say "seven hundred thirty-eight." But that sentence is actually the *expanded form* of the numeral — you're naming each position's contribution.

$738 = 7 \times 10^2 + 3 \times 10^1 + 8 \times 10^0$

$= 7 \times 100 + 3 \times 10 + 8 \times 1$

$= 700 + 30 + 8$

The 7 is in the hundreds place, so it means 7 times 100. The 3 is in the tens place, so it means 3 times 10. The 8 is in the ones place, so it means 8 times 1. Add them up: 700 + 30 + 8 = 738. This is what "seven hundred thirty-eight" means: you're adding the contributions of each position.

Reverse the process: take the expanded form and collapse it. $5 \times 10^3 + 0 \times 10^2 + 4 \times 10^1 + 9 \times 10^0$ becomes $5 \times 1000 + 0 + 40 + 9 = 5,049$. The digits are 5, 0, 4, 9. Write them in order from highest position to lowest: 5049. Notice the 0 in the hundreds position? That zero is doing work. It's saying "there are no hundreds." Without it, the numeral would be 549, which means something completely different.

This is so automatic for you that you probably don't think about it. But this is the whole machinery of our numeral system. The position tells you what power of 10 to multiply by. Zero tells you "this position is empty." That's place value. And once you understand it, you can apply it to any base, not just base 10.

### Common misconceptions

**Place value is about position, not about the name of the position.** The number 237 doesn't "have" hundreds and tens and ones. The numeral 237 has a digit in the hundreds position ($10^2$), a digit in the tens position ($10^1$), and a digit in the ones position ($10^0$). The position is what matters. When you switch to base 7, the positions will mean something different (powers of 7, not powers of 10), but the machinery stays the same.

**Zero is not "nothing" — it's a digit.** The number 204 has three digits: 2, 0, and 4. The 0 is a legitimate digit that means "zero items in the tens place." That's why 204 and 24 are different numbers. Without the zero in the middle, 24 reads as 2 tens + 4 ones. With the zero, 204 reads as 2 hundreds + zero tens + 4 ones. The zero is doing work.

---

## Concept 2 — How other cultures solved the problem without place value

Different civilizations, with different needs and different symbols, developed different systems. Some used place value early. Some invented alternatives. All of them faced the same core challenge: how do you write down large numbers without drowning in symbols?

### The Babylonians: place value without zero

The Babylonians, around 1800 BCE, used a *positional system* based on powers of 60, not powers of 10. Sixty, from the Akkadian *šūšu*, appears to have been chosen because 60 has many divisors: you can divide it evenly by 2, 3, 4, 5, 6, 10, 12, 15, 20, 30. Mathematically, 60 is more versatile than 10.

The Babylonians used two symbols: a wedge (⋀) for 1, repeated up to 9 times, and a wider wedge (◁) for 10, repeated up to 5 times. So the symbol for 27 would be: ◁◁ followed by ⋀⋀⋀⋀⋀⋀⋀. Additive within each position, but positional across positions.

To convert a Babylonian numeral to base 10, you use powers of 60 just as you'd use powers of 10 in our system. Suppose the Babylonian numeral has two "digits" (two groups): the first group represents 4, the second represents 27. Then the value is:

$$4 \times 60^1 + 27 \times 60^0 = 4 \times 60 + 27 \times 1 = 240 + 27 = 267$$

The system worked beautifully for astronomy and land measurement. But it had a gap: there was no symbol for zero. A blank space had to serve the purpose. This created ambiguity. The numerals for 101, 110, and 11 (in base 60) could look nearly identical if the scribe wasn't careful. Over time, the Babylonians did develop a marker for an empty position — a symbol that looked like a double wedge — but it took centuries.

Babylonian place value still echoes in how we measure time: 60 seconds in a minute, 60 minutes in an hour. And in how we measure angles: 1 degree = 60 arcminutes, 1 arcminute = 60 arcseconds.

### The Mayans: positional with zero and an astronomical twist

The Mayans, in Mesoamerica, developed a place-value system based on powers of 20 around 400 CE. They had a dedicated symbol for zero — a glyph that resembled a shell or an empty eye socket. The system was fully positional: different positions meant different powers of 20. And it was written *vertically*, with the lowest power at the bottom and higher powers above, like a stack.

$$\text{(top digit)} \times 20^2 + \text{(middle digit)} \times 20^1 + \text{(bottom digit)} \times 20^0$$

So if the bottom is 9, the middle is 8, and the top is 6, the value is:

$$6 \times 400 + 8 \times 20 + 9 \times 1 = 2,400 + 160 + 9 = 2,569$$

The Mayans used dots for 1 through 4, a horizontal bar for 5, and combinations of bars and dots for 6 through 19. At 20, they would move to the next position. This is why historians call it base 20: once you've counted through 20 symbols (0–19), you start a new position.

Here's where it gets interesting: the Mayans used base 20 for daily counting but a slightly modified system for their calendar. The calendar system used 1, 20, then 20×18 = 360, then 20×18×20 = 7,200. Why 18 instead of 20? Because 360 is close to the actual number of days in a solar year (365.25). They were engineering their numeral system to fit astronomy.

### The Romans: no position, pure addition with subtraction tricks

The Roman system never used place value. It relied entirely on addition (and a few subtraction tricks). The symbols were I (1), V (5), X (10), L (50), C (100), D (500), M (1,000). Larger numbers required new symbols — an overline to mean "multiply by 1,000" — but the system was fundamentally additive.

The Romans developed a *subtractive* convention: instead of writing 4 as IIII (four ones), they wrote IV (one before five). Instead of 9 as VIIII, they wrote IX (one before ten). This convention made numerals shorter, but it also meant you had to understand the rule: a smaller numeral before a larger one means subtraction.

The Roman system was adequate for accounting and record-keeping in an empire. It failed for science. You cannot easily multiply XXVII by XLII in your head or on wax. The system doesn't scale well. It died out as soon as Hindu-Arabic numerals arrived in Europe, because those numerals made arithmetic teachable to ordinary people.

### Trade-off: repetition, position, or subtraction?

Every ancient system faced a choice:
- Use *repetition* of symbols (tally marks, basic Roman numerals). Easy to understand, drowns you in symbols for large numbers.
- Use *position* (Babylonian base 60, Mayan base 20, eventual Hindu-Arabic base 10). Compact and works for any magnitude, but requires understanding the concept of place value and (ideally) a zero.
- Use *subtraction* (Roman subtractive notation). A compromise, but requires knowing the rules, and it doesn't help with multiplication or division.

The Hindu-Arabic system chose position and zero, and that choice let mathematicians and merchants compute faster, teach arithmetic more easily, and scale to any number. It's not inherently "better" — it's better *for multiplication and division*, which were the operations that mattered most once commerce and science needed to grow.

### Worked example — converting from Roman numerals to base 10

Roman numeral: **MMCMXLVIII**

Read it left to right, applying the addition and subtraction rules:
- MM = 2 × 1,000 = 2,000
- CM = 900 (1,000 − 100)
- XL = 40 (50 − 10)
- V = 5
- III = 3

Sum: 2,000 + 900 + 40 + 5 + 3 = **2,948**

Reverse: Convert 2,948 to Roman numerals.
- 2,000 = MM
- 900 = CM (one less than 1,000)
- 40 = XL (one less than 50)
- 8 = VIII (five plus three)

Result: **MMCMXLVIII**

### Common misconceptions

**Different bases aren't "wrong" bases.** Base 60 is mathematically elegant and divisible by more numbers than base 10. Mayan base 20 was astronomically accurate. Roman numerals served an empire for centuries. They're all solutions to a real problem: representing quantity. They just have different costs. Base 10 is dominant now because of historical accident and because it matches our finger count, not because it's mathematically superior.

**"Position" and "place value" mean the same thing.** Babylonian numerals were positional but didn't have a dedicated zero symbol. Mayan numerals were positional and had zero. Roman numerals were not positional at all. The machinery is different in each case.

---

## Concept 3 — Generalizing place value: any base, any symbols

Now that you've seen how different cultures invented different systems, you're ready for the leap: place value is not specific to base 10. It's a *generalizable machinery*. If you understand how it works in base 10, you can apply it to any base.

Here's the insight: **all positional systems follow the same rules.** Whether you're working in base 10, base 60, base 20, or base 2, the machinery is identical. The position of a digit determines which power of the base you multiply it by. Zero (or an empty position) means "skip this power." Add up all the place values and you get the quantity. The symbols are different, the base is different, but the principle is the same. This is why learning base conversion is so important: once you can convert between any two bases, you've grasped the universal principle underneath all positional systems.

### Why bases matter: how many symbols do you need?

In base 10, we use 10 symbols: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9. Why 10? Because we group by tens — every time we've used up all our symbols, we move to the next position.

In base 6, we'd use 6 symbols: 0, 1, 2, 3, 4, 5. Once we've counted through 5, the next number is 10 in base 6. That 1 means "one group of six" and that 0 means "zero ones." In base 6 notation, $10_6 = 6$ in base 10.

In base 2 (the language of computers), we use 2 symbols: 0 and 1. Every time we count up from 1, we move to a new position. The sequence goes: $0_2, 1_2, 10_2, 11_2, 100_2, 101_2, 110_2, 111_2, 1000_2, \ldots$

For bases larger than 10, we run out of digits. We use letters. In base 12 (which some mathematicians argue is more practical than base 10), we'd use: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A (representing 10), B (representing 11). Then $10_{12} = 12$ in base 10.

Here's the scale shift: **a base larger than 10 needs letters because we've only invented 10 digits.** We use A = 10, B = 11, C = 12, etc. This isn't mystical. It's a notational choice.

### Converting any base to base 10 using expanded form

The machinery is identical to base 10. Write the numeral in expanded form using powers of the base.

Example: Convert $3024_6$ (a base 6 numeral) to base 10.

The numeral has 4 digits. Reading left to right, the positions represent $6^3$, $6^2$, $6^1$, and $6^0$.

$$3024_6 = 3 \times 6^3 + 0 \times 6^2 + 2 \times 6^1 + 4 \times 6^0$$

Calculate:
$$= 3 \times 216 + 0 \times 36 + 2 \times 6 + 4 \times 1$$
$$= 648 + 0 + 12 + 4 = 664_{10}$$

The base 6 numeral $3024_6$ represents the same quantity as the base 10 numeral $664$. Different notations, same number.

Example: Convert $4B7_{14}$ (a base 14 numeral using the letter B to mean 11) to base 10.

$$4B7_{14} = 4 \times 14^2 + 11 \times 14^1 + 7 \times 14^0$$
$$= 4 \times 196 + 11 \times 14 + 7 \times 1$$
$$= 784 + 154 + 7 = 945_{10}$$

### Converting base 10 to any other base using division

The reverse process is trickier conceptually but mechanical in execution: divide repeatedly by the base, keep track of remainders, and read the remainders *in reverse order*.

Example: Convert $298_{10}$ to base 6.

Divide by 6 repeatedly:
- $298 \div 6 = 49$ remainder $4$
- $49 \div 6 = 8$ remainder $1$
- $8 \div 6 = 1$ remainder $2$
- $1 \div 6 = 0$ remainder $1$

Read the remainders from bottom to top: **1, 2, 1, 4**. So $298_{10} = 1214_6$.

Check: $1 \times 6^3 + 2 \times 6^2 + 1 \times 6^1 + 4 \times 6^0 = 216 + 72 + 6 + 4 = 298$. ✓

Example: Convert $100_{10}$ to base 2.

Divide by 2 repeatedly:
- $100 \div 2 = 50$ remainder $0$
- $50 \div 2 = 25$ remainder $0$
- $25 \div 2 = 12$ remainder $1$
- $12 \div 2 = 6$ remainder $0$
- $6 \div 2 = 3$ remainder $0$
- $3 \div 2 = 1$ remainder $1$
- $1 \div 2 = 0$ remainder $1$

Read the remainders from bottom to top: **1, 1, 0, 0, 1, 0, 0**. So $100_{10} = 1100100_2$.

Notice: $100$ in base 10 takes only 3 digits, but in base 2 it takes 7 digits. Smaller bases require more digits to represent the same quantity. This is why computers using base 2 need a lot of digits, but they have the advantage that their "digits" (bits) are easy to represent electronically: high current or low current, on or off.

### Common misconceptions

**Larger bases don't make "bigger" numbers.** The numeral $24_6$ and the numeral $24_{10}$ look the same, but they mean different things. $24_6 = 2 \times 6 + 4 = 16_{10}$. The base subscript is not optional; it's part of the meaning.

**There's no "best" base for all purposes.** Base 10 is human-friendly (matches finger count) and adequate for most purposes. Base 60 was better for ancient astronomy and measurement. Base 2 is essential for computer architecture. Base 12 divides more evenly than base 10. The choice depends on what you're trying to do.

**Converting between bases is a process, not a trick.** Expanded form for converting *to* base 10. Repeated division for converting *from* base 10. Memorize the process and you can convert any base to any other base.

---

## Integration — the three systems, side by side

You're now at a market stall looking at a linen price. The merchant from Cairo writes it in Egyptian numerals (an ancestor of our 0–9). The Roman visitor writes XXVII. The Mayan trader writes it vertically using dots and bars. The Hindu merchant writes 27. The computer scientist translates it to binary: 11011.

All five representations describe the same quantity. But they expose different structures.

- **Egyptian/Hindu-Arabic:** Place value with repeated symbols (for small numbers) or position (for large numbers). Eventually, we abandoned repetition and went purely positional.
- **Roman:** Pure addition with a subtraction trick. No place value. Compact for dates and monuments, useless for mathematics.
- **Mayan:** Pure place value with a clear zero symbol. Vertically stacked. Elegant and mathematically sound.
- **Binary:** Place value in base 2. Requires many digits but can be stored and processed by machines.

The deepest insight: **place value is the innovation that makes arithmetic teachable**. Once you have place value and zero, multiplication stops being a puzzle and becomes a process. A merchant's apprentice in 1500 CE, using Hindu-Arabic numerals, could multiply prices in an hour of training. A Roman accountant needed years of study to do the same calculation. That difference — that single shift in notation — transformed commerce and eventually science.

---

## Exercises

### Warm-up

**4.1** *(Understanding place value.)* Write the following numerals in expanded form using exponents.
- (a) 5,247
- (b) 30,905
- (c) 1,000,001

**4.2** *(Converting between bases.)* Convert the following base 6 numerals to base 10.
- (a) $34_6$
- (b) $105_6$
- (c) $523_6$

**4.3** *(Identifying legal symbols.)* For each base, list the legal symbols.
- (a) Base 5
- (b) Base 8
- (c) Base 12

### Application

**4.4** *(Converting from base 10.)* Convert the following base 10 numerals to the specified base.
- (a) 50 to base 7
- (b) 100 to base 2
- (c) 45,134 to base 13

**4.5** *(Arithmetic in a different base.)* Create a base 4 addition table. Then use it to calculate $132_4 + 213_4$.

**4.6** *(Historical systems.)* Convert the Roman numeral MDCCCLXXIII to base 10. Then verify by converting the base 10 result back to Roman numerals.

### Synthesis

**4.7** *(Comparing systems.)* The number one thousand is written as:
- 1,000 in base 10
- 1750 in base 8
- 15E8 in base 16 (where E represents 14)

(a) Verify each conversion. (b) Explain why base 16 uses fewer digits. (c) Why might computer scientists prefer base 16 or base 8 when discussing large numbers, instead of base 2?

**4.8** *(Multiplication across bases.)* In base 5, calculate $23_5 \times 14_5$. Build a base 5 multiplication table if needed. Verify by converting both to base 10, multiplying, and converting back.

### Challenge

**4.9** *(Thinking about divisibility.)* Base 12 has divisors 2, 3, 4, and 6. Base 10 has divisors 2 and 5. Base 6 has divisors 2 and 3. (a) Which base would be best for dividing a quantity into thirds? Explain. (b) What about dividing into fifths? (c) Design a base that would make dividing by 3, 4, and 5 all easy. What base would you choose and why?

**4.10** *(Open-ended: ancient commerce.)* You are a merchant in Babylon in 600 BCE. You've just learned about the Hindu-Arabic system (imagine it's been translated into your language). Write a one-paragraph argument for why your fellow merchants should abandon Babylonian base 60 numerals and adopt this new system. What concrete advantage would you highlight?

---

## Chapter summary

You now understand why a written numeral is not the same as the abstract number it represents. You know that the Hindu-Arabic system's power comes from two ideas: **place value** (position determines meaning) and **zero** (a symbol for an empty position). Those two ideas, invented over centuries in India, eventually spread worldwide and made arithmetic fast enough for commerce and science to accelerate.

You've also seen that place value is not an accident of base 10. It's a generalizable principle. You can build a positional system in any base. You can convert between any two bases using expanded form or repeated division. A base 6 system works exactly like base 10, just with different positions and different symbols. Base 2 works the same way, which is why computers can use it: the machinery is identical, only the base changes.

The last skill you should be able to demonstrate: given any base and any numeral written in that base, you can determine whether the numeral is valid (uses only legal symbols), convert it to base 10, and explain why a different base might be better or worse for a specific purpose.

The thing to watch going forward: **whenever you see a numeral, ask what base it's in**. In this book, we'll mostly stick to base 10 because it's standard. But in computers, in cryptography, in some scientific fields, other bases do real work. The machinery you learned in this chapter is the foundation for understanding how they work.

---

## Connections forward

Chapter 5 moves into algebra — equations and functions. You'll use the place value system and decimal notation constantly. Every time you see a number like 2.5 or 3.14, you're reading a *decimal numeral*, which extends place value into negative powers of 10. The 5 in 2.5 is in the tenths position ($10^{-1}$). That's the same machinery you learned here, just with negative exponents.

Then in Chapter 6 (Money management), you'll work with interest rates, prices, and percentages. All of those require clear understanding of what each digit means in base 10. You'll also encounter situations where base 2 and base 16 appear (in computer science, if you take that path), but the conversion skills are the same.

Most importantly, the conceptual insight — that notation is a choice, and different choices have different costs — will reappear in algebra (different ways to write equations), statistics (different ways to visualize data), and geometry (different coordinate systems). The idea is always the same: find the notation that makes the problem clear.

---

**What would change my mind:** If I discovered that place value didn't originate in India in the 5th–7th centuries but earlier, or in a different place, I would revise the historical framing. The mathematical machinery would stay unchanged.

**Still puzzling:** Why base 20 for the Mayans? The leading hypothesis is that it matches counting on fingers and toes together (20 total). But I haven't found definitive archaeological evidence for the origin story. The choice seems culturally pragmatic, not mathematically necessitated.

**Tags:** place-value, numeral-systems, bases, Hindu-Arabic, Babylonian, Mayan, Roman, base-conversion, mathematical-notation, Aryabhata, Brahmagupta, zero, positional-systems
