---
layout: default
title: Part 2. Set Up GitHub Copilot
parent: Workshops
nav_order: 2
---

# Part 2. Set Up GitHub Copilot

Creating an AI working environment with Copilot

**Duration:** 30 min | **Tools:** GitHub Codespaces, Copilot, R, dplyr, ggplot2

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

### Why all this setup?

We designed this environment so you have a **safe, personal space** to try things out, experiment, and learn by doing. When you **fork** this repository, you get your own private copy—so you can run code, chat with Copilot, and make changes freely, without affecting the original materials.

{: .note}
**GitHub Codespaces** lets you experiment, learn, and explore how your code, data, and AI tools connect—all in one place.

Prior experience with GitHub is *not* required to follow along, but to participate fully you'll need a free GitHub account (see [Setup](../setup.md)). The rest of the series builds on the Codespace environment you set up here.

The concepts we cover are general and apply to many languages and tools—what you learn here carries over to many environments, and this is just one way of putting the pieces together.

## Launch your Codespace

Start by following these steps to create your own copy of the workshop materials and launch them in a browser-based coding environment (codespace), giving you a safe space to experiment and learn hands-on.


<div class="setup-slides">
  <iframe src="{{ '/slides/index.html' | relative_url }}" title="GitHub Copilot: Codespace Setup slides" allowfullscreen></iframe>
</div>

<p><a href="{{ '/slides/index.html' | relative_url }}" target="_blank">Open the setup slides in a new tab &rarr;</a></p>



<style>
.setup-slides {
  position: relative;
  width: 100%;
  padding-top: 56.25%; /* 16:9 aspect ratio */
  margin: 1rem 0;
  border: 1px solid #ccc;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 2px 3px 13px rgba(0, 0, 0, 0.06);
}
.setup-slides iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 0;
}
</style>

Once your Codespace opens in the browser, you'll see a full coding environment ready to use—just like in the screenshot below.

![GitHub Codespace environment: code editor with file tree, terminal, and Copilot chat panel]({{ '/img/github_codespace.png' | relative_url }})


{: .note}
Your Codespace is given an automatically generated name, so it won't match the examples. After you **fork** this repository, you'll have your own copy of the code under your GitHub account—so any changes you make are tracked and saved to your personal repository.

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

## Resources

- [GitHub Codespaces documentation](https://docs.github.com/en/codespaces)
- [GitHub Copilot documentation](https://docs.github.com/en/copilot)
- [Palmer Penguins dataset](https://allisonhorst.github.io/palmerpenguins/)

---

**Previous:** [Part 1. Concepts and Context](01_concepts_and_context.md)  
**Next:** [Part 3. Explore, Prompt, and Build with GitHub Copilot](03_explore_prompt_and_build_with_github_copilot.md)
