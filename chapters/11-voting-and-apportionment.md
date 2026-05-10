# Chapter 11 — Voting and Apportionment

## TL;DR

Every voting system we will meet violates at least one fairness criterion—a structural fact about democracy known as Arrow's Impossibility Theorem. The same impossibility applies to apportionment: no method distributes seats to states without triggering paradoxes that contradict basic fairness. The choice of voting and apportionment method is not a technical detail. It is a political choice with consequences.

## Cold open

It is Tuesday morning in a town of 100 voters, and three school-board candidates are on the ballot: Alice, Bob, and Carol. The polls open. When they close, the tallies are: Alice 40 votes, Bob 37 votes, Carol 23 votes. Alice has the most. The election officer announces Alice is the winner and moves on.

But wait. Carol's voters overwhelmingly preferred Bob to Alice. In a head-to-head matchup between Bob and Alice, Bob would have beaten her 60 to 40. She won the election despite a clear majority preferring someone else. This is not a flaw in how the town counted. It is a structural property of the voting method they chose: *plurality voting*, in which the candidate with the most votes wins, regardless of whether they have a majority.

Now imagine the town adds a fourth option: a write-in campaign for Dorothy emerges halfway through the day. Dorothy ends up with 8 votes. The new totals: Alice 40, Bob 37, Carol 23, Dorothy 8. Alice still wins. But now Bob has 45 votes combined from the people who would prefer him. The presence of Dorothy—a candidate who lost badly and had no realistic chance—changed the outcome between Alice and Bob. This is called the *spoiler effect*, and it emerges from a different kind of flaw: the independence of irrelevant alternatives criterion.

These are not hypothetical problems. In the 2000 U.S. presidential election in Florida, Ralph Nader's 97,488 votes for the Green Party came almost entirely from voters whose second choice was Al Gore. Without Nader on the ballot, Gore would have won the state by thousands of votes and the presidency. But Nader was on the ballot, and George W. Bush won.

This chapter investigates what a fair voting system would look like—and proves that no such system exists.

### Learning objectives

By the end of this chapter you will be able to:

- **Apply** six different voting methods to election data (plurality, runoff, ranked-choice, Borda count, pairwise comparison, approval voting).
- **Evaluate** a voting method against four fairness criteria (majority, Condorcet, monotonicity, independence of irrelevant alternatives).
- **State and explain** Arrow's Impossibility Theorem and what it implies for democratic choice.
- **Calculate** the standard divisor and standard quota for apportionment.
- **Apply** four apportionment methods (Hamilton, Jefferson, Adams, Webster) and compare their results.
- **Identify** and construct examples of three apportionment paradoxes (Alabama, population, new-states).
- **Explain** the Balinski-Young Impossibility Theorem and why no apportionment method satisfies all fairness criteria.

### Prerequisites

Comfort with percentages, fractions, and basic division. Ability to compare numbers and rank them in order. Willingness to think about what "fairness" means and how it can fail.

### Why this chapter matters

Every democracy must decide: How will we elect representatives? How will we count votes? How will we distribute legislative seats among states or provinces? These choices are made as technical matters—the math must be correct, the ballots must be counted. But the choice of *which method* to use is not technical. It is political. This chapter teaches you how different methods change outcomes, what trade-offs each method makes, and what structural impossibilities constrain all of them. When you understand this, you cannot claim that a voting method is "fair" without defending exactly which fairness you value and which you are willing to lose.

---

## Concept 1 — Voting methods and how they differ

The story of voting methods begins with a question: What does "winning" an election mean?

In a two-candidate race—a referendum on a single issue—winning is clear. The candidate with more than half the votes has a *majority*, and that candidate should win. But elections with three or more candidates break this clarity into pieces.

When no candidate has a majority, one candidate has a *plurality*, from the Latin *plus*, meaning "more"—the most votes of any single candidate, even if fewer than half. The question becomes: Does plurality voting (awarding the seat to the candidate with the most votes) satisfy fairness?

**Plurality voting.** The candidate with the most votes wins, regardless of whether that is a majority. This is the method used in most U.S. elections. It is fast, simple, and transparent. 

Here is what it costs: If voters are divided into three groups that prefer candidates A, B, and C respectively, it is entirely possible that A wins with 35 percent of the vote while B and C each receive 32 percent—even though 65 percent of voters prefer either B or C to A. Moreover, a fourth candidate D can split the vote and change the outcome: when D enters and takes votes from B, suddenly A wins even though the electorate's underlying preferences have not changed.

**Runoff voting.** If no candidate wins a majority, the two candidates with the most votes advance to a second election. Voters then choose between these two finalists. The candidate with the majority in the runoff wins.

