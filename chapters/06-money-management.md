# Chapter 6 — Money Management

## Three Suggested Titles

1. **The Machinery of Interest: From Simple to Compound to Trapped**
2. **What Money Costs — And What It Builds**
3. **Interest Works Both Ways**

---

## TL;DR

Interest is fundamentally the cost of using someone else's money over time. The difference between simple and compound interest is the difference between arithmetic and exponential growth — and understanding which you face is the difference between building wealth and drowning in debt.

---

## Cold Open

You walk into a coffee shop on a Tuesday morning and spend $6 on a latte. You don't think about it; you swipe, you sip, you leave. That $6 comes out of your checking account.

Now suppose you're 25 years old, and suppose you buy that $6 latte every single weekday for the next 40 years until you retire at 65. That's roughly 200 lattes per year, 8,000 lattes total. Cost: $48,000. Out of your checking account, sure, but you'd have noticed that. You'd plan for it.

But here's what you didn't notice: suppose instead you took that $6 every weekday and put it into a savings account earning 3% compound interest annually. Forty years later, that coffee money would have grown to over $100,000. The interest alone—the money the bank paid you—would be more than $50,000. You spent nothing beyond the lattes, yet you built wealth.

Now reverse it. Suppose you put that same $6 per week on a credit card charging 24% annual percentage rate, and you only pay the minimum payment. You don't add anything else to the card. Just $6 a week, 40 years, same rhythm. By the time you retire, you won't have spent $48,000. You'll have spent nearly $200,000, and you'll still owe money. The interest alone will have cost you $150,000. You're worse than broke—you're trapped.

The machinery is the same in both cases: an initial amount, a time horizon, an interest rate. What changes is direction. This chapter teaches you to read the direction and understand the math underneath it. Because the math is not complicated. It is, in fact, simpler than most people think. And once you see it, you cannot unsee it. You will walk past the coffee shop differently. You will look at a credit card offer differently. You will know what questions to ask before you sign anything.

This chapter has real stakes for your life.

### Learning Objectives

By the end of this chapter you will be able to:

- **Distinguish** simple interest from compound interest and explain why the difference matters over time.
- **Calculate** the future value of money earning compound interest, with various compounding frequencies.
- **Understand** the exponential growth curve and recognize when you're riding it upward or falling down it.
- **Compute** loan payments and understand how amortization tables work.
- **Read** a credit card statement and know exactly what you owe and why.
- **Compare** the real cost of borrowing across different loan structures and interest rates.
- **Recognize** predatory lending and the mechanisms that trap people in debt.

### Prerequisites

Arithmetic with decimals. The percent symbol (%). The formula $A = P(1 + r)^t$ (which we will build together; you do not need to memorize it yet). Willingness to follow a calculation all the way through and check your work.

### Why This Chapter Matters

Money is the first place a person meets exponential growth. Compound interest, whether it works for you or against you, is the same exponential mechanism that drives population growth, epidemic spread, radioactive decay, and Moore's law. It is one of the most powerful ideas in mathematics. When it works in your favor—when you save early and let time do the work—you experience one of the most beautiful patterns in mathematics in your own bank account. When it works against you—when you borrow without understanding the rate—you experience one of the harshest. The math is honest. The question is whether you read it before you sign.

---

## Concept 1 — Interest: What It Is and Why It Exists

You have $1,000. I want to borrow it. I ask you to lend it to me for one year. You agree. But why should you? You're giving up the use of that money for a year. If you'd invested it in a savings account, you'd have earned something. If you'd spent it, you'd have had a year of experiences or goods you now forgo. I'm asking you to wait. The payment for waiting is called *interest*, from the Latin *interesse*, which means "to be in between"—the amount that sits between what you lend and what you get back.

Suppose we agree: you'll lend me $1,000, and I'll pay you back $1,050 at the end of the year. The $50 extra is the interest. The $1,000 is called the *principal*, from the Latin for "first" or "original." The $50 is the cost to me of borrowing, and the reward to you for waiting.

How much is $50 on a $1,000 loan? It's 50/1000 = 0.05 = 5%. We call this the *annual percentage rate*, or APR. It is the percent of the principal that gets paid (or charged) per year. The APR is the language every financial instrument speaks: savings accounts, bonds, car loans, mortgages, credit cards. Learn to read the APR and you can compare any two loans in an instant.

