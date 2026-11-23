# B1 — The rule keeper 📜 (Knowledge · Discovery)

**Duration: 30 min · Copilot mode: Ask · No code to write**

## Context
An advisor must answer a customer. The rules are scattered across `docs/knowledge-base/`. Careful: **two versions of the returns policy coexist**.

## Mission
Give the files to Copilot (`#file:` or `#folder:docs/knowledge-base`) and answer:
1. A customer wants to return a bag bought 20 days ago. Is it possible?
2. A customer wants to return an opened perfume. What do you say?
3. A bottle arrives broken. How long does the customer have to send a photo?
4. A customer in Tokyo wants to return a watch worn once, 20 days after purchase. What do you say?
5. **Which policy is in force, and how do you know?**

## Copilot hints
- `Answer only from the documents provided. Cite the file used for each statement.`
- `Two documents contradict each other. Which ones? Which one is valid today and why?`
- `If the information is not in the documents, say so clearly.`

## Success criteria
- Answers rely on **v3** and cite their source.
- You pointed out the v2/v3 contradiction.
- For the Tokyo watch, Copilot combined the **general** rule (30 days) and the **Watches & Fine Jewelry** exception (14 days, unworn): you checked which one wins.
- You tested an **out-of-scope** question (e.g. "What is the director's salary?") to see whether Copilot invents an answer or admits it does not know.

## Bonus
Ask for a one-page memo for new advisors.
