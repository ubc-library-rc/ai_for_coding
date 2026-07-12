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

To get started with these workshops, you don’t need any complicated setup or coding background—just a few basics:

- **A free [GitHub account](https://github.com/signup)**
  
  If you don’t have a GitHub account, go to [github.com/signup](https://github.com/signup) and create one. Be sure to check your email and confirm your account before you start.

- **Access to GitHub Copilot**  
  
  After creating your GitHub account, you may need to enable GitHub Copilot before it can be used in your Codespace. If you don’t see Copilot as an option in your Codespace or editor, go to [github.com/settings/copilot](https://github.com/settings/copilot) and click **Start using Copilot Free**.

- **A modern web browser**  
  Chrome, Edge, Firefox, or Safari all work—no software installation is needed on your computer.


{: .warn}
Only use GitHub Copilot with files that can be made public. All files in a Copilot _workspace_ may be indexed and shared with AI tools, even if you don't enter them into the chat. Never use GitHub Copilot with personal or confidential data. More detail: [UBC AI guidance](ubc_ai_policy.html).

---

## Launch your Codespace

Follow along the slides below

<!-- Interactive step-by-step: Launching your Codespace -->

<div class="reveal">
  <div class="slides">
    <section>
      <h3>Step 1: Open the Repository</h3>
      <img src="../img/p1.png" alt="Open exercises repository" style="max-width:100%; border:1px solid #ccc; border-radius:8px;">
      <p>Go to <a href="https://github.com/ubc-library-rc/ai-for-coding-exercies" target="_blank">github.com/ubc-library-rc/ai-for-coding-exercies</a> and sign in with your GitHub account.</p>
    </section>
    <section>
      <h3>Step 2: Click Code</h3>
      <img src="../img/p2.png" alt="Click the Code button" style="max-width:100%; border:1px solid #ccc; border-radius:8px;">
      <p>Click on the green <b>Code</b> button near the top right of the repository page.</p>
    </section>
    <section>
      <h3>Step 3: Open Codespaces Tab</h3>
      <img src="../img/p3.png" alt="Go to Codespaces tab" style="max-width:100%; border:1px solid #ccc; border-radius:8px;">
      <p>Switch to the <b>Codespaces</b> tab in the menu that appears.</p>
    </section>
    <section>
      <h3>Step 4: Create Codespace</h3>
      <img src="../img/p4.png" alt="Create codespace on main" style="max-width:100%; border:1px solid #ccc; border-radius:8px;">
      <p>Click <b>Create codespace on main</b> to launch a new Codespace.</p>
    </section>
    <section>
      <h3>Step 5: Wait for Setup</h3>
      <img src="../img/p5.png" alt="Codespace setup progress" style="max-width:100%; border:1px solid #ccc; border-radius:8px;">
      <p>Wait a few moments—first time builds may take a minute or two. Your Codespace is ready when it shows "Active".</p>
    </section>
    <section>
      <h3>Step 6: Start Coding!</h3>
      <img src="../img/p6.png" alt="Start coding in Codespaces" style="max-width:100%; border:1px solid #ccc; border-radius:8px;">
      <p>You now have a full coding environment with Python, workshop libraries, and Copilot ready to go—directly in your browser.</p>
    </section>
  </div>
</div>

<!-- 
  This block uses basic reveal.js-style sectioning.
  If you want to fully enable reveal.js interactive features, you'll need to include its JS/CSS in your layout or project-level config.
  Otherwise, readers can scroll through step visuals as a vertical "slideshow".
-->

<style>
.reveal .slides section {
  margin-bottom: 45px;
  padding-bottom: 12px;
  border-bottom: 1px dashed #ddd;
}
.reveal .slides img {
  margin: 22px 0 12px 0;
  background: #f7f7f7;
  box-shadow: 2px 3px 13px #0001;
}
@media (max-width: 900px) {
  .reveal .slides img { max-width: 100%; }
}
</style>

1. Open the exercises repository at **[github.com/ubc-library-rc/ai-for-coding-exercies](https://github.com/ubc-library-rc/ai-for-coding-exercies)** and sign in with your GitHub account.
2. Click the green **`< > Code`** button, then open the **Codespaces** tab.
3. Click **Create codespace on main**.
4. Wait a few minutes while your Codespace builds — first-time builds can be slow. It's ready when the status shows **"Active."**

Your Codespace opens in the browser as a full coding environment. Python, the workshop libraries, and GitHub Copilot are already installed, so there's nothing else to set up.

{: .note}
Your Codespace is given an automatically generated name, so it won't match the examples. To reopen it later, go to [github.com/codespaces](https://github.com/codespaces) and click your Codespace's name.

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

[Part 1: Concepts and Context](workshops/01_concepts_and_context.md)  

[Part 2: Set Up GitHub Copilot](workshops/02_set_up_github_copilot.md)  

[Part 3: Explore, Prompt, and Build with GitHub Copilot](workshops/03_explore_prompt_and_build_with_github_copilot.md)

Workshops build on each other, but you can go at your own pace if you prefer.
