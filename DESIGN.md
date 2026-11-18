# DESIGN — Fil (gameday-fil)

> Journal de design, tenu par Claude. Versions datées, jamais écrasées.
> Dossier de travail : `G-DESIGN/` (PAGES, REFS, STYLE, planches).

## V1 — 2026-11-18 — trois directions sur la page Jeu

Statut : **en attente de validation de Gaia**.

Livré :
- `G-DESIGN/REFS.md` : Raycast et Mobbin ouverts et décodés.
- `G-DESIGN/PAGES.md` : 4 pages proposées (Post, Jeu, Carte de fin, Séries & classement) + 4 questions produit ouvertes.
- `G-DESIGN/planches/v1/01-fil.html` : direction de départ (blanc, bulle grise, violet, arcs de réponse).
- `G-DESIGN/planches/v1/02-console.html` : direction sombre et dense, fils orthogonaux.
- `G-DESIGN/planches/v1/03-pelote.html` : direction qui s'écarte (papier crème, une seule ficelle continue, titre serif).

Décisions :
- Le motif « fil » sert la règle : quand l'ordre est faux, les fils se croisent et remontent ; quand l'ordre est juste, ils deviennent courts et rangés. Le joueur voit son erreur sans texte.
- La couleur d'accent est réservée aux fils qui remontent (réponse placée avant son message) : un seul signal, une seule couleur.
- Heures masquées tant qu'une bulle n'est pas verrouillée (hypothèse, voir `PAGES.md` question 2).
- Contenu de démo inventé, sans marque ni personne réelle : groupe « Flat 4B », 4 colocs, malentendu sur « Gerald ».

## V1.1 — 2026-11-18 — direction 01 retenue, delta « jeu »

Statut : **direction 01 retenue par Gaia** ; delta en revue.

Retour de Gaia : « le design blanc gris violet est bien, on le garde, mais épaissis les lignes, que l'on sente que c'est un jeu et pas un chat ».

Livré :
- `G-DESIGN/planches/v1/01b-fil-jeu.html` (la 01 reste intacte pour comparaison).

Décisions :
- Fils : 3,5 px gris quand ils sont dans le bon sens, 5 px violet quand ils remontent, extrémités rondes, une pastille cerclée de blanc à chaque bout.
- Bulles devenues tuiles : coins égaux 14 px (fin du coin de messagerie), bord 2 px, bord bas 3 px en relief.
- Avatars cerclés d'encre 2 px, poignée de glisser plus épaisse, bouton 50 px avec bord bas 4 px.
- Palette et typo inchangées. Directions 02 et 03 abandonnées.

## V1.2 — 2026-11-18 — identité affirmée, plus « jeu » dans l'ensemble

Statut : en revue.

Retour de Gaia : « affirme plus l'identité visuelle, que ça ait l'air plus gamifié dans son ensemble ».

Livré :
- `G-DESIGN/planches/v1/01c-fil-identite.html` (01 et 01b restent intactes).

