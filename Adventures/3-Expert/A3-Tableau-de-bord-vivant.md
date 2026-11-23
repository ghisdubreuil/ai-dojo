# A3 — Le tableau de bord vivant 📊  (Data · Expert)

**Durée : 90 min · Mode Copilot : Agent · Python + tests**

## Contexte
Le directeur retail veut un tableau de bord interactif qu'il consulte chaque lundi, avec des alertes automatiques et la **confiance** dans les chiffres affichée.

## Mission
Avec **Agent mode**, construisez une application (Streamlit conseillée) qui :
1. Réutilise votre pipeline de nettoyage (A2) comme module testé.
2. Affiche CA, panier moyen, marge par division et par catégorie, filtres par région (6)/division (3)/boutique/période, et une vue matrice division × région.
3. Montre une section **« Qualité des données »** (lignes écartées, raisons).
4. Détecte et explique les **anomalies** (ex : Tokyo mars 2026).
5. Est couverte par au moins 5 tests (`pytest`).

## Hints Copilot
- Commencez par `Fais-moi un plan avant de coder : architecture, fichiers, tests. N'écris rien avant que je valide.`
- Créez `.github/copilot-instructions.md` avec vos conventions (français, tests, pas de dépendances inutiles), et observez la différence.
- `Relis ton code comme un relecteur critique : quels risques de calcul faux ?`

## Critères de réussite
- `streamlit run app.py` fonctionne dans le Codespace.
- Les chiffres du dashboard **coïncident avec ceux de A2**.
- Vous avez demandé à l'agent de **justifier** un chiffre et vérifié indépendamment.

## Bonus
Faites générer une page « Comment lire ce dashboard » pour les non-techniques.
