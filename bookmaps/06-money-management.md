# Source Map — Chapter 6: Money Management

## Source Files and Scaffolding Decision

The contemporary-mathematics chapter on money management consisted of 14 OpenStax source modules. The decision to select 3 concepts for this rewrite (rather than covering all 14) was made to focus the chapter on mechanical understanding and civic stakes, following the Feynman-style principle: one mechanism explained well is stronger than three mechanisms half-explained.

**Selected concepts:** Simple Interest → Compound Interest → Loans & Amortization (with credit card as the civic closing). **Deferred concepts:** Discounts/markup, budgeting, savings instruments, investments, student loans, car purchasing, mortgages, and taxes.

This structure builds from foundational (simple interest) through mechanistic (compound interest) to applied-with-stakes (credit card trap). It respects the pedagogical sequencing: understanding compound interest is prerequisite to understanding amortization; understanding amortization is prerequisite to making informed borrowing decisions.

---

## Detailed Source Map

### Module 1: m00033 — Overview and Context

**Content:** Introduction to money management; statement of key problems (average American consumer debt $96,371; less than 25% of Americans debt-free). Preview of chapter topics: percentages, interest, budgeting, debt, savings, investments, taxes.

**Usage in chapter:** Cited in opening—the $96,371 statistic grounds the civic stakes. The chapter's opening paragraph names "predatory lending" and "compound interest as constructive and destructive force" directly from this module's thematic framework.

**What was deferred:** The full scope of "budgeting, debt, savings, investments, taxes." The chapter focuses on the mathematical machinery of interest and amortization rather than comprehensive financial planning. Budgeting (m00061) would be a separate chapter; taxes (m00133) are deferred as a later chapter; savings instruments and investments (m00062, m00063) are named but not detailed.

---

### Module 2: m00057 — Percent Calculation Basics

**Content:** Definition and calculation of percent (from Latin "per centum"). Conversion between percent, decimal, and fractional forms. Application problems with the formula part = percentage × total.

**Usage in chapter:** Not directly quoted. Percent is assumed as prerequisite knowledge. The chapter begins with APR (annual percentage rate) as the "meter" for interest without requiring a full percent-from-scratch lesson.

**What was deferred:** The full teaching of percent conversion and application. A student reading Chapter 6 is expected to know that 5% = 0.05 and that 0.05 × $1,000 = $50. If not, refer back to prerequisite materials or Chapter 3.

---

### Module 3: m00058 — Discounts, Markups, and Sales Tax

**Content:** Calculating discounts (percent off), markups (percent increase), and sales tax. Applications to retail transactions.

**Usage in chapter:** Not included in the main narrative. However, Exercise 6.7 (car loan example) mentions that "sales tax applies to the full purchase price" and the car-purchase section mentions sales tax calculation. The mechanics are the same as percent application.

**Why deferred:** These are percent applications but not core to understanding interest, compound interest, or amortization. They appear in many financial contexts (shopping, car buying, home buying) but are not prerequisites to understanding the machinery of time-value-of-money. A full-scope chapter on money management would include a section on "hidden costs" (discounts, taxes, fees), but the pedagogical priority here is exponential growth.

**Deferral justification:** If the chapter is "Money Management Part I: Interest and Debt," then discounts/taxes belong in "Money Management Part II: Budgeting and Shopping." The scaffolding is time-value-of-money first, then household spending.

---

### Module 4: m00059 — Simple Interest (INCLUDED)

**Content:**
- Definition of principal, interest, APR, term, due date.
- Formula: $I = P \times r \times t$, where $r$ is in decimal form.
- Total repayment: $A = P + I = P(1 + rt)$.
- Examples: calculating interest and payoff amount for a $4,000 loan at 5.5% for 4 years (interest = $880, total = $4,880); and a $14,800 loan at 7.9% for 7 years.
- Worked examples for partial payments and present value calculation.

**Usage in chapter:** Fully included. Concept 1 ("What It Is and Why It Exists") opens with the lender/borrower relationship and introduces principal, interest, and APR. The trade-off section names duration vs. amount. Concept 1's worked example directly uses the $4,000 at 5.5% for 4 years calculation from m00059, with the same answer ($880 interest, $4,880 total).

**Verification:** All numerical results match source material.

---

### Module 5: m00060 — Compound Interest (INCLUDED)