This preserves majority rule for the final outcome. It also eliminates spoilers in the first round—if you vote for your true favorite in round one and they do not advance, it does not matter whether a fourth candidate draws votes away from them or not. The trouble is time and cost: voters must return to the polls twice. Different voters may show up in round two, changing the outcome. And if a voter's first-choice candidate is eliminated, that voter has no voice in round two at all.

**Ranked-choice voting** (also called *instant runoff voting*) simulates multiple runoffs without asking voters to return. Each voter submits a single ballot ranking the candidates in order: first choice, second choice, third choice, and so on. 

In the first round, only first-choice votes are counted. If no candidate has a majority, the candidate with the fewest first-choice votes is eliminated. Second-choice votes from those ballots are then redistributed. This continues until one candidate reaches a majority.

Ranked-choice preserves majority rule without multiple trips to the polls. It eliminates some spoiler effects because voters can rank their true favorite first without fear of wasting their vote. But the method has a hidden cost: it is possible for a candidate to be *harmed* by receiving additional votes. Suppose candidate A is winning in round two. Some voters, seeing this, change their round-two ballot to move A up from second choice to first choice. Counterintuitively, this can hurt A—by shifting votes away from other candidates, it changes who gets eliminated in round three, and A might then lose. The method violates monotonicity, the principle that voting for a candidate more enthusiastically should never hurt that candidate.

**Borda count method.** Rank the candidates. Award points based on rank: if there are $n$ candidates, the first-place vote is worth $n - 1$ points, the second-place vote is worth $n - 2$ points, and so on, down to zero points for last place. The candidate with the most total points wins.

Example: Five voters rank three candidates—Red, Blue, Green. Voter 1 ranks Red 1st (2 points), Blue 2nd (1 point), Green 3rd (0 points). If all five voters rank them identically, Red gets $5 \times 2 = 10$ points, Blue gets $5 \times 1 = 5$ points, Green gets $0$.

Borda count has a particular strength: it tends to favor compromise candidates—those who are not anyone's first choice but are broadly acceptable. If the electorate divides between two extreme candidates (one loved by 45%, hated by 55%), and a moderate who is acceptable to everyone, Borda count will often elect the moderate. Some view this as wisdom. Others view it as a failure to respect the intensity of preferences from the largest group.

**Pairwise comparison** (Condorcet method). Compare each candidate to every other candidate in head-to-head matchups. For each pair, the candidate preferred by the majority wins that matchup. Award one point for each win. The candidate with the most points wins the election.

A candidate who beats every other candidate in head-to-head matchups is called a *Condorcet candidate*. If one exists, pairwise comparison will elect them. The problem: a Condorcet candidate does not always exist. Voters' preferences can form a *cycle*: A beats B, B beats C, C beats A. In such cases, there is no clear winner. Moreover, removing a candidate who lost badly can change who wins between two other candidates.

**Approval voting.** Each voter approves any number of candidates—zero, one, some, or all. A voter need not rank them. The candidate approved by the most voters wins.

This is simple: voters give a thumbs-up or thumbs-down to each candidate. It avoids spoilers and allows voters to express indifference. But it has a vulnerability: candidates can encourage supporters to approve *only* them and no one else, effectively collapsing the election into plurality voting. And like pairwise comparison, it is vulnerable to changes in the candidate pool.

### Worked example — comparing methods on a single election

Suppose 100 voters rank three restaurants: Rainbow China (R), Dough Boys Pizza (D), Taco City (T).

$$\begin{array}{cccc}
\text{Number of voters} & 35 & 30 & 35 \\
R & 1 & 3 & 2 \\
D & 2 & 1 & 3 \\
T & 3 & 2 & 1
\end{array}$$

The ballots break down as:
- 35 voters: R first, D second, T third
- 30 voters: D first, T second, R third
- 35 voters: T first, R second, D third

**Plurality.** Count first-place votes only: R gets 35, D gets 30, T gets 35. There is a tie between R and T. (In practice, a tiebreaker is needed. Plurality can fail to produce a clear winner.)

**Runoff.** R and T advance. The 30 voters who chose D second-prefer... let's say they split: 20 to R, 10 to T. Then R wins 55-45 in the runoff. (The outcome depends on assumptions about how D voters would break.)

**Ranked-choice.** D has the fewest first-place votes (30), so D is eliminated in round one. The 30 voters who ranked D first now have T as their second choice (from the table). First-place votes in round two: R = 35, T = 30 + 35 = 65. T wins with a majority.

