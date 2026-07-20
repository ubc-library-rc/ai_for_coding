---
layout: default
title: Part 1. Concepts and Context
parent: Workshops
nav_order: 1
---

# Part 1. Concepts and Context

Learning introductory concepts and context for AI-assisted coding.

**Duration:** 30 min

---

## Learning Objectives

By the end of this workshop, you will:

- Have a conceptual understanding of how LLMs work
- Learn how to write clear, intelligible prompts that AI tools respond to best
- Understand the privacy risks inherent in LLMs like Copilot

---

## Behind the Scenes: How LLMs Work

Large language models (LLMs) are trained on massive amounts of public code and documentation. This means they're skilled at recognizing syntax, identifying common programming patterns, and suggesting relevant fixes.

Before getting the most out of AI-assisted coding, it’s important to understand how the underlying models work. LLMs, like those powering Copilot, don't understand language the way humans do. While we read text as **words and meaning**, the model breaks text into **tokens** — small chunks that may be a whole word, part of a word, or even a single character. Tokens are the model's real unit of work: they determine how much it can "remember" at once and how much usage costs.

**Context window:** AI agents can only pay attention to a limited chunk of text at any one time — your current prompt, recent chat history, and whatever code or files you explicitly share. Think of it like a sticky note: if you add too much, older details may fall off and be forgotten. The short, focused prompts we use in this workshop stay well within that limit, so it's just helpful background — something to keep in mind once you move on to larger, real-world projects.

Every time you interact with Copilot or any AI tool, it starts from whatever info you provide *that session*.

**What this means in practice:**

- LLMs learned general coding patterns from huge amounts of **public** code and documentation online.
- Every time you use Copilot, the model works from **what you share** in that moment — not your entire project by default.
- **Better context → better answers.** Vague or missing context → generic or incomplete outputs.

```mermaid
flowchart TD
    A[You write a prompt, describing what you need help with] --> B[Copilot reviews your prompt and recent conversation]
    B --> C{Did you provide enough detail and context?}
    C -- Yes --> D[Copilot gives a helpful answer: code, explanation, or suggested fix tailored to your request]
    C -- No --> E[Copilot provides a generic guess or asks follow-up questions to get more information]
```



---

## The Prompt Formula

The quality of what you get back depends heavily on how you ask. A well-structured prompt gives the model the context it needs to be genuinely useful — instead of a vague guess. When asking for help with code or data, try framing your request around these four parts:

**Context + Task + Constraints + Format**

```
Context: What data or code are you working with?
Task: What do you want to accomplish?
Constraints: Any specific tools, libraries, or limits?
Format: How should the AI present the answer?
```

### Example 1: Vague vs. Clear

**Less helpful:**  

> "Tell me about my research data on penguins."

![Copilot chat responding to the vague prompt "Tell me about my research data on penguins" with a generic answer]({{ '/img/copilot_sample_chat.png' | relative_url }})

*Notice how the prompt answer is vague and general about penguins datasets*

**Much better:**  

> "I have a CSV file with penguins data. How many columns does it have? Show me the column names as a list."

Put the pieces together and you'll get a better response.


### Example 2: Stating Your Tools (Constraints)

> "I have a `penguins.csv` dataset. Using the dplyr package in R, can you calculate the average ... (some metrics of interest)? Show the results as a table."

This example makes your request clear and specific.

| Prompt Component | Sample |
| :--- | :--- |
| **Context** | *"I have a `penguins.csv` dataset..."* |
| **Task** | *"...calculate the average flipper length by species..."* |
| **Constraints** | *"...using the dplyr package in R..."* |
| **Format** | *"...and show the result as a table."* |

```mermaid
flowchart LR
    A[State tool: dplyr in R]
    B[Name data file: penguins.csv]
    C[Define calculation: average flipper length by species]
    D[Request output: table]
    A --> B --> C --> D
```

---

## Data Privacy with LLMs

Data privacy is a major concern when using Large Language Models (LLMs) such as GitHub Copilot or ChatGPT. Anything you input—your code, prompts, or datasets—might be sent to and seen by the tool’s servers. For this reason, throughout this workshop, we are using non-confidential **Palmer Penguins** data for coding and analysis activities in [Part 2](02_set_up_github_copilot.md) and [Part 3](03_explore_prompt_and_build_with_github_copilot.md).

{: .warn}
**Only use [GitHub Copilot](https://github.com/features/copilot) with files that can be made public.** All files in a Copilot *workspace* may be indexed and shared with AI tools, even if you don't enter them into the chat. Never use GitHub Copilot with personal or confidential data.

More detail: [UBC AI guidance](../ubc_ai_policy.html).

---

## Additional Resources

- [UBC AI guidance](../ubc_ai_policy.html)
- [GitHub Copilot Trust Center](https://resources.github.com/copilot-trust-center/)
- [Models and pricing for GitHub Copilot](https://docs.github.com/en/copilot/reference/copilot-billing/models-and-pricing)
- [Palmer Penguins dataset](https://allisonhorst.github.io/palmerpenguins/)

---

**Next:** [Part 2. Set Up GitHub Copilot](02_set_up_github_copilot.md)