Décisions :
- **Logotype « fil »** : sans arrondie très grasse, le point du i est un rond violet et un fil violet ondule après le l.
- **En-tête de jeu** : logotype à gauche, puces « #019 » et « 6 day streak » à droite (bord 2 px + bord bas, style bouton de jeu).
- **Plateau** : les tuiles blanches sont posées sur un plateau gris `#f1f2f4` à coins 20 px, légèrement creusé.
- **Cases numérotées 1 à 8** à gauche de chaque tuile : elles remplacent les avatars et servent d'ancrage aux fils. Case verrouillée = pleine violette.
- **Compteur de nœuds** (« 3 tangles left ») = nombre de fils qui remontent ; but lisible en un chiffre : ramener à 0.
- **Le violet devient la couleur du jeu** (et plus seulement le signal d'erreur) : logotype, bouton principal, nœuds, cases verrouillées. Le gris reste pour les fils dans le bon sens. Bord bas du bouton `#4b3bc4`.
- Police : la sans arrondie n'est pas installée sur la machine de rendu (repli sur Noto Sans). Dans l'appli, il faudra embarquer une police arrondie sous licence libre.

## V1.3 — 2026-11-18 — identité renforcée, mobile qui s'affiche

Statut : en revue.

Retour de Gaia : « pas mal, à renforcer encore ; en revanche la version mobile ne s'affiche pas ».

Correctif (toutes les planches 01, 01b, 01c, 02, 03) :
- Le cadre mobile était coupé à droite quand la planche s'ouvrait dans une fenêtre plus étroite que 1980 px sans que le script de mise à l'échelle s'applique (débordement horizontal masqué). Le débordement n'est plus masqué et la mise à l'échelle passe par un vrai zoom : la planche entière, mobile compris, tient dans la fenêtre. Vérifié à 1100 px de large.

Livré :
- `G-DESIGN/planches/v1/01d-fil-identite-2.html` (mobile à gauche, en premier).

Décisions :
- **Bandeau violet** en tête du jeu, bord bas `#4b3bc4`, logotype en blanc : Fil se reconnaît dans le feed avant toute lecture.
- **Plateau à picots** : trame de points `#d8dbe2` tous les 14 px, bord 2 px.
- Relief plus franc : tuiles avec bord bas 4 px, cases avec bord bas 2 px, puces avec bord bas 3 px.
- **Pastille de nœuds** : rond violet 44 px, chiffre blanc.
- Mobile : bouton « Check order » pleine largeur (54 px) à portée de pouce, pastille de nœuds à sa gauche.

## V2 — 2026-11-18 — style validé, déclinaison des pages

Statut : style **validé** par Gaia (planche 01d) ; pages Post, Carte de fin, Séries & classement **en revue**.

Livré :
- `G-DESIGN/STYLE.md` : palette, typo, grille, composants, mouvement, états, ton.
- `G-DESIGN/planches/v1/10-post.html`
- `G-DESIGN/planches/v1/11-carte-de-fin.html`
- `G-DESIGN/planches/v1/12-series-classement.html`

Décisions :
- **Post** : bandeau + nom du groupe du jour en très gros, plateau avec les 8 tuiles sans texte et les fils emmêlés visibles (on voit le jeu sans rien dévoiler), un seul bouton « Untangle » et le nombre de joueurs du jour.
- **Carte de fin** : pastille violette avec le nombre de vérifications, « Untangled. », série +1 dans le bandeau ; le fil se relit dans l'ordre avec les heures, et le message du malentendu porte une étiquette violette (la chute). Action principale : « Comment your take » ; secondaire : « Stats » ; compte à rebours du prochain fil.
- **Séries & classement** : deux cartes. Série (grand chiffre violet, record, 14 derniers jours en cases) et communauté du jour (joueurs, % qui ont démêlé, moyenne, répartition des vérifications). La barre du joueur est la seule en violet plein. Pas de classement nominatif.
- Les nouvelles questions produit (6 à 8) sont dans `PAGES.md`.

## LOCK — 2026-11-18 — style verrouillé

Statut : **style verrouillé** par Gaia (`/lock`). Les 4 pages ont leur planche validée.

Planches de référence :
- Jeu : `planches/v1/01d-fil-identite-2.html`
- Post : `planches/v1/10-post.html`
- Carte de fin : `planches/v1/11-carte-de-fin.html`
- Séries & classement : `planches/v1/12-series-classement.html`

Les planches 01, 01b, 01c, 02, 03 restent dans le dossier comme historique d'exploration ; elles ne font pas référence.

Fin des explorations. Toute évolution du style passe par une nouvelle version datée dans ce journal. Le verrouillage ne tranche pas les 8 questions produit de `PAGES.md` : elles restent ouvertes pour le développement.

Changelog :
- 2026-11-18 : création du journal, V1.
- 2026-11-18 : V1.1, direction 01 retenue, traits épaissis (planche 01b).
- 2026-11-18 : V1.2, identité affirmée : logotype, plateau, cases, compteur (planche 01c).
- 2026-11-18 : V1.3, bandeau violet, plateau à picots, mobile en premier (planche 01d) ; correctif d'affichage du mobile sur toutes les planches.
- 2026-11-18 : V2, style 01d validé, STYLE.md, planches 10 Post, 11 Carte de fin, 12 Séries & classement.
- 2026-11-18 : LOCK, style verrouillé, 4 pages validées.
