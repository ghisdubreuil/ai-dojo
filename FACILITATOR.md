# Facilitator guide

## Recommended format: 3-hour dojo (8–20 people)
| Time | Session |
|---|---|
| 0:00–0:20 | Welcome, goals. Walk through the [introduction to Copilot](./docs/00-getting-started-with-copilot.md), then everyone follows the [click-by-click setup](./docs/01-setup-click-by-click.md) (Parts 1 to 4) |
| 0:20–0:35 | [Warm-up adventure](./Adventures/StartHere.md) together |
| 0:35–1:15 | Round 1: everyone picks a track (A/B/C) and a level |
| 1:15–1:30 | Break + 2 participant demos |
| 1:30–2:30 | Round 2: move up a level, or switch track |
| 2:30–3:00 | Debrief: "what Copilot did well / badly / what I verified" |

## Choosing a level
- **Discovery**: has never written code. Ask mode, nothing to install.
- **Builder**: comfortable with Excel or formulas. Copilot writes, you review.
- **Expert**: curious, has touched a script or a BI tool. Plan/Agent modes, tests, GitHub.

Golden rule: **you can go up or down at any time.** Someone stuck in Builder drops to the Discovery adventure of the same track without losing the business thread.

## Facilitator posture
- Never correct for them: ask "how can you verify that?".
- Celebrate Copilot's mistakes caught by participants more than correct answers.
- Pair an Expert with a Discovery participant (pair programming) for Round 2.

## Points of attention
- Licences: each participant needs Copilot access (check your plan). Verify **before** the day.
- Codespaces quota: arrange for an organisation or account to cover usage.
- Data: everything is fictional, but repeat the rule "never put real confidential data in a prompt" for real-world use.
- A model's numbers are not to be believed, they are to be verified.
- Copilot's interface changes often: **do a full dry run the day before** (setup guide + warm-up + one Discovery adventure) and fix any label that differs from the guide.
- Consider adding screenshots of your own screen to the setup guide after the dry run (a `docs/images/` folder works well).
- Have a facilitator or buddy per 4–5 participants during the setup: most blockers happen in the first 10 minutes (sign-in, Codespace quota, Copilot seat).
- Discovery adventures use small files on purpose: a chat assistant cannot reliably add up a 21,000-row file. This is itself a lesson to share.

## Reference solutions
Solutions are deliberately not in this repository. Keep them in a private branch, or have Copilot produce its own.

## Debrief: 4 questions
1. What did you get Copilot to do that you would not have dared try alone?
2. Where did it go wrong, and how did you notice?
3. Which task in your job could follow the same pattern?
4. What must **always** stay human?