**Borda count.** Each candidate gets 2 points for first place, 1 for second, 0 for third.
- R: $35 \times 2 + 35 \times 1 + 30 \times 0 = 70 + 35 = 105$
- D: $30 \times 2 + 35 \times 1 + 35 \times 0 = 60 + 35 = 95$
- T: $35 \times 2 + 30 \times 1 + 35 \times 0 = 70 + 30 = 100$

R wins with 105 points.

**Pairwise comparison.** 
- R vs D: 35 + 35 = 70 voters prefer R to D. D gets 30. R wins.
- R vs T: 35 + 30 = 65 voters prefer R to T. T gets 35. R wins.
- D vs T: 30 + 35 = 65 voters prefer D to T. T gets 35. D wins.

R wins 2 matchups, D wins 1, T wins 0. R is the Condorcet candidate and the pairwise comparison winner.

**Approval voting.** Suppose voters approve all candidates they rank in the top two. Then:
- 35 voters approve R and D (top two for them)
- 30 voters approve D and T (top two for them)
- 35 voters approve T and R (top two for them)

Approval counts: R = 35 + 35 = 70, D = 35 + 30 = 65, T = 30 + 35 = 65. R wins.

Notice: R wins under plurality (tied), Borda, pairwise comparison, and approval voting. But T wins under ranked-choice. D never wins under any method. The choice of method matters.

### Common misconceptions

**"If a candidate wins the most votes, they should win."** Plurality voting does give the most votes to the winner, but it does not require that candidate to be preferred by a majority. Many voters may prefer *anyone else*. Plurality voting confuses "received the most votes" with "is the voters' true preference."

**"Ranked-choice voting is fair because it does runoffs."** Ranked-choice voting does simulate runoffs and prevents some spoiler effects. But it violates monotonicity: voting for a candidate higher on your ballot can cause them to lose. This is not intuitive, but it is real.

**"Borda count is unfair because it ignores first-place votes."** Borda count does not ignore first-place votes. It weights them more heavily. The trade-off is that it elevates compromise candidates and can elect someone with no first-place votes at all if that person is broadly acceptable.

---

## Concept 2 — Fairness criteria and Arrow's Impossibility Theorem

Now that we understand voting methods, we can ask: Which method is fairest?

To answer that, we must define fairness. Here are four criteria that most people would find reasonable.

**Majority criterion.** If one candidate receives a strict majority of first-place votes (more than 50 percent), that candidate should win.

This is intuitive: if more than half the voters put someone in first place, they should win. Most systems pass this criterion. Plurality always does. Ranked-choice always does (the majority candidate will be the first to reach a majority in the runoff simulation). Pairwise comparison does (the majority candidate beats everyone else in head-to-head). But Borda count sometimes fails: a candidate with 51 percent first-place votes might have low second and third rankings, while a compromise candidate with 0 percent first-place votes ranks second everywhere and wins.

**Condorcet criterion** (head-to-head criterion). If one candidate beats every other candidate in a head-to-head matchup, that candidate should win.

This is also intuitive: if a candidate would win in a direct comparison against each opponent, they should win the full election. Pairwise comparison always satisfies this (by construction—if a Condorcet candidate exists, they win). But plurality, ranked-choice, and Borda count can all fail. In our restaurant example, R was the Condorcet candidate but lost in ranked-choice.

**Monotonicity criterion.** If a candidate wins, and then some voters change their ballots to rank that candidate *higher* (without any other change), that candidate should still win.

This is intuitive: voting for a candidate more enthusiastically should not hurt them. Plurality, pairwise comparison, and Borda count all satisfy this. But ranked-choice violates it. In ranked-choice, a candidate can be hurt by receiving additional votes in a position that changes the elimination order in later rounds.

**Independence of irrelevant alternatives (IIA).** If a candidate wins, and then a losing candidate is removed from the ballot, the original winner should still win.

This captures the spoiler idea: the outcome between A and B should not change when we add or remove C. All four methods fail this. When we remove a third candidate, the remaining candidates inherit votes, and the winner can change.

### The impossibility theorem

In 1972, economist Kenneth Arrow proved a stunning result: **No voting system based solely on ranked preferences can satisfy all four of these fairness criteria simultaneously.**

Here is what this means: You must choose. You cannot have a voting system that simultaneously gives the majority their first choice (majority criterion), elects Condorcet candidates (Condorcet criterion), avoids rewarding a candidate for receiving more votes (monotonicity), and ignores the presence or absence of also-ran candidates (IIA).

Every system makes a choice about which criterion to violate. Plurality and ranked-choice satisfy majority and monotonicity but violate Condorcet and IIA. Pairwise comparison satisfies majority and Condorcet but violates monotonicity and IIA. Borda count violates majority but satisfies Condorcet, monotonicity, and... no, it violates IIA like all the others.

