# REFS — Fil

> Références ouvertes le 2026-11-18 dans le navigateur (page d'accueil + défilement, styles calculés relevés sur la page).
> On prend des **principes**, jamais un layout, un texte, un asset ou une marque.

## Raycast — raycast.com

Observé :
- Fond quasi noir (`#07080a`), surfaces posées par **transparence de blanc** (5 %, 10 %, 20 %) plutôt que par des gris pleins. Rayons courts et constants : 6, 10, 12 px.
- Une seule famille sans-serif (Inter) tenue par 3 graisses (400, 500, 600). Titre 64 px / 600 ; sous-titre 20 px / 500 dont la **deuxième phrase est grisée** (`#6a6b6c`) : la hiérarchie se fait par la valeur, pas par la taille.
- Listes denses : lignes à 13 px, étiquettes de section à 11 px en blanc 60 %, champ de recherche en blanc 40 %. Beaucoup d'items, aucun bruit.
- Un **mono** (Geist Mono / JetBrains Mono, 12 px) réservé aux métadonnées : raccourcis, versions, petites étiquettes en capitales. Jamais pour le texte courant.
- Une seule couleur vive, utilisée en touches (étiquette mono, pastilles), jamais en aplat.

À retenir pour Fil :
1. **Densité maîtrisée** : 8 messages doivent tenir dans le cadre sans défiler, en lignes régulières à hauteur fixe.
2. **Hiérarchie par la valeur** : le nom de l'expéditeur, l'heure et l'aide passent en gris ; seul le texte du message est en encre pleine.
3. **Mono = métadonnées** : heures, n° du jour, compteur. Ça colle à la direction de départ (« mono pour les heures »).
4. **Une seule couleur active** et des surfaces par transparence.

## Mobbin — mobbin.com

Observé (la page ne charge pas ses feuilles de style dans le navigateur intégré ; jetons relevés dans le CSS public de la page) :
- Fond blanc, une seule surface grise `#f4f4f4`. Pas de couleur d'interface : la couleur vient des captures d'écran présentées.
- Sans-serif géométrique (Saans) pour l'interface, **un serif (Recital) réservé aux titres** : contraste de deux voix, une calme, une expressive.
- Échelle typo nette et espacée : 12 / 14 / 16 / 20 / 32 / 44 / 60 / 80 px.
- Rayons en familles : 8 px (petits contrôles), 16–20 px (cartes), 32 px et pilule (`9999px`) pour les boutons.
- Mouvement : une courbe dominante `cubic-bezier(.22,1,.36,1)` (sortie rapide, arrivée douce), plus une courbe à rebond `cubic-bezier(.34,1.56,.64,1)` pour les petits retours.
- La bibliothèque d'écrans elle-même (patterns de messagerie) est derrière connexion : **non consultée**. Ce qui suit vient des conventions générales des messageries, pas d'un écran précis de Mobbin.

À retenir pour Fil :
1. **Une seule surface de bulle** (`#f1f2f4` dans la direction de départ, très proche du `#f4f4f4` observé) sur blanc : la bulle se lit sans bordure.
2. **Deux voix typographiques** possibles : une voix calme pour les bulles, une voix expressive pour le titre du jour (exploré en direction 03).
3. **Courbe de mouvement unique** `(.22,1,.36,1)` pour le glisser-déposer, rebond `(.34,1.56,.64,1)` réservé au moment où une bulle se verrouille.
4. **États de conversation** (conventions de messagerie) : nom de l'expéditeur au-dessus de la première bulle d'une série, avatar à initiale, heure en petit, regroupement des messages consécutifs d'une même personne.
