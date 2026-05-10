# Chapter 7 — Probability

## Suggested titles

- How to Count When You Can't Count: Combinatorics and the Measurement of Chance
- The Weight of Possibility: Probability as a Tool for Decision-Making
- Casinos and Coin Flips: Why Some Bets Win and Others Don't (Long Run Edition)

## TL;DR

Probability is the language for measuring how likely something is—not as a gesture, but as a number between 0 and 1. To assign that number, you first have to count the ways an event can happen and divide by the total ways anything can happen. Once you have a probability, you can predict the average outcome of repeating an experiment many times over. That average—the expected value—is how casinos stay profitable.

---

## Cold open

The Las Vegas casino is crowded on a Friday night. At a roulette table in the corner, a woman in a blue dress places $100 on black. The croupier spins the wheel. It is a machine of pure indifference: a small ball, a rotating cylinder, 37 slots (18 black, 18 red, 1 green zero). The ball bounces, settles. Black. She wins $100. She places another $100 on black. Red. She loses. Again black. She wins again. 

By the end of the night, she has won four times and lost six times. She is down $200. She leaves frustrated, convinced she was unlucky. The croupier returns to work. In the long run—over millions of spins, millions of bets—this wheel will do exactly what it is designed to do: transfer money, slowly and steadily, from the pockets of players to the vault of the casino. The players' bad luck is not bad luck at all. It is mathematics.

This chapter teaches the language that casino managers, insurance adjusters, weather forecasters, and political strategists use to talk about uncertainty. It is the language of probability: how to measure chance, how to count the possibilities when counting is hard, and how to know what will happen *on average* when nothing is certain about what happens *next*.

### Learning objectives

By the end of this chapter you will be able to:

- **Count** large sets of outcomes using the multiplication rule, permutations, and combinations, without listing them.
- **Define** sample spaces and events; distinguish theoretical, empirical, and subjective probability.
- **Compute** probabilities using counting tools and the complement rule.
- **Interpret** conditional probability and apply the multiplication rule for probability.
- **Calculate** expected values and use them to evaluate whether a game or investment is worthwhile.

### Prerequisites

Arithmetic with whole numbers, fractions, and decimals. Comfort with the idea that outcomes can be organized into sets (you met this in Chapter 1).

### Why this chapter matters

Every later chapter uses probability. Statistics sorts data into sets and asks what probability distribution they follow. Voting theory analyzes whether a voting method is fair by computing the probability of a tie. Money management uses probability to price insurance and bonds. Probability is the mathematics of uncertainty, and uncertainty is everywhere.

---

## Concept 1 — Counting Principles: The Multiplication Rule, Permutations, and Combinations

A bakery offers customized cupcakes. For the cake, you have three choices: vanilla, chocolate, strawberry. For the frosting, four: vanilla, chocolate, lemon, strawberry. How many different cupcakes are possible?

You could list them: vanilla-vanilla, vanilla-chocolate, vanilla-lemon, vanilla-strawberry, chocolate-vanilla, chocolate-chocolate, and so on. You would end up with twelve combinations. But listing works only when the set is small.

In a more realistic scenario, you are dealing a 5-card poker hand from a standard deck of 52 cards. There are over 2.5 million possible hands. Listing them is not practical. You need a shortcut.

### The multiplication rule for counting

The multiplication rule, also called the fundamental counting principle, is the foundational shortcut. It says this: *If there are n ways to accomplish one task and m ways to accomplish a second task, then there are $n \times m$ ways to accomplish both tasks in sequence.*

For the cupcakes, task one (choose cake) has 3 ways. Task two (choose frosting) has 4 ways. Together: $3 \times 4 = 12$ ways.

For a more complex example: a standard 6-character license plate consists of 3 letters followed by 3 digits. There are 26 letters to choose from and 10 digits (0 through 9). The number of possible plates is:

$$26 \times 26 \times 26 \times 10 \times 10 \times 10 = 17,576,000$$

Each choice multiplies the possibilities. This is the engine of combinatorics—the mathematics of counting possibilities.

#### Why the rule works, and when it breaks

