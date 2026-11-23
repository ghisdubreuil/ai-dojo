# B2 — The Maison voice ✒️ (Knowledge · Builder)

**Duration: 45–60 min · Copilot: Chat + prompt files · Little code**

## Context
Customer replies vary from one advisor to another. You will configure Copilot so it **always** answers in the Maison's tone and with the right rules.

## Mission
1. Create a **prompt file** `.github/prompts/reply-to-customer.prompt.md` that:
   - applies the tone of `docs/knowledge-base/brand-tone-guide.md`,
   - relies only on v3 of the policy (with regional and division exceptions),
   - adapts the tone to the customer's region (`customer_region`),
   - cites the rule used,
   - flags when the case must be **escalated**.
2. Use it on 5 tickets from `data/support_tickets.csv` (pick varied cases: return, breakage, urgent delivery, billing, information).
3. Ask Copilot to review each draft: `Check this draft against the tone guide. List the gaps.`

## Copilot hints
- `Help me write a reusable VS Code prompt file to reply to a Maison Orélia customer ticket. Ask me first for any missing information.`
- `Which elements of a good prompt are missing from my version?`

## Success criteria
- 5 drafts using formal address, none of the banned words, with the signature.
- At least one case where Copilot **escalates** or refuses to promise a delivery date.
- You improved the prompt file **at least twice** after seeing flaws.

## Bonus
Compare a reply with and without the prompt file: what changes?
