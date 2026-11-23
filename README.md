# 🏰 Dojo Copilot Métier — Maison Orélia

Un dojo GitHub Copilot pour **non-techniques**, avec des cas d'usage métier réalistes. Inspiré du format « choose-your-own-adventure » de [Copilot Adventures](https://github.com/microsoft/copilotadventures), appliqué à la data, aux agents de connaissance et à la transformation de workflows.

> Maison Orélia est une maison de luxe **fictive**. Toutes les données sont synthétiques.

## Comment ça marche
1. Cliquez sur **Code → Codespaces → Create codespace**. Tout est préinstallé.
2. Commencez par l'[aventure d'échauffement](./Adventures/StartHere.md) (15 min).
3. Choisissez une **piste** et un **niveau**. Vous pouvez changer à tout moment.

| Piste | 🟢 Découverte (sans code) | 🟡 Builder (Copilot écrit, vous relisez) | 🔴 Expert (agents, tests, GitHub) |
|---|---|---|---|
| **A. Data analyse** | [Le mystère des ventes](./Adventures/1-Decouverte/A1-Le-Mystere-des-ventes.md) | [Nettoyer et analyser](./Adventures/2-Builder/A2-Nettoyer-et-analyser.md) | [Le tableau de bord vivant](./Adventures/3-Expert/A3-Tableau-de-bord-vivant.md) |
| **B. Agent knowledge** | [Le gardien des règles](./Adventures/1-Decouverte/B1-Le-Gardien-des-regles.md) | [La plume de la Maison](./Adventures/2-Builder/B2-La-Plume-de-la-Maison.md) | [L'agent de connaissance](./Adventures/3-Expert/B3-Agent-de-connaissance.md) |
| **C. Workflow** | [Cartographier le processus](./Adventures/1-Decouverte/C1-Cartographier-le-processus.md) | [Le grand tri](./Adventures/2-Builder/C2-Le-Grand-Tri.md) | [Le workflow de bout en bout](./Adventures/3-Expert/C3-Le-Workflow-de-bout-en-bout.md) |

Chaque piste suit le même fil : **comprendre → construire → industrialiser**.

## Contenu
- `Adventures/` : les 9 aventures + l'échauffement
- `data/` : ventes, produits, boutiques, tickets SAV (fictifs, avec anomalies volontaires)
- `docs/` : base de connaissance et processus actuel (avec versions contradictoires volontaires)
- `mon-travail/` : votre dossier de travail
- [`FACILITATEUR.md`](./FACILITATEUR.md) : déroulé d'un dojo de 3 h, posture, débrief

## Principes pédagogiques
- On apprend en **vérifiant** Copilot, pas en lui faisant confiance.
- Chaque aventure a des **critères de réussite** observables.
- Le métier d'abord, la technique ensuite.