The implication is profound: There is no neutral voting method. Every choice is a political choice.

### Worked example — where Arrow's theorem appears in practice

Consider a three-way race for mayor: Alice (centrist), Bob (left), Carol (right). Voters break down:

$$\begin{array}{cccc}
\text{Voters} & 40\% & 35\% & 25\% \\
\text{First} & \text{Alice} & \text{Bob} & \text{Carol} \\
\text{Second} & \text{Bob} & \text{Carol} & \text{Alice} \\
\text{Third} & \text{Carol} & \text{Alice} & \text{Bob}
\end{array}$$

- Plurality: Alice wins with 40 percent. (Majority criterion: satisfied.)
- Ranked-choice: Bob is eliminated first with 35 percent. Bob's voters have Carol second, but Carol's voters have Alice second. The 25 percent who voted for Carol move to Alice. Alice gets 40 + 25 = 65 percent in round two. Alice wins. (Majority criterion: satisfied.)
- Pairwise comparison: Alice beats Bob 65-35. Alice beats Carol 75-25. Bob beats Carol 75-25. Alice wins 2 matchups. (Condorcet criterion: satisfied. Alice is a Condorcet candidate.)
- Borda count: Alice = 40×2 + 35×0 + 25×1 = 80 + 25 = 105. Bob = 35×2 + 40×0 + 25×0 = 70. Carol = 25×2 + 40×0 + 35×0 = 50. Alice wins. (Majority criterion: satisfied.)

All four methods elect Alice. But imagine that Carol drops out. Then the ballots are:

$$\begin{array}{ccc}
\text{Voters} & 40\% & 35\% & 25\% \\
\text{First} & \text{Alice} & \text{Bob} & \text{Alice}
\end{array}$$

Now Alice has 65 percent on first-place votes. But notice: under pairwise comparison, Bob now beats Alice 60-40. This would reverse the outcome if we had a three-way matchup. The three-candidate Condorcet winner (Alice) is not the same as the two-candidate winner (Bob). This seems unfair. Arrow's theorem says this is unavoidable.

### Common misconceptions

**"Arrow's Impossibility Theorem means democracy is impossible."** No. It means you cannot avoid making trade-offs. Democracies are possible; they just must choose which fairness criteria they value most.

**"Arrow's Impossibility Theorem applies to all voting systems."** It applies to systems where the input is a ranking of candidates and the output is a single winner. Rating systems (where voters give numerical scores rather than rankings) may avoid some of these problems, though new problems emerge.

**"If we just use the 'right' voting method, we can make voting fair."** The theorem says there is no right method—no method that satisfies all fairness criteria. The question is not which method is fair. The question is which fairnesses you value most and which you are willing to sacrifice.

---

## Concept 3 — Apportionment and distributing indivisible resources

Voting asks: Who wins? Apportionment asks: How many winners are there, and how are they divided?

In the United States, the House of Representatives has 435 seats. These seats are distributed to the 50 states based on population. After each census, the apportionment is recalculated. The same problem arises in many contexts: allocating university faculty to departments, distributing school resources among districts, dividing parliamentary seats among political parties.

The problem is this: Population divided by seats almost never gives a whole number. If California has 39,613,000 people and the U.S. has 331,449,281, then California's "fair share" of 435 seats is:

$$\frac{39,613,000}{331,449,281} \times 435 \approx 52.19 \text{ seats}$$

But you cannot give California 52.19 seats. You must give them 52 or 53. The fractional part—0.19—must go somewhere. This is the *apportionment problem*: How do you fairly distribute indivisible things when the math produces fractions?

**The standard divisor and standard quota.** To standardize the problem, we calculate the *standard divisor*, the ratio of total population to total seats:

$$\text{Standard divisor} = \frac{\text{Total population}}{\text{Number of seats}}$$

For the U.S., this is approximately 758,960 people per seat. Each state's *standard quota* is its population divided by the standard divisor. This is the state's "fair share" as a decimal.

**Hamilton's method.** (Also called the Vinton method or method of largest remainders.) Give each state its lower quota (round down). Then, give the remaining seats, one at a time, to the states with the largest fractional parts of their standard quotas.

Example: Five states, 100 seats, populations of 100, 150, 200, 300, 250. Total = 1000. Standard divisor = 10.

$$\begin{array}{cccc}
\text{State} & \text{Population} & \text{Standard Quota} & \text{Lower Quota} \\
A & 100 & 10.0 & 10 \\
B & 150 & 15.0 & 15 \\
C & 200 & 20.0 & 20 \\
D & 300 & 30.0 & 30 \\
E & 250 & 25.0 & 25
\end{array}$$

