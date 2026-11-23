# 🏰 Copilot Business Dojo — Maison Orélia

A dojo for **non-technical people** using the **GitHub Copilot desktop app**, built around realistic business use cases. Each participant picks a **track** and a **level**, and can move up or down at any time.

> Maison Orélia is a **fictional** luxury house. All data is synthetic.

## Start here
1. Do the [prerequisites](./docs/00-prerequisites.md): install Git and the **GitHub Copilot desktop app**, sign in, and fork this project. Do it a day before.
2. Read the [15-minute introduction](./docs/01-getting-started-with-copilot.md).
3. Follow the [app tour](./docs/02-setup-click-by-click.md).
4. Do the [warm-up adventure](./Adventures/StartHere.md).
5. Pick a track and a level. Discovery adventures are written step by step, click by click.

## The fictional organisation
**3 divisions** (Fashion · Fragrance & Beauty · Watches & Fine Jewelry) × **6 regions** (UK · US · APAC · Japan · Europe · Swiss & Others). Details in [`docs/organisation.md`](./docs/organisation.md).

## Adventures
| Track | 🟢 Discovery (no code) | 🟡 Builder (Copilot writes, you review) | 🔴 Expert (agents, tests, GitHub) |
|---|---|---|---|
| **A. Data analysis** | [The sales mystery](./Adventures/1-Discovery/A1-The-Sales-Mystery.md) | [Clean and analyze](./Adventures/2-Builder/A2-Clean-and-Analyze.md) | [The living dashboard](./Adventures/3-Expert/A3-The-Living-Dashboard.md) |
| **B. Knowledge agent** | [The rule keeper](./Adventures/1-Discovery/B1-The-Rule-Keeper.md) | [The Maison voice](./Adventures/2-Builder/B2-The-Maison-Voice.md) | [The knowledge agent](./Adventures/3-Expert/B3-The-Knowledge-Agent.md) |
| **C. Workflow** | [Map the process](./Adventures/1-Discovery/C1-Map-the-Process.md) | [The great sort](./Adventures/2-Builder/C2-The-Great-Sort.md) | [The end-to-end workflow](./Adventures/3-Expert/C3-The-End-to-End-Workflow.md) |

Each track follows the same thread: **understand → build → industrialise**.

## Contents
- `docs/`: prerequisites, introduction to the Copilot app, app tour, organisation, current process, knowledge base (with deliberately contradictory versions)
- `Adventures/`: the 9 adventures + the warm-up
- `data/`: raw sales (12 stores), a clean monthly summary, a small dirty sample, products (23 items, 3 divisions), stores (6 regions), support tickets — fictional, with deliberate anomalies
- `my-work/`: your working folder
- [`FACILITATOR.md`](./FACILITATOR.md): 3-hour agenda, posture, debrief

## Teaching principles
- We learn by **verifying** Copilot, not by trusting it.
- Every adventure has observable **success criteria**.
- Business first, technology second.
