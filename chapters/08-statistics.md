# Chapter 8 — Statistics

## Three title options

1. **What the Data Actually Shows: Reading numbers in a world of polling, surveys, and NBA contracts**
2. **The Shape of Certainty: How we gather facts, measure them, and make sense of what we find**
3. **Numbers as evidence: From the polling booth to the paycheck, what statistics let us see**

---

## TL;DR

Statistics is the mathematics of learning from data—the practice of collecting it honestly (sampling without bias), understanding what it's telling you (measures of center and spread), and knowing when to trust a pattern versus when to mistrust it (normal distribution and confidence). A single number tells you almost nothing. The story the data tells is in how it's spread out, where the middle really is, and what happens when you compare an individual value to the whole population.

---

## Cold open: The moment the poll arrives

Your phone rings at 6:15 p.m. on a Tuesday. A recorded voice says this is a political opinion survey. Do you answer? If you do, you are now part of data. You answer five questions. Then you hang up.

On the other end, a polling firm collects your response along with 1,499 others. They weight the data—they adjust the numbers so that the respondents roughly match the demographics of the actual voting population. Then they announce: "Our poll shows candidate A leads candidate B 52% to 48%." They publish a margin of error: "plus or minus three percentage points."

What just happened is statistics. You generated data. The polling firm organized it, summarized it, and made a claim: *this is what the population thinks, within these bounds*. The claim is only as good as the data itself. If the 1,500 people who answered are skewed—too many wealthy people, too many urban people, too many morning people who answer their phones—then the summary will lie.

This chapter teaches you how to see whether a claim like that one can be trusted.

### Learning objectives

By the end of this chapter you will be able to:

- **Recognize** sources of bias in data collection and **evaluate** sampling methods.
- **Interpret** measures of center (mean, median, mode) and **choose** the right one for the question you're asking.
- **Calculate** and **understand** measures of spread (range, standard deviation).
- **Apply** the 68-95-99.7 rule to normally distributed data.
- **Compute** percentiles and z-scores to **compare** values across different populations.
- **Read** the story a histogram tells—symmetry, skew, outliers—and **detect** when someone is using a graph to mislead.

### Prerequisites

Arithmetic with whole numbers, decimals, and fractions. Ability to read and create a coordinate plane. Willingness to think about where numbers come from and what they might be hiding.

### Why this chapter matters

Statistics sits between mathematics and the real world. In Chapters 6 and 7, you learned probability—the mathematics of what *should* happen if a process is random and fair. Statistics is what you do when the real world doesn't cooperate with theory. You have actual data. It's messy. It has people in it, or measurements, or votes, or salaries. Your job is to extract the truth without letting the mess (or a dishonest narrator) fool you.

Every time you see "the data shows," a number quoted as fact, a bell curve on a report card, or a margin of error on a poll, you are looking at a statistical claim. This chapter teaches you to ask hard questions of those claims.

---

## Concept 1 — Where does data come from, and why it matters

**Cold open: The night the Literary Digest got it wrong**

October 1936. The Literary Digest, a weekly magazine of enormous prestige, had predicted the outcome of every U.S. presidential election since 1916. Sixteen years without error. The magazine sent surveys to ten million Americans. Two million sent responses back. The Digest tabulated the numbers and made their prediction: Kansas governor Alf Landon would defeat the incumbent Franklin Delano Roosevelt, 57% to 43%.

The election happened. Roosevelt won, 61% to 39%. The Digest's margin of error wasn't a rounding mistake or a statistical hiccup. It was catastrophic—18 percentage points off in one direction.

What went wrong?

The survey reached ten million people. That's an enormous number. Surely with that much data, the result should be reliable. But reliability isn't just about size. It's about who you're asking.

The Digest's sample came from three sources: their own magazine subscribers (wealthy); telephone directories (still only wealthy households in 1936); and auto-registration lists (again, wealthy—most Americans did not own cars). The Digest mailed surveys to people from these lists. About one in four responded. The respondents were systematically richer than the overall population.

The year was 1936, in the depths of the Great Depression. Roosevelt was beloved by the poor and working-class voters. Those voters were not in the Digest's sample. They couldn't afford magazine subscriptions or cars or phones. The sample, though large, was **biased**—skewed toward a group that had reasons to vote differently from the population as a whole.

### Sampling methods and their pitfalls

When you cannot measure an entire population, you must choose a sample. The way you choose that sample decides whether you can trust the result.