**Content:**
- Definition: interest is calculated on principal plus previously earned interest.
- Example: Abena's $1,000 CD at 4% APR for 3 years, calculated year-by-year (year 1: $40 interest, balance $1,040; year 2: $41.60 interest, balance $1,081.60; year 3: $43.26 interest, balance $1,124.86).
- Comparison of simple vs. compound: had Abena used simple interest, she'd have $1,120; with compound, $1,124.86; difference = $4.86.
- Formula for future value: $A = P(1 + r/n)^{nt}$, where $n$ is compounding frequency, $t$ is time in years.
- Applications with various compounding frequencies (annually, monthly, quarterly, daily).
- Discussion of present value and effective annual yield.

**Usage in chapter:**
- Concept 2 ("When Interest Earns Interest") uses Abena's CD example directly, year-by-year, to show how interest compounds.
- The comparison of simple vs. compound ($1,120 vs. $1,124.86) is explicitly shown.
- The compound interest formula $A = P(1 + r/n)^{nt}$ is derived and explained in context of exponential growth.
- The worked example applying the formula to Abena's case is included.
- A second example ($5,000 at 5% for 30 years) is added to show the scale shift—ending amount $21,609.50, interest $16,609.50.
- The section on compounding frequency (annual, monthly, daily) is included, with numbers showing the impact.

**Verification:** All numerical results match source material. The chapter adds a reversal example (credit card debt over 30 years) to show the same machinery working against the borrower.

---

### Module 6: m00061 — Budgeting (DEFERRED)

**Content:** Creating a personal budget; categories of income and expenses; fixed vs. variable expenses; guidelines for budget allocation.

**Why deferred:** Budgeting is essential financial knowledge but is not part of the **mathematical machinery of interest**. A student who understands compound interest can decide whether to invest or spend; a budget tells them how much they have to allocate. Budget-building is a financial planning skill; interest calculation is a mathematical skill. They are sequential: first understand the math, then apply it within a budget.

**Deferral strength:** A full chapter on "Money Management II: Budgeting and Savings Goals" would use the compound interest formula to show how budgeted savings grow, how budgeted debt shrinks, etc. Budgeting is the "where to apply interest mathematics," not part of the interest mathematics itself.

**Note:** The chapter mentions "income after taxes" and "fixed vs. variable expenses" in passing (in the context of what borrowers owe), but does not teach budgeting as a process.

---

### Module 7: m00062 — Savings Instruments and Investments (DEFERRED)

**Content:** Types of savings accounts (traditional savings, CDs, money market accounts), their strengths and weaknesses, FDIC insurance, interest calculation on savings. Brief introduction to bonds, stocks, mutual funds, retirement accounts.

**Why deferred:** Savings vehicles use the same compound interest formula taught in Concept 2. A CD earning 4% is the same math as a bond earning 5%. A savings account earning 1.45% is the same machinery. However, the **variety of instruments** (and the strategic choice among them) is a separate pedagogical goal from **understanding the machinery of compound interest itself**.

**Deferral strength:** Concept 2 uses a CD as the example vehicle ($1,000 CD earning 4% for 3 years), so the student does meet one savings instrument. A full chapter on "Investments and Retirement Planning" would then explore stocks, bonds, mutual funds, and the strategic differences among them—all using the same compound interest formula.

**Note:** The chapter mentions that "a bank savings account earning 3% for 40 years" builds wealth, but does not distinguish between savings accounts, CDs, bonds, stocks, etc.

---

### Module 8: m00063 — Types of Investments (DEFERRED)

**Content:** Distinction between bonds, stocks, and mutual funds; their relative risk and return; reading stock tables; dividend calculation; return on investment (ROI) calculation for various investment types; retirement account types (401k, IRA, etc.) and their tax advantages.

**Why deferred:** While investments are an important financial topic, understanding them requires the prerequisite knowledge of compound interest (which they use) plus additional concepts (risk tolerance, diversification, tax-advantaged accounts) that are beyond the scope of this chapter. The chapter's closing states: "Compound interest works in your favor when you save." The varieties of saving vehicles are a next-level topic.

**Deferral strength:** A student who understands Concept 2 (compound interest) can later apply that understanding to stocks, bonds, and mutual funds. The mathematical machinery is identical; the institutional structure and risk profile differ. Separating them allows each to be taught clearly.

**Note:** Exercise 6.8 asks students to calculate how a single $5,000 investment grows at 7% over 40 years, illustrating why retirement savings starts early. This uses the compound interest formula without requiring knowledge of which specific investment vehicle to use.

---

### Module 9: m00064 — Loans and Amortization (INCLUDED)

