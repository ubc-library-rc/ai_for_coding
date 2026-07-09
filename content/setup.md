---
layout: default
title: Setup
nav_order: 1.3
---

# Setup
{: .no_toc }

These workshops are set up to run **entirely in your browser** using **GitHub Codespaces**, which provides a simple way to incorporate AI into the coding process. You do **not** need to install Python, an editor, or any libraries on your own computer. When you launch your Codespace, Python and libraries (including **pandas** and **matplotlib**) are already installed and ready to go.

We use **Python** in these workshops because it is widely used for data analysis and integrates well with GitHub Copilot. You can write and run Python code alongside AI chat in the same workspace, which is practical for real projects.

The concepts we cover are general and apply to many languages and tools—what you learn throughout the workshop can apply to many environments and tools, and this is just one way of doing things.

Complete this page before the hands-on workshops (Part 2 and 3). We will use **GitHub Copilot** for AI-assisted coding, and **Python** with **pandas** and **matplotlib** to run examples.

---

## What you need
{: .no_toc }

- TOC
{:toc}

To follow along you only need:

- A **free [GitHub account](https://github.com/signup)**
- Access to **GitHub Copilot** (the free tier is enough for this workshop)
- A modern **web browser** (Chrome, Edge, Firefox, or Safari)

{: .warn}
Only use GitHub Copilot with files that can be made public. All files in a Copilot _workspace_ may be indexed and shared with AI tools, even if you don't enter them into the chat. Never use GitHub Copilot with personal or confidential data. More detail: [UBC AI guidance](ubc_ai_policy.html).

---

## Launch your Codespace

Follow along the slides below

<iframe src="https://scribehow.com/embed/How_to_Launch_a_GitHub_Codespace_for_Coding_Exercises__ndrCCbUcQnCtdToUSEweZQ" width="800" height="679" allow="fullscreen" style="aspect-ratio: 1 / 1; border: 0; min-height: 480px"></iframe>

1. Open the exercises repository at **[github.com/ubc-library-rc/ai-for-coding-exercies](https://github.com/ubc-library-rc/ai-for-coding-exercies)** and sign in with your GitHub account.
2. Click the green **`< > Code`** button, then open the **Codespaces** tab.
3. Click **Create codespace on main**.
4. Wait a few minutes while your Codespace builds — first-time builds can be slow. It's ready when the status shows **"Active."**

Your Codespace opens in the browser as a full coding environment. Python, the workshop libraries, and GitHub Copilot are already installed, so there's nothing else to set up.

{: .note}
Your Codespace is given an automatically generated name, so it won't match the examples. To reopen it later, go to [github.com/codespaces](https://github.com/codespaces) and click your Codespace's name.

---

## Check your setup

1. In your Codespace, create a new file named `setup_check.ipynb`.
2. Add a code cell with the code below and run it (click the ▷ Run button next to the cell).

   ```python
   import pandas as pd
   import matplotlib.pyplot as plt
   print("Setup worked!")
   ```

If you see **`Setup worked!`** with no errors, you're ready for the workshops. If prompted to choose a kernel, pick the recommended Python environment.

---

## Palmer Penguins dataset

We'll use the Palmer Penguins dataset throughout the workshop. It's already included in your Codespace at `data/penguins.csv` — no download needed. (If you're working outside a Codespace, you can [download penguins.csv](../data/penguins.csv) and save it in a `data` folder.)

Preview of the data we'll work with:

| species | island | bill_length_mm | bill_depth_mm | flipper_length_mm | body_mass_g | sex | year |
|---------|--------|----------------|---------------|-------------------|-------------|-----|------|
| Adelie | Torgersen | 39.1 | 18.7 | 181 | 3750 | male | 2007 |
| Adelie | Torgersen | 39.5 | 17.4 | 186 | 3800 | female | 2007 |
| Adelie | Torgersen | 40.3 | 18.0 | 195 | 3250 | female | 2007 |
| Chinstrap | Dream | 46.5 | 17.9 | 192 | 3500 | female | 2007 |
| Gentoo | Biscoe | 46.1 | 13.2 | 211 | 4500 | female | 2007 |

**344 rows × 8 columns**

![Palmer Penguins illustrations](../img/lter_penguins.png)

**Source:** [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/)  
**Artwork:** [Illustrations](https://allisonhorst.github.io/palmerpenguins/articles/art.html) by [@allison_horst](https://twitter.com/allison_horst)

---
## Quick start workshops
{: .no_toc }

**Previous:** [Workshop 1: Concepts and Context](workshops/01_fundamentals.md)  
**Next:** [Workshop 2: Data Analysis & Visualization](workshops/02_data_analysis_visualization.md)  
**Then:** [Workshop 3: Explore, Prompt, and Build with GitHub Copilot](workshops/03_building_with_ai.md)

Workshops build on each other, but you can go at your own pace if you prefer.
