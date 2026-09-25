# PROMPT MAÎTRE — Fiches formules d'un ou plusieurs cours

> **Mode d'emploi**
> Copie tout ce prompt dans une nouvelle conversation et joins :
> 1. **le ou les PDF de cours** (fiche de cours et/ou fiche de synthèse visuelle). Tu peux joindre **plusieurs cours d'un coup** ;
> 2. **`index.html`** (pour les matières, les modules et les couleurs) ;
> 3. **`formules.html`** (la liste des cours à mettre à jour) — **obligatoire** ;
> 4. **les 2 fichiers modèles** : `formules-colligatives.html` et `formules-colligatives-explications.html` (référence exacte pour le code et le style) — **obligatoires** ;
> 5. facultatif : les **annales corrigées** du cours (sujet + correction), pour illustrer les astuces et les pièges.
>
> Rien d'autre à remplir : tout se déduit des pièces jointes.

---

## Ce que tu dois déduire des pièces jointes

- **Titre du cours**, **matière** et **module** : à lire dans le PDF du cours (en-tête, titre, mention « Module X »).
- **Couleur de la matière** : à reprendre dans `index.html` (variable `--c-…` utilisée par cette matière dans le tableau `MODULES`, avec le même titre de matière et le même module que sur l'index).
- **Nom court pour les fichiers** : dérivé du titre du cours, en minuscules, sans accents ni espaces (ex. « Propriétés colligatives » → `colligatives`, « Systèmes gazeux » → `gazeux`, « Effets biologiques des rayonnements ionisants » → `effets-biologiques`).
- Si la matière du PDF ne correspond clairement à aucune matière de l'index, ou si plusieurs sont possibles, **demande-moi avant de continuer**.
- Si `formules.html` ou les fichiers modèles manquent, **demande-les avant de générer** (ne pas reconstruire le style « de mémoire »).
- Les PDF peuvent être des **scans** (pas de texte sélectionnable) : les lire comme des images, page par page, sans en sauter.
- Rappelle-moi en une ligne, au début de ta réponse, ce que tu as identifié (cours · matière · module · couleur · nom de fichier ; une ligne pour l'ensemble si plusieurs cours).

---

## Ce que je veux

À partir du PDF, crée les fiches formules de ce ou ces cours en reprenant **exactement** le système déjà construit pour « Propriétés colligatives » (fichiers modèles joints). **Méthode imposée** : partir du code des deux fichiers modèles et ne remplacer que les données (titre, sur-titre, tableau `data`, encart du fil, moyens mnémotechniques, liens). Le code, la mise en page et les comportements restent identiques.

Livrables (par cours) :

1. `formules-<nom-court>.html` : la **page tableau 2 colonnes** (page d'entrée du cours).
2. `formules-<nom-court>-explications.html` : la **page d'explication**.

Et une seule fois :

3. `formules.html` mis à jour : ajouter le ou les cours dans la liste (bonne matière, bon module, couleur de l'index ; créer la matière si elle n'existe pas encore dans la liste), dans l'ordre des fiches de cours.
4. **Ne pas** modifier `index.html` (le bouton « Mes formules » existe déjà et pointe vers `formules.html`).

Livre les fichiers à télécharger (pas de publication en lien claude.ai), car je les dépose dans mon dépôt GitHub. Tous les liens entre pages doivent être **relatifs** (même dossier). Lors d'une correction, ne relivre que les fichiers qui ont changé.

---

## Qu'est-ce qu'une « formule » ? (impératif)

Une formule, c'est **quelque chose qui peut donner lieu à un calcul**.

- **À garder** : les relations mathématiques (égalités, lois, proportionnalités exploitables comme τ ∝ Z³/E³), les **constantes et conversions d'unités** (1 atm = 101 325 Pa, 1 eV = 1,602.10⁻¹⁹ J, masses des particules…), et les **valeurs numériques du cours qui servent dans un calcul** (P<sub>Vsat</sub> à 37 °C, facteurs W<sub>R</sub> et W<sub>T</sub>…).
- **À exclure** : les définitions, classifications et notions qualitatives, même si elles s'écrivent avec un « = » (isotopes / isobares / isomères, méson = quark + anti-quark, spin, liste des changements d'état exo/endo, point triple, « portée < parcours », domaines de prépondérance des effets, « D₀ élevée = cellule radio-résistante »…).
- Si une notion qualitative est indispensable pour comprendre une formule gardée, la mentionner **dans l'explication** de cette formule, pas comme item.
- **Contenu rayé = hors programme** : ne prendre **aucune** formule, valeur ou notion barrée dans le PDF (texte rayé, cadre ou schéma barré d'une croix), même partiellement lisible. Ne pas s'en servir non plus dans les explications, le fil ou les moyens mnémotechniques. Si une formule gardée ne se comprend qu'avec un élément rayé, me le signaler dans la réponse.

---

## Règles de fidélité (impératives)

- Toutes les formules, unités, constantes, exemples et valeurs viennent **exclusivement** du ou des PDF fournis (fiches de cours, et annales si elles sont jointes). Aucune connaissance extérieure, aucune simplification qui change le sens.
- Si une valeur utile manque dans le PDF (ex. unités d'une formule, valeur d'une constante), **ne pas l'inventer** : la laisser de côté et me le signaler dans la réponse.
- Si le PDF contient une **erreur ou une incohérence** (formule qui contredit le texte, valeurs différentes entre deux fiches, notation ambiguë comme « log » pour ln), ne pas corriger en silence : l'indiquer dans un ⚠️ de l'explication **et** dans ma réponse.
- Seule exception : on peut expliquer **le sens des symboles** d'une formule (ex. ρ = masse volumique, g = pesanteur) pour que la formule soit compréhensible.
- Les exemples chiffrés des **annales jointes** peuvent illustrer les 💡 et ⚠️ (en citant l'année).
- **Étoiles ★** = notion tombée au concours : reprendre exactement le nombre d'étoiles indiqué dans le PDF (1 à 3). Si le PDF ne contient aucune indication d'étoiles, n'en mets aucune et signale-le-moi (ne jamais les inventer). Étoiles **dorées/jaunes** (`#e8a900`), jamais noires.
  - Une étoile ne va sur une formule que si elle porte **sur cette formule ou sur la notion qu'elle exprime**. Si l'étoile porte sur une notion voisine (ex. « nécessite un chauffage ★ » à côté de « 100 °C à 1 bar »), ne pas l'attribuer à la formule : la mentionner dans l'explication.
  - Une formule étoilée reste une **formule de base** (pas une déduite), sinon elle disparaît du filtre « ★ Concours ». Si elle se retrouve par calcul, le dire dans son explication.
  - Pas de caractère ★ dans les champs `u` (unités) : les étoiles passent uniquement par `st`.
- Les **formules déduites** sont des formules qu'on obtient par calcul direct à partir d'autres formules du cours (substitution, isolement d'une variable, cas particulier α = 0 / α = 1, somme, différence…). Chaque formule déduite = **un item à part entière**, placé juste après sa formule mère, avec :
  - la liste des formules dont elle vient (formule mère en premier) ;
  - les étapes « Comment la retrouver » (2 à 3 étapes courtes).

---

## Organisation du contenu

- Sections **A, B, C, D, E…** qui suivent l'ordre logique du cours, chacune avec un titre et ses pages de référence (ex. « p.4-5 »). Pas de section avec une seule formule : la fusionner avec une section voisine.
- Couleurs de section : A `#2f86a8`, B `#d0632e`, C `#c9971c`, D `#6f5aa8`, E `#a64b4b`, F `#b0527f` (ajouter `--F` dans les deux pages, et `#F{--sec:var(--F)} #F h2{background:var(--F)}` dans la page explication, seulement si une 6ᵉ section existe). Vert des formules déduites : `#3f9a6a`.
- Numérotation continue par section : A1, A2… B1, B2… (formules déduites comprises).
- Pour chaque formule : `k` (identifiant), `st` (étoiles 0-3), `q` (nom / question), `d` (courte définition), `f` (formule), `u` (unité, constante, valeur), `x` (explication, page explication uniquement), `der` (liste des formules mères si déduite).
- **Nom `q` neutre** : le nom ne doit pas contenir la réponse, puisqu'il reste visible en mode 🙈 (ex. « Seuil des paires et énergie de masse de l'électron » plutôt que « Pourquoi 1,022 MeV = 2 × 511 keV »).
- **Fractions** : tout quotient s'écrit numérateur au-dessus du dénominateur (`<span class='frac'><span>num</span><span>dén</span></span>`, ou le raccourci `fr(num, dén)` défini avant `data`), sans parenthèses au dénominateur. Les unités (g/L, mol/kg…) restent en ligne.
- **Notation des noyaux** (si le cours en a) : A et Z empilés à gauche du symbole via le raccourci `nuc(A, Z, "X")`, qui produit `<span class='nw'><span class='nuc'><span>A</span><span>Z</span></span>X</span>`, avec le CSS `.nw{white-space:nowrap}` et `.nuc{display:inline-flex;flex-direction:column;align-items:flex-end;vertical-align:middle;font-size:.58em;line-height:1.05;margin-right:.1em}` ajouté aux deux pages.
- Indices en `<sub>`, lettres grecques en caractères Unicode (ω, π, Δ, θ, α, Σ, ρ).
- Les références `@k` dans les explications doivent toutes pointer vers une formule existante.

---

## Page 1 — Tableau 2 colonnes (`formules-<nom-court>.html`)

**Vue de référence (par défaut)**
- En-tête : petit sur-titre (module · matière, repris de l'index), grand titre du cours, ligne « N formules · ★ tombées au concours · 🔁 formules déduites, reliées à leur formule de base ».
- Barre de boutons (collante en haut) : **🙈 Cacher les formules**, **← Cours** (lien vers `formules.html`, poussé à droite), **📖 Explications** (lien vers la page explication).
- Une étiquette de colonnes au-dessus : « Définition » / « Formule · unité · constante ».
- **Un bloc par section** : coins arrondis (16px), ombre douce, fond de page légèrement grisé pour faire ressortir les blocs ; en-tête du bloc teinté de la couleur de section, avec la lettre dans une pastille carrée colorée.
- Chaque ligne = 2 colonnes :
  - gauche : petit code coloré (A1…) au-dessus du nom en gras, étoiles dorées ; les lignes étoilées ont un léger dégradé doré côté définition ;
  - droite : formule en grand (police STIX Two Text, gras) sur fond teinté de la couleur de section, unité/constante en dessous dans une petite étiquette arrondie (radius 8px, pas en pilule).
- **Petit espace (6px, gris) entre chaque formule principale** (avec ses déduites).
- **Formules déduites** (comme la page explication) : chacune dans sa **propre carte**, décalée à droite sous sa formule mère, cadre vert fin, reliée par un **trait vert fin** (vertical + petit trait horizontal) partant de la formule mère ; mention « 🔁 Déduite de **B2** » sur une seule ligne au-dessus du nom. **Texte et fond identiques aux autres formules** (ne pas les mettre en vert, elles ne doivent pas ressortir davantage). Les cartes déduites sont un peu **plus étroites** (marge à droite).
- **Tous les traits verticaux définition / formule sont alignés** sur toute la page, formules déduites comprises (utiliser `container-type:inline-size` sur le bloc et `grid-template-columns: 42cqw …` ; pour les cartes déduites, retrancher le décalage).

**Mode 🙈 (entraînement)** — **reprendre tel quel le code du modèle `formules-colligatives.html`, qui me convient parfaitement ; ne rien réécrire.** Pour mémoire, ce qu'il fait :
- Le bouton devient « ↩ Revenir à la page de référence ». La page de référence est masquée et remplacée par un **tableau neutre** :
  - **aucun repère** : pas de sections, pas de codes, pas de mention « déduite », pas de décalage, pas l'étiquette de colonnes ni la ligne de légende de l'en-tête ;
  - **toutes les formules mélangées** aléatoirement (nouvel ordre à chaque ouverture) ;
  - **étoiles conservées** (★ dorées, léger fond doré, cadre doré) ;
  - numéros 1, 2, 3… qui suivent simplement l'ordre du tirage.
- Panneau « Entraînement » en haut : compteur « X / N révélées », barre de progression dorée, boutons **🔀 Mélanger** et **🙈 Tout recacher**.
- Chaque formule = une carte arrondie avec ombre ; côté formule floutée avec « 👁 Révéler » au centre ; un toucher révèle formule + unité (fond vert clair, numéro qui passe au vert).

---

## Page 2 — Explication (`formules-<nom-court>-explications.html`)

- En-tête : titre « <Cours> : les formules », sous-titre (module · matière · formules expliquées), légende (★ tombée au concours, d'après la fiche de cours · ★★★ la plus fréquente · 🔁 formule déduite = cadre vert).
- Barre de boutons : **← Tableau des formules** (lien vers la page 1), **🙈 Réviser (vue épurée)**, **★ Concours**, **Sans les déduites**, compteur.
- **Encart « Le fil qui relie tout »** (fond doré clair, barre dorée à gauche) : une ligne qui enchaîne les formules clés du cours avec des flèches (uniquement des formules présentes dans la page).
- **Encadré « Moyens mnémotechniques »** : 6 à 10 astuces courtes tirées du cours et portant sur les formules gardées (2 colonnes sur ordinateur, 1 sur téléphone).
- Sections colorées A à E (F si besoin) avec leurs pages de référence.
- **Cartes** : cadre de 2px gris-bleu (`#b9c0cc`) **d'épaisseur identique sur les 4 côtés** (ombre douce sans décalage), coins arrondis, espace généreux entre cartes. Dans la carte :
  - haut : définition (code coloré, étoiles, nom, définition courte, « 🔁 Déduite de … » si déduite) et formule (grande, avec unité) **côte à côte** sur ordinateur, **l'une sous l'autre** sur téléphone ;
  - bas : explication sur toute la largeur, en texte gris discret ;
  - séparations intérieures : **traits pleins de 1,5px** de la couleur du cadre (pas de pointillés, pas de gros trait coloré).
- **Explication** de chaque formule : 2-3 phrases qui disent ce que la formule signifie concrètement, puis `💡` astuce/moyen mnémotechnique, `⚠️` piège (dont les pièges des annales et les incohérences du PDF), et pour les déduites un encadré vert clair **« 🔁 Comment la retrouver »** avec les étapes numérotées.
- **Arbre** : les formules déduites sont décalées sous leur formule mère, reliées par un trait vert fin (vertical + horizontal) ; les connecteurs ne s'appliquent qu'aux enfants directs (`.tree > li`) pour ne pas toucher aux listes d'étapes.
- **Mode 🙈 de cette page (différent de la page 1, c'est voulu)** : vue épurée floutée, les cartes restent à leur place ; masquer explications, encart du fil, moyens mnémotechniques, légende et « Déduite de » ; garder visibles le nom **et** la définition ; flouter formule + unité ; un toucher sur la carte révèle. Revenir en haut de page au changement de vue.
- **★ Concours** : n'afficher que les formules étoilées. **Sans les déduites** : masquer les formules déduites.

---

## Page 3 — Liste des cours (`formules.html`)

- Ajouter chaque cours dans le tableau `MATIERES` en haut du script : `{ title:"<cours>", info:"N formules", href:"formules-<nom-court>.html" }`, dans la bonne matière (titre, module, couleur de l'index). Créer la matière si besoin. N = nombre total de formules (déduites comprises).
- Ne rien changer d'autre au style de la page.

---

## Style commun et contraintes techniques

- Polices : Source Sans 3 (texte) et STIX Two Text (formules), via Google Fonts, avec polices de secours.
- Mode sombre géré (variables CSS sous `prefers-color-scheme: dark`).
- Page responsive, **vérifiée à ~390px de large** (téléphone) et sur ordinateur : rien ne doit déborder ni se superposer ; les équations longues (noyaux) ne doivent pas se couper au milieu d'un symbole.
- Vérifier aussi : aucune erreur JavaScript, le mode 🙈 de la page 1 (N cartes, compteur, révélation), et qu'aucune référence `@k` ne reste affichée telle quelle.
- Pièges déjà rencontrés à éviter :
  - une règle de colonnes pour ordinateur ne doit pas écraser la mise en page téléphone (placer les grilles desktop dans `@media (min-width:…)` ou réaffirmer la grille mobile) ;
  - une ancienne règle de flou ne doit pas empêcher la révélation (vérifier la priorité CSS) ;
  - pas d'ombre décalée qui épaissit le bas d'un cadre ;
  - pas de `localStorage` indispensable au fonctionnement.

---

## Réponse attendue

1. Une ligne : cours · matière · module · couleur · nom de fichier identifiés.
2. Les fichiers à télécharger.
3. Un court résumé par cours : nombre de formules de base, nombre de formules déduites, sections créées (un tableau si plusieurs cours).
4. La liste des éléments rayés écartés (une ligne par cours, s'il y en a).
5. La liste de ce qui manquait ou posait problème dans le PDF (valeurs non données, incohérences, notations ambiguës, cours sans étoiles sur les formules), s'il y en a.
