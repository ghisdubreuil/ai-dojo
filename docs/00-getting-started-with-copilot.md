# Getting started with GitHub Copilot (15-minute introduction)

You do not need to know how to code to follow this dojo. You need to know how to **ask clearly** and **check what you get back**. This page covers both.

> The Copilot interface evolves quickly. If a button or mode has a slightly different name on your screen, look for the closest equivalent. The ideas below stay the same.

## 1. What Copilot can do for you
| Capability | What it looks like | Used in this dojo |
|---|---|---|
| **Inline suggestions** | Grey text appears as you type in a file. Press `Tab` to accept, `Esc` to dismiss. | Builder and Expert |
| **Chat** | A conversation panel where you ask questions, request explanations or ask for changes. | All levels |
| **Agents** | You describe a goal; Copilot reads files, edits them, runs commands and iterates. | Expert |

## 2. Open Copilot Chat
1. In your Codespace, click the **chat icon** at the top of the window, or open the Chat view from the sidebar.
2. If you are asked to sign in, use your GitHub account that has Copilot access.
3. Type your message in the box at the bottom and press `Enter`.

Handy extras:
- **Inline chat**: select some text or code in a file and press `Ctrl+I` (Windows/Linux) or `⌘I` (Mac) to ask about that selection only.
- **Slash commands**: type `/` in the chat box to see shortcuts (for example `/plan`).

## 3. Choose the right mode
Use the agent/mode picker in the chat box.

| Mode | What it does | Use it when |
|---|---|---|
| **Ask** | A back-and-forth conversation. It does **not** edit files or run commands. | You want to understand, explore, or draft text. **Start here.** |
| **Plan** | Researches, asks you questions, and proposes a plan. It waits for your approval before acting. | The task is bigger than one step, or you are not sure of the approach. |
| **Agent** | Acts with more autonomy: it edits files, runs commands, fixes its own mistakes. | You know what you want and are ready to review the result. |

Rule of thumb: **Ask → Plan → Agent**. The more power you give it, the more carefully you review.

## 4. Give Copilot the right context
Copilot only knows what it can see. Point it to your material with `#` mentions:

| Type this | To give Copilot |
|---|---|
| `#file:data/sales.csv` | a specific file |
| `#folder:docs/knowledge-base` | a whole folder |
| `#codebase` | the whole project (it searches for what is relevant) |

You can also attach images (screenshots, mockups) to the chat. Always **name the important files explicitly** instead of hoping Copilot picks them up.

## 5. Write a good prompt: GCCF
| Letter | Meaning | Example |
|---|---|---|
| **G**oal | What you want | "Find which store had an unusual sales drop in 2026." |
| **C**ontext | Which files, who is the audience | "Use #file:data/sales.csv and #file:data/stores.csv. I am presenting to the retail director." |
| **C**onstraints | Rules to respect | "Only use the data provided. If you are unsure, say so." |
| **F**ormat | How to answer | "A table of 5 rows, then 3 bullet points." |

Weak: `Analyze the sales.`
Strong: `Using #file:data/sales.csv and #file:data/products.csv, compute net revenue per division per month (quantity × price × (1 − discount)). Show the method, then a table. List any data-quality issue you notice before computing.`

Useful follow-ups: "Explain this step as if I were new to the company", "Shorter", "Why did you choose that rule?", "What could be wrong with this answer?"

## 6. The verification loop (the most important habit)
Copilot is fast and fluent, and **sometimes wrong with confidence**. For every result:
1. **Ask for the method**: "Show me how you computed this."
2. **Cross-check** with a second way: a smaller sample, a manual calculation, another question.
3. **Test the edges**: ask something it cannot know and see whether it admits it or invents.
4. **Review before accepting**: when Copilot edits files, read the changes and use *Keep* or *Undo*.
5. **Own the result**: you are responsible for what you send or publish.

## 7. Make Copilot yours (customization)
Copilot can follow your team's rules automatically. These are plain text files stored in the repository:

| File | Purpose |
|---|---|
| `.github/copilot-instructions.md` | Rules that apply to **every** chat in this project (language, tone, conventions). |
| `.github/prompts/*.prompt.md` | **Reusable prompts** you can run on demand (for example "reply to a customer"). |
| `.github/agents/*.agent.md` | **Custom agents** with a specific role and set of tools. |

This repository already includes a `.github/copilot-instructions.md`. Open it, then ask Copilot a question and notice how the answers follow those rules.

## 8. Safety and good practice
- **Never paste real confidential data** (customer data, contracts, credentials) into a prompt unless your organization explicitly allows it. This dojo uses fictional data only.
- Check your organization's AI usage policy before using Copilot at work.
- Do not accept code or text you cannot explain at a high level. Ask Copilot to explain it.
- Share your best prompts with your colleagues; good prompts are reusable assets.

## 9. If something does not work
| Problem | Try |
|---|---|
| No chat icon / "Copilot not available" | Check you are signed in with the right GitHub account and that your Copilot seat is active. |
| Answers ignore your files | Add them explicitly with `#file:` or `#folder:`. |
| The answer is too long or vague | Add constraints and a format ("5 bullet points, no jargon"). |
| It went in the wrong direction | Start a **new chat** and restate your goal with what you learned. |
| A file was changed badly | Use *Undo* in the chat or the source-control panel to revert. |

## 10. Cheat sheet
- **Ask** to understand · **Plan** to think · **Agent** to do.
- Mention files with `#file:`, folders with `#folder:`.
- Prompt = **Goal + Context + Constraints + Format**.
- Always: **method, cross-check, review**.

Ready? Go to the [warm-up adventure](../Adventures/StartHere.md).
