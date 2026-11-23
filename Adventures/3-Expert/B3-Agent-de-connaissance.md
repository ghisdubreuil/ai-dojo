# B3 — L'agent de connaissance 🧠  (Knowledge · Expert)

**Durée : 90 min · Mode Copilot : Agent · Python**

## Contexte
Plutôt que de coller les documents à la main, la Maison veut un **agent** capable de répondre aux questions des conseillers en s'appuyant sur la base de connaissance, avec citations et refus honnête.

## Mission
Construisez `mon-travail/agent_connaissance.py` (ligne de commande) qui :
1. Charge les documents de `docs/base-connaissance/` **en ignorant les versions obsolètes** (fichiers `-obsolete`).
2. Retrouve les passages pertinents pour une question (recherche par mots-clés suffit ; un moteur d'embeddings est un bonus).
3. Répond **uniquement** avec ces passages et **cite le fichier**.
4. Répond « je ne sais pas » quand aucune source ne couvre la question.
5. Est évalué par un jeu de **15 questions-réponses** que vous écrivez (`mon-travail/evaluation.csv`) avec score de justesse et de fidélité aux sources.

## Hints Copilot
- `Aide-moi à définir ce qu'est une bonne réponse pour cet agent : critères mesurables.`
- `Écris 15 questions pièges : version obsolète, hors périmètre, question à moitié couverte.`
- `Où l'agent risque-t-il d'halluciner ? Ajoute des garde-fous.`

## Critères de réussite
- 100 % des réponses du jeu d'évaluation citent une source ou disent « je ne sais pas ».
- Au moins 3 questions-pièges détectées correctement.
- Vous pouvez expliquer pourquoi la **qualité de la base** compte autant que le modèle.

## Bonus
Ajoutez la détection de contradiction entre deux documents.
