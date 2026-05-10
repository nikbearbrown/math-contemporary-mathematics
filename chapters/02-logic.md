# Chapter 2 — Logic

## Cold open

It is 1954 in the United States Supreme Court building in Washington, and a lawyer named Thurgood Marshall is standing up to argue the *Brown v. Board of Education* case. He is not just restating the facts. He is constructing a chain of logical statements: education is important to citizens; separate facilities are not equal facilities; therefore, segregation in schools violates the equal protection of the law.

Fifty years later, a lawyer named Ruth Bader Ginsburg is doing something similar, only now she is arguing that Social Security benefits should not discriminate based on sex. If a man is entitled to survivor benefits, and a woman's situation is identical in every relevant way, then she must be entitled to the same benefits. The logic is relentless.

Neither lawyer was using the word "logic" the way this chapter uses it. But both were doing exactly what logic is: taking claims that can be identified as true or false, arranging them systematically, and showing that a conclusion follows inevitably from the premises. If you believe the premises, you must believe the conclusion. There is no escape.

This chapter teaches you that machinery. Propositions, connectives, truth values, valid arguments. By the end, you will be able to see why some arguments hold and others fall apart. You will be able to construct arguments that cannot be refuted without rejecting one of the premises. That is a tool that matters. In law, in politics, in any conversation where you need to be right and need to be understood.

### Learning objectives

By the end of this chapter you will be able to:

- **Identify** logical statements and distinguish them from non-statements (questions, commands, exclamations).
- **Represent** simple propositions symbolically and **construct** negations of propositions in both words and symbols.
- **Translate** between English and symbolic form for compound statements using AND, OR, and NOT.
- **Construct** truth tables for compound statements and **determine** the validity of statements.
- **Apply** the law of detachment, law of denying the consequent, and chain rule to **determine** whether a logical argument is valid.
- **Identify** logical equivalences (including De Morgan's Laws) and **apply** them to simplify complex statements.

### Prerequisites

Comfort reading and writing English sentences. Willingness to think carefully about what words mean. Arithmetic with true and false (T and F) instead of numbers.

### Why this chapter matters

Chapter 1 taught you to group things into sets using AND, OR, and NOT. This chapter teaches you to group ideas using the same words. The algebra of sets and the algebra of logic are the same algebra, wearing different names. Logic is the infrastructure of law, mathematics, computer science, and every field where a mistake in reasoning has consequences. Every deductive argument — from a legal brief to a math proof to a line of code — is either valid or invalid. This chapter teaches you which is which, and why it matters.

---

## Concept 1 — Propositions, truth values, and negation

You walk into a café and someone hands you a menu. "The daily special is mushroom soup." You read it and understand it. It makes a claim that can be tested: is the soup mushroom, or is it something else? Either it is true or it is false. There is no middle ground.

A **logical statement**, or **proposition**, is a complete sentence that makes a claim decidable as true or false.

"The daily special is mushroom soup" is a statement. Either the menu's claim is right or it is wrong.

"What time does the café close?" is not a statement. It is a question. Questions cannot be true or false; they are requests for information.

"Please order the soup" is not a statement. It is a command. You cannot evaluate it as true or false.

"Tiger Woods won the Master's golf championship at least five times" is a statement, and as of 2021 it is true — he won in 1997, 2001, 2002, 2005, and 2019.

"All roses are red" is a statement, and it is false — there are pink roses, yellow roses, white roses.

### Representing statements symbolically

In logic, we represent statements with lowercase letters. The first statement might be $p$. The next is $q$. The next is $r$. This is shorthand. Instead of writing "Tiger Woods won the Master's five times" every time we reference it, we just write $p$.

Let me show you with a concrete example. Suppose:

$p$ = "It is raining in Boston right now."
$q$ = "The sidewalks are wet."

Both are statements. Both have truth values — they are either true or false. Neither of us can see the sidewalk in Boston, so we cannot determine their truth values right now. But the statements themselves are well-formed. They *have* truth values. We just don't know what they are.

When you use a statement in an argument, you are saying: "I claim this has a truth value. I am not asking whether it is true; I am asserting that it is decidable as true or false."

### Negating statements

If I say "It is raining in Boston," and you disagree, you might say "It is not raining in Boston." You have negated the statement. The **negation** of a statement reverses its truth value. If the original statement is true, the negation is false. If the original statement is false, the negation is true.

In English, we negate by adding or removing the word *not*:

- "Michael Phelps was an Olympic swimmer" negated is "Michael Phelps was not an Olympic swimmer."
- "Emma Stone does not have green eyes" negated is "Emma Stone has green eyes."

In symbolic form, we use a tilde: $\sim$. If $p$ represents a statement, then $\sim p$ (read as "not $p$") represents its negation.

$$p = \text{It is raining in Boston.}$$
$$\sim p = \text{It is not raining in Boston.}$$

If $p$ is true, $\sim p$ is false. If $p$ is false, $\sim p$ is true. The double negation rule says: $\sim(\sim p) = p$. Negating twice gives you back the original.

### Quantified statements and their negations

Some statements use quantifiers — words like *all*, *some*, and *none* that express how many things satisfy a condition.

"All horses are mammals" is a statement. It claims that the set of horses is a subset of the set of mammals.

"Some birds can fly" is a statement. It claims that at least one bird (and possibly many) can fly.

"No penguins are arctic birds" is a statement. It claims that the sets of penguins and arctic birds have no overlap.

The negation of a quantified statement requires care. It is tempting to say: the negation of "All horses are mammals" is "No horses are mammals." But that is wrong. The negation must only break the original claim, not go further.

The negation of "All A are B" is "Some A are not B" — meaning at least one exception exists.

The negation of "Some A are B" is "No A are B" — meaning no exceptions exist.

The negation of "No A are B" is "Some A are B" — meaning at least one overlap exists.

Why? Because the negation of a statement must have the opposite truth value. If I say "All roses are red" (false), the negation is "Some roses are not red" (true). If I say "Some horses are white" (true), the negation is "No horses are white" (false).

### Worked example — negating quantified statements

**Given:** Three statements about birds.

$p$ = "All eagles are birds."
$q$ = "Some penguins can fly."
$r$ = "No ostriches have long beaks."

**Write the negation of each in words and symbolic form.**

For $p$: "All eagles are birds." This is true (eagles are indeed birds). The negation breaks the universal claim: "Some eagles are not birds." Symbolically: $\sim p$.

For $q$: "Some penguins can fly." This is false (penguins cannot fly). The negation flips it: "No penguins can fly." Symbolically: $\sim q$.

For $r$: "No ostriches have long beaks." This is false (ostriches do have long beaks). The negation claims at least one exception: "Some ostriches have long beaks." Symbolically: $\sim r$.

**General lesson:** The negation of a quantified statement reverses the quantifier itself:
- All → Some...not
- Some → None
- None → Some

Memorize this pattern. It will save you from logical errors when you encounter claims like "All people prefer chocolate" and need to construct a counterargument.

### Common misconceptions

**The negation is not always "not" at the end.** "It is not the case that all eagles are birds" is grammatically correct, but it is clunky. The cleaner negation is "Some eagles are not birds." Both are logically equivalent, but clarity wins.

**The negation of "Some A are B" is "No A are B," not "Some A are not B."** The negation must flip the claim entirely, not weaken it. If I claim "Some students passed the exam," the negation is not "Some students did not pass" (which is trivially true on almost every exam). The negation is "No students passed."

**Negation is not the same as disagreement.** If I say "The sky is blue," and you say "The sky is gray," you are contradicting me, but "The sky is gray" is not the negation of "The sky is blue." The negation is "The sky is not blue." Contradiction requires knowledge; negation is just a logical flip.

---

## Concept 2 — Compound statements and truth tables

You are sitting in a café and listening to two conversations. In one corner, someone says: "I like coffee AND I like tea." In another, someone says: "I will have coffee OR I will have tea." These are simple sentences, but they make different claims.

The first uses a conjunction — an AND statement. It claims two things are both true.

The second uses a disjunction — an OR statement. It claims at least one of two things is true (and possibly both).

A **compound statement** joins two or more simple statements using logical connectives. The main connectives are:

- AND (symbol: $\land$) — conjunction. Both statements must be true for the compound to be true.
- OR (symbol: $\lor$) — disjunction. At least one statement must be true for the compound to be true.
- NOT (symbol: $\sim$) — negation. Reverses the truth value.
- IF...THEN (symbol: $\rightarrow$) — conditional. "If $p$, then $q$" is false only when $p$ is true and $q$ is false.

To understand compound statements, we build **truth tables** — systematic tables showing all possible truth values for the components and the overall statement.

### Building a truth table for AND and OR

For a single statement $p$, there are 2 possible truth values: true (T) or false (F).

For two statements $p$ and $q$, there are $2 \times 2 = 4$ possible combinations:

| $p$ | $q$ |
|---|---|
| T | T |
| T | F |
| F | T |
| F | F |

Now add columns for $p \land q$ (the conjunction) and $p \lor q$ (the disjunction):

| $p$ | $q$ | $p \land q$ | $p \lor q$ |
|---|---|---|---|
| T | T | T | T |
| T | F | F | T |
| F | T | F | T |
| F | F | F | F |

**Read the table:**

- Row 1: Both $p$ and $q$ are true. So $p \land q$ is true (both parts of the AND are true). And $p \lor q$ is true (at least one part of the OR is true).
- Row 2: $p$ is true but $q$ is false. So $p \land q$ is false (the AND breaks because one part fails). And $p \lor q$ is true (the OR holds because at least $p$ is true).
- Row 3: $p$ is false but $q$ is true. So $p \land q$ is false. And $p \lor q$ is true.
- Row 4: Both are false. So $p \land q$ is false. And $p \lor q$ is false (neither part of the OR is true).

The key insight: AND is picky. Both parts must be true. OR is forgiving. One true part is enough.

### Worked example — compound statements in context

Let $p$ = "The store opens at 9am" and $q$ = "The store is open on Sundays." You are standing outside at 9am on a Sunday. What can you conclude?

If the premises are both true ($p \land q$), then you can expect the store to be open. The compound statement is true.

If $p$ is true but $q$ is false (the store opens at 9am but not on Sundays), then $p \land q$ is false. The compound statement breaks.

If you just know "The store opens at 9am OR it opens on Sundays," and you arrive at 9am on a Sunday, you know at least one condition is met. The disjunction is true.

**General lesson:** When you encounter a compound claim, identify the connective. AND requires both parts. OR requires one.

### Common misconceptions

**"Or" in logic is inclusive, not exclusive.** In English, "or" sometimes means one or the other but not both (exclusive or): "You can have chocolate or vanilla — pick one." In logic, OR means one or the other or both: the disjunction $p \lor q$ is true when both $p$ and $q$ are true. Logicians are generous.

**AND and OR are not the same, even if the conclusion is the same.** "I have a dog and a cat" and "I have a dog or a cat" make different claims. The first says I have both. The second says I have at least one. If I have both, both statements are true. But they mean different things.

**Truth tables are not opinions.** A truth table is a mechanical tool. It does not depend on context or interpretation. $p \land q$ is false whenever at least one of $p$ or $q$ is false. Always.

---

## Concept 3 — Valid logical arguments

You are listening to a lawyer in court. She says: "If you tampered with the evidence, you are guilty of obstruction. You tampered with the evidence. Therefore, you are guilty of obstruction."

The form of that argument is:
- Premise 1: If $p$, then $q$.
- Premise 2: $p$ is true.
- Conclusion: Therefore, $q$ is true.

This form is called the **law of detachment** (also called *modus ponens*). It is valid. If both premises are true, the conclusion must be true.

Let me show you why. Create a truth table for the conditional $p \rightarrow q$:

| $p$ | $q$ | $p \rightarrow q$ |
|---|---|---|
| T | T | T |
| T | F | F |
| F | T | T |
| F | F | T |

Read this carefully. The conditional is false only in one case: when $p$ is true and $q$ is false. In all other cases, it is true.

Now apply the premises:
- We know $p \rightarrow q$ is true (premise 1).
- We know $p$ is true (premise 2).

Look at the truth table. When is $p \rightarrow q$ true AND $p$ is true? Only in row 1, where $q$ is also true. So the conclusion must be true. The argument is valid.

### Worked example — using the law of detachment

**Given two premises:**
- Premise 1: "If it rains, then the soccer game is cancelled."
- Premise 2: "It is raining."

**Determine the valid conclusion.**

Premise 1 has the form $p \rightarrow q$, where $p$ = "It rains" and $q$ = "The game is cancelled."

Premise 2 says $p$ is true.

By the law of detachment, the conclusion is $q$: "The soccer game is cancelled."

This is valid. If you believe both premises, you must believe the conclusion.

**Contrast:** Suppose premise 2 were "The game is cancelled." Now you know $q$ is true, but you cannot conclude that $p$ is true. The game might be cancelled for other reasons (a lightning strike, a venue malfunction). This argument form is called *affirming the consequent*, and it is invalid. Do not use it.

### De Morgan's Laws — a scale shift

Return to Chapter 1 on sets. We showed that $(A \cup B)' = A' \cap B'$ — the complement of a union is the intersection of the complements. This is a duality, and it appears again here in logic.

The same duality appears in logic. De Morgan's Laws say:

$$\sim(p \land q) \equiv \sim p \lor \sim q$$

Read it: "Not (p and q)" is logically equivalent to "not p or not q."

In plain English: If it is false that both things happened, then at least one of them did not happen. The two phrasings carry the same content; trace through the cases and the equivalence is forced.

The dual:

$$\sim(p \lor q) \equiv \sim p \land \sim q$$

"Not (p or q)" is equivalent to "not p and not q." If neither thing happened, then each thing did not happen.

This is a tool, not a theorem. It lets you rewrite statements to clarify them. If I say "It is not the case that you studied hard and you passed the test," I can rewrite it as "You did not study hard, or you did not pass the test" — which is often clearer.

### Worked example — applying De Morgan

**Given:** "It is not the case that both Alice and Bob showed up."

**Rewrite without the phrase "it is not the case that."**

Let $p$ = "Alice showed up" and $q$ = "Bob showed up."

The given statement is $\sim(p \land q)$.

By De Morgan's Law: $\sim(p \land q) \equiv \sim p \lor \sim q$.

So the equivalent statement is: "Alice did not show up, or Bob did not show up."

This is clearer. You know at least one of them is missing.

### Common misconceptions

**Validity is not the same as truth.** A valid argument can have false premises. Example: "If the Earth is flat, then the Moon orbits the Earth. The Earth is flat. Therefore, the Moon orbits the Earth." The form is valid (law of detachment), but the first premise is false, so the conclusion is unreliable. A **sound** argument is valid and has all true premises.

**Not every argument with the right words is valid.** "If it rains, the game is cancelled. The game is cancelled. Therefore, it rained." This looks like the law of detachment, but it is *affirming the consequent*, an invalid form. The game could be cancelled for other reasons. The premises do not force the conclusion.

**Truth tables are tools for checking validity.** If you want to know whether an argument form is valid, build a truth table. If the final column is all true (a tautology), the form is valid. If there is a false row, the form is not valid.

---

## Integration — the courtroom argument, re-examined

Return to Thurgood Marshall's argument in *Brown v. Board*. His premises were:

1. Education is vital to citizens.
2. Separate facilities are not equal facilities.
3. If separate is not equal, then segregation violates equal protection.
4. Therefore, segregation in schools violates equal protection.

This has the form of the law of detachment applied twice:
- From premises 1 and 2: Segregation means separate facilities.
- From premise 3 and that conclusion: Segregation violates equal protection.

The argument is valid. If you accept the premises, you must accept the conclusion.

But notice something: Marshall's power came not from the logical form alone, but from the premises themselves. Premises 1 and 2 rest on evidence — testimony from educators, statistics on school resources, expert analysis of what "separate" and "equal" mean. Logic makes the chain of reasoning ironclad. Evidence makes the premises credible.

The combination is formidable. A valid argument with true premises is sound. A sound argument, once heard, is hard to refute. You would have to reject one of the premises or deny that the form is valid. In *Brown*, the Supreme Court could not do either.

This is why logic matters in law, in science, in any field where stakes are high. A logically valid argument with credible premises is nearly impossible to attack.

---

## Exercises

### Warm-up

**Exercise 2.1** *(LO: identify statements).* For each of the following, determine whether it is a logical statement. If it is, determine its truth value (true or false) if you can, or state that the truth value cannot be determined.

(a) "The Eiffel Tower is in Paris."
(b) "How old are you?"
(c) "Please sit down."
(d) "All prime numbers are even."

**Exercise 2.2** *(LO: negate statements).* Write the negation of each statement in words and in symbolic form.

(a) $p$ = "The coffee shop is open today." Write $\sim p$.
(b) $q$ = "Some students failed the exam." Write $\sim q$.
(c) $r$ = "No birds have fur." Write $\sim r$.

**Exercise 2.3** *(LO: compound statements).* Let $p$ = "It is raining" and $q$ = "I have an umbrella."

(a) Write $p \land q$ in English.
(b) Write $p \lor q$ in English.
(c) Write $\sim p \land q$ in English.

### Application

**Exercise 2.4** *(LO: truth tables).* Construct a truth table for the statement $p \land \sim q$.

**Exercise 2.5** *(LO: truth tables).* Construct a truth table for the statement $p \lor \sim q$. Is this statement a tautology (always true)? Explain.

**Exercise 2.6** *(LO: logical equivalence).* Show that $p \rightarrow q$ is logically equivalent to $\sim p \lor q$ by constructing a truth table for the biconditional $(p \rightarrow q) \leftrightarrow (\sim p \lor q)$ and confirming the final column is all true.

**Exercise 2.7** *(LO: De Morgan's Laws).* Write each statement using De Morgan's Law, without the phrase "it is not the case that."

(a) "It is not the case that I both study hard and pass the test."
(b) "It is not the case that either the door is locked or the window is locked."

### Synthesis

**Exercise 2.8** *(LO: valid arguments).* For each pair of premises, determine the valid conclusion using the law of detachment, or state that no valid conclusion follows.

(a) Premise 1: "If you finish your homework, you can watch TV." Premise 2: "You finished your homework." Conclusion: ?

(b) Premise 1: "If I study hard, I will pass." Premise 2: "I passed." Conclusion: ? (Is this valid?)

**Exercise 2.9** *(LO: compound statements and validity).* Let $p$ = "The alarm rings," $q$ = "I wake up," and $r$ = "I get to class on time." Translate the following into English and determine whether the argument is valid.

Premise 1: $p \rightarrow q$
Premise 2: $q \rightarrow r$
Conclusion: $p \rightarrow r$

(This is the chain rule. Is it valid?)

**Exercise 2.10** *(LO: converse, inverse, contrapositive).* The statement is: "If all mammals are warm-blooded, then whales are warm-blooded."

(a) Identify the hypothesis $p$ and conclusion $q$.
(b) Write the contrapositive in words.
(c) Is the contrapositive logically equivalent to the original statement?

### Challenge

**Exercise 2.11** *(LO: De Morgan's Laws and negation).* Construct a truth table to verify De Morgan's Law: $\sim(p \land q) \equiv \sim p \lor \sim q$. (Hint: Build columns for $p$, $q$, $\sim p$, $\sim q$, $p \land q$, $\sim(p \land q)$, and $\sim p \lor \sim q$. Then verify that the last two columns are identical.)

**Exercise 2.12** *(LO: complex arguments).* A lawyer is constructing an argument. She says: "If the defendant had opportunity and motive, then the defendant is guilty. The defendant did not have opportunity. Therefore, the defendant is not guilty." Is this argument valid? Construct a truth table to check, or explain using the forms you have learned.

---

## Chapter summary

You can now do five things you probably could not do before.

You can read a sentence and immediately recognize whether it is a logical statement or a question, command, or exclamation. You can negate a statement — not by just adding "not," but by understanding what negation actually does to the truth value.

You can take English sentences joined by "and" or "or," translate them into symbolic form, and build a truth table to see all possible truth combinations. You can read that truth table and say: "In this case the statement is true. In this case it is false."

You can recognize valid argument forms: the law of detachment, the law of denying the consequent, the chain rule. When you see premises in one of these forms, you can confidently draw a conclusion.

You can apply De Morgan's Laws to rewrite statements and make them clearer. Instead of struggling with "it is not the case that both X and Y," you can rephrase it as "not X or not Y."

Most importantly, you can see the skeleton of any logical argument. Every argument is a set of premises joined by logical connectives, leading to a conclusion. If the form is valid and the premises are true, the conclusion is unavoidable. If the form is invalid, you can point to the flaw. That is power.

---

## Connections forward

Chapter 3 turns to numbers. But everything you learned here — how statements combine, how truth works, how a chain of reasoning holds or breaks — applies to mathematics. A proof is a logical argument with mathematical statements. An equation is a conditional: if the setup is true, then this must follow.

Probability, which you will meet in Chapter 7, is also logic dressed in numbers. Every probability statement is a conditional about a universe of possibilities. Chapter 8 on statistics uses the same logical rules to ask: what can we conclude from data?

And voting, apportionment, graph theory — every technical chapter in this book rests on logical reasoning. This chapter is the foundation. Now you have it.

---

## What would change my mind

I would revise this chapter if I found that the central three concepts (propositions, truth tables, valid arguments) do not align with how logic is actually used in the book's later chapters. I am confident they do, but if a deeper scan of Chapters 6, 7, and 11 reveals that deductive arguments are secondary to statistical reasoning or constraint-based optimization, I would reorganize to put the heavier weight on truth tables and logical equivalence as tools for simplifying claims.

## Still puzzling

I remain uncertain whether a liberal-arts audience grasps the distinction between logical validity and soundness without repeated examples and a full worked case. Marshall's courtroom argument in the integration section attempts to make this concrete, but I suspect it will require classroom discussion and perhaps additional examples in the solutions manual.