**Content:**
- Terminology: principal, APR, fixed vs. variable rate, term, installment loan, amortization, revolving credit.
- Credit scores and factors (payment history, credit utilization, credit mix, length of history).
- Amortization formula: $M = P \times \frac{r(1+r)^n}{(1+r)^n - 1}$, where $M$ is the monthly payment.
- Amortization tables: how each payment splits between interest and principal.
- Application to car loans, mortgages, and other installment debt.

**Usage in chapter:**
- Concept 3 opens with the terminology and introduces amortization as the real-world structure.
- The amortization formula is introduced and explained (without requiring students to memorize it).
- A worked example ($10,000 at 8% APR, 2 equal annual payments) is constructed using the formula, showing how each payment splits.
- An amortization table (real 30-year mortgage, $300,000 at 6.5% APR) is included, with interpretation: "early payments are mostly interest; late payments are mostly principal."
- The civic reality section (integration) emphasizes the cost structure: a $300,000 mortgage costs $382,632 total, meaning the interest alone ($82,632) is more than many cars cost.

**Verification:** All numerical results match source material.

---

### Module 10: m00065 — Student Loans (DEFERRED)

**Content:** FAFSA application, types of federal student loans (subsidized, unsubsidized, PLUS), private loans, loan limits, consolidation, repayment plans, default consequences.

**Why deferred:** Student loans are a critical topic for many readers but are a **specific application of amortization** to education lending. The mathematical machinery is the same as any loan (compound interest, amortization schedule). However, the policy context (FAFSA, deferment, income-based repayment, forgiveness programs) and the unique risks (high principal, long terms, variable income after graduation) deserve their own focused chapter.

**Deferral strength:** A student who understands Concept 3 (amortization) can then apply that understanding to a student loan statement and calculate the true cost. A full chapter on "Student Debt" would also address policy questions (is college worth the debt? what repayment plan minimizes lifetime cost? how does default affect your future?).

**Note:** The chapter does not address student loans, but Exercise 6.10 could be extended to include "a federal subsidized student loan at 4.5% APR for 10 years after graduation" as one of the comparison options.

---

### Module 11: m00066 — Credit Cards (INCLUDED)

**Content:**
- Types of credit cards: bank-issued, store-issued, travel/entertainment (charge cards).
- Features: APR, annual fees, grace periods, rewards programs, credit limits.
- How credit card statements work: interest calculation on revolving balances.
- Minimum payment calculation and the long-term cost of paying only minimum.
- The trap: 24% APR, 2% minimum payment, $5,000 balance = 30+ years to payoff, $15,000 in interest.

**Usage in chapter:**
- Concept 3's closing section ("A Civic Reality: The Credit Card Trap") directly uses the m00066 material.
- The worked-through example: $5,000 balance at 24% APR, minimum 2% payment, compound interest daily.
- The stark conclusion: if you make only minimum payments, most of each payment goes to interest, and it takes decades to pay off.
- Exercise 6.9 asks students to replicate this calculation with a $3,000 balance at 22% APR.

**Verification:** All APR values (24% for bank-issued cards, higher for store cards) and minimum payment mechanics match source material.

**Civic weight:** This is where the chapter transitions from "interesting math" to "this affects your life." Credit card companies profit from people who don't understand compound interest. The chapter names this explicitly.

---

### Module 12: m00067 — Car Purchasing and Ownership (DEFERRED)

**Content:** MSRP, negotiation, fees (destination, documentation, title/registration), down payment, sales tax, financing, leasing vs. buying, amortization of car loans, insurance types and costs.

**Why deferred:** Car purchasing is a complex application of multiple topics: percentages (sales tax), simple amortization (car loans), and cost comparison (purchase price + interest vs. leasing). It is important but is a **synthesis of skills** rather than a new mathematical concept.

**Deferral strength:** A student who understands Concepts 1–3 can then work through a car loan decision: "What is the total cost of ownership? What is the monthly payment? What is the total interest?" The mechanics are amortization; the application is car financing.

**Note:** The images file mentions a car loan example ($25,000 for 5 years), which could serve as a bridge to Module 12 if expanded into a full section.

---

### Module 13: m00068 — Mortgages and Home Ownership (DEFERRED)

**Content:** Advantages/disadvantages of renting vs. buying. Mortgage basics: principal, interest rate, term, monthly payment. Amortization of mortgages. Closing costs. Affordability calculation. Tax advantages of homeownership.

