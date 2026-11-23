# C2 — Le grand tri 📬  (Workflow · Builder)

**Durée : 45–60 min · Mode Copilot : Edit · Python (Copilot écrit, vous relisez)**

## Contexte
Chaque matin, le coordinateur classe 240 tickets à la main. Vous allez automatiser ce tri et mesurer ce que ça donne.

## Mission
Créez `mon-travail/trier_tickets.py` qui lit `data/tickets_sav.csv` et ajoute :
- une **catégorie** : retour, echange, reparation, livraison, casse, facturation, info, suivi ;
- une **priorité** : `haute` (cadeau, événement, « urgent », casse, double facturation), `normale` sinon ;
- un **score de confiance** et un indicateur `a_verifier` quand le message est ambigu.

Résultat : `mon-travail/tickets_tries.csv` + un résumé (nombre par catégorie et priorité).

## Hints Copilot
- `Propose-moi d'abord des règles simples par mots-clés, avant tout modèle complexe.`
- `Teste ton script sur 10 tickets que je choisis et montre-moi les erreurs.`
- `Quels messages risquent d'être mal classés ? Ajoute un cas « à vérifier ».`

## Critères de réussite
- Chaque ticket a une catégorie, une priorité et un statut de confiance.
- Vous avez vérifié **à la main 15 tickets** et calculé le taux de bon classement.
- Vous pouvez dire quels types de tickets doivent **rester** traités par un humain.

## Bonus
Ajoutez un export par conseiller (répartition équilibrée de la charge).
