# PAGES — Fil

> Statuts : à dessiner / en revue / validée. **Style verrouillé (/lock) le 2026-11-18 : les 4 pages sont validées.**
> Chaque planche montre le cadre desktop 1440 × 900 et le cadre mobile 390 × 844 côte à côte.

| # | Page | Rôle | Contenu clé | Statut |
|---|------|------|-------------|--------|
| 1 | **Post** | État dans le feed : donner envie d'ouvrir le fil du jour | En-tête du post, n° du jour, nom du groupe de discussion, aperçu flou des bulles, série du joueur, bouton « Untangle » | **validée** — `10-post.html` |
| 2 | **Jeu** | Écran principal, une seule règle : « Put the chat back in order » | 8 bulles mélangées, fils qui relient chaque réponse au message auquel elle répond, glisser-déposer, bouton « Check order » | **validée** — style 01d (`01d-fil-identite-2.html`) |
| 3 | **Carte de fin** | Résultat + boucle quotidienne + accroche commentaire | Fil remis en ordre (lecture complète, le malentendu révélé), nombre de vérifications, série, part de la communauté qui a réussi, bouton commenter, prochain fil dans HH:MM | **validée** — `11-carte-de-fin.html` |
| 4 | **Séries & classement** | Montrer la communauté et la série | Série perso, résultats du jour de la communauté (répartition du nombre de vérifications) | **validée** — `12-series-classement.html` |

Les états sont dessinés sur la planche de leur page, pas comme des pages à part : Jeu (glisser, vérifié, verrouillé), Post (chargement, déjà joué, erreur), Carte de fin (1 vérification, premier jour, boutons pressés), Séries (série cassée, avant d'avoir joué).

## Questions produit ouvertes (non tranchées)

Les planches V1 montrent une hypothèse pour chacune ; rien n'est décidé. Le verrouillage porte sur le style, pas sur ces questions : elles restent à trancher avant le développement.

1. **Retour après « Check order »** : les planches supposent que les bulles bien placées se verrouillent et révèlent leur heure, et que le joueur peut revérifier. Nombre de vérifications illimité ou plafonné ?
2. **Heures masquées** : si les heures sont visibles, l'ordre se lit tout seul. Les planches les masquent (`··:··`) jusqu'au verrouillage. À confirmer.
3. **« Un malentendu »** : le joueur doit-il seulement remettre l'ordre, ou aussi désigner le message du malentendu ? Les planches ne montrent que la remise en ordre ; le malentendu est révélé sur la carte de fin.
4. **Liens de réponse** : les fils entre bulles supposent que chaque message connaît le message auquel il répond (donnée du générateur). À confirmer côté contenu généré.
5. **En-tête de jeu (planche 01c)** : la série du joueur et un compteur de nœuds (« 3 tangles left », nombre de réponses placées avant leur message) sont affichés pendant la partie. Le compteur donne-t-il trop d'information au joueur ? À confirmer.
6. **Post déjà joué** (planche 10, états) : le post affiche « Untangled · 2 checks », un bouton « See results » et le compte à rebours. À confirmer.
7. **Accès aux stats** : depuis la carte de fin (bouton « Stats ») ; retour par « Back to the thread ». Faut-il aussi un accès depuis le post avant de jouer ? Les planches montrent alors la communauté sans la répartition (pas de spoiler).
8. **Chiffres de la communauté** : les planches affichent nombre de joueurs, % qui ont démêlé le fil, moyenne et répartition des vérifications. Pas de classement nominatif (choix de design, à confirmer).
