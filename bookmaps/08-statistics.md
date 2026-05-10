# Source map — Chapter 8: Statistics

## Source files (9 modules from OpenStax Contemporary Mathematics)

1. **m00001** — Introduction: Candace Parker salary as hook
2. **m00002** — Sampling and data gathering (sampling techniques, Literary Digest case study, frequency distributions)
3. **m00003** — Data visualization (bar charts, pie charts, stem-and-leaf plots, histograms, misleading graphs)
4. **m00004** — Measures of central tendency (mode, median, mean; when to use each)
5. **m00005** — Measures of dispersion (range, standard deviation)
6. **m00006** — Percentiles and quantiles
7. **m00007** — Normal distribution and 68-95-99.7 rule
8. **m00008** — Z-scores and applications (college entrance exams, coin flipping, analyzing real data)
9. **m00009** — Scatter plots, correlation, and regression

## Concept coverage in rewrite

### Covered — Core three concepts

**Concept 1: Data collection and sampling bias**
- Source: m00002 (sampling methods, Literary Digest case, non-response bias)
- Rewrite: Cold open with Literary Digest 1936 failure; five sampling types (simple random, systematic, stratified, cluster, convenience); sources of bias (selection, non-response, measurement)
- Depth: Sufficient for decision-making; not exhaustive on advanced sampling designs
- Worked example: High school dress code survey; which method to use and why

**Concept 2: Measures of center and spread**
- Source: m00004 (mode, median, mean, when to use each) + m00005 (range, standard deviation)
- Rewrite: WNBA salary case (Parker) to motivate why three measures of center exist; mean (equal share), median (typical), mode (most common); trade-offs between mean and median under skew. Range (simple, limited) vs. standard deviation (comprehensive). Why they matter (deciding between colleges, evaluating consistency).
- Depth: Computational and interpretive; includes full formula for standard deviation but emphasis on understanding, not just rote calculation
- Worked examples: Test scores (mean, median, mode comparison); SAT college comparison (standard deviation effect)

**Concept 3: Normal distribution and confidence**
- Source: m00007 (normal distribution, 68-95-99.7 rule) + m00008 (z-scores, percentiles, applications to test scores, coin flipping) + m00006 (percentiles)
- Rewrite: John Kerrich coin-flipping story as hook; bell-shaped distributions in nature; the 68-95-99.7 rule with heights example; z-scores as standardized comparison tool; integration with percentiles. Application: comparing SAT to ACT scores; understanding margins of error in polling.
- Depth: Computational and applied; includes formula for z-score and percentile-to-z correspondence; explicit connection between percentiles and confidence intervals
- Worked examples: Heights (68-95-99.7), college placement test (z-score decision), SAT vs ACT comparison (z-score application)

### Deferred — Why and what remains

**Visualization (m00003)** — *Deferred, not core to statistical thinking*
- Rationale: Data visualization (bar charts, pie charts, histograms, stem-and-leaf plots) is a design skill, valuable but orthogonal to understanding what data *are* and how to *interpret* them. The chapter acknowledges visualization exists ("graphs can mislead") but does not scaffold building charts step-by-step. A student who understands sampling, measures of center, and normal distribution can learn charting from a tool tutorial. The inverse is not true.
- Retained: Brief mention of "bar chart," "histogram," "stem-and-leaf plot" in context of distribution shape; warning about misleading graphs (scaling, infographics distorting area vs. height); no figures.

**Percentiles detail (m00006)** — *Integrated, not standalone*
- Rationale: Percentiles are most meaningful in the context of the normal distribution. A percentile rank answer the question "what percentage of the population is below this value?" This makes sense when you're comparing individuals to a distribution. The rewrite integrates percentiles into the normal distribution section (e.g., "one standard deviation above the mean is the 84th percentile") rather than treating them as a separate topic.

**Scatter plots and regression (m00009)** — *Deferred, too large for this scope*
- Rationale: Regression is a modeling technique that requires understanding covariance, the concept of "best fit," and interpretation of $r^2$. While the source includes it, the rewrite prioritizes depth on foundational concepts (sampling, center, spread, normal distribution) over breadth. Scatter plots and regression belong in a later chapter or course (linear modeling, multivariate analysis).
- What it would require: Additional Concept 4 section, worked examples with real data (exam scores, salary vs. experience), discussion of causation vs. correlation. Beyond scope of "statistics foundations."

## Source-level notes

### Module m00001 — Introduction
- **Used:** The Candace Parker salary hook, adapted. The source motivates the chapter by asking: how do you estimate the value of a variable (salary) based on others (points per game, rebounds, experience)? Regression is the tool. The rewrite uses it to motivate the question of what "average" salary means (opening to Concept 2).

### Module m00002 — Sampling
- **Used:** Literary Digest case (full narrative preserved), sampling techniques (all five types), non-response bias, definitions of "unit" and "data"
- **Trimmed:** The detailed worked example about auditing tax returns; instead, a simpler high school dress code example
- **Preserved:** George Gallup sidebar context (he did it right, Digest did it wrong; defines quality sampling)

### Module m00003 — Visualization
- **Used:** Only the conceptual point: "a picture is worth a thousand words"; category vs. quantitative data distinction
- **Trimmed:** All step-by-step bar chart construction, pie chart tutorial, stem-and-leaf plot building, histogram tutorial, Google Sheets walkthroughs
- **Warning preserved:** Misleading graphs section (scaling axes, infographics distort area), but no deep dive

### Module m00004 — Measures of center
- **Used:** All three measures (mode, median, mean); definitions and examples; when to use each (the trade-off); worked examples; common misconceptions
- **Preserved:** The logic that mean is pulled by extremes, median is robust, mode is for most common value; the example contrasting datasets with same mean but different spreads (1,2,3,4,5 vs. 1,2,3,4,10)