The rule works because each choice is *independent*. The letter you choose for position 1 does not limit which letters you can choose for position 2. If the first choice affected the second, you cannot use simple multiplication; you must adjust the count for the remaining possibilities.

Here is where that matters: suppose you are drawing cards from a deck without replacement—once you draw a card, it stays out. The first draw has 52 possibilities. The second draw has only 51 (one card is gone). If you draw two cards in order, the number of possible ordered outcomes is $52 \times 51 = 2,652$, not $52 \times 52 = 2,704$. Independence failed; you adjusted the count accordingly.

### Permutations: When order matters

A permutation is an ordered arrangement. If you are filling the top three finisher spots in a race of 8 swimmers, you care which swimmer is first, which is second, which is third. 1st, 2nd, 3rd is different from 2nd, 1st, 3rd.

For the first place finisher, there are 8 choices. Once that swimmer is done, 7 remain for second. Once second is decided, 6 remain for third. By the multiplication rule:

$$8 \times 7 \times 6 = 336$$

There are 336 different ways to award the podium.

This pattern—multiply a descending sequence—shows up constantly. Mathematicians noticed and gave it a name: *factorial*. The notation $n!$ (read "$n$ factorial") means the product of all positive whole numbers from 1 to $n$.

$$5! = 5 \times 4 \times 3 \times 2 \times 1 = 120$$
$$8! = 8 \times 7 \times 6 \times 5 \times 4 \times 3 \times 2 \times 1 = 40,320$$

By convention, $0! = 1$. This keeps certain formulas clean.

The number of permutations of $n$ objects taken $r$ at a time is:

$$P(n, r) = {}_nP_r = \frac{n!}{(n - r)!}$$

For the swimmers: $P(8, 3) = \frac{8!}{(8 - 3)!} = \frac{8!}{5!} = \frac{8 \times 7 \times 6 \times 5!}{5!} = 8 \times 7 \times 6 = 336$. The factorials cancel, leaving the product of 3 descending numbers—exactly what we calculated.

### Combinations: When order doesn't matter

A combination is a selection where order does not matter. In most card games, a hand of 5 cards is the same whether you draw them in the order A-K-Q-J-10 or 10-J-Q-K-A. The hand is what counts.

Here is the relationship: the number of permutations of $n$ objects taken $r$ at a time is equal to the number of combinations times the number of ways to order those $r$ objects:

$$P(n, r) = C(n, r) \times r!$$

Rearrange:

$$C(n, r) = \frac{P(n, r)}{r!} = \frac{n!}{r!(n - r)!}$$

For a 5-card hand from 52 cards:

$$C(52, 5) = \frac{52!}{5!(52 - 5)!} = \frac{52!}{5! \times 47!} = \frac{52 \times 51 \times 50 \times 49 \times 48}{5 \times 4 \times 3 \times 2 \times 1} = \frac{311,875,200}{120} = 2,598,960$$

There are 2,598,960 possible 5-card poker hands.

#### The trade-off: precision vs. listed outcomes

When order matters (positions matter, sequence matters), use permutations. When it doesn't (a committee of 3 people with equal authority, a hand of cards, a lottery number), use combinations.

The trade-off is that permutations give larger counts. A smaller set of combinations can be rearranged into many permutations. This is not a flaw; it is the point. Combinations answer "how many ways can I choose?" Permutations answer "how many orders can that choice take?"

### Common misconceptions

**Permutations and combinations are not interchangeable.** A race where 1st and 2nd matter uses permutations. A committee where all members are equal uses combinations. Using the wrong tool gives a wildly wrong answer.

**The multiplication rule requires independence.** If your second choice depends on the first (drawing without replacement, choosing a second person who is not the first), adjust the count for the reduced available options.

**Factorials grow very fast.** $10! = 3,628,800$. The number of ways to arrange a standard 52-card deck is $52!$ — approximately $8 \times 10^{67}$, a number so large that if a new arrangement were created every microsecond since the Big Bang, we would have covered only a tiny fraction of all possible arrangements.

---

## Concept 2 — Basic Probability: Sample Spaces, Events, and Three Ways to Assign Probability