Sum of lower quotas: 10 + 15 + 20 + 30 + 25 = 100. All fractional parts are 0. No additional seats remain. Hamilton's apportionment is exactly the standard quota.

But fractional parts usually arise. Suppose the populations are 101, 151, 199, 300, 249. Standard divisor = 1000/100 = 10.

$$\begin{array}{cccccc}
\text{State} & \text{Population} & \text{Standard Quota} & \text{Lower Quota} & \text{Fractional} & \text{Final} \\
A & 101 & 10.1 & 10 & 0.10 & 10 \\
B & 151 & 15.1 & 15 & 0.10 & 15 \\
C & 199 & 19.9 & 19 & 0.90 & 20 \\
D & 300 & 30.0 & 30 & 0.00 & 30 \\
E & 249 & 24.9 & 24 & 0.90 & 25
\end{array}$$

Sum of lower quotas: 10 + 15 + 19 + 30 + 24 = 98. Two seats remain. The largest fractional parts are 0.90 (states C and E). They each get one additional seat. C and E go from 19 and 24 to 20 and 25. Hamilton's apportionment: A = 10, B = 15, C = 20, D = 30, E = 25. Total = 100.

**Jefferson, Adams, and Webster methods.** These modify the standard divisor instead of the standard quota. 

Jefferson's method uses a modified divisor *smaller* than the standard divisor, which increases all quotas. Round each modified quota down. The modified divisor is adjusted until the sum of the rounded quotas equals the house size.

Adams's method does the opposite: it uses a modified divisor *larger* than the standard divisor, which decreases quotas. Round each modified quota up (to the ceiling). Adjust until the sum equals the house size.

Webster's method uses traditional rounding: round each modified quota to the nearest integer. The modified divisor is adjusted until the sum of the rounded quotas equals the house size.

The key difference: Hamilton favors neither large nor small states but can produce paradoxes. Jefferson favors large states. Adams favors small states. Webster is balanced but can also produce paradoxes.

### Common misconceptions

**"Apportionment should just be proportional."** It is. The problem is that proportionality produces fractions, and fractions must be converted to whole numbers. There is no unique way to do this.

**"The most accurate method is best."** Accuracy and fairness are different. Accuracy asks: How close are the final quotas to the standard quotas? Fairness asks: Do small states get squashed? Is there a consistent rule? Do paradoxes arise?

**"All apportionment methods give the same answer."** They do not. Jefferson, Adams, and Webster methods can give different answers from Hamilton and from each other.

---

## Concept 4 — Apportionment paradoxes and the second impossibility theorem

Just as Arrow proved that no voting method satisfies all fairness criteria, mathematicians Balinski and Young proved in 1983 that **no apportionment method can simultaneously satisfy all fairness criteria.**

Here are three paradoxes that can occur.

**The Alabama paradox.** In 1880, when the Census Bureau computed apportionments for the U.S. House under different house sizes, they found that Alabama would get 8 seats if the house had 299 seats, but only 7 seats if the house had 300 seats. The house was *growing*, but Alabama's representation *shrank*. This seems absurd: adding seats should help, not hurt.

The Alabama paradox occurs because of the fractional parts. When the house grows from 299 to 300 seats, the standard divisor changes. Alabama's standard quota might grow (from, say, 7.18 to 7.21), but because the fractional parts of *other* states change as well, Alabama might lose in the "battle" for remaining seats.

Hamilton's method is vulnerable to the Alabama paradox. Jefferson, Adams, and Webster methods are not (though all three violate the quota rule in other ways).

**The population paradox.** A state's population grows faster than another state's, yet the fast-growing state loses a seat while the slow-growing state gains one.

Example: State B grows from 613 to 626 (2.12 percent growth) while state C grows from 239 to 242 (1.26 percent growth). Yet C gains a seat from 2 to 3, while B loses one from 7 to 6. This seems backwards. Hamilton's method can produce this.

**The new-states paradox.** A new state is added to the union. To accommodate it, the house size is increased by the number of seats the new state should receive. Yet an existing state loses a seat it previously had, even though its population has not changed.

When Oklahoma became a state in 1907, the House grew from 386 to 391 seats (Oklahoma was allocated 5). Yet when seats were reapportioned under Hamilton's method, New York lost a seat. New York's population had not changed. The only change was the addition of Oklahoma.

All three paradoxes violate basic intuition: adding resources or population should not hurt you. Yet they can occur under standard apportionment methods.

Balinski and Young proved: **No apportionment method can satisfy the quota rule (every state gets either its lower quota or upper quota) and simultaneously avoid all three paradoxes.**