A **simple random sample** gives every member of the population an equal chance of being selected. If you have a list of all voters and you use a random number generator to pick 1,500 of them, that's a simple random sample. The Digest did not do this. They selected from lists they happened to have.

A **systematic random sample** is chosen from an ordered list (like voter registration, alphabetical by last name, or every tenth name on a list). You decide what fraction of the population you want to sample—say, 2%, which is 1 in 50. You randomly pick a starting point (between 1 and 50, say you pick 23), then select every 50th name after that (23, 73, 123, ...). This is faster than pure random sampling and works well if the list itself has no pattern. The advantage: easier to implement at scale.

A **stratified sample** divides the population into groups (strata)—age groups, income brackets, regions, political affiliation—then randomly samples within each group. If you're surveying a school with grades 9–12, and you want to know student opinion, you might randomly sample 25 ninth-graders, 25 tenth-graders, 25 eleventh-graders, and 25 twelfth-graders. This guarantees representation from each group. The Digest should have done something like this, stratified by income level. They did not.

A **cluster sample** selects entire clusters at random—say, five city blocks are chosen at random, and every household on those blocks is surveyed. Convenient if the survey must be done in person. Less useful if the clusters themselves are not representative (surveying all households on five blocks in a wealthy neighborhood, when you want to know something about the city, will produce biased data).

The **bias** comes from the method itself. If you stand on a street corner and survey the first five people you see, you're committing what's called a **convenience sample**. It's not random. You're more likely to stop people who look friendly, who have time, who are walking slowly. The result will be biased toward whatever traits correlate with friendliness and leisure.

Non-response is another source of bias. The Digest sent two million surveys. One million came back. Why didn't the other million? Perhaps people who are angry at the government are more likely to respond. Perhaps people with strong political opinions are more likely to care enough to mail a survey back. If responders differ systematically from non-responders, the result is biased, even if the original list was random.

### A worked example — identifying the sampling method

You are a high school principal. You want to know whether students support a new dress code policy. Which sampling method makes sense, and why?

**The question:** Do we use simple random, systematic, stratified, or cluster sampling?

**The reasoning:** You want the result to be trustworthy. A simple random sample from the entire student body would work. You have a list of all students. A random number generator picks 100 of them. You ask each one. Cost is minimal, method is unbiased. That works.

But you might worry: what if ninth-graders feel differently from seniors? You could stratify by grade, randomly sampling 25 ninth-graders, 25 tenth-graders, 25 eleventh-graders, 25 seniors. You now guarantee that each grade is represented. The result is still unbiased, and you have bonus information: which grade supports or opposes the dress code.

A cluster sample would mean: you randomly select five homeroom classes and survey every student in those five classes. This is convenient; you can do it during lunch. But it's risky. If homerooms are assigned by grade or ability level, one random selection might overrepresent students from one grade or with one ability level. The sample could be biased without you knowing it.

A convenience sample—standing at the lunch table and asking whoever sits down—would be the worst choice. You'd systematically miss students who eat somewhere else, skip lunch, or don't speak up in crowds.

**Best choice:** Simple random or stratified random, depending on whether you care about breakdowns by grade.

### Common misconceptions

**"A large sample is always reliable."** The Digest's sample of two million was enormous. It was still biased. Size matters only if the method is unbiased. A small random sample is more trustworthy than a large biased one.

**"If my survey gets responses from 100 people, that's enough."** Enough for what? It depends on the population, the diversity of the population, the margin of error you can tolerate, and whether the method is random. This is a question for another course (sampling design). For now: random method first, then size.

**"Random means I choose however I feel like."** No. Random means every unit has a known, equal probability of being chosen, and the choice is made by a method outside human judgment. You don't get to decide "this person looks representative." A random number generator decides.

---

## Concept 2 — The story in the middle: Measures of center and spread

**Cold open: What does "average" salary mean to you?**

The professional women's basketball player Candace Parker signed a contract with the Chicago Sky in 2021. Her salary: $190,000. The average salary in the WNBA that year was $144,000 per year. By that measure, Parker was above average—well paid, relatively speaking.

But the median WNBA salary that year was much lower: $102,000.

Parker's salary was above the mean but far above the median. Which is the "real" average?

Both. And neither. They measure different things.

The **mean**, also called the arithmetic average, is the sum of all values divided by how many values there are. Compute it, sum everything up, divide by the count:

$$\text{Mean} = \frac{\text{sum of all values}}{n}$$

