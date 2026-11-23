# B3 — The knowledge agent 🧠 (Knowledge · Expert)

**Duration: 90 min · Copilot modes: Plan then Agent · Python**

## Context
Rather than pasting documents by hand, the Maison wants an **agent** that answers advisors' questions from the knowledge base, with citations and honest refusals.

## Mission
Build `my-work/knowledge_agent.py` (command line) that:
1. Loads the documents in `docs/knowledge-base/` **while ignoring obsolete versions** (files ending in `-obsolete`).
2. Retrieves the passages relevant to a question (keyword search is enough; an embedding engine is a bonus).
3. Answers **only** from those passages and **cites the file**.
4. Answers "I don't know" when no source covers the question.
5. Is evaluated on a set of **15 question/answer pairs** you write (`my-work/evaluation.csv`), scored for correctness and faithfulness to the sources.

## Copilot hints
- `Help me define what a good answer is for this agent: measurable criteria.`
- `Write 15 trap questions: obsolete version, out of scope, half covered.`
- `Where is the agent likely to hallucinate? Add guardrails.`

## Success criteria
- 100% of the answers in your evaluation set cite a source or say "I don't know".
- At least 3 trap questions are handled correctly.
- You can explain why the **quality of the knowledge base** matters as much as the model.

## Bonus
Add detection of contradictions between two documents.
