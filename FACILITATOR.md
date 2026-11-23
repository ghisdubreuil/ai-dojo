# Facilitator guide

## Before the day
See the checklist for facilitators in [`docs/00-prerequisites.md`](./docs/00-prerequisites.md#10-for-the-facilitator-before-the-day): company SSO sign-in, Copilot access and app policy, software installation, the company template, a dry run on each operating system.

## Recommended format: 3-hour dojo (8–20 people)
| Time | Session |
|---|---|
| 0:00–0:20 | Welcome, goals. Walk through the [introduction to Copilot](./docs/01-getting-started-with-copilot.md), then everyone follows the [app tour](./docs/02-setup-click-by-click.md) (Parts 1 to 6) |
| 0:20–0:35 | [Warm-up adventure](./Adventures/StartHere.md) together |
| 0:35–1:15 | Round 1: everyone picks a track (A/B/C) and a level |
| 1:15–1:30 | Break + 2 participant demos |
| 1:30–2:30 | Round 2: move up a level, or switch track |
| 2:30–3:00 | Debrief: "what Copilot did well / badly / what I verified" |

## Choosing a level
- **Discovery**: has never written code. **Interactive** mode, read-only by instruction, nothing more to install.
- **Builder**: comfortable with Excel or formulas. Copilot writes, you review.
- **Expert**: curious, has touched a script or a BI tool. **Plan** and **Autopilot** modes, tests, GitHub issues and pull requests.

Golden rule: **you can go up or down at any time.** Someone stuck in Builder drops to the Discovery adventure of the same track without losing the business thread.

## Facilitator posture
- Never correct for them: ask "how can you verify that?".
- Celebrate Copilot's mistakes caught by participants more than correct answers.
- Pair an Expert with a Discovery participant (pair programming) for Round 2.

## Points of attention
- Access: participants sign in with their company login (SSO) and Copilot access is provided by the company. Verify **before** the day, along with the organisation's Copilot app policy.
- Software installation: Git and the app must be installed **before** the day (corporate laptops often block installs).
- Data: everything is fictional, but repeat the rule "never put real confidential data in a prompt" for real-world use.
- A model's numbers are not to be believed, they are to be verified.
- The Copilot app is new and evolves quickly: **do a full dry run the day before**, on **each operating system** in the room, and fix any label that differs from the guides.
- Consider adding screenshots of your own screen to the app tour after the dry run (a `docs/images/` folder works well).
- There is no read-only mode: teach the safety sentence and the habit of checking **Changes**.
- The app has no built-in file viewer in its documentation: participants open files with their computer's normal programs (spreadsheet for CSV, Notepad or TextEdit for Markdown).
- Have a facilitator or buddy per 4–5 participants during the setup: most blockers happen in the first 10 minutes (software installation, company sign-in, Copilot access).
- Discovery adventures use small files on purpose: adding up 21,000 rows in conversation is where assistants slip. This is itself a lesson to share.

## Reference solutions
Solutions are deliberately not in this repository. Keep them in a private branch, or have Copilot produce its own.

## Debrief: 4 questions
1. What did you get Copilot to do that you would not have dared try alone?
2. Where did it go wrong, and how did you notice?
3. Which task in your job could follow the same pattern?
4. What must **always** stay human?