### The Trade-Off: APR vs. Duration

An APR tells you the *rate* but not the *cost*. A 5% APR on $1,000 for one year costs $50. On $1,000 for two years, it costs $100 (if the interest is simple—which we'll define in a moment). On $1,000 for ten years, it costs $500. But here's the trade-off: a 5% APR on $100,000 for one year costs $5,000. Same rate, much higher cost. The APR is like a speed limit on a highway. It tells you the rate per unit of time. The *total distance* depends on how long you drive. The *total interest* depends on how much you borrowed and how long you owe it.

### Simple Interest — The Honest Calculation

Let's define *simple interest* carefully. When interest is simple, the interest is calculated only on the principal. It does not earn interest itself.

The formula is straightforward:

$$I = P \times r \times t$$

where:
- $I$ is the interest (in dollars)
- $P$ is the principal (in dollars)
- $r$ is the annual percentage rate, written as a decimal (so 5% becomes 0.05)
- $t$ is the time in years

The total amount owed at the end is:

$$A = P + I = P + (P \times r \times t) = P(1 + rt)$$

Let's work through an example.

### Worked Example — Simple Interest on a Short-Term Loan

You borrow $4,000 from a bank at 5.5% APR for 4 years. How much interest will you pay, and how much will you owe at the end?

*Given:* $P = 4000$, $r = 0.055$, $t = 4$.

*Calculate the interest:*

$$I = P \times r \times t = 4000 \times 0.055 \times 4 = 880$$

You will pay $880 in interest.

*Calculate the total owed:*

$$A = P + I = 4000 + 880 = 4880$$

You will owe $4,880 at the end of 4 years. You borrowed $4,000 and you're paying $880 extra for the privilege of using that money for 4 years.

*Check against intuition:* 5.5% of $4,000 is $220 per year. Over 4 years, that's $880. Matches.

### Common Misconceptions About Simple Interest

**"Simple interest means it's cheap."** No. Simple interest is just an honest way to calculate interest. Whether it's cheap depends on the APR and how long you borrow. 24% simple interest for 5 years is brutal even though the calculation is simple.

**"Simple interest is what credit cards use."** Actually, no—and that's important. Credit cards use compound interest, which we'll meet in the next section. This is a crucial difference.

**"If I borrow more, the interest rate goes up."** No. The APR is fixed in the contract. Borrow more, and the *absolute amount* of interest goes up, but not the rate. The rate is the rate.

---

## Concept 2 — Compound Interest: When Interest Earns Interest

Here is where the machinery changes.

With simple interest, the interest amount never grows. Year after year, the same calculation: $I = P \times r \times t$. With *compound interest*, the interest gets added back to the principal. In the next period, you calculate interest on the new total. Interest earns interest.

This seems like a small change. It is not.

Let's see it in action with a specific example.

### Worked Example — Compound Interest Step by Step

Abena invests $1,000 in a certificate of deposit (CD) at a bank. The CD earns 4% APR, compounded annually. How much will the CD be worth after 3 years?

*Year 1:* The bank calculates interest on the principal: $I = 1000 \times 0.04 \times 1 = 40$. The CD is now worth $1,000 + 40 = 1,040$.

*Year 2:* Now the bank calculates interest on the *new* amount, $1,040$: $I = 1040 \times 0.04 \times 1 = 41.60$. The CD is now worth $1,040 + 41.60 = 1,081.60$.

*Year 3:* Interest on $1,081.60$: $I = 1081.60 \times 0.04 \times 1 = 43.264 \approx 43.26$. The CD is now worth $1,081.60 + 43.26 = 1,124.86$.

After 3 years, the CD is worth $1,124.86.

Now compare: with simple interest, Abena would have earned $1,000 \times 0.04 \times 3 = 120$, for a total of $1,120. With compound interest, she earned $1,124.86. The difference is $4.86. It seems small. It is. But the effect grows with time.

### The Formula for Compound Interest — And What It Means

Calculating compound interest year by year is tedious. There's a formula:

$$A = P\left(1 + \frac{r}{n}\right)^{nt}$$

where:
- $A$ is the amount at the end (in dollars)
- $P$ is the principal
- $r$ is the annual percentage rate as a decimal
- $n$ is the number of times per year the interest compounds (annually $n=1$, monthly $n=12$, daily $n=365$)
- $t$ is the time in years
- The notation $x^y$ means "$x$ raised to the power $y$" or "$x$ multiplied by itself $y$ times"

For Abena's CD:
- $P = 1000$
- $r = 0.04$
- $n = 1$ (compounded annually)
- $t = 3$

$$A = 1000\left(1 + \frac{0.04}{1}\right)^{1 \times 3} = 1000(1.04)^3 = 1000 \times 1.124864 = 1124.86$$

The term $(1.04)^3$ is the key. It means $1.04 \times 1.04 \times 1.04 = 1.124864$. Each year, the amount multiplies by 1.04. That is exponential growth.

### What Compound Interest Does Over Decades

Let's see what happens with a longer timeline. You invest $5,000 at 5% APR compounded annually. How much will it be worth after 30 years?

$$A = 5000\left(1 + 0.05\right)^{30} = 5000(1.05)^{30}$$

Calculate $(1.05)^{30}$: multiply 1.05 by itself 30 times. On a calculator: $(1.05)^{30} \approx 4.3219$. So:

$$A = 5000 \times 4.3219 = 21,609.50$$

You invested $5,000. You got back $21,609.50. The interest alone was $16,609.50—more than three times your original investment. You did nothing except wait. Time did the work. This is the power of compound interest working in your favor.

Now reverse it. You owe $5,000 on a credit card at 24% APR compounded monthly. You make no payments and add nothing new. After 30 years:

$$A = 5000\left(1 + \frac{0.24}{12}\right)^{12 \times 30} = 5000(1.02)^{360}$$

Calculate $(1.02)^{360}$: this is exponential growth over 360 months. The result is approximately $6,881,900. You owe nearly seven million dollars on a $5,000 debt. You did nothing except ignore the bill. Time did the work against you.

(In practice, a credit card company would pursue you before this happened. The point is mathematical: the machine works the same way in both directions. Direction matters.)

### Compounding Frequency

The formula has a subtle piece: the $n$, the number of times per year interest compounds.

A savings account compounded *annually* ($n=1$) calculates interest once per year.

One compounded *monthly* ($n=12$) calculates interest twelve times per year.

One compounded *daily* ($n=365$) calculates interest every day.

The more often interest compounds, the higher the final amount. Here's why: each time interest is added, the next period's interest is calculated on a slightly larger balance. More frequent additions mean more opportunities for interest to earn interest.

To see the effect, suppose you invest $1,000 at 6% APR for 5 years under different compounding regimes:

- Annually: $A = 1000(1.06)^5 = 1338.23$
- Monthly: $A = 1000(1 + 0.06/12)^{60} = 1000(1.005)^{60} = 1348.85$
- Daily: $A = 1000(1 + 0.06/365)^{1825} \approx 1349.83$

The difference between annual and monthly is about $10. Between monthly and daily, about $1. But that's on $1,000. On $1,000,000, the difference between monthly and daily would be $1,000. Banks care about compounding frequency because they manage large amounts. You should care because you want to understand the machinery—and because credit card companies quote APR but compound daily, which is why their effective rate is higher than they initially state.

### Worked Example — Comparing Simple and Compound Over Time

You borrow $10,000 at 8% APR for 5 years.

*Simple interest:* $I = 10000 \times 0.08 \times 5 = 4000$. Total owed: $14,000$.

*Compound interest (annually):* $A = 10000(1.08)^5 = 10000 \times 1.4693 = 14,693$. Total owed: $14,693.

The difference: $693. Over 5 years, that's about $139 per year extra, just because the interest itself earns interest.

### Common Misconceptions About Compound Interest

**"Compound interest is always better than simple interest."** Only if you're the one earning it. If you're the one paying it (as a borrower), compound interest is worse—it costs you more. The direction matters.

**"Compound interest requires you to add money each time."** No. The interest automatically gets added. That's the definition. You do nothing.

**"If two accounts have the same APR, they return the same amount."** Not if they compound at different frequencies. Annual compounding and monthly compounding at the same APR will give different results.

---

## Concept 3 — Loans and Amortization: How You Actually Pay Things Back

In the real world, you don't wait 30 years and then pay. You make monthly payments. A $300,000 mortgage isn't paid back in a lump sum at the end of 30 years; it's paid back in 360 monthly payments. A car loan is the same. A credit card is the same. These are called *amortization* arrangements—from the Latin *amortire*, "to kill," "to extinguish." Each payment "kills" a piece of the debt.

The trick is figuring out how much each payment should be so that the debt is exactly zero on the final payment.

### How Amortization Works — The Machinery

Here's the key insight: each payment goes partly toward *principal* (reducing what you owe) and partly toward *interest* (paying the lender for the time value of money).

Early in the loan, most of the payment goes toward interest. Late in the loan, most goes toward principal. By the end, the debt is zero.

Here's a concrete example.

### Worked Example — A Simple Amortization (Two Payments)

You borrow $10,000 at 8% APR. You will pay it back in two equal annual payments. How much is each payment?

For a loan with compound interest, the payment $M$ that amortizes the principal $P$ over $n$ periods at rate $r$ per period is:

$$M = P \times \frac{r(1+r)^n}{(1+r)^n - 1}$$

This formula is derived from compound interest algebra; you don't need to memorize it. But you do need to understand what it does: it solves for the payment that makes the final balance exactly zero.

For our example: $P = 10000$, $r = 0.08$, $n = 2$.

$$M = 10000 \times \frac{0.08(1.08)^2}{(1.08)^2 - 1} = 10000 \times \frac{0.08 \times 1.1664}{0.1664} = 10000 \times 0.5608 = 5608$$

Each payment is $5,608.

Now let's trace the debt:

*After Payment 1 ($5,608):*
- Interest accrued during year 1: $10000 \times 0.08 = 800$
- Balance before payment: $10000 + 800 = 10800$
- Payment applied: $5,608$
- Remaining balance: $10800 - 5608 = 5192$

*After Payment 2 ($5,608):*
- Interest on remaining balance: $5192 \times 0.08 = 415.36$
- Balance before payment: $5192 + 415.36 = 5607.36$
- Payment applied: $5,608$ (rounding handles the remaining $0.64)
- Remaining balance: $0$

The debt is extinguished. The total paid was $5,608 + 5,608 = 11,216$. The interest total was $11,216 - 10,000 = 1,216$. On a $10,000 loan for 2 years at 8%, you paid 12.16% extra.

### Amortization Tables: Reading Your Loan Statement

When you take out a real loan—a mortgage, a car loan—the lender gives you an *amortization table*. It shows you, for each payment, how much goes to interest, how much goes to principal, and what the balance is afterward.

Here is an abbreviated version of a real mortgage amortization for the first three months and the last three months of a 30-year, $300,000 mortgage at 6.5% APR:

| Month | Payment | Principal | Interest | Balance |
|-------|---------|-----------|----------|---------|
| 1 | $1,896.20 | $359.79 | $1,536.41 | $299,640.21 |
| 2 | $1,896.20 | $361.85 | $1,534.35 | $299,278.36 |
| 3 | $1,896.20 | $363.92 | $1,532.28 | $298,914.44 |
| ... | ... | ... | ... | ... |
| 358 | $1,896.20 | $1,880.53 | $15.67 | $3,790.68 |
| 359 | $1,896.20 | $1,893.08 | $3.12 | $1,897.60 |
| 360 | $1,896.20 | $1,897.60 | ($1.40) | $0 |

Notice: at the beginning, you're paying $1,536 in interest per month and only $360 toward the debt. At the end, you're paying almost all principal and almost no interest. The payment stays constant; the *composition* changes.

Also notice: the total paid is $1,896.20 × 360 = $682,632. You borrowed $300,000 and paid back $682,632. The interest is $382,632—more than the original loan! This is the cost of using that money for 30 years. It is also why paying extra principal early (when you can) saves enormous amounts of interest: each dollar of principal paid early prevents 30 years of interest from being added to future payments.

### A Civic Reality: The Credit Card Trap

A credit card is a loan with a devastating structure.

With a mortgage or car loan, you have a fixed term. You know when it ends. You have a fixed monthly payment. You know what you owe.

With a credit card, you can pay the minimum payment and carry the balance indefinitely. The interest rate is typically 18–25% APR (some are higher). Interest compounds daily. And here is the trap: if you only pay the minimum payment, the interest grows faster than the principal shrinks.

Suppose you carry a $5,000 balance at 24% APR on a credit card. The minimum payment is typically 2–3% of the balance. Let's say 2%. So your first minimum payment is $100.

You pay $100. How much goes to principal? The daily interest on $5,000 at 24% APR is $5000 \times 0.24 / 365 = $3.29 per day. Over 30 days, that's about $99. So of your $100 payment, $99 goes to interest and $1 to principal. You're now owed $4,999. But next month, the interest is nearly the same: $99.80. And again, most of your $99.80 minimum payment goes to interest.

The math is brutal. If you make only minimum payments on a $5,000 card at 24% APR, it will take you over 30 years to pay it off. You will have paid over $15,000 in interest alone—three times the original debt. And that assumes you never add another charge.

This is not an accident. Credit card companies profit from people who don't understand compound interest. The APR is disclosed; it's not secret. But the effective cost—the time it takes to pay off and the total interest—is not obvious unless you do the math.

This is the moment when this chapter stops being abstract. This is where the math has teeth.

---

## Integration — The Machinery Visible

You now see the same machine three times:

*Simple interest* is the base case: interest on principal, no compounding. Cost is proportional to time. $I = Prt$.

*Compound interest* is what actually happens in the world. Interest on principal, and then interest on that interest. Cost grows *exponentially* with time. $A = P(1 + r/n)^{nt}$.

*Amortization* is the reality: you don't wait for the end. You make periodic payments. Each payment is divided between interest (the cost of time) and principal (the cost of the amount). The monthly payment is fixed, but early on, most of it is interest. Near the end, most is principal. This is why paying extra early saves so much.

The direction matters. When you save, compound interest works for you. When you borrow, it works against you. The APR is the meter; the time is the fuel. The longer you wait, the more the machine runs.

The civic reality: predatory lending exploits people who don't understand this. Credit cards are designed so that minimum payments don't cover the interest. Student loans can have terms so long that graduates pay more in interest than in principal. Payday loans charge APRs so high (often 400%) that a two-week loan costs you a third of the amount borrowed. These are not accidents. These are structures designed to exploit the gap between what the contract says (the APR) and what people understand (how much it will actually cost over time).

Your job is not to become a mathematician. Your job is to look at the APR, the term, and ask: what is the total cost? How much interest will I actually pay? What would happen if I paid extra early? These are not hard questions once you've seen the machinery.

---

## Exercises

### Warm-up

**Exercise 6.1** *(LO: simple interest).* You borrow $8,000 at 6% APR for 3 years using simple interest. How much interest will you pay, and how much will you owe at the end?

**Exercise 6.2** *(LO: APR vs. total cost).* Two different loan offers: Loan A is $10,000 at 5% APR for 5 years (simple interest). Loan B is $10,000 at 7% APR for 3 years (simple interest). Which loan will cost you more in total interest, and by how much?

**Exercise 6.3** *(LO: compound interest formula).* You invest $2,000 at 4% APR, compounded annually, for 10 years. Use the formula $A = P(1+r)^t$ to find how much you will have at the end.

**Exercise 6.4** *(LO: effect of time on compound interest).* You invest $1,000 at 6% APR, compounded annually. How much will you have after (a) 5 years, (b) 10 years, (c) 20 years? What do you notice about how the amount grows?

### Application

**Exercise 6.5** *(LO: comparing simple vs. compound).* You borrow $5,000 at 8% APR for 5 years. (a) Calculate what you would owe with simple interest. (b) Calculate what you would owe with compound interest (compounded annually). (c) How much extra does compound interest cost you?

**Exercise 6.6** *(LO: daily compounding).* A savings account advertises "5% APR compounded daily." You deposit $10,000. After 3 years, how much will you have? Use $n = 365$ in the compound interest formula.

**Exercise 6.7** *(LO: reading an amortization table).* You take out a car loan for $25,000 at 5% APR for 5 years (60 monthly payments of approximately $471.78). The first month, your payment is split as $104.17 in interest and $367.61 in principal. (a) How much of the loan principal have you paid off after the first payment? (b) If you paid an extra $100 toward principal in month 1, how much total interest would you save over the life of the loan? (Hint: that extra $100 would have earned interest for 59 more months.)

### Synthesis

**Exercise 6.8** *(LO: long-term compound interest).* You are 25 years old. You invest $5,000 in a retirement account earning 7% APR, compounded annually. You make no further contributions. You retire at 65 (40 years later). How much will that one $5,000 investment have grown to? What does this tell you about the power of starting early?

**Exercise 6.9** *(LO: the credit card trap).* You have a $3,000 balance on a credit card at 22% APR. The minimum payment is 2% of the balance. (a) What is your first minimum payment? (b) If interest compounds monthly, approximately how much interest accrues in the first month? (c) How much of your first payment goes to principal? (d) If you only ever make minimum payments and never add more charges, why is it mathematically hard to pay off this card?

**Exercise 6.10** *(LO: real-world comparison).* Compare three loans for $20,000: (A) 0% APR for 5 years, (B) 5% APR for 5 years, (C) 8% APR for 7 years. Calculate the total cost of each (principal + interest), and determine which is cheapest and which is most expensive. Explain why the answer might not be what you expected.

### Challenge

**Exercise 6.11** *(LO: open-ended, backward calculation).* You want to retire with $1,000,000. You have 30 years to save. If you can earn 6% APR on your savings compounded annually, how much do you need to invest today (as a single lump sum) to reach that goal? Rearrange the compound interest formula to solve for $P$ instead of $A$.

**Exercise 6.12** *(LO: model predatory lending).* Research the APR on a typical payday loan (often 400% or higher). Calculate what it would cost to borrow $500 for 2 weeks at that rate. Then annualize the cost: what would you owe if you took out a payday loan every 2 weeks for a full year without ever paying down the principal? Write a short paragraph about why people in financial hardship fall into payday loan traps and what you would want them to understand about the math.

---

## Chapter Summary

You now understand three key ideas, each more powerful than it first appears.

*Simple interest* shows you that the cost of borrowing is proportional to how much you borrow and how long you borrow it. The APR is the annual meter; time is the multiplier.

*Compound interest* shows you that time is exponential, not linear. A debt that compounds for decades becomes drastically larger than simple arithmetic suggests. An investment that compounds for decades becomes drastically larger than simple arithmetic suggests. Same machine, opposite direction. This is why starting to save early, even with a small amount, builds wealth that seems impossible until you run the calculation.

*Amortization* shows you that in the real world, you don't wait. You make regular payments. Early payments are mostly interest; late payments are mostly principal. This is why paying extra early saves enormous amounts: you prevent decades of interest from compounding on every dollar of principal you pay down now.

The civic reality is that this machinery is not complicated, but it is exploited. Credit card companies count on people not understanding that a $5,000 balance at 24% will take 30 years and $15,000 to pay off if you make only minimum payments. Payday lenders count on desperation, not stupidity. Student loan structures can be designed so graduates spend decades paying interest. Predatory mortgage lending targets people who don't understand how an APR becomes a real cost.

Your protection is to ask one question before you sign anything that involves borrowing: "What is the total cost, and how long until I'm done?" That question is not rude. That question is not complicated. That question is the difference between understanding what you're agreeing to and discovering it years later when it's too late.

---

## Connections Forward

Chapter 7 (Probability) will use the same exponential growth machinery but apply it to randomness: how likely events accumulate over time, how rare events become less rare when you have many trials, how to read odds and expected value.

Chapter 8 (Statistics) will take data—real numbers collected from the real world—and ask what the data tell us. The civic stakes here are as high as in this chapter: misleading statistics can hide predatory practices, misleading statistics can hide discrimination, misleading statistics can be used to manipulate you. You will learn to read the numbers and ask whether they're telling you truth.

In Chapter 11 (Voting and Apportionment), you will meet another exponential effect: how small biases in a voting system can compound into large distortions of representation. Same machine, different domain.

---

## What Would Change My Mind

If I were shown evidence that credit card companies are structuring minimum payments to accelerate payoff and reduce interest costs, I would revise the chapter's assessment of predatory design. The evidence I'm aware of suggests the opposite, but I'm open to being wrong.

## Still Puzzling

I don't fully understand why financial literacy is not a universal requirement in American schools, given how directly it affects every person's life trajectory. Compound interest is taught in calculus classes but not in high school graduation requirements. That gap seems like a policy failure, not a pedagogical one.

---

## Tags

compound-interest, exponential-growth, APR, amortization, predatory-lending, credit-cards, personal-finance, civic-stakes, financial-literacy
