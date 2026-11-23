# C3 — Le workflow de bout en bout 🔗  (Workflow · Expert)

**Durée : 90–120 min · Mode Copilot : Agent + Copilot coding agent · Python + GitHub**

## Contexte
Vous avez cartographié (C1), trié (C2), et construit une base de règles (B2/B3). Il reste à **assembler** : du ticket entrant au brouillon de réponse, avec un humain au bon endroit.

## Mission
Concevez et implémentez un pipeline `mon-travail/pipeline_sav.py` :
1. **Entrée** : `tickets_sav.csv`.
2. **Tri** : catégorie et priorité (C2).
3. **Enrichissement** : règle applicable (base de connaissance) et décision `repondre` / `escalader`.
4. **Brouillon** de réponse dans le ton de la Maison.
5. **Sortie** : un CSV de travail pour les conseillers + un rapport hebdomadaire (volumes, délais cibles, % escaladés).
6. Aucune réponse n'est « envoyée » : **validation humaine** obligatoire (champ `statut = a_valider`).

Puis, dans GitHub :
7. Créez une **issue** décrivant une amélioration (ex : nouvelle catégorie « cadeau ») et assignez-la au **Copilot coding agent**. Relisez sa pull request.

## Hints Copilot
- `Avant de coder, liste les risques de ce workflow (réponse erronée, promesse de délai, données personnelles) et propose un garde-fou pour chacun.`
- `Fais un schéma Mermaid du pipeline cible et vérifie qu'il correspond au code.`

## Critères de réussite
- Le pipeline tourne de bout en bout et produit les deux sorties.
- Chaque brouillon porte `statut = a_valider`.
- Vous avez relu la PR de l'agent et laissé **au moins un commentaire** argumenté.

## Bonus
Planifiez le rapport via GitHub Actions chaque lundi.
