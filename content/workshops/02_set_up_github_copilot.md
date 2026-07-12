---
layout: default
title: Part 2. Set Up GitHub Copilot
parent: Workshops
nav_order: 2
---

# Part 2. Set Up GitHub Copilot

Creating AI working environment with Copilot

**Duration:** 30 min | **Tools:** GitHub Codespaces, Copilot, Python, pandas, matplotlib

{: .warn}
**Only use [GitHub Copilot](https://github.com/features/copilot) with files that can be made public.** All files in a Copilot _workspace_ may be indexed and shared with AI tools, even if you don't enter them into the chat. Never use GitHub Copilot with personal or confidential data.

More detail: [UBC AI guidance](../ubc_ai_policy.html).

---

## Learning objectives

By the end of this workshop, you will:

- Launch a GitHub Codespace for the workshop exercises
- Familiarize yourself with GitHub Copilot setup and working environment
- Maintain an active, lead role when engaging with AI tools

---

## Launch your Codespace

Follow the steps below to open the exercises repository in a browser-based coding environment.

<div class="setup-steps">
  <section class="setup-step">
    <h3>Step 1: Open the Repository</h3>
    <img src="{{ '/img/p1.png' | relative_url }}" alt="Open exercises repository">
    <p>Go to <a href="https://github.com/ubc-library-rc/ai-for-coding-exercies" target="_blank">github.com/ubc-library-rc/ai-for-coding-exercies</a> and sign in with your GitHub account.</p>
  </section>
  <section class="setup-step">
    <h3>Step 2: Click Code</h3>
    <img src="{{ '/img/p2.png' | relative_url }}" alt="Click the Code button">
    <p>Click the green <strong>Code</strong> button near the top right of the repository page.</p>
  </section>
  <section class="setup-step">
    <h3>Step 3: Open Codespaces Tab</h3>
    <img src="{{ '/img/p3.png' | relative_url }}" alt="Go to Codespaces tab">
    <p>Switch to the <strong>Codespaces</strong> tab in the menu that appears.</p>
  </section>
  <section class="setup-step">
    <h3>Step 4: Create Codespace</h3>
    <img src="{{ '/img/p4.png' | relative_url }}" alt="Create codespace on main">
    <p>Click <strong>Create codespace on main</strong> to launch a new Codespace.</p>
  </section>
  <section class="setup-step">
    <h3>Step 5: Wait for Setup</h3>
    <img src="{{ '/img/p5.png' | relative_url }}" alt="Codespace setup progress">
    <p>Wait a few moments—first-time builds may take a minute or two. Your Codespace is ready when it shows "Active".</p>
  </section>
  <section class="setup-step">
    <h3>Step 6: Start Coding!</h3>
    <img src="{{ '/img/p6.png' | relative_url }}" alt="Start coding in Codespaces">
    <p>You now have a full coding environment with Python, workshop libraries, and Copilot ready to go—directly in your browser.</p>
  </section>
</div>

<style>
.setup-steps .setup-step {
  margin-bottom: 2rem;
  padding-bottom: 1rem;
  border-bottom: 1px dashed #ddd;
}
.setup-steps .setup-step:last-child {
  border-bottom: none;
  margin-bottom: 0;
}
.setup-steps img {
  display: block;
  max-width: 100%;
  margin: 1rem 0 0.75rem;
  border: 1px solid #ccc;
  border-radius: 8px;
  background: #f7f7f7;
  box-shadow: 2px 3px 13px rgba(0, 0, 0, 0.06);
}
</style>

1. Open the exercises repository at **[github.com/ubc-library-rc/ai-for-coding-exercies](https://github.com/ubc-library-rc/ai-for-coding-exercies)** and sign in with your GitHub account.
2. Click the green **`< > Code`** button, then open the **Codespaces** tab.
3. Click **Create codespace on main**.
4. Wait a few minutes while your Codespace builds — first-time builds can be slow. It's ready when the status shows **"Active."**

Your Codespace opens in the browser as a full coding environment. Python, the workshop libraries, and GitHub Copilot are already installed for you—thanks to a special configuration file called `.devcontainer` that ensures everything is set up automatically. There's nothing else you need to set up!

{: .note}
Your Codespace is given an automatically generated name, so it won't match the examples. To reopen it later, go to [github.com/codespaces](https://github.com/codespaces) and click your Codespace's name.

---

## Palmer Penguins dataset

We'll use the Palmer Penguins dataset throughout the workshop. It's already included in your Codespace at `data/penguins.csv` — no download needed. (If you're working outside a Codespace, you can [download penguins.csv]({{ '/data/penguins.csv' | relative_url }}) and save it in a `data` folder.)

Preview of the data we'll work with:

| species | island | bill_length_mm | bill_depth_mm | flipper_length_mm | body_mass_g | sex | year |
|---------|--------|----------------|---------------|-------------------|-------------|-----|------|
| Adelie | Torgersen | 39.1 | 18.7 | 181 | 3750 | male | 2007 |
| Adelie | Torgersen | 39.5 | 17.4 | 186 | 3800 | female | 2007 |
| Adelie | Torgersen | 40.3 | 18.0 | 195 | 3250 | female | 2007 |
| Chinstrap | Dream | 46.5 | 17.9 | 192 | 3500 | female | 2007 |
| Gentoo | Biscoe | 46.1 | 13.2 | 211 | 4500 | female | 2007 |

**344 rows × 8 columns**

![Palmer Penguins illustrations]({{ '/img/lter_penguins.png' | relative_url }})

**Source:** [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/)  
**Artwork:** [Illustrations](https://allisonhorst.github.io/palmerpenguins/articles/art.html) by [@allison_horst](https://twitter.com/allison_horst)

---

## Explore Copilot in your Codespace

Open Copilot Chat (`Ctrl+Cmd+I` on macOS, or `Ctrl+Alt+I` on Windows/Linux).

We'll focus on **Agent mode** today — it helps you build multi-step workflows quickly. Other modes:

- **Ask:** quick coding questions or short snippets
- **Debug:** help fixing errors
- **Plan:** outline or structure a coding task

Choose **Auto mode** for now. On the free plan, this gets you started quickly while the system handles model selection.

---

## Quick practice: your first Copilot chart

Load the data, then ask Copilot to build a simple bar chart.

```python
import pandas as pd
import matplotlib.pyplot as plt

penguins = pd.read_csv("data/penguins.csv").dropna()

species_colors = {
    "Adelie": "#4878d0",
    "Chinstrap": "#ee854a",
    "Gentoo": "#6acc65",
}
```

**Copilot prompt:**

> "Create a bar chart showing how many penguins are in each species. Use the species_colors dictionary for bar colors. Add count labels on top of each bar."

Expected output:

![Chart 1 bar plot output]({{ '/img/chart1_barplot.png' | relative_url }})

---

## Key Takeaways

- Launch the exercises repo in a **Codespace** — Python, libraries, and Copilot are pre-installed
- The workshop data lives at **`data/penguins.csv`** in your Codespace
- Use **Agent mode** in Copilot Chat for multi-step coding tasks
- Write **clear prompts** with data, task, and output format — better prompts give better code

---

## Resources

- [GitHub Codespaces documentation](https://docs.github.com/en/codespaces)
- [GitHub Copilot documentation](https://docs.github.com/en/copilot)
- [Palmer Penguins dataset](https://allisonhorst.github.io/palmerpenguins/)

---

**Previous:** [Part 1. Concepts and Context](01_concepts_and_context.md)  
**Next:** [Part 3. Explore, Prompt, and Build with GitHub Copilot](03_explore_prompt_and_build_with_github_copilot.md)
