# B2 — The Maison voice ✒️ (Knowledge · Builder)

**Duration: 60 min · Modes: Plan, then Interactive · Little code**

## Context
Customer replies vary from one advisor to another. You will give Copilot a reusable **skill** so it **always** answers in the Maison's tone and with the right rules.

> A **skill** is a folder with a `SKILL.md` file: a title, a short description of when to use it, and the instructions. Copilot loads it when the task matches. Skills live in `.github/skills/`. You can see the skills Copilot knows in the **Customize** area of the sidebar. (Check in your dry run that the app lists your new skill; if not, mention the skill by name in your prompt.)

## Mission
1. Ask Copilot to create the skill `.github/skills/reply-to-customer/SKILL.md` that:
   - applies the tone of `docs/knowledge-base/brand-tone-guide.md`,
   - relies only on v3 of the policy (with regional and division exceptions),
   - adapts the tone to the customer's region (`customer_region`),
   - cites the rule used,
   - flags when the case must be **escalated**.
2. Use it on 5 tickets from `data/support_tickets.csv` (pick varied cases: return, breakage, urgent delivery, billing, information).
3. Ask Copilot to review each draft: `Check this draft against the tone guide. List the gaps.`

## How to work in the app
1. Start a session on `ai-dojo` in **Plan** mode. Describe the skill; read the plan; approve.
2. Switch to **Interactive**. Check **Changes**: you should see the new `SKILL.md`.
3. Open `SKILL.md` from your project folder and read it as if you were a new advisor: is it clear?
4. In a **new session**, ask: `Use the reply-to-customer skill to answer ticket T0007 in @support_tickets.csv.`

## Prompt ideas
- `Help me write a reusable skill to reply to a Maison Orélia customer ticket. Ask me first for any missing information.`
- `Which elements of a good instruction are missing from my skill?`

## Success criteria
- 5 drafts using formal address, none of the banned words, with the signature.
- At least one case where Copilot **escalates** or refuses to promise a delivery date.
- You improved the skill **at least twice** after seeing flaws.

## Bonus
Compare a reply with and without the skill: what changes?
