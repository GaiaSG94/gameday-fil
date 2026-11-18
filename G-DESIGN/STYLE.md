# STYLE — Fil

> **Style verrouillé (/lock) le 2026-11-18.** Validé par Gaia sur la planche `planches/v1/01d-fil-identite-2.html`, décliné sur `10-post`, `11-carte-de-fin`, `12-series-classement`.
> Fin des explorations : toute évolution passe par une nouvelle version notée dans `DESIGN.md`.
> Toute nouvelle planche suit ce fichier. Une seule couleur d'accent, une seule échelle typo.

## 1. Principe

Fil est un **jeu de plateau** dont les pièces sont des messages. Trois idées tiennent tout le style :
1. **Le fil est le motif** : les liens entre messages sont des cordes épaisses ; rangées, elles sont grises et courtes ; emmêlées, elles remontent et passent en violet.
2. **Tout a du relief** : chaque élément cliquable a un bord bas plein, comme une pièce qu'on presse.
3. **Le violet est la couleur du jeu** : bandeau, logotype, bouton principal, nœuds, cases verrouillées. Rien d'autre n'est coloré.

## 2. Palette

| Rôle | Hex | Usage |
|------|-----|-------|
| Fond | `#ffffff` | fond du jeu, tuiles |
| Plateau | `#f1f2f4` | plateau, surfaces secondaires, tuile désactivée |
| Picots | `#d8dbe2` | trame de points du plateau (tous les 14 px) |
| Bord tuile | `#e2e4e9` | bord 2 px des tuiles et cartes |
| Relief tuile | `#d6d9e0` | bord bas 4 px des tuiles |
| Fil rangé | `#c9ccd4` | liens dans le bon sens |
| Accent | `#6c5ce7` | couleur du jeu (voir §1) |
| Accent bas | `#4b3bc4` | bord bas des éléments violets |
| Accent clair | `#efedfd` | fond d'une tuile verrouillée, barres secondaires |
| Encre | `#16181d` | texte, bords des cases et puces |
| Encre 2 | `#5d6270` | texte secondaire, noms d'expéditeur |
| Encre 3 | `#9aa0ab` | aide, heures masquées |

Interdits : dégradés, deuxième couleur vive, ombres floues fortes (une seule ombre portée douce, réservée à la tuile en cours de glisser).

## 3. Typographie

- **Sans arrondie** (à embarquer dans l'appli : police arrondie sous licence libre ; repli `ui-rounded, system-ui`).
- **Mono** pour les métadonnées : heures, n° du jour, compteurs, étiquettes en capitales (`ui-monospace`, à embarquer aussi).

| Rôle | Police | Taille / graisse |
|------|--------|------------------|
| Logotype « fil » | sans arrondie | 38 px desktop, 32 px mobile / 900, approche −0,04 em |
| Grand chiffre (résultat, pastille) | sans arrondie | 24 / 36 / 56 px / 900 |
| Titre d'écran | sans arrondie | 22 px / 800 |
| Consigne | sans arrondie | 15 px (14 mobile) / 400, partie clé en 700 encre |
| Message (tuile) | sans arrondie | 14 px (13 mobile) / 500 |
| Nom d'expéditeur | sans arrondie | 12 px / 700, encre 2 |
| Bouton | sans arrondie | 16 px (17 mobile) / 700 |
| Étiquette | mono | 11 px / 600–700, capitales, espacement 0,06–0,08 em |
| Heure, chiffre de case | mono | 11–12 px / 500–800 |

## 4. Grille et cadre

- Le jeu vit **dans le cadre du post** : 736 px de large sur desktop, 390 px sur mobile ; il ne sort jamais du post.
- Marges intérieures : 20 px desktop, 14 px mobile. Plateau inséré de 14 px (8 px mobile).
- Pas vertical : 4 px. Lignes de tuiles : 44 px desktop, 50 px mobile (2 lignes de texte possibles).
- Ordre vertical fixe : **bandeau → consigne → plateau → pied (action)**. L'action principale est toujours en bas, à portée de pouce.

## 5. Composants

- **Bandeau** : fond accent, bord bas 4 px accent bas, logotype blanc à gauche, puces à droite.
- **Puce** : hauteur 30 px (28 mobile), fond blanc, bord 2 px encre, bord bas 3 px encre, rayon pilule, texte mono 13 px ; le chiffre important en accent 900.
- **Plateau** : fond `#f1f2f4` + picots, bord 2 px `#e3e5ea`, creux intérieur 3 px, rayon 20 px.
- **Tuile** : fond blanc, bord 2 px, bord bas 4 px, rayon 14 px, nom + message, heure mono à droite, poignée 3 barres.
- **Case numérotée** : rond 26 px, fond blanc, bord 2,5 px encre, bord bas 2 px, chiffre mono 800. Point d'ancrage des fils.
- **Fil** : 3,5 px `#c9ccd4` dans le bon sens ; 5 px accent quand il remonte ; extrémités rondes ; part de la case.
- **Bouton principal** : fond accent, texte blanc 700, hauteur 50 px (54 mobile, pleine largeur), rayon pilule, bord bas 4 px accent bas.
- **Bouton secondaire** : fond blanc, bord 2 px encre, bord bas 3 px encre, mêmes dimensions.
- **Pastille** : rond 44 px accent, chiffre blanc 900, bord bas 3 px accent bas, étiquette mono à côté.
- **Carte** : fond blanc, bord 2 px `#e2e4e9`, bord bas 4 px `#d6d9e0`, rayon 16 px.
- **Barre de données** : fond `#efedfd`, valeur du joueur en accent plein, rayon 6 px.

## 6. Mouvement

- Courbe unique `cubic-bezier(.22,1,.36,1)`, 220 ms : glisser, réordonner, ouvrir une carte.
- Rebond `cubic-bezier(.34,1.56,.64,1)`, 320 ms, réservé au verrouillage d'une tuile et à l'arrivée du résultat.
- Les fils se redessinent en suivant la tuile (pas de saut).
- Appui sur un élément en relief : il descend de la hauteur de son bord bas (le bord disparaît), 80 ms.

## 7. États

| État | Règle |
|------|-------|
| Repos | tuile blanche, heure masquée `··:··` |
| Glisser | tuile soulevée de 6 px, échelle 1,02, bord + bord bas accent, ombre douce ; case au bord accent |
| Verrouillée | fond accent clair, case pleine accent, heure révélée en accent |
| Désactivé | élément enfoncé (sans bord bas), opacité 38 % |
| Chargement | plateau vide avec 8 tuiles grises sans texte, fils absents, texte d'attente mono |
| Erreur | carte blanche dans le plateau, phrase courte + bouton secondaire « Try again » |
| Réussite | bandeau inchangé, grand chiffre 900, fils tous gris et courts |

## 8. Ton et contenu

- UI en anglais, phrases courtes, familières, un peu absurdement vraies. Le nom « Fil » ne se traduit pas.
- Aucune marque réelle, aucune personne réelle, aucun emoji, aucun theming Reddit (pas de mascotte, pas de karma).