You roll a standard die. The *sample space*, from Chapter 1 vocabulary you have inherited, is the set of all possible outcomes: $S = \{1, 2, 3, 4, 5, 6\}$. An *event* is a subset of the sample space. The event "roll an even number" is $E = \{2, 4, 6\}$.

The *probability* of an event, written $P(E)$, is a number between 0 and 1 (inclusive) that expresses how likely the event is. If $P(E) = 0$, the event is impossible (it has no outcomes in the sample space). If $P(E) = 1$, the event is certain (it includes all outcomes). Everything in between represents some degree of possibility.

### Method 1: Theoretical probability

If the sample space consists of equally likely outcomes, the theoretical probability of an event is:

$$P(E) = \frac{n(E)}{n(S)}$$

where $n(E)$ is the number of outcomes in the event and $n(S)$ is the total number of outcomes in the sample space.

A standard 52-card deck has 13 hearts. If you draw one card at random:

$$P(\text{draw a heart}) = \frac{13}{52} = \frac{1}{4} = 0.25$$

Theoretical probability works when you can identify all equally likely outcomes. This is where counting tools from Concept 1 shine. The number of 5-card poker hands is $C(52, 5) = 2,598,960$. The number of hands that are a "royal flush" (10, J, Q, K, A of the same suit) is 4 (one per suit). So:

$$P(\text{royal flush}) = \frac{4}{2,598,960} \approx 0.00000154$$

This is a theoretical probability. You do not have to deal out millions of hands to know how rare a royal flush is.

#### The critical assumption: equally likely outcomes

Theoretical probability collapses if outcomes are not equally likely. Suppose your die is weighted so that 6 comes up twice as often as any other number. The sample space is still $\{1, 2, 3, 4, 5, 6\}$, but the outcomes are not equally likely. The formula $P(\text{roll a 6}) = 1/6$ no longer applies. You would need a different method—one that accounts for the actual probabilities of the outcomes.

### Method 2: Empirical probability

When outcomes are not equally likely, or when the sample space is too complex to enumerate, use empirical probability. An empirical probability is based on the observed frequency of an event in repeated trials:

$$P(E) = \frac{\text{number of times } E \text{ occurred}}{\text{total number of trials}}$$

A baseball player has 122 hits in 531 plate appearances so far this season. The empirical probability that he gets a hit on his next at-bat is:

$$P(\text{hit}) = \frac{122}{531} \approx 0.2297$$

This is not perfect. If his next plate appearance is against a left-handed pitcher and he historically struggles against left-handed pitching, the true probability is different. But if you have no better information, observed frequency is a reasonable estimate.

Empirical probability improves with sample size. A few trials introduce noise; thousands of trials smooth out randomness and reveal the underlying pattern. This is the Law of Large Numbers: as an experiment repeats, the observed average approaches the theoretical average.

### Method 3: Subjective probability

Sometimes you cannot list outcomes (so theoretical probability fails), and you have no past data (so empirical probability is impossible). A new rocket system is tested. The engineer says "I estimate a 2% chance of catastrophic failure." This is a subjective probability—an educated guess based on the engineer's knowledge and intuition.

Subjective probabilities are valid when they are necessary. But they are the least reliable. They vary person to person. They can be biased by overconfidence or fear. Use them only when the other two methods are unavailable.

### The complement rule: Easier to calculate the opposite

For any event $E$, the complement $E'$ (read "$E$ prime" or "not $E$") is the set of all outcomes not in $E$. Since every outcome either is or isn't in $E$:

