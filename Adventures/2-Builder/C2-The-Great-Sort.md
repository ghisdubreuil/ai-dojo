# C2 — The great sort 📬 (Workflow · Builder)

**Duration: 60 min · Modes: Plan, then Interactive · Python (Copilot writes and runs, you review)**

**Before you start:** Python must be available (see [prerequisites, Part 7](../../docs/00-prerequisites.md#7-for-builder-and-expert-levels-only-optional-until-you-get-there)).

## Context
Every morning, the coordinator sorts 240 tickets by hand. You will automate the sort and measure how well it works.

## Mission
Get Copilot to create `my-work/sort_tickets.py` that reads `data/support_tickets.csv` and adds:
- a **region** (from `customer_region`) and a **division** inferred from the product named in the message;
- a **category**: return, exchange, repair, delivery, breakage, billing, info, follow_up;
- a **priority**: `high` (gift, event, "urgent", breakage, double billing), otherwise `normal`;
- a **confidence score** and a `needs_review` flag when the message is ambiguous.

Output: `my-work/sorted_tickets.csv` + a summary (count per category and priority).

## How to work in the app
1. Start a session on `ai-dojo` in **Plan** mode; describe the mission; approve the plan.
2. Switch to **Interactive**; review **Changes**; ask Copilot to run the script and show the summary.
3. Open `my-work/sorted_tickets.csv` from your project folder in a spreadsheet.

## Prompt ideas
- `First propose simple keyword rules, before any complex model.`
- `Test your script on 10 tickets I choose and show me the errors.`
- `Which messages are likely to be misclassified? Add a "needs review" case.`

## Success criteria
- Every ticket has a category, a priority and a confidence status.
- You **manually checked 15 tickets** in the spreadsheet and computed the correct-classification rate.
- You can say which types of tickets must **stay** with a human.

## Bonus
Add an export per advisor (balanced workload).
