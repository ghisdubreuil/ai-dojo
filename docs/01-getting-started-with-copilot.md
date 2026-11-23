# Getting started with the GitHub Copilot app (15-minute introduction)

You do not need to know how to code to follow this dojo. You need to know how to **ask clearly** and **check what you get back**. This page covers both.

> The app is new and evolves quickly. If a button or label on your screen has a slightly different name, look for the closest equivalent. The ideas below stay the same.

## 1. What the GitHub Copilot app is
The GitHub Copilot app is a **desktop application** (Windows, macOS, Linux) where you give work to an AI assistant. It reads your project, answers questions, creates and edits files, and can run commands. You stay in charge: you steer it and review what it did.

Two ways to talk to Copilot in the sidebar:
| Where | What it is | Use it for |
|---|---|---|
| **Chats** | General conversations that do not need their own workspace. | Brainstorming, clarifying a question before a task. |
| **Sessions** | A working area tied to your project. Copilot can read the project files, create files, and run tests. | Everything in this dojo: analyse files, answer from documents, build things. |

## 2. Anatomy of a session
When you start a session you see, below the prompt box, a row of drop-downs:
| Drop-down | Meaning | Dojo setting |
|---|---|---|
| **Environment** | **This computer** or **Cloud** (a GitHub-hosted sandbox). | **This computer** (Discovery). |
| **Workspace** | **New worktree** (a separate working copy) or **Current checkout** (your project folder as it is). | **Current checkout**, so the files are in your project folder. |
| **Mode** | How much freedom Copilot has (see below). | **Interactive** (Discovery). |
| **Model** and **reasoning effort** | Which AI model answers and how much it "thinks". | Leave the defaults. |
| **Tool permissions** (inside the mode menu) | When Copilot must ask your permission to do something. | **Assisted**. |

### The three modes
| Mode | What it does | Use it when |
|---|---|---|
| **Interactive** | Copilot suggests changes and **waits for your input** before going further. | **Start here.** You want to stay in control. |
| **Plan** | Copilot writes a **plan** first. You review and approve it before it acts. | The task has several steps, or you are not sure of the approach. |
| **Autopilot** | Copilot works **on its own**: writes, tests, iterates, without waiting. | The task is clear and you will review the result at the end. |

There is **no read-only "ask" mode**. When you only want answers, you tell Copilot not to change anything (see section 5) and you check the **Changes** button afterwards (section 6).

### Tool permissions
| Setting | What happens |
|---|---|
| **Ask every time** | Copilot asks before **each** action. Very safe, many clicks. |
| **Assisted** | The app approves safe actions itself and asks you for the risky ones. **Recommended for this dojo.** |
| **Approve all** | Copilot never asks. **Do not use this setting** during the dojo. |

When a permission request appears, **read it**: allow it if it concerns reading files or running a calculation inside the project. Refuse anything that touches files outside the project, installs software, or deletes things. If unsure, refuse and ask your facilitator.

## 3. Give Copilot the right context
Copilot only knows what it can see. In the **prompt box**:
| Type this | To do this |
|---|---|
| `@` | Add a **file** to your message. A list opens; type a few letters of the file name and click the file. |
| `#` | Reference a GitHub **issue** or pull request. |
| `/` | Open the list of **commands** (shortcuts). |

You can also name paths in your sentence ("read `docs/knowledge-base/returns-policy-v3.md`"): the session can read your project files. Still, **name the important files explicitly** instead of hoping Copilot picks them.

## 4. Write a good prompt: GCCF
| Letter | Meaning | Example |
|---|---|---|
| **G**oal | What you want | "Find which store had an unusual sales drop in 2026." |
| **C**ontext | Which files, who is the audience | "Use `data/monthly_summary.csv`. I am presenting to the retail director." |
| **C**onstraints | Rules to respect | "Only use the data provided. If you are unsure, say so. Do not modify any file." |
| **F**ormat | How to answer | "A table of 5 rows, then 3 bullet points." |

Weak: `Analyze the sales.`
Strong: `Using @monthly_summary.csv, compute total units per division per month for 2025. Show the method, then a table. List any data-quality issue you notice first. Do not modify any file.`

Useful follow-ups: "Explain this step as if I were new to the company", "Shorter", "Why did you choose that rule?", "What could be wrong with this answer?"

## 5. Start every Discovery session with a safety sentence
Because there is no read-only mode, begin each session with:
```
Rule for this session: do not create, modify or delete any file unless I explicitly ask you to. Answer only from the project files.
```
You will then check that it held (next section).

## 6. The verification loop (the most important habit)
Copilot is fast and fluent, and **sometimes wrong with confidence**. For every result:
1. **Ask for the method**: "Show me how you computed this."
2. **Cross-check** with a second way: look at the file yourself, a smaller sample, another question.
3. **Test the edges**: ask something it cannot know and see whether it admits it or invents.
4. **Review the changes**: click **Changes** above the prompt box to see exactly which files Copilot created or modified. In a read-only task it should show **nothing**.
5. **Own the result**: you are responsible for what you send or publish.

## 7. Make Copilot yours (customization)
The app has a **Customize** area in the sidebar for plugins, skills and tools. Customizations are plain files stored in the project:
| File or folder | Purpose |
|---|---|
| `.github/copilot-instructions.md` | General rules for working in this project (language, tone, conventions). |
| `.github/skills/` | **Skills**: reusable know-how that Copilot loads when relevant (for example "reply to a customer"). Used in the Builder level. |
| `.github/agents/` | **Custom agents** with a specific role. |

This project already includes `.github/copilot-instructions.md`. Open it with your file manager and notice how Copilot's answers follow those rules.

## 8. Safety and good practice
- **Never paste real confidential data** (customer data, contracts, credentials) into a prompt unless your organisation explicitly allows it. This dojo uses fictional data only.
- Check your organisation's AI usage policy before using Copilot at work.
- Do not accept text or files you cannot explain at a high level. Ask Copilot to explain.
- Share your best prompts with colleagues; good prompts are reusable assets.

## 9. If something does not work
| Problem | Try |
|---|---|
| The app says you are not signed in | Sign in again with the GitHub account that has Copilot. |
| Answers ignore your files | Add them with `@` and name them in your sentence. |
| The answer is too long or vague | Add constraints and a format ("5 bullet points, no jargon"). |
| It went in the wrong direction | Start a **new session**, restate your goal with what you learned. |
| A file was changed that should not have been | Click **Changes** to see it, then ask Copilot: "Undo your changes to that file." |
| Too many permission requests | Check that **Tool permissions** is set to **Assisted** (not **Ask every time**). |

## 10. Cheat sheet
- **Interactive** to stay in control · **Plan** to think first · **Autopilot** to delegate.
- `@` adds a file · `/` opens commands · `#` references issues.
- Prompt = **Goal + Context + Constraints + Format**.
- Always: **method, cross-check, look at Changes**.

Next: the [app tour](./02-setup-click-by-click.md), then the [warm-up adventure](../Adventures/StartHere.md).
