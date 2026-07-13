---
layout: default
title: Part 3. Explore, Prompt, and Build with GitHub Copilot
parent: Workshops
nav_order: 3
---

# Part 3. Explore, Prompt, and Build with GitHub Copilot


**Duration:** 30 min | **Tools:** GitHub Copilot, Jupyter notebook, Python (pandas, matplotlib)

{: .warn}
**Only use [GitHub Copilot](https://github.com/features/copilot) with files that can be made public.** All files in a Copilot _workspace_ may be indexed and shared with AI tools, even if you don't enter them into the chat. Never use GitHub Copilot with personal or confidential data.

More detail: [UBC AI guidance](../ubc_ai_policy.html).

---

## Learning objectives

By the end of this workshop, you will:

- Complete a Jupyter notebook EDA report on Palmer Penguins using step-by-step Copilot prompts
- Apply the prompt formula (Context + Task + Constraints + Format) from [Part 1](01_concepts_and_context.md)
- Use tables and plots to answer what makes penguins heavier—and verify Copilot output yourself

---

## Your research question

Keep one question in mind for every prompt in this workshop:

> **What makes a penguin heavier?**

In the data, we measure this with the **`body_mass_g`** column (body mass in grams). Every step below adds evidence toward your answer.

---

## Open the notebook

In your Codespace (from [Part 2](02_set_up_github_copilot.md)), open:

**`analysies.ipynb` in the exercises repo**

- **Markdown cells** = section goals and your written findings
- **Code cells** = where you paste Copilot-generated code, run it, and check the output

---

## Step 1: Load and inspect

**Goal:** Load `data/penguins.csv`, understand its structure, and list columns that could explain `body_mass_g`.

**Suggested Prompt in Copilot Chat:**

```
Context: I am working in analysies.ipynb with data/penguins.csv.
Research question: "What makes a penguin heavier?"
Task: Load the CSV with pandas. Print row count, column names, data types, and missing values per column.
Also list which columns could help explain body_mass_g.
Constraints: Use pandas only. Keep the code in one cell.
Format: Print readable labels before each output.
```

**What to check before moving on:**

- Does the file path match `data/penguins.csv`?
- Do you see 8 columns and about 344 rows?
- Are species names spelled correctly (Adelie, Chinstrap, Gentoo)?

---

## Step 2: Clean data

**Goal:** Keep rows with complete values for body mass and key predictors; report how many rows you kept.

**Suggested Prompt in Copilot Chat:**

```
Context: Same notebook. Research question: "What makes a penguin heavier?" Use the penguins DataFrame from the previous cell.
Task: Drop rows with missing values in body_mass_g, bill_length_mm, bill_depth_mm, flipper_length_mm, species, sex, island, and year.
Constraints: Use pandas; store the result as penguins_clean.
Format: Print row count before cleaning, after cleaning, and percent retained.
```

**What to check before moving on:**

- Did the row count go down (missing values removed)?
- Are you using `penguins_clean` for the rest of the notebook?

---

## Step 3: Summary tables

**Goal:** Build numeric evidence — average body mass by species and a ranked view of numeric associations.

**Suggested Prompt in Copilot Chat:**

```
Context: Same notebook; use penguins_clean. Research question: "What makes a penguin heavier?"
Task: Create (1) a summary table by species with count and average body_mass_g, and (2) a ranked list of numeric columns correlated with body_mass_g.
Constraints: Use pandas only.
Format: Print both tables with values rounded to one decimal place.
```

**What to check before moving on:**

- Which species has the highest average body mass?
- Which numeric column has the strongest correlation with body mass?
- Do the numbers match what you expect from the data?

Example correlation output (optional):

![Numeric correlation heatmap](../../img/workshop3_heatmap_numeric-correlation-matrix.png)

---

## Step 4: Visualize

**Goal:** Add plots that support your answer — relationship and group comparison.

**Suggested Prompt in Copilot Chat:**
```
Context: Same notebook; use penguins_clean. Research question: "What makes a penguin heavier?"
Use species_colors if helpful (Adelie #4878d0, Chinstrap #ee854a, Gentoo #6acc65).
Task: Create a scatter plot of flipper_length_mm (x) vs body_mass_g (y), colored by species, with title and axis labels.
Then add a box plot of body_mass_g by species.
Constraints: Use matplotlib only.
Format: Show both plots and add a one-line comment on what each plot suggests.
```

**What to check before moving on:**

- Does the scatter plot show a positive trend (longer flippers → heavier penguins)?
- Does the box plot show clear differences between species?
- Do the visuals agree with your summary tables?

Example outputs:

![Scatter: body mass vs flipper length](../../img/workshop3_scatter_body-mass_vs_flipper-length.png)

![Box plot: body mass by species](../../img/workshop3_boxplot_body-mass_by_species.png)

---

## Optional

> "Fit a simple linear regression predicting body_mass_g from flipper_length_mm and bill_length_mm using penguins_clean. Print the coefficients and a one-sentence interpretation."

---

## Key takeaways

1. **One clear question** keeps every Copilot prompt focused
2. **Notebook structure** — load → clean → summarize → visualize → interpret
3. **Copilot drafts; you verify** — check row counts, labels, and whether plots match the tables
4. **Use the prompt formula** — Context + Task + Constraints + Format (from Part 1)

---

## Resources

- [pandas documentation](https://pandas.pydata.org/docs/)
- [Matplotlib documentation](https://matplotlib.org/stable/index.html)
- [UBC AI guidance](../ubc_ai_policy.html)

---

**Previous:** [Part 2. Set Up GitHub Copilot](02_set_up_github_copilot.md)

Congratulations — you built a short, evidence-based EDA report with Copilot from data to conclusion.