The **median** is the middle value when data are sorted from smallest to largest. If you line up every WNBA salary from lowest to highest, the median is the salary of the player in the middle. Half the league makes less; half makes more. Half makes less than $102,000.

The **mode** is the value that appears most often. If 50 players on the roster make $90,000 and everyone else makes different amounts, $90,000 is the mode. It's the most common salary.

Each answers a different question.

**When to use the mean:** When you want to know the total and divide it fairly. If the WNBA's total payroll one year was $14 million and the league had 100 players, the mean salary is $140,000. If you wanted to redistribute paychecks equally, everyone would get $140,000. The mean captures the idea of "equal share."

**When to use the median:** When you want to know what a typical player earns. The median is less sensitive to extreme outliers. If one superstar makes $500,000 and the rest make $90,000–$150,000, the median tells you the middle salary (which is the real experience of most players), while the mean gets pulled upward by the superstar's salary.

**When to use the mode:** When you want to know the most common value. If you're a new player and you ask "how much do most WNBA players make," the mode is the answer. It's the value you're most likely to land on if you're randomly assigned a salary.

### A worked example — choosing the right measure of center

You collect test scores from your class: 85, 92, 78, 81, 88, 75, 90, 86, 100, 82.

Compute the mean, median, and mode. Which best represents a "typical" student performance?

**Mean:** Sum: 85 + 92 + 78 + 81 + 88 + 75 + 90 + 86 + 100 + 82 = 857. Count: 10. Mean = 857/10 = 85.7.

**Median:** Sort the data: 75, 78, 81, 82, 85, 86, 88, 90, 92, 100. Since there are 10 values (even), the median is the average of the 5th and 6th values: (85 + 86)/2 = 85.5.

**Mode:** No value appears twice. There is no mode (or we could say all values are modes equally). Not useful here.

**Which is best?** The mean and median are very close (85.7 vs 85.5). The distribution is nearly symmetric. Either measure tells you: a typical student scored in the mid-80s. The mode doesn't exist, so we don't use it. Pick either mean or median; they agree.

### Measures of spread: When the middle isn't enough

Imagine two classes with the same mean test score of 80. In class A, every student scored between 75 and 85. In class B, half scored 100 and half scored 60. The mean is the same. The story is very different.

Class A's students are clustered around the mean. Class B's students are spread out, far from it. Statistics calls this spread **dispersion**. Two measures capture it.

The **range** is the simplest: the difference between the highest and lowest values. Class A's range: 85 − 75 = 10. Class B's range: 100 − 60 = 40. The range tells you how far apart the extremes are. But it only looks at two values, so it can be deceiving. One student who scored unusually high or low inflates it.

The **standard deviation** is the average distance of data points from the mean. It's more complicated to compute, but more honest. The formula is:

$$s = \sqrt{\frac{\sum{(x - \overline{x})}^{2}}{n - 1}}$$

Where $x$ is each data value, $\overline{x}$ (said "x-bar") is the mean, $n$ is the count, and $\Sigma$ means "add these all up."

Here's the process: (1) Compute the mean. (2) Subtract the mean from each value. (3) Square those differences. (4) Add them up. (5) Divide by $n-1$. (6) Take the square root.

Example: Test scores 75, 80, 85 (mean = 80).
- Differences from mean: −5, 0, 5.
- Squared: 25, 0, 25.
- Sum: 50.
- Divide by $n-1 = 2$: 50/2 = 25.
- Square root: $\sqrt{25} = 5$.

Standard deviation is 5. It measures roughly how far a typical score is from 80.

### A worked example — interpreting spread

Two colleges reported mean SAT scores of 1100. College A's standard deviation is 50. College B's is 150. What does this tell you?

**At College A:** Typical students score within 50 points of 1100 (so, between 1050 and 1150). Most are clustered near the mean. It's a selective college; scores are consistent.

**At College B:** Typical students scatter widely around 1100. You might score 950 or 1250. The college admits a more diverse range of students, or there's more variation in student preparation.

If you're a student deciding where to apply, this matters. If you scored 1200, you're above average at both schools, but you're more notably above average at College B. If you scored 900, you're below average at both, but you might have a better shot at College B, since they admit students across a wider range.

### Common misconceptions

**"The mean and median should always be close."** Only if the data are symmetric and roughly bell-shaped. If the data are skewed (bunched on one side with a tail stretching the other way), the mean gets pulled toward the tail and the median stays more central.

**"A low standard deviation means the data are bad."** No. Low standard deviation means the data are tightly clustered around the mean. That's often good—it suggests consistency. High standard deviation might mean there's real diversity in the population, or it might mean you have outliers. You have to look at the data, not just the number.