$$P(E) + P(E') = 1$$

Rearrange:

$$P(E) = 1 - P(E')$$

Why is this useful? Often it is easier to calculate the probability of the opposite of what you want. If you are looking for "at least one success," it is easier to calculate "zero successes" and subtract from 1.

Example: You flip a fair coin 3 times. What is the probability of getting at least one heads? The opposite is "no heads at all" (i.e., TTT). The probability of three tails in a row is:

$$P(\text{TTT}) = \frac{1}{2} \times \frac{1}{2} \times \frac{1}{2} = \frac{1}{8}$$

So:

$$P(\text{at least one heads}) = 1 - \frac{1}{8} = \frac{7}{8}$$

Without the complement rule, you would have to count all outcomes with at least one heads: HHH, HHT, HTH, HTT, THH, THT, TTH. That is 7 outcomes. You get the same answer, but the complement rule is faster when the sample space is large.

### Common misconceptions

**Probability is not a guarantee.** A 90% probability of rain does not mean it will rain 90% of the time in that location. It means that on days when conditions are like today, rain occurs in 90% of cases.

**Theoretical and empirical probabilities can disagree short-term.** Flip a fair coin 10 times. You might get 7 heads and 3 tails. The empirical probability of heads is 0.7, but the theoretical probability is 0.5. Both are correct in their context. Over thousands of flips, empirical converges to theoretical.

**"Independent" and "equally likely" are different.** Two events are independent if the outcome of one does not affect the probability of the other (flipping a coin twice). Outcomes are equally likely if each has the same probability (a fair die). These are related but separate ideas.

---

## Concept 3 — Expected Value: What the Average Outcome Means for Decision-Making

Go back to the roulette table. You place $1 on black. If black comes up (18 chances out of 37), you win $1 and keep your original $1. If red or green comes up (19 chances out of 37), you lose your $1. Should you play?

To decide, calculate the *expected value*: the average amount you would win or lose per spin if you played many times.

$$E(X) = (1) \times P(\text{black}) + (-1) \times P(\text{not black})$$
$$= (1) \times \frac{18}{37} + (-1) \times \frac{19}{37}$$
$$= \frac{18}{37} - \frac{19}{37} = -\frac{1}{37} \approx -0.027$$

The expected value is negative. On average, each $1 bet costs you about 2.7 cents. Over 1,000 bets, you would expect to lose about $27.

The formula for expected value is:

$$E(X) = \sum n(O) \times P(O)$$

where $n(O)$ is the numerical value of outcome $O$, and $P(O)$ is its probability. The Greek letter sigma ($\sum$) means "add up."

### Worked example: Roulette vs. a fair game

An American roulette wheel has 38 slots: 18 red, 18 black, 2 green (0 and 00). A common bet is "red or black." You bet $1. If your color comes up, you win $1 (plus your original $1 back). If it doesn't, you lose your $1.

**American roulette (the actual casino game):**

$$E(X) = (1) \times \frac{18}{38} + (-1) \times \frac{20}{38} = \frac{18 - 20}{38} = -\frac{2}{38} = -\frac{1}{19} \approx -0.0526$$

The expected loss is about 5.26 cents per dollar bet.

**A fair game (hypothetical):**

Suppose someone offered you a game where you bet $1, and if a fair coin lands heads, you win $1. If it lands tails, you lose your $1.

$$E(X) = (1) \times \frac{1}{2} + (-1) \times \frac{1}{2} = 0$$

The expected value is zero. Over many plays, you break even. This is why casinos never offer fair games; they offer games where the expected value is negative for the player and positive for the house.

### Why expected value matters: The Law of Large Numbers

Expected value predicts the long-run average. If you make a single bet, you do not know the outcome—you might get lucky and win. But if you make 1,000 bets, the Law of Large Numbers says that your average winnings per bet will be very close to the expected value.

A lottery ticket costs $2. The expected payout is perhaps $0.50. If you buy one ticket, you might win big (and the expected value prediction is wrong). If you buy 10,000 tickets over many years, your average return per ticket will be approximately $0.50. You will lose about $1.50 per ticket, or $15,000 total.

This is not bad luck. This is mathematics. Casinos, insurance companies, and lotteries use expected value to guarantee profit *in the long run*, even though any single customer might win or lose in the short run.

### A scale shift: From a single bet to a casino's edge

Here is the flip side: a casino's advantage on a single roulette spin is small—a negative expected value of 1/19 of the bet, about 5 cents per dollar. But the casino makes thousands of bets per day. On a busy Friday night, a single roulette table might handle 100 spins per hour, $1 billion in total bets over a year.

One percent of $1 billion is $10 million. That is the casino's expected profit from one table in one year. Multiply that by 100 tables in one building, and you understand why casinos have spectacular architecture and free drinks. The profit comes not from beating individual players—many nights, a particular player walks away ahead—but from the mathematical certainty that in aggregate, across all players and all spins, the house keeps its edge.

### Common misconceptions

**Expected value is not the most likely outcome.** If you roll a die, the expected value is 3.5. You will never roll a 3.5. Expected value is a weighted average, not a prediction for a single trial.

**Expected value is not a guarantee.** If a game has an expected value of $0.50, you might lose all your money before the "law of large numbers" has time to work. Expected value predicts the long-run average, not the short-run result.

**Positive expected value does not mean you will be rich.** If you have an edge (expected value > 0), you will make money in the long run—but only if you have enough capital to survive the short-term variance (the ups and downs). A professional poker player with a positive expected value of $50 per hand still needs a bankroll to weather a bad losing streak.

---

## Integration — The Casino and the Counterintuitive Math of Advantage

Return to the casino from the cold open. The woman played roulette for hours, made dozens of bets, and lost money. She might have been skilled enough to understand the multiplication rule and calculate that a royal flush is rare. She might have known the theoretical probability of red or black. But she did not think in terms of expected value.

Here is the casino's calculation, which you can now follow:

A roulette wheel (American, with 38 slots) pays out the following for a $1 bet on red:
- Probability red comes up: 18/38
- You win: $1 (profit, plus your original $1 back)
- Probability red doesn't come up: 20/38
- You lose: $1 (you forfeit your original bet)

Expected value to the player:

$$E(X) = (1) \times \frac{18}{38} + (-1) \times \frac{20}{38} = \frac{18 - 20}{38} = -\frac{2}{38} \approx -0.053$$

On every $1 bet, the player expects to lose about 5.3 cents.

Now consider the casino's perspective. For every $1 wagered on red by all players combined, the casino expects to pocket about 5.3 cents. If $10 million in bets are placed on red in a year:

$$\text{Casino profit} = 10,000,000 \times 0.053 = 530,000$$

The casino is not cheating. The wheel is fair—each slot has an equal chance. The advantage comes from the structure of the payoff: the casino keeps the bet on a loss, and pays out only a 1:1 ratio on a win. This tiny asymmetry, repeated thousands of times, becomes an iron mathematical law.

The woman's mistake was not unlucky. It was logical. She saw red come up, and "went with the hot hand." She believed patterns. What she should have seen was expected value: a number that never changes, calculated once, true forever: **-0.053**.

Over months of play, the Law of Large Numbers guarantees that she loses about 5.3 cents per dollar wagered. There is no strategy, no system, no hot hand that changes that. Probability, over time, is destiny.

---

## Exercises

### Warm-up

**Exercise 7.1** *(LO: multiplication rule, permutations, combinations.)* A state license plate consists of 2 letters followed by 4 digits. (a) How many license plates are possible? (b) If the letter Q and the digit 0 are not allowed, how many are possible?

**Exercise 7.2** *(LO: permutations.)* In how many ways can 5 people be arranged in a line?

**Exercise 7.3** *(LO: theoretical probability.)* A standard deck is shuffled and one card is drawn. Find the probability that the card is: (a) a queen, (b) a red card, (c) a card that is not a heart.

### Application

**Exercise 7.4** *(LO: combinations and theoretical probability.)* A committee of 3 people is to be chosen from a group of 8. (a) In how many ways can this be done? (b) If the group consists of 5 women and 3 men, what is the probability that the committee consists of at least 2 women?

**Exercise 7.5** *(LO: empirical probability.)* A weather forecaster predicts rain for 35 of the past 100 days, and on those 35 days, it actually rained on 31 of them. (a) What is the empirical probability of rain, given the forecast? (b) What is the empirical probability that the forecast is correct?

**Exercise 7.6** *(LO: complement rule.)* A bag contains 5 red, 4 blue, and 3 green balls. You draw 2 balls without replacement. What is the probability that at least one is red?

### Synthesis

**Exercise 7.7** *(LO: conditional probability and multiplication rule for probability.)* A bag contains 10 coins: 7 fair coins (probability 0.5 of heads) and 3 biased coins (probability 0.8 of heads). You pick a coin at random and flip it twice. (a) What is the probability of getting 2 heads? (b) Given that you got 2 heads, what is the probability you picked a biased coin? (This is a "reverse" probability problem.)

**Exercise 7.8** *(LO: expected value.)* A lottery costs $2 to play. If your ticket matches all 6 numbers, you win $1 million. The probability of winning is 1 in 14 million. Otherwise, you lose your $2. What is the expected value?

**Exercise 7.9** *(LO: expected value and decision-making.)* You are offered two games. Game A: Flip a fair coin. Heads, you win $3. Tails, you lose $2. Game B: Roll a fair die. If you roll 1 or 2, you win $2. If you roll 3 or higher, you lose $1. Which game has a higher expected value? Which would you rather play, and why?

### Challenge

**Exercise 7.10** *(LO: integration and open-ended reasoning.)* A casino offers a new game: Roll two dice. If the sum is 7 or 11, you win $5. If the sum is 2, 3, or 12, you lose $10. Otherwise, the game is a push (no win, no loss). You bet $1 to play. What is the expected value? Is this a game the casino should offer?

**Exercise 7.11** *(LO: binomial reasoning.)* You are asked to guess randomly on a 10-question multiple-choice test. Each question has 4 options, so your probability of guessing correctly on any question is 0.25. Using the binomial formula (covered in the source materials but not emphasized here), or by direct calculation for a small example, estimate the probability of getting at least 5 questions correct by random guessing. (Hint: It is easier to calculate the complement.)

---

## Chapter summary

You now understand the tools that statisticians, casino managers, and decision-makers use to talk about uncertainty.

You can count large sets of objects without listing them, using the multiplication rule for straightforward sequences of choices, permutations when order matters, and combinations when it does not. You know the difference between theoretical probability (counting equally likely outcomes), empirical probability (observing past frequency), and subjective probability (educated guess). You know how to apply the complement rule to simplify calculations.

You understand that expected value is the long-run average outcome of an experiment—not a guarantee for any single trial, but a mathematical law that holds once an experiment repeats enough times. You know that this is how casinos, insurance companies, and lotteries make money: they set up games where the expected value is negative for the customer and positive for the house. No cheating required. Just mathematics, compounded across thousands of repetitions.

You have learned that probability is not about luck. It is about what *must* happen in the long run. The woman at the roulette table was not unlucky. She was foreseeable. The casino was not winning because it was smart. It was winning because the numbers guarantee it.

The thing to watch for, going forward, is **sample space**. Probability begins with a clear definition of what is possible. Sloppy sample spaces lead to sloppy probabilities. State the sample space first. Everything else follows.

What you should now be able to teach a friend who asks: why casinos always win, how to count possibilities without listing them, and why a bet with a negative expected value will drain your money over time—not because you are unlucky, but because the math does not care.

---

## Connections forward

Chapter 8 is Statistics. You will learn that statistics is built on probability: how to collect data, organize it into distributions, and use those distributions (which themselves are probability distributions) to infer facts about populations too large to survey entirely. The binomial distribution you saw in the source materials is one example of how probability and statistics merge.

Chapter 11, on Voting and Apportionment, applies probability to political questions: If a voting method is fair in theory, does it stay fair in practice? Here, expected value takes on a new meaning—the expected fairness of an election method, or the expected power of a voter in a voting system.

The casino, the lottery, the insurance premium, the weather forecast, the clinical trial—all rest on probability. Uncertainty is the condition of human life. Probability is the tool that converts uncertainty into a language we can reason with.

The roulette wheel spins. The outcome is unknown. But the average outcome over a thousand spins is not unknown. It is mathematics. And mathematics does not lie.

---

## What would change my mind

If the Law of Large Numbers were false—if the long-run average did not converge to the expected value—the entire framework would collapse. But the law has been proven and verified in countless experiments over three centuries. Nothing in this chapter would shift if a player got lucky at a casino; that is foreseeable variance, not a refutation of expected value.

---

## Still puzzling

The deepest puzzle in probability is the one that stumped gamblers for centuries: why does the long-run average converge to the expected value? The Law of Large Numbers *proves* it happens, but the question of *why*—the mechanism by which randomness produces order—remains beautiful and somewhat mysterious. You would study this more deeply in a formal probability course.

---

## Tags

#probability #counting #expected-value #law-of-large-numbers #permutations #combinations #casino #uncertainty