This means: Choose. Hamilton satisfies the quota rule but can produce paradoxes. Jefferson, Adams, and Webster avoid the paradoxes but violate the quota rule—sometimes allocating to a state more or fewer seats than that state's standard quota allows.

### Worked example — comparing apportionment methods

Three states, 51 seats, populations:

$$\begin{array}{cc}
\text{State} & \text{Population} \\
\text{Hawaii} & 201,500 \\
\text{Honolulu} & 974,600 \\
\text{Kalawao} & 100 \\
\text{Kauai} & 72,300 \\
\text{Maui} & 167,400
\end{array}$$

Total population: 1,415,900. Standard divisor: 1,415,900 / 51 ≈ 27,762.75.

Standard quotas:
- Hawaii: 201,500 / 27,762.75 ≈ 7.26 (lower quota 7, upper quota 8)
- Honolulu: 974,600 / 27,762.75 ≈ 35.10 (lower 35, upper 36)
- Kalawao: 100 / 27,762.75 ≈ 0.004 (lower 0, upper 1)
- Kauai: 72,300 / 27,762.75 ≈ 2.60 (lower 2, upper 3)
- Maui: 167,400 / 27,762.75 ≈ 6.03 (lower 6, upper 7)

Hamilton's method: Start with lower quotas: 7, 35, 0, 2, 6. Sum = 50. One seat remains. The largest fractional part is Kalawao (0.004)? No—Kalawao has 0 as the lower quota, so 0.004 is not a fractional part. The fractional parts from the lower quotas are: 0.26, 0.10, remaining (treat 0 as 1.00 since there is a state), 0.60, 0.03. The largest is Kalawao at 1.00 (any allocation is improvement), then Kauai at 0.60. Give the remaining seat to Kauai. Final: 7, 35, 0, 3, 6. This violates the quota rule for Kalawao (allocated 0, quota 0.004—not between lower and upper).

Actually, most apportionment methods guarantee each state at least 1 seat. If we apply that: Start with 1 seat to each state. Now we have 5 seats allocated and 46 remaining. Standard quota (accounting for the mandatory 1): 201,500 / 27,762.75 ≈ 7.26 → 6 additional seats (since they already have 1). Continue the process.

The details become arithmetic-heavy. The key insight: different methods allocate different numbers. Jefferson might give Honolulu more (favoring large states). Adams might give smaller states more (favoring small states). Webster would balance but still differ from Hamilton.

### Common misconceptions

**"Apportionment paradoxes mean the system is broken."** They mean the system must make trade-offs. You cannot avoid paradoxes without violating the quota rule or another fairness principle.

**"The Alabama paradox is rare and doesn't matter."** It is rare in practice because we do not change the house size often. But it reveals a deep tension: adding resources can hurt some recipients because the divisor changes.

**"If we just switched methods, we'd fix the problem."** Switching to Jefferson avoids the Alabama paradox but makes the system biased toward large states. Switching to Adams eliminates the paradox but biases toward small states. There is no escape.

---

## Integration — a town's three problems solved three ways

Return to the town of 100 voters and three restaurant options. Different voting methods produce different winners. Now add a second problem: the town council has 51 seats, and five districts have populations of 201,500, 974,600, 100, 72,300, and 167,400.

**The voting question:** Which restaurant method reveals fairness?

- Plurality avoids Condorcet candidates winning and is simple, but allows spoilers.
- Ranked-choice prevents some spoilers and guarantees a majority winner, but violates monotonicity.
- Borda elevates compromise candidates, but can ignore strong majorities.
- Pairwise ensures Condorcet candidates win and satisfies head-to-head fairness, but produces ties and fails IIA.
- Approval is simple and prevents vote-splitting, but can degenerate into plurality.

If the town cares most about majority rule and avoiding spoilers, ranked-choice is reasonable. If they care about Condorcet candidates, pairwise comparison is necessary (though ties must be resolved). If they care about simplicity, plurality is pragmatic (though at the cost of accepting spoilers). The choice reflects political values.

**The apportionment question:** How many council seats per district?

- Hamilton respects the quota rule but can produce paradoxes. It is neutral between large and small districts.
- Jefferson produces no paradoxes but favors large districts and violates the quota rule. This might harm the small district (Kalawao) by allocating fewer seats than it deserves.
- Adams avoids paradoxes but favors small districts, potentially overrepresenting Kalawao.
- Webster balances but still violates the quota rule and can produce paradoxes.

If the town cares about strict proportionality, Hamilton. If they fear that adding a new district might cause paradoxes, Jefferson, Adams, or Webster. The choice is political.