---

## Concept 3 — The normal distribution: Reading a curve, understanding confidence

**Cold open: The bell curve, and why it's everywhere**

John Kerrich was an English mathematician. In 1940, he was in Denmark on a research visit. Germany invaded. Kerrich was captured and placed in an internment camp for the duration of the war—five years.

He had all the time in the world. He had a coin. He decided to test a theory mathematically: if you flip a fair coin many, many times, the number of heads you get should be normally distributed—that is, the results should form a symmetric, bell-shaped histogram.

While imprisoned, Kerrich flipped a coin 10,000 times and recorded the results. He broke the 10,000 flips into groups of 100 flips, and counted how many heads appeared in each group of 100. Then he made a histogram of the results.

The histogram was bell-shaped. Symmetric. Normal distribution. The mathematics held up. Kerrich had just proved, through sheer tedious action, that a pattern every statistician expected was real.

### The normal distribution in nature

Many measurements in nature produce bell-shaped distributions. Heights of people in a population. Test scores. Birth weights. Circumferences of tree trunks of the same species. Time it takes to run a marathon. The distribution of many repeated measurements, if they're measuring the same underlying thing without systematic error, tends to cluster around the mean, taper off symmetrically on both sides, and form a curve.

This is so common that it has a name: the **normal distribution**. And because it's so common, we have a set of rules—the **68-95-99.7 rule**—that tell us how to interpret any normally distributed dataset, knowing only two numbers: the mean and the standard deviation.

### The 68-95-99.7 rule

If data are normally distributed with mean $\mu$ (mu, Greek for "mean") and standard deviation $s$, then:

- **68%** of the data fall within one standard deviation of the mean. That is, between $\mu - s$ and $\mu + s$.
- **95%** fall within two standard deviations: between $\mu - 2s$ and $\mu + 2s$.
- **99.7%** fall within three standard deviations: between $\mu - 3s$ and $\mu + 3s$.

**Example:** Adult male heights in the United States are normally distributed with mean 70 inches and standard deviation 2.5 inches.

- **68%** of men are between 67.5 inches (70 − 2.5) and 72.5 inches (70 + 2.5) tall.
- **95%** are between 65 inches (70 − 5) and 75 inches (70 + 5) tall.
- **99.7%** are between 62.5 inches (70 − 7.5) and 77.5 inches (70 + 7.5) tall.

This means if you randomly meet an adult male, there's a 68% chance he's between 5'7.5" and 6'0.5". There's a 95% chance he's between 5'5" and 6'3". And there's only a 0.3% chance he's shorter than 5'2.5" or taller than 6'5.5".

### Percentiles and the language of normal distributions

Sometimes it's useful to ask: "What percentage of the population is below a certain value?" That percentage is the **percentile rank**.

If a male is 72 inches tall, what percentile is he at? He's one standard deviation above the mean (70 + 2.5 = 72.5 is one standard deviation; 72 is close). From the 68-95-99.7 rule, 68% of the population is within one standard deviation of the mean. That leaves 32% outside—16% below one standard deviation below the mean, and 16% above one standard deviation above the mean. So someone at exactly one standard deviation above the mean is at about the 84th percentile (50% below the mean + 34% between the mean and one standard deviation above = 84%).

We can use this to compare individuals from different populations.

**Example:** Candace Parker scored 1450 on the SAT. Her friend scored 29 on the ACT. Which is the better score?