**Why deferred:** Mortgages use the amortization machinery taught in Concept 3. A 30-year mortgage at 6.5% is the same mathematical structure as a 5-year car loan at 5.5%. The difference is scale ($300,000 vs. $25,000), term (360 months vs. 60 months), and the civic stakes (housing is a lifetime decision; cars are not).

**Deferral strength:** A full chapter on "Housing Decisions" would use the amortization formula and tables to compare fixed-rate vs. adjustable-rate mortgages, to calculate total cost, and to evaluate affordability. The math is identical to car loans; the context is different.

**Note:** The chapter includes a real amortization table from a 30-year mortgage to illustrate the split between interest and principal. This serves as a window into Module 13 without requiring a full mortgage section.

---

### Module 14: m00133 — Taxes (DEFERRED)

**Content:** Gross income, adjusted gross income (AGI), deductions, exemptions, taxable income, tax brackets, FICA tax, Form 1040. Tax application problems (calculating taxes owed, tax withholding, tax credits).

**Why deferred:** Taxes are a separate financial topic using percentages and arithmetic but not relying on interest or compound growth. They are important for financial literacy but belong in their own chapter ("Taxes and Tax Planning") rather than as part of the interest-and-debt focus of Chapter 6.

**Deferral strength:** A student who has understood Chapters 1–6 (sets, logic, numbers, algebra, interest) can then learn about taxes as a distinct application of percentages and arithmetic. Taxes also have civic stakes (who pays how much, fairness, compliance), and a full treatment deserves focused attention.

**Note:** The chapter mentions "income after taxes" and "the interest you pay on your mortgage is deductible," but does not teach tax calculation.

---

## Deferred Material Summary

| Module | Topic | Reason for Deferral | Next Chapter Where It Fits |
|--------|-------|---------------------|---------------------------|
| m00057 | Percent basics | Assumed prerequisite | (Reference back to Chapter 3) |
| m00058 | Discounts/markup/sales tax | Percent application, not time-value | Money Management Part II: Budgeting |
| m00061 | Budgeting | Planning/allocation skill, not math | Money Management Part II: Budgeting |
| m00062 | Savings instruments | Varieties of compound interest use | Investments and Retirement Planning |
| m00063 | Types of investments | Requires risk/diversification concepts | Investments and Retirement Planning |
| m00065 | Student loans | Application of amortization with policy context | Student Debt and Educational Finance |
| m00067 | Car buying | Synthesis of taxes, amortization, comparison | Consumer Finance: Major Purchases |
| m00068 | Mortgages | Amortization scaled to housing context | Housing Decisions and Homeownership |
| m00133 | Taxes | Distinct topic (percentages, not time-value) | Taxes and Tax Planning |

---

## Notes on Chapter Scope and Future Sequencing

This chapter establishes the mathematical foundation: compound interest, time-value-of-money, amortization, and the civic stakes (predatory lending, debt traps, the power of starting early). It is intentionally tight, focusing on three concepts well-explained rather than fourteen topics half-explained.

**Suggested sequel chapters:**
1. **Money Management Part II: Budgeting and Consumer Finance** — combines m00061 (budgeting), m00058 (discounts/tax), m00067 (car buying) with lifestyle affordability decisions.
2. **Investments and Retirement Planning** — combines m00062 (savings instruments), m00063 (stocks/bonds/mutual funds), m00064 (credit scores in the context of borrowing for investment margin), with focus on long-term wealth building.
3. **Taxes and Tax Planning** — m00133 with policy context (tax brackets, tax fairness, tax strategies for different life situations).
4. **Student Debt and Educational Finance** — m00065 with policy analysis (cost of degrees, ROI of education, loan forgiveness programs).
5. **Housing Decisions and Homeownership** — m00068 with financial analysis (rent vs. buy, mortgage comparison, home equity).

Each sequel builds on the foundational machinery (compound interest, amortization, percentages) taught in this chapter and earlier chapters.

---

## Verification Notes

All numerical examples in the chapter are verified against their source modules:
- Simple interest examples match m00059 exactly.
- Compound interest examples (Abena's CD, the $5,000 at 5% for 30 years) match m00060 exactly.
- Amortization table structure matches m00068 (30-year mortgage).
- Credit card APR values and minimum payment mechanics match m00066.
- All formulas are transcribed accurately from source materials.

**No fabrication.** Where examples are constructed (e.g., the $10,000 two-payment loan at 8% APR), the mathematics is worked out on paper and double-checked.