### Module m00005 — Measures of spread
- **Used:** Range (simple definition and example), standard deviation (full formula, six-step computation, interpretation as "typical distance from mean"), worked examples
- **Interpretation focus:** Not "how to calculate" (technology does that) but "what does the number mean" (college comparison example)

### Module m00006 — Percentiles
- **Used:** Definition, quartile/quintile terminology, connection to median (50th percentile), worked example
- **Trimmed:** The detailed methods for computing percentiles manually vs. with Google Sheets; instead, brief integration: "if you know the mean and standard deviation, you can estimate the percentile"
- **Integration:** Merged into normal distribution section; referenced in z-score section

### Module m00007 — Normal distribution
- **Used:** Everything. The normal distribution is central to the rewrite. The 68-95-99.7 rule, the bell curve, identification of mean and standard deviation from a graph, worked examples, applications, common misconceptions.
- **Preserved:** John Kerrich story (moved to opening of Concept 3 for motivation), the observation that natural phenomena produce bell curves, the careful walk-through of the 68-95-99.7 rule with worked examples

### Module m00008 — Z-scores and applications
- **Used:** Z-score formula and computation, percentile correspondence, college entrance exam example (SAT vs. ACT), coin-flipping (unusual outcomes detection), analysis of real data (Average SAT scores, detecting when a result is unusual)
- **Trimmed:** The detailed Google Sheets walkthroughs; instead, the logic ("use z-scores to compare across distributions") with a worked example (Parker's SAT vs. friend's ACT)

### Module m00009 — Scatter plots and regression
- **Not used in chapter text.** Too large; deferred to future chapter. If included, would require:
  - Definition of response vs. explanatory variable
  - Creation and interpretation of scatter plots
  - Correlation coefficient (r)
  - Regression line (best fit)
  - Predictions from the model
  - Limitations (correlation ≠ causation; curved relationships; outlier effects)

## Pedagogical choices in the rewrite

1. **Scene-based openings.** Each concept opens with a scenario (Literary Digest, WNBA salary, Kerrich's coin flips), not abstract definitions. Reader enters the problem before encountering terminology.

2. **Trade-offs explicit.** When three measures of center exist, the rewrite doesn't just define them; it explains the trade-off: mean (sensitive to extremes, but captures total) vs. median (robust, but doesn't capture distribution spread). This is more useful than "here are three tools."

3. **Integration over isolation.** Percentiles and z-scores are integrated into the normal distribution section because they're tools for the same question: "Where does this person stand relative to the population?" This is more coherent than separate sections.

4. **Civic stakes named.** The Literary Digest section explicitly names why this matters: polling errors can swing elections. The margin of error section names why we need it: we cannot survey all voters, so we must report confidence. This connects the math to the world.

5. **Worked examples use context.** Rather than "Let x = 10, y = 5," examples use WNBA salaries, test scores, college entrance exams, heights—things students recognize. This anchors the math.

6. **Visual details deferred.** The chapter does not teach how to build a histogram or bar chart. It teaches what a histogram tells you (distribution shape) and how to lie with one (manipulate scale). This keeps focus on statistical thinking rather than chart-building technique.

## Validation against source

**Does the rewrite preserve the core of the source?** Yes. All learning objectives from the source modules are addressed:
- Sampling techniques and bias ✓
- Measures of center ✓
- Measures of spread ✓
- Normal distribution and percentiles ✓
- Z-scores and applications ✓
- Reading and interpreting distributions ✓

**What's lost?** Visualization techniques, regression, detailed percentile computation methods, and Google Sheets tutorials. These are real tools, but they are not core statistical reasoning.

**What's gained?** Narrative coherence (three concepts, three scenes), explicit trade-offs, and connection to civic use (polling, testing, hiring). The rewrite trades breadth for depth and clarity.

## Deferred material (for future chapters or courses)

- Data visualization (bar, pie, histogram creation): Chapter 3 material (representation), not statistics proper
- Scatter plots and regression: Multivariate analysis (Chapter 9+)
- Hypothesis testing: Inferential statistics (post-intro course)
- Confidence intervals (advanced): Built on z-scores and normal distribution, but requires more probability background
- Bayesian reasoning: Alternative framework to frequentist; out of scope
- Time-series analysis, ANOVA, non-parametric tests: Advanced statistics

## Source preservation notes

**Figures:** The source includes many figures (histograms, normal curves, z-score tables, scatter plots). The rewrite structure calls for 7 key figures (see images/08-statistics.md). These should be created or adapted from high-quality sources (they are not provided in OpenStax source modules as images; the source notes where they belong but does not include graphics files).

**Worked examples:** The rewrite preserves the structure of worked examples (given, reasoning, answer, check) but changes content to focus on the three core concepts. Number of worked examples per concept: 2 (Concept 1), 2 (Concept 2), 2 (Concept 3). Total: 6 worked examples + 10 exercises.

**Exercises:** The source includes "Check Your Understanding" sections after each module. The rewrite consolidates these into 10 tiered exercises (2 warm-up, 2 application, 2 synthesis, 2 challenge). All test the learning objectives but in a tighter, more coherent set.

---

**Conclusion:** The rewrite is faithful to the source's learning objectives while reshaping the narrative around three core concepts: sampling (honesty in data collection), measures of center and spread (understanding what the middle is), and normal distribution (reading curves, making comparisons). Material on visualization, percentile computation, and regression is deferred to later chapters, not because it's unimportant, but because pedagogical depth requires scope limits. A student who masters this chapter will be equipped to read polls critically, choose the right average for the question, and understand confidence intervals.
