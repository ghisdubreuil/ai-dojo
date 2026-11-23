# A2 — Nettoyer et analyser 🧹  (Data · Builder)

**Durée : 45–60 min · Mode Copilot : Ask puis Edit · Python (Copilot écrit, vous relisez)**

## Contexte
La direction veut un chiffre d'affaires fiable par boutique et par mois. Mais `data/ventes.csv` est sale. Vous allez produire un **script reproductible** plutôt qu'un calcul fait une fois à la main.

## Mission
Créez `mon-travail/analyse_ventes.py` qui :
1. Charge les trois CSV.
2. **Nettoie** : doublons, quantités négatives, SKU inconnus, dates au format `JJ/MM/AAAA`, canal manquant (à marquer « inconnu »).
3. Affiche un **rapport de qualité** : combien de lignes retirées / corrigées, pourquoi.
4. Calcule le CA net par boutique et par mois.
5. Produit un graphique `mon-travail/ca_par_boutique.png` mettant en évidence Tokyo en mars 2026.

## Hints Copilot
- `Écris un script Python avec pandas qui charge #file:data/ventes.csv et liste tous les problèmes de qualité que tu détectes, avant de rien corriger.`
- `Ajoute des commentaires en français expliquant chaque règle de nettoyage.`
- `Explique-moi ligne par ligne ce que fait la fonction de nettoyage.`
- Si ça casse : copiez l'erreur dans le chat avec `Corrige cette erreur et explique-moi la cause`.

## Critères de réussite
- Le script tourne avec `python mon-travail/analyse_ventes.py` sans erreur.
- Le rapport de qualité chiffre chaque type d'anomalie.
- Vous pouvez expliquer, avec vos mots, **une** règle de nettoyage et pourquoi elle est justifiée.

## Bonus
Faites ajouter une règle : alerter si le CA mensuel d'une boutique chute de plus de 30 % vs la moyenne des 3 mois précédents.
