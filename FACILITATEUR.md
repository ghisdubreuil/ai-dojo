# Guide du facilitateur

## Format conseillé : dojo de 3 h (8–20 personnes)
| Durée | Séquence |
|---|---|
| 0:00–0:15 | Accueil, objectifs, création du Codespace par chaque participant |
| 0:15–0:30 | Aventure d'échauffement ([StartHere](./Adventures/StartHere.md)) en commun |
| 0:30–1:15 | Round 1 : chacun choisit sa piste (A/B/C) et son niveau |
| 1:15–1:30 | Pause + démos de 2 participants |
| 1:30–2:30 | Round 2 : on monte d'un niveau, ou on change de piste |
| 2:30–3:00 | Restitution : « ce que Copilot a bien fait / mal fait / ce que j'ai vérifié » |

## Choisir son niveau
- **Découverte** : jamais écrit de code. Mode Ask, zéro installation.
- **Builder** : à l'aise avec Excel ou les formules. Copilot écrit, on relit.
- **Expert** : curieux, a déjà touché à un script ou à un outil de BI. Agent mode, tests, GitHub.

Règle d'or : **on peut descendre ou monter à tout moment**. Une personne qui bloque en Builder passe sur le Découverte de la même piste, sans perdre le fil métier.

## Posture de l'animateur
- Ne jamais corriger à la place : poser la question « comment peux-tu le vérifier ? ».
- Valoriser les erreurs de Copilot détectées plus que les réponses correctes.
- Binômer un Expert avec un Découverte (pair programming) pour le Round 2.

## Points de vigilance
- Licences : chaque participant a besoin d'un accès Copilot (Business/Enterprise ou Free). À vérifier **avant** le jour J.
- Quota Codespaces : prévoir une organisation qui les prend en charge.
- Données : tout est fictif, mais rappeler la règle « jamais de données réelles dans un prompt » sur le SI réel.
- Les chiffres d'un LLM ne se croient pas, ils se vérifient.

## Solutions de référence
Les corrigés ne sont volontairement pas dans le repo. Gardez-les dans une branche privée, ou demandez à Copilot de produire les siens.

## Débrief : 4 questions
1. Qu'avez-vous fait faire à Copilot que vous n'auriez pas osé tenter seul ?
2. Où s'est-il trompé, et comment l'avez-vous vu ?
3. Quelle tâche de votre métier pourrait suivre le même schéma ?
4. Qu'est-ce qui doit **toujours** rester humain ?
