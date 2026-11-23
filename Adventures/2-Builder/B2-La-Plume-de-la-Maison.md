# B2 — La plume de la Maison ✒️  (Knowledge · Builder)

**Durée : 45–60 min · Mode Copilot : Chat + prompt files · Peu de code**

## Contexte
Les réponses clients varient d'un conseiller à l'autre. Vous allez configurer Copilot pour qu'il réponde **toujours** dans le ton de la Maison et avec les bonnes règles.

## Mission
1. Créez un **prompt file** `.github/prompts/repondre-client.prompt.md` qui :
   - impose le ton de `docs/base-connaissance/guide-ton-de-marque.md`,
   - ne s'appuie que sur la v3 de la politique (avec exceptions par région et par division),
   - adapte le ton à la région du client (`region_client`),
   - cite la règle utilisée,
   - signale quand il faut **escalader**.
2. Utilisez-le sur 5 tickets de `data/tickets_sav.csv` (choisissez des cas variés : retour, casse, livraison urgente, facturation, info).
3. Faites relire chaque réponse à Copilot avec la consigne : `Vérifie ce brouillon contre le guide de ton. Liste les écarts.`

## Hints Copilot
- `Aide-moi à écrire un prompt file VS Code réutilisable pour répondre à un ticket client de Maison Orélia. Pose-moi d'abord les questions qui te manquent.`
- `Quels éléments d'un bon prompt manquent dans ma version ?`

## Critères de réussite
- 5 brouillons respectant le vouvoiement, sans mots interdits, avec signature.
- Au moins un cas où Copilot **escalade** ou refuse de promettre un délai.
- Vous avez amélioré le prompt file **au moins deux fois** après avoir vu des défauts.

## Bonus
Comparez la réponse avec et sans le prompt file : qu'est-ce qui change ?
