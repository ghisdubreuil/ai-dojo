# A1 — Le mystère des ventes 🔎  (Data · Découverte)

**Durée : 30 min · Mode Copilot : Ask · Aucun code à écrire**

## Contexte
La direction de Maison Orélia vous demande : « Que s'est-il passé dans nos ventes ? » Vous disposez de `data/ventes.csv`, `data/produits.csv` et `data/boutiques.csv`.

## Mission
Répondre en langage simple à 4 questions, en vous aidant de Copilot Chat (`#file:data/ventes.csv` pour lui donner le fichier) :
1. Quelles sont les 3 boutiques qui vendent le plus (en chiffre d'affaires) ?
2. Quelle catégorie de produits pèse le plus ?
3. Y a-t-il une saisonnalité visible ?
4. **Une boutique a-t-elle eu un comportement anormal sur 2026 ?**

## Hints Copilot
- `À partir de #file:data/ventes.csv et #file:data/produits.csv, calcule le CA par boutique (quantité × prix × (1 - remise)). Explique ta méthode.`
- `Donne-moi un tableau mois par mois pour la boutique que tu trouves étrange.`
- `Quelles questions me recommandes-tu de poser ensuite à la direction ?`

## Critères de réussite
- Vous avez identifié l'anomalie de **Tokyo Ginza en mars 2026**.
- Vous avez demandé à Copilot **comment il a calculé** ses chiffres.
- Vous avez repéré au moins 2 problèmes de qualité de données (doublons, quantités négatives, dates mal formatées…).

## Bonus
Demandez à Copilot de rédiger un mail de 5 lignes à la direction avec vos 3 conclusions.
