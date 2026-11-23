# B3 — The knowledge agent 🧠 (Knowledge · Expert)

**Duration: 90 min · Modes: Plan, then Interactive · Python**

**Before you start:** Python must be available (see [prerequisites, Part 7](../../docs/00-prerequisites.md#7-for-builder-and-expert-levels-only-optional-until-you-get-there)).

## Context
Rather than attaching documents by hand, the Maison wants an **agent** that answers advisors' questions from the knowledge base, with citations and honest refusals.

## Mission
Get Copilot to build `my-work/knowledge_agent.py` (command line) that:
1. Loads the documents in `docs/knowledge-base/` **while ignoring obsolete versions** (files ending in `-obsolete`).
2. Retrieves the passages relevant to a question (keyword search is enough; an embedding engine is a bonus).
3. Answers **only** from those passages and **cites the file**.
4. Answers "I don't know" when no source covers the question.
5. Is evaluated on a set of **15 question/answer pairs** you write (`my-work/evaluation.csv`), scored for correctness and faithfulness to the sources.

## How to work in the app
1. Start a session in **Plan** mode. Ask Copilot first to propose evaluation criteria with you; approve the plan.
2. Switch to **Interactive**; review **Changes**; ask Copilot to run the agent on your 15 questions and show the scores.
3. Open `my-work/evaluation.csv` from your project folder and read the failures.

## Prompt ideas
- `Help me define what a good answer is for this agent: measurable criteria.`
- `Write 15 trap questions: obsolete version, out of scope, half covered.`
- `Where is the agent likely to hallucinate? Add guardrails.`

## Success criteria
- 100% of the answers in your evaluation set cite a source or say "I don't know".
- At least 3 trap questions are handled correctly.
- You can explain why the **quality of the knowledge base** matters as much as the model.

## Bonus
Add detection of contradictions between two documents.