**The civic weight accumulates.** By this point, a careful reader sees: Neither voting nor apportionment is a math problem. Both are political choices dressed in mathematics. The math constrains the choices (you cannot have everything), but it does not determine them. Arrow's and Balinski-Young's theorems are not failures of mathematics. They are descriptions of democracy's structure. Democracy is not a system that can be made perfect by choosing the right rules. It is a system in which any set of rules will privilege some groups and principles at the expense of others. The question is not "What is the fair system?" The question is "Which fairnesses does our community value most, and which are we willing to sacrifice?"

---

## Exercises

### Warm-up

**Exercise 11.1** *(LO: apply voting methods).* Five voters rank three candidates A, B, C as follows:

$$\begin{array}{ccccc}
\text{Voter} & 1 & 2 & 3 & 4 & 5 \\
\text{First} & A & B & C & A & B \\
\text{Second} & B & C & A & C & A \\
\text{Third} & C & A & B & B & C
\end{array}$$

(a) Who wins by plurality (most first-place votes)?
(b) Who wins by ranked-choice voting?
(c) Calculate the Borda scores and determine the winner.

**Exercise 11.2** *(LO: fairness criteria).* In Exercise 11.1, does the plurality winner satisfy the Condorcet criterion? Construct a pairwise comparison and check.

**Exercise 11.3** *(LO: apportionment).* Three states have populations 1000, 1500, 2500. There are 20 seats to apportion. (a) Calculate the standard divisor. (b) Calculate each state's standard quota. (c) Apply Hamilton's method to determine the final apportionment.

### Application

**Exercise 11.4** *(LO: voting methods and trade-offs).* A committee of 20 people votes on four projects: A, B, C, D. Use a voting method (your choice) to determine the winner from this preference distribution:

$$\begin{array}{cccc}
\text{Number of voters} & 8 & 7 & 5 \\
A & 1 & 4 & 2 \\
B & 2 & 1 & 4 \\
C & 3 & 2 & 1 \\
D & 4 & 3 & 3
\end{array}$$

State which method you chose and justify the choice.

**Exercise 11.5** *(LO: apportionment methods and comparison).* Five states have populations of 5000, 7000, 8000, 12,000, 18,000. Apportion 100 seats using both Hamilton's method and Jefferson's method. Compare the results. Which state benefits most from each method?

**Exercise 11.6** *(LO: identify apportionment paradoxes).* A country has three states with populations A = 6, B = 6, C = 2. Apportion 10 seats using Hamilton's method. Then apportion 11 seats. Does the Alabama paradox occur? Explain.

### Synthesis