The SAT has mean 1060 and standard deviation 195 across test-takers. Parker's score: 1450. How far above the mean is she? $(1450 - 1060) / 195 = 390 / 195 = 2$ standard deviations. So she's at the 97.5th percentile (roughly—the exact value depends on calculation, but 95% are within 2 standard deviations, so she's above the 95th percentile, closer to the 97.5th).

The ACT has mean 21 and standard deviation 5. Her friend's score: 29. How far above the mean? $(29 - 21) / 5 = 8 / 5 = 1.6$ standard deviations. That puts the friend at roughly the 95th percentile.

Parker's SAT score is at a higher percentile. **Parker's score is better**, even though 1450 and 29 are incommensurable numbers from different tests. The normal distribution lets us compare.

### Z-scores: The tool for comparing

A **z-score** quantifies how many standard deviations a value is from the mean:

$$z = \frac{x - \mu}{s}$$

where $x$ is the value, $\mu$ is the mean, and $s$ is the standard deviation.

Parker's z-score on the SAT: $z = (1450 - 1060) / 195 = 2.0$. She scored 2 standard deviations above the mean.

Her friend's z-score on the ACT: $z = (29 - 21) / 5 = 1.6$. The friend scored 1.6 standard deviations above the mean.

A higher z-score means a higher percentile. Parker's z-score of 2.0 beats 1.6. Parker did better relative to her peers.

### A worked example — using the normal distribution to make decisions

Your college gives incoming students a placement test for math. Scores are normally distributed with mean 65 and standard deviation 8. If you score 73, are you placed in the regular calculus section or a remedial pre-calculus section? (The cutoff: students at the 60th percentile or higher go to calculus.)

**Compute your z-score:** $(73 - 65) / 8 = 8 / 8 = 1$ standard deviation above the mean.

**Use the 68-95-99.7 rule:** One standard deviation above the mean puts you at roughly the 84th percentile. (68% are within one standard deviation, so 68%/2 = 34% are between the mean and one standard deviation above. Add the 50% below the mean: 50% + 34% = 84%.)

**Conclusion:** You're at the 84th percentile. You exceed the 60th percentile cutoff. You're placed in calculus.

### Common misconceptions

**"A z-score of 2 means you scored twice as much as someone with a z-score of 1."** No. A z-score measures position relative to the mean, not magnitude. A z-score of 2 means you're twice as far from the mean as someone with a z-score of 1. If the mean is 100 and the standard deviation is 10, then z=1 corresponds to a score of 110, and z=2 corresponds to a score of 120. You didn't score twice as much; you scored 10 points higher.

**"The normal distribution applies to all data."** Many datasets are approximately normal, but not all. Data can be skewed, bimodal, or shaped like something else entirely. Always plot your data before assuming it's normal.

**"99.7% means absolutely everyone fits in three standard deviations."** No. It means 99.7% do. There's always a tail. The remaining 0.3% lies beyond three standard deviations. When you're dealing with millions of people, that 0.3% can be a lot.

---

## Integration: From sampling to confidence

Return to the telephone poll from the opening. A polling firm calls 1,500 people. They find that 52% say they'll vote for candidate A, and 48% say candidate B. The margin of error is reported as ±3 percentage points.

What does that margin of error actually mean?

It means: **if we repeated this survey many times with different random samples of 1,500 people, the true population percentage would fall within 3 percentage points of our sample percentage about 95% of the time.**

This is statistics doing its real job. We cannot survey all 200 million eligible voters. We survey 1,500 (a sample). Our sample mean is 52%. The true population mean is unknown. But if our sampling method is unbiased (truly random, diverse, no non-response bias), the normal distribution tells us something: the sample mean is likely to be close to the true population mean, within a band we can calculate.

The width of that band (the margin of error) depends on three things:

1. **Sample size.** Larger samples produce narrower margins of error. Bigger sample, more confident in the result.

2. **Variability in the population.** If the population is divided 50-50 on an issue, the sample will bounce around more than if it's 90-10. A more divided population requires a larger sample to be precise.

3. **Desired confidence level.** Do you want to be 68% confident? 95% confident? 99.7% confident? Higher confidence requires a wider margin of error. You trade off precision for certainty.

That's where the 68-95-99.7 rule reappears. A margin of error based on the 95% confidence level is the most common. Hence the "±" reporting: "52%, margin of error ±3, 95% confidence."

The polling firm is saying: We're 95% confident that the true population percentage for candidate A is between 49% and 55%.

---

## Exercises

### Warm-up

**Exercise 8.1** *(LO: identify sampling bias.)* You are a polling firm hired by a local newspaper. Which of the following is a method you could use to sample opinion on a proposed school budget?

(a) Call 200 random households from the county voter registration list.
(b) Stand at the grocery store and ask 200 people who walk by.
(c) Send an email to everyone on the school's district email list and ask them to respond.

For each, identify whether it's simple random, systematic, stratified, cluster, or convenience sampling, and explain one source of bias.

**Exercise 8.2** *(LO: choose a measure of center.)* The salaries (in thousands) at a small company are: 30, 32, 31, 29, 28, 31, 32, 35, 34, 95. Compute the mean, median, and mode. Which measure best represents a "typical" employee salary, and why?

**Exercise 8.3** *(LO: interpret standard deviation.)* Two neighborhoods have the same mean home price of $400,000. Neighborhood A has a standard deviation of $30,000. Neighborhood B has a standard deviation of $120,000. What does this tell you about the two neighborhoods?

### Application

**Exercise 8.4** *(LO: apply the 68-95-99.7 rule.)* Test scores in a large university course are normally distributed with mean 75 and standard deviation 8. What percentage of students score between 67 and 83?

**Exercise 8.5** *(LO: compute and interpret z-scores.)* A student scores 1200 on the SAT (mean 1060, standard deviation 195) and 28 on the ACT (mean 21, standard deviation 5). Compute the z-score for each test. Which score is better (higher percentile), and by how much?

**Exercise 8.6** *(LO: interpret margins of error.)* A poll shows 58% of voters support a ballot measure, with a margin of error of ±4 percentage points at 95% confidence. What does this mean? If the true population percentage is 54%, is that consistent with the poll?

### Synthesis

**Exercise 8.7** *(LO: integrate sampling, measures of center, and normal distribution.)* You are launching a new product. You survey 100 random customers: 72% say they'll buy. The standard error (essentially, the margin of error) is 4%. What does this tell you about the true percentage of all customers who will buy? If you run this survey again, will you get exactly 72%? Why or why not?

**Exercise 8.8** *(LO: recognize bias and evaluate data claims.)* A gym claims "users lose an average of 20 pounds in three months." They gathered this statistic by surveying people at the gym who had completed the three-month program. Identify three sources of bias in this data collection. How would you redesign the study to reduce bias?

### Challenge

**Exercise 8.9** *(LO: apply multiple concepts.)* A researcher wants to study the effect of a new teaching method on test scores. She compares two schools: School A uses the new method, School B uses the traditional method. School A's students score mean 82 (SD 10). School B's students score mean 79 (SD 12). Does this prove the new method works? What confounding factors might explain the difference? What would a better study design look like?

**Exercise 8.10** *(LO: open-ended, points forward.)* You notice a news headline: "Study shows chocolate lovers are happier." The study surveyed 500 chocolate lovers and found 73% reported high happiness, compared to 64% of non-chocolate lovers. Critique this study. What sampling bias might exist? What confounding variable might explain the correlation? What would you want to know before believing the headline?

---

## Chapter summary

You can now do three things you probably could not do an hour ago.

You can **recognize where data come from** and whether the method is likely to produce honest results. You understand the Literary Digest failure: a large sample is only as good as the method that created it. Random sampling, stratification, and awareness of non-response bias are your tools.

You can **choose the right measure of center** for the question you're asking. The mean, median, and mode each answer a different question. You understand that the median is robust to outliers while the mean is sensitive to them, and you can use that knowledge to decide which one to quote depending on what story you want to tell (and to recognize when someone else is doing the same).

You can **apply the normal distribution** to data and understand what a standard deviation means. If data are normally distributed, you can instantly estimate what percentage of the population falls in any band around the mean. You can compute z-scores to compare individuals across different populations.

You understand that a **margin of error is not a guess**. It's a statement of confidence built on the normal distribution, the sample size, and the variability of the population. When a poll says 52% ± 3%, they are saying: "We're 95% confident the true percentage is between 49% and 55%."

The thing to watch for, going forward, is **how the data were collected**. A claim is only as good as its source. You have learned to ask: Was the sample biased? Are they comparing apples to oranges? Did they choose a measure of center that inflates their case? Are they hiding the margin of error? These questions are your defense against being fooled.

What you should now be able to teach a friend who asks: Why a random sample matters more than a big sample; when to use the median instead of the mean; what 95% confidence actually means.

---

## Connections forward

In Chapter 7 (Probability), we learned that probability is the mathematics of what *should* happen if a process is random and fair. This chapter is statistics—what *actually* happened when we measured the real world. Probability told us the theory. Statistics measured whether the theory held up.

Later, if you take a course in inference or experimental design, you'll learn to construct confidence intervals (the cousins of margins of error), to test hypotheses (to ask "is this difference real or just random noise?"), and to build models that predict one variable from another. All of those techniques rest on the foundation you've built here: understanding sampling, measures of center and spread, and the normal distribution.

In Chapters 11 and 12, you'll encounter voting methods and graph theory. Statistics appears in both. Elections are predictions—if we sample some voters, can we forecast the outcome? Graphs represent networks of data. Both chapters benefit from the discipline you've learned: how to look at data honestly, to recognize bias, and to understand the limits of what numbers can claim.

For now, the skill is this: when someone says "the data shows," you have questions. You know to ask where the data came from, what it really measures, and whether the person reporting it has a reason to lie.
