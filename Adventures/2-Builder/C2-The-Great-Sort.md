# C2 — The great sort 📬 (Workflow · Builder)

**Duration: 45–60 min · Copilot modes: Plan → Agent in small steps · Python (Copilot writes, you review)**

## Context
Every morning, the coordinator sorts 240 tickets by hand. You will automate the sort and measure how well it works.

## Mission
Create `my-work/sort_tickets.py` that reads `data/support_tickets.csv` and adds:
- a **region** (from `customer_region`) and a **division** inferred from the product named in the message;
- a **category**: return, exchange, repair, delivery, breakage, billing, info, follow_up;
- a **priority**: `high` (gift, event, "urgent", breakage, double billing), otherwise `normal`;
- a **confidence score** and a `needs_review` flag when the message is ambiguous.

Output: `my-work/sorted_tickets.csv` + a summary (count per category and priority).

## Copilot hints
- `First propose simple keyword rules, before any complex model.`
- `Test your script on 10 tickets I choose and show me the errors.`
- `Which messages are likely to be misclassified? Add a "needs review" case.`

## Success criteria
- Every ticket has a category, a priority and a confidence status.
- You **manually checked 15 tickets** and computed the correct-classification rate.
- You can say which types of tickets must **stay** with a human.

## Bonus
Add an export per advisor (balanced workload).