**Exercise 11.7** *(LO: understand Arrow's theorem).* Explain in your own words: Why does Arrow's Impossibility Theorem imply that there is no neutral voting method? Give an example of a voting method and the fairness criterion it violates.

**Exercise 11.8** *(LO: apply multiple apportionment methods and compare).* A school district must distribute 45 teachers among four schools with enrollments of 400, 600, 800, 1200. (a) Calculate the standard divisor and standard quota for each school. (b) Apply Hamilton's method. (c) Apply Webster's method with an initial divisor of 65. (d) Explain how the methods differ and which schools are advantaged by each.

### Challenge

**Exercise 11.9** *(LO: synthesis across voting and apportionment).* A small country has three regions and must elect 100 representatives to parliament. The regions have populations of 10,000, 15,000, and 25,000. Each region votes by ranked-choice voting to select its local representatives, then these representatives are apportioned to the three regions according to the total population. 

(a) Apportion 100 seats to the three regions using Hamilton's method. 
(b) Suppose Region 1's population grows to 11,000. Reapportion 100 seats. Did Region 1 gain or lose representation? Is this the population paradox?
(c) Suppose the country adds a fourth region with 8,000 people and increases parliament to 105 seats. Reapportion. Does the new-states paradox occur?

**Exercise 11.10** *(LO: open-ended, extension).* Research a real-world election or apportionment that produced a surprising or controversial result (e.g., the 2000 U.S. presidential election, the 1880 Alabama paradox, a recent ranked-choice election). Describe what happened, identify which voting or apportionment method was used, and explain which fairness criterion or paradox was involved. Write 300–400 words.

---

## Chapter summary

You can now do five things you could not do before.

You can apply six different voting methods to election data and understand the trade-offs each makes: plurality is simple but allows spoilers; ranked-choice guarantees a majority but violates monotonicity; Borda favors compromise candidates but ignores strong majorities; pairwise ensures Condorcet candidates win but produces ties; approval is simple but can degenerate.

You can evaluate any voting method against four fairness criteria: majority, Condorcet, monotonicity, and independence of irrelevant alternatives. You understand that Arrow's Impossibility Theorem proves no method satisfies all four.

You can calculate standard divisors and standard quotas and apply four apportionment methods: Hamilton respects the quota rule but produces paradoxes; Jefferson, Adams, and Webster avoid paradoxes but violate the quota rule and bias toward large or small states.

You can identify and construct three apportionment paradoxes: the Alabama paradox (adding seats hurts a state), the population paradox (fast growth doesn't prevent losing seats), and the new-states paradox (adding a state causes an existing state to lose seats).

You understand the Balinski-Young Impossibility Theorem: no apportionment method simultaneously satisfies all fairness criteria.

Most importantly, you see that both voting and apportionment are not technical problems with technical solutions. They are political choices. Every choice privileges some groups and principles over others. Democracy is not a system that can be perfected by finding the right rules. It is a system in which the rules themselves embody values. The choice of voting method, apportionment method, and electoral district boundaries are choices about what kind of representation we want and what trade-offs we accept.

---

## Connections forward

Chapter 12 turns to graph theory and networks. When you apportion seats or design voting districts, you are partitioning a geographic space—a graph. Gerrymandering (intentionally drawing district boundaries to favor one political party) is a graph problem. Mathematicians now use graph algorithms to detect and correct unfair districts, testing thousands of alternate boundaries to see whether the current one is an outlier. The math of elections and representation continues into the structures of geography.

---

## Glossary of terms

**Plurality:** The candidate or option with the most votes (but possibly fewer than a majority).

**Runoff voting:** A second election between the top two candidates when no one wins a majority in the first round.

**Ranked-choice voting (RCV):** Voters rank candidates in order. Rounds of elimination and vote redistribution continue until one candidate reaches a majority.

**Borda count method:** Candidates receive points based on their ranking. The candidate with the most total points wins.

**Pairwise comparison:** Candidates are compared in head-to-head matchups. The candidate who wins the most matchups wins the election.

**Condorcet candidate:** A candidate who beats every other candidate in head-to-head matchups.

**Approval voting:** Voters approve any number of candidates. The candidate approved by the most voters wins.

**Majority criterion:** If one candidate has more than 50% of first-place votes, they should win.

**Condorcet criterion:** If a Condorcet candidate exists, they should win.

**Monotonicity criterion:** Ranking a winning candidate higher should not cause them to lose.

**Independence of irrelevant alternatives (IIA):** Removing a losing candidate should not change the outcome between two other candidates.

**Arrow's Impossibility Theorem:** No voting system based on ranked preferences can satisfy all four fairness criteria.

**Apportionment:** The process of distributing indivisible items (seats, resources) based on population or another measure.

**Standard divisor:** Total population divided by the number of items to apportion. The population per item.

**Standard quota:** A state or district's population divided by the standard divisor. Its "fair share" as a decimal.

**Lower quota:** The standard quota rounded down.

**Upper quota:** The standard quota rounded up.

**Hamilton's method:** Give each state its lower quota. Distribute remaining items to states with the largest fractional parts.

**Jefferson's method:** Use a modified divisor smaller than the standard divisor. Round each quota down. Adjust the divisor until the sum equals the house size.

**Adams's method:** Use a modified divisor larger than the standard divisor. Round each quota up. Adjust until the sum equals the house size.

**Webster's method:** Use a modified divisor. Round each quota to the nearest whole number. Adjust until the sum equals the house size.

**Quota rule:** Every state receives either its lower quota or upper quota (no more, no less).

**Alabama paradox:** Adding seats to the total causes a state to lose seats.

**Population paradox:** A faster-growing state loses seats while a slower-growing state gains or retains.

**New-states paradox:** Adding a new state causes an existing state to lose a seat.

**Balinski-Young Impossibility Theorem:** No apportionment method can simultaneously satisfy the quota rule and avoid all three paradoxes.

---

## What would change my mind

This chapter's reading is that voting and apportionment methods are not technical choices but political ones, and that impossibility theorems constrain all of them. I would revise this if: (1) empirical evidence showed that real-world voting behavior systematically favors one criterion over others, such that a method satisfying that criterion provably produces better outcomes; or (2) a new apportionment method were discovered that avoids all three paradoxes while respecting the quota rule, contradicting Balinski-Young. Neither is likely, but either would require major revision.

## Still puzzling

I do not yet fully understand why ranked-choice voting violates monotonicity while simultaneously eliminating many spoiler effects. The intuition is that changing a candidate's rank changes who gets eliminated in later rounds, which can cascade. But a deeper theory of *when* monotonicity fails (not just *that* it fails) remains unclear to me.

---

Tags: voting, apportionment, democracy, Arrow's theorem, Balinski-Young, fairness, mathematical impossibility, civic stakes, Electoral College, gerrymandering.
