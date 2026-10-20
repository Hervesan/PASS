# Prompt — Générer des contrôles d'entraînement (PASS/LAS Médisup) et les ranger dans « Je m'entraîne »

> À coller dans une nouvelle conversation, avec les pièces jointes listées en section 1.
> Remplace les éléments entre [crochets].

---

## Contexte

Je suis en première année de médecine (PASS/LAS, prépa Médisup Tours/Orléans). Je révise la matière **[NOM DE LA MATIÈRE — ex. Biophysique du milieu intérieur]** (module **[M1/M2/M3/M4]**).
Le contrôle **[nom du contrôle, ex. Contrôle n°2 ou ECB n°1]** du **[date]** porte sur les cours suivants : **[liste des cours du programme, ou capture Médisup Connect jointe]**.

Je veux que tu me génères des sujets d'entraînement sur ce programme, avec leur corrigé (tips réflexes inclus), en PDF, puis que tu les ajoutes à la rubrique « Je m'entraîne » de mon site de révision.

**Avant de rédiger, regarde si la matière a une fiche en section 11 (« Calibrage par matière »).** Si oui, ses consignes **priment** sur les règles générales des sections 2 et 3 pour les points qu'elle traite. Une fiche peut distinguer deux cibles : **contrôle** (contrôle de matière) et **ECB** (examen commun du module). Applique les lignes qui correspondent à la cible de ma demande ; une ligne sans précision vaut pour les deux. Sans fiche, applique les règles générales.

## 1. Pièces jointes

- **Programme du contrôle** : capture(s) Médisup Connect ou liste des cours, avec le **numéro du contrôle Médisup** (vérifie-le sur le planning : c'est lui qui donne le numéro du bloc sur le site).
- **Contrôle modèle** (si j'en ai un) : sujet + corrigé d'un contrôle Médisup officiel, de préférence le plus récent **de la même matière et de la même cible** (contrôle ou ECB) (ex. `controles/BMI_Controle1_Medisup_sujet.pdf`).
- **Fiches de cours** (« FC actu ») ou fiches de synthèse de chaque cours, jointes ou dans mon dépôt GitHub `hervesan/PASS` (`Fiche_visuelle_<cours>.pdf`).
- **Annales classées** (« ACC sujet ») de chaque cours, et leurs **corrigés** (« ACC correc ») si je les ai.
- **Questions d'entraînement / QCM supplémentaires** Médisup (« Questions d'entraînement », « QCM supplémentaires séance n°… »).
- **controles.html** de mon site (et `index.html` si le bouton « Je m'entraîne » n'existe pas encore).

Les PDF sont souvent des scans : lis-les visuellement page par page. Lis **tous** les documents en entier, y compris les « Annales Classées Corrigées Supplémentaires » en fin de fichier, avant de rédiger.

## 2. Règles de contenu (impératives)

1. **Programme strict** : uniquement les cours du programme de ce contrôle. Aucun autre chapitre, même s'il figure dans mes fichiers ou dans les annales jointes.
2. **Fidélité au cours** : chaque proposition doit être vérifiable dans la fiche du cours concerné. Aucune connaissance extérieure, aucune simplification qui change le sens. Si la fiche contredit une connaissance générale, suis la fiche et signale-le-moi en fin de réponse. N'utilise pas une notion présente en annales si elle est absente des fiches, mais liste-la-moi.
3. **Annales ACC et contrôles Médisup officiels = calibrage uniquement** : ils servent à jauger le niveau de difficulté, le type de questions et les pièges. **Aucune question ne doit être proche ou similaire à une question d'annale ACC ou d'un contrôle officiel** : ni même scénario avec d'autres chiffres, ni énoncé reformulé, ni même combinaison de propositions. Les **notions** abordées peuvent être réutilisées, sous un angle ou dans une situation différente (calcul à rebours, mise en situation nouvelle, croisement de deux notions…).
4. **Questions d'entraînement / QCM supplémentaires** : utilisables librement (formats, scénarios, questions liées du type « les questions 11 et 12 concernent… »).
5. **Priorités** : plus de poids sur les notions marquées ★ dans les fiches et sur les cours qui tombent le plus aux annales, tout en couvrant aussi des notions jamais testées.
6. **Contrôles suivants** : si je demande un n°3, n°4…, va chercher d'autres parties du cours et d'autres types de questions que dans les contrôles précédents, sans répéter de question.

## 3. Règles de construction d'un contrôle

1. **Modèle** : reprends le ton, la présentation et le style d'énoncé du contrôle modèle (« QRM. À propos de…, quelles affirmations sont exactes ? »). Sans contrôle modèle, prends le format de mes contrôles déjà présents dans `controles/`.
2. **Nombre de questions** : **[17-18]** par contrôle (c'est moi qui le fixe : ne copie pas le nombre de questions ni la pondération par cours du contrôle officiel) ; durée ≈ 2 min par question.
3. **Toujours 5 propositions** (A à E).
4. **Chaque question indique son type** (« QRM » ou « QRU ») juste avant l'énoncé.
5. **Équilibre QRM/QRU** calé sur le contrôle modèle (ex. 10 QRM / 5 QRU → 11 QRM / 6 QRU pour 17 questions) ; à défaut, environ 60 % de QRM.
6. **Nombre de bonnes réponses** variable d'une QRM à l'autre (de 2 à 4).
7. **Couverture** : tous les cours du programme, dans l'ordre du programme ; répartition indiquée sur la page de garde (ex. « cours X : Q1-3 »).
8. **Mélange des propositions** : dans les QRM, mélange l'ordre des propositions pour que les bonnes réponses ne tombent pas toujours sur les mêmes lettres. Dans les QRU numériques, garde les valeurs par ordre croissant (comme aux annales) mais fais varier le rang de la bonne réponse d'une question à l'autre.
9. **Pièges** :
   - en calcul, chaque mauvaise proposition correspond à une erreur classique (facteur oublié, conversion non faite — mmol/L → mol/m³, °C → K, kJ → J, min → s —, rayon/diamètre, résultat intermédiaire pris pour le résultat final, division au lieu de multiplication…) ;
   - en connaissance, reprends les pièges de formulation des annales : mots absolus (« toujours », « uniquement », « seul », « la totalité »), inversions (sympathique/parasympathique, afférent/efférent, cellules A/B…), chiffres ou unités faussés (millions/milliards, mm/cm, par minute/par seconde), définitions croisées.
10. **Difficulté des calculs — niveau intermédiaire** : ni aussi élémentaires que dans les contrôles Médisup (simples puissances de 10, un seul facteur ×0,2 ou ×2, un nombre entier de périodes), ni des calculs lourds (plusieurs conversions enchaînées, grands exposants à manipuler, relations peu utilisées). Vise une ou deux étapes, avec au plus une conversion d'unité ou un piège de raisonnement par calcul. Une partie des calculs peut être glissée dans des items de QRM, pas seulement dans les QRU.
11. **Calculs faisables à la main** : données « rondes », avec les **mêmes conventions que les annales** (ex. 1 mmHg = 136 Pa avec g = 10 ; K_c = 1,86 ; ω plasma = 300 mosmol/L ; s CO₂ = 0,03 mmol.L⁻¹.mmHg⁻¹ ; pKa bicarbonate = 6,1). Les constantes et valeurs nécessaires vont dans une ligne « Données : ».
12. **Log et exponentielles — varier les situations** : alterne des calculs aux valeurs choisies pour un résultat évident (log 10 = 1, nombre entier de périodes…) et des calculs qui nécessitent une aide numérique. Les deux types peuvent coexister dans un même contrôle ; quand je demande plusieurs contrôles, veille à ce que l'ensemble de la série contienne les deux.
13. **Aides numériques** : un tableau « Calcul / Résultat » **uniquement** pour les calculs non faisables de tête (exponentielles, logarithmes, fractions peu commodes), comme dans les annales Médisup. **Aucune aide** pour un calcul faisable de tête (carrés simples, produits, puissances de 10).

## 4. Corrigé

- Un **tableau récapitulatif** des réponses en tête du corrigé.
- Pour **chaque proposition** : « A. Vrai » / « B. Faux » + justification courte (la règle ou la valeur du cours), avec le calcul complet quand il y en a un.
- Pour les QRU : la bonne réponse + le calcul + d'où vient chacune des principales valeurs pièges.
- Pour chaque question, un encadré **« Tips réflexes »** construit selon la section 5 (pas de fichier séparé pour les tips d'un contrôle généré).

## 5. Tips réflexes (encadré de chaque question du corrigé)

**Où les mettre :**
- **Contrôle généré par toi** : les tips vont uniquement dans le corrigé, en encadré sous chaque question. Pas de fichier séparé.
- **Contrôle dont le corrigé est fourni** (ex. contrôle officiel Médisup, dont on ne modifie pas le corrigé) : les tips vont dans un PDF séparé, `[Matiere]_Controle[N]_Medisup_tips.pdf`. Même contenu et mêmes règles, sous forme de tableau Q | Tip réflexe | Tranche, avec un bandeau de titre bordeaux (#993556) « [Matière] · Contrôle [n°] — tips réflexes », des lignes alternées rose très pâle (#FBEAF0), le numéro de question en gros à gauche et 2 pages au maximum. Vérifie chaque verdict contre le corrigé fourni et aligne-toi sur ses conventions ; signale-moi tout écart.

### Objectif
Pour chaque question, le raisonnement éclair qui permet de valider ou d'éliminer certaines propositions **sans calculer et sans mobiliser de connaissance isolée**. Un tip est de la **méthode**, pas du cours, et ce n'est PAS une correction.

### Ce qu'est un tip (et ce qu'il n'est pas)
- **Oui** :
  - bornes et logique (ex. « Moins d'une période écoulée ⇒ il reste plus de la moitié des noyaux : toute proposition ≤ 0,5 est fausse ») ;
  - raisonnement en facteurs / proportionnalité et sens de variation (ex. « P ÷ 2 ⇒ V × 2 ; T baisse ⇒ V un peu moins : le résultat est entre 2 et 4 L ») ;
  - unités, dimensions, conversions, ordres de grandeur qui écartent les valeurs hors d'échelle ;
  - une **relation « mère » qui regroupe plusieurs formules du cours**, avec la manière de s'en servir (ex. « Retiens P₁V₁/T₁ = P₂V₂/T₂ : elle regroupe Boyle-Mariotte, Charles et Gay-Lussac ; il suffit de barrer ce qui ne change pas ») — c'est le modèle de tip à privilégier : un outil réutilisable qui simplifie le raisonnement ;
  - un fait de cours **uniquement** s'il s'agit d'une règle générale réutilisable (ex. « Une seule particule émise ⇒ spectre de raies ») ou s'il désamorce un piège classique des annales (isochore/adiabatique, sympathique/parasympathique, 511 keV/1,022 MeV, homonymes…).
- **Non** :
  - un fait isolé (ex. « Le photon a un spin 1 », « L'uranium 238 est naturel ») ;
  - un calcul mené jusqu'au résultat : pour une question de calcul, un tip n'apparaît que s'il élimine des propositions sans calculer (encadrement, borne, ordre de grandeur, sens de variation) ;
  - un simple rappel de la convention du corrigé (« Médisup considère que… ») : ça va dans la liste des écarts de fin de réponse, pas dans un tip ;
  - un réflexe sur le nombre de bonnes réponses d'une QRM (« une QRM peut être entièrement vraie », « il y a forcément un faux ») : ce nombre dépend de la matière et de la cible (section 11), ce n'est pas une méthode.
- **Méthode de démarrage type** : pour les questions de calcul ou de lecture de structure, le tip applique à la question les étapes systématiques propres à ce type de problème, toujours les mêmes, pour lancer le raisonnement. Exemples :
  - gaz parfaits : ce qui reste constant → kelvins et pression absolue → raisonner en facteurs → encadrer quand deux effets s'opposent → la fraction ne change pas, seule la pression partielle change ;
  - mécanique (forces, énergie) : système et bilan des forces → ce qui est constant (vitesse constante ⇒ ΔEc = 0 ; sans frottements ⇒ énergie mécanique conservée) → choix de l'outil (théorème de l'énergie cinétique ou conservation) → signe de chaque travail → unités SI ;
  - décroissance radioactive : nombre de périodes écoulées (entier ⇒ ÷ 2ⁿ ; moins d'une période ⇒ plus de la moitié ; remonter le temps ⇒ multiplier) ;
  - atténuation : épaisseur ÷ CDA = n, puis ÷ 2ⁿ ; vérifier si l'on demande la fraction transmise ou atténuée ;
  - charge d'un peptide : ne garder que N-term, C-term et chaînes latérales → charge de départ = nombre de groupes basiques → chaque pKa franchi retire 1 ;
  - formule dessinée : 1 sommet = 1 C, compter à partir du C=O inclus → compter les doubles liaisons dessinées → identifier chaque fonction et chaque liaison ;
  - molécule dessinée non nommée : repérer les fonctions et les motifs caractéristiques (oses et ose aminé, tête polaire, liaison amide ou ester) → en déduire la famille → l'identifier ;
  - schéma réactionnel dessiné : repérer le réactif et ses conditions → prévoir le produit (régiosélectivité, stéréochimie) → comparer au produit dessiné, conditions comprises ;
  - hybridation / VSEPR : sp<sup>x</sup> avec x = nombre de voisins + doublets libres − 1 ; un carbone neutre n'a jamais de doublet libre ;
  - thermodynamique : lire les signes de ΔH et ΔS avant tout calcul (ΔG = ΔH − TΔS) ; convention : ce que le système reçoit est positif.
  Ces méthodes figurent dans le tip de chaque question concernée (pas d'encadré séparé).
- **Question sans tip** : garder l'encadré « Tips réflexes » avec une ligne vide.

### Format
- Dans le corrigé, sous les justifications de chaque question : un encadré rose très pâle (#FBEAF0), titre « Tips réflexes » en bordeaux (#993556).
- Deux colonnes : Tip réflexe | Tranche.
- 0 à 3 tips par question, chacun rédigé en **une ou deux phrases** qui expliquent le raisonnement (pas de formule télégraphique).
- Colonne « Tranche » : les lettres concernées, ✓ en vert (#3B6D11) si validées, ✗ en rouge (#A32D2D) si éliminées.

### Règles de fiabilité (les plus importantes)
1. Uniquement des tips sûrs à 100 %. Mieux vaut moins de tips, voire aucun, qu'un tip approximatif.
2. Pas d'indices seuls : mots absolus, items jumeaux, valeurs multiples ou « presque » ne suffisent jamais. Un mot absolu n'élimine un item que si le tip donne le contre-exemple précis. Un mot absolu peut être vrai.
3. En QRM, éliminer des items ne prouve pas que les autres sont vrais : ne mets ✓ que si le tip le prouve. En QRU, si 4 items sont éliminés, le 5e est validé.
4. Calculs : convertir les unités d'abord ; raisonner sur les chiffres puis sur les puissances de 10. Un ordre de grandeur peut éliminer une proposition hors d'échelle, jamais valider une proposition en QRM.
5. Si tu n'es pas certain d'un item, ne le tranche pas.

### Vérification propre aux tips
- Relis chaque ligne : le tip est-il vrai en général, et pas seulement dans ce contrôle ? Tranche-t-il vraiment ce qu'il annonce ?
- Vérifie chaque verdict ✓/✗ contre ton propre corrigé (ou le corrigé fourni) : aucune contradiction n'est admise.

## 6. Vérifications avant livraison

1. Recalcule chaque réponse avec les formules des fiches et vérifie que chaque distracteur est bien faux.
2. Vérifie chaque proposition dans la fiche du cours concerné.
3. Compare chaque question à **toutes** les questions des annales ACC et des contrôles officiels fournis : aucune ne doit être proche ; remplace celles qui le sont.
4. Vérifie que chaque question relève d'un cours du programme.
5. Vérifie qu'aucune aide numérique ne porte sur un calcul faisable de tête.
6. Si la matière a une fiche en section 11, vérifie que le contrôle la respecte point par point **pour la cible demandée** (contrôle ou ECB) : part de QRU, forme des QRU, durée, nombre de bonnes réponses, formes de questions (molécules dessinées, questions liées, schémas…), niveau des calculs.
7. Applique la vérification propre aux tips (section 5).
8. Si j'ai fourni les corrigés d'annales ou de contrôles officiels, vérifie que tes conventions et raisonnements sont cohérents avec eux et signale-moi tout écart (ex. une valeur du cours différente de celle des annales, ou une notation qui change de sens d'une annale à l'autre).

## 7. Format du PDF

- A4, en-tête « Module [X] – [Matière] » / « Contrôle d'entraînement n°[N] · contrôle Médisup n°[n] du [date] », pagination.
- **Page 1** : titre, encadré (durée, consignes QRU/QRM, répartition QRM/QRU, cours et numéros de questions, mention « calculatrice non autorisée », NOM / Prénom / Note), puis **grille de réponses** (cases a–e, type rappelé à côté de chaque numéro). Les consignes QRM reprennent **mot pour mot** celles du sujet officiel de la matière (section 11).
- **Énoncé** : une question ne doit jamais être coupée entre deux pages ; données en italique sous l'énoncé ; structures dessinées en image vectorielle, lisibles à l'impression. Un énoncé commun à plusieurs questions est annoncé par « Énoncé commun aux questions [n] et [n+1] : » et reste sur la même page que ses questions.
- **Corrigé** : nouvelle page, tableau récapitulatif puis un bloc par question.
- Indices et exposants en vrai format (pas de caractères Unicode ² ₃ qui s'affichent mal).
- Nom de fichier : `[Matiere]_C[n°Médisup]_entrainement[N].pdf` (ex. `Biochimie_C2_entrainement3.pdf`) ; pour un ECB : `[Matiere]_ECB[n]_entrainement[N].pdf`.
- Après génération, **ouvre le rendu** pour vérifier la mise en page.

## 8. Intégration au site — rubrique « Je m'entraîne »

Mon site est un ensemble de fichiers HTML locaux (un `index.html` + un fichier par matière + `formules.html` + `controles.html`). Même style que l'index : fond papier `#F6F4EE`, polices Fraunces / IBM Plex Sans / IBM Plex Mono, une couleur par matière (variables `--c-…`).

- **Bouton sur l'index** (« Je m'entraîne », icône de singe) : il existe déjà ; ne le recrée que s'il est absent.
- **Page `controles.html`** existante : **ne change ni sa structure ni son style**, complète seulement les données en haut du script :
  - `MATIERES` (code, module, titre, couleur, lien vers le fichier matière) : ajoute la matière si elle est nouvelle, avec son icône dans `ICONS` ;
  - `COURS_<MATIERE>` : les intitulés des cours ;
  - `CONTROLES` : **un objet par contrôle Médisup** (`key`, `matiere`, `numero` = numéro du contrôle Médisup, `date` de passage, `programme`, `officiel`, `entrainements`) ;
  - sujet officiel pas encore distribué ⇒ `officiel:null` (la page affiche « Sujet officiel à venir ») ;
  - chaque entraînement : `id` unique, `n` (1, 2, 3… dans l'ordre de création), `date` de création, `nbQ`, `qrm`, `qru`, `duree`, `cours` (cours + notions abordées + numéros de questions), `pdfs`, `note` d'une ligne (page de début du corrigé).
- **Ne modifie jamais l'`id` d'un sujet existant** : le suivi « Fait / Note » enregistré dans le navigateur en dépend.
- Si `controles.html` existe déjà, **ajoute** les nouveaux contrôles sans supprimer les anciens.
- Les PDF sont rangés dans un dossier `controles/` à côté des pages.
- Livraison : `controles.html` (et `index.html` seulement s'il a changé) + un **zip** contenant les pages + le dossier `controles/`.

## 9. En fin de réponse

Brièvement :
- les sources utilisées ;
- les points où la fiche diverge d'une connaissance générale ou des corrigés d'annales / de contrôles officiels ;
- les notions présentes en annales mais écartées parce qu'absentes des fiches ;
- les questions laissées sans tip.

## 10. Quand je fournis un contrôle officiel passé (sujet + corrigé)

1. **Intègre-le** dans le bloc du contrôle correspondant : remplace `officiel:null` par le bloc officiel (Sujet, Corrigé, Tips), avec les numéros de questions par cours dans `programme`. Si le numéro ou la date diffèrent de ce qui était prévu, corrige le bloc sans toucher aux `id` des entraînements.
2. **Fiche Tips** séparée, au format de la section 5.
3. **Autoévaluation** de mes entraînements sur ce programme, comparés au sujet officiel, **menée matière par matière** (un ECB se découpe en autant d'autoévaluations que de matières) :
   - couverture, question par question (préparée directement / partiellement / pas du tout), et liste des notions de l'officiel absentes de mes entraînements ;
   - niveau de difficulté (connaissances et calculs), longueur des énoncés, rythme par question ;
   - typologie : part QRM/QRU, forme des QRU, nombre de bonnes réponses par QRM (minimum, maximum, moyenne), restitution vs application, structures dessinées (nommées ou non), schémas réactionnels, figures à lire, questions liées par un énoncé commun, questions mêlant plusieurs chapitres ;
   - poids de chaque cours dans l'officiel, pour information (je reste maître de la pondération) ;
   - mes erreurs ou formulations douteuses repérées en relisant mes entraînements ;
   - **estimation de la note** : si je réussis mes entraînements (ex. 80 % de questions justes), quelle note puis-je espérer à l'officiel, avec les facteurs qui la font monter ou baisser (rythme, formats inconnus, calculs plus ou moins lourds) ;
   - ce qu'il faut changer pour les prochains entraînements **de cette matière**.
4. **Mets à jour la fiche de la matière en section 11** (crée-la si elle n'existe pas) avec ce que l'autoévaluation a appris, en précisant la cible (contrôle ou ECB) quand les deux sources divergent. **Ne modifie jamais les règles générales des sections 2 et 3** à partir d'un seul contrôle d'une seule matière : chaque matière a son propre style.
5. Signale-moi les **verdicts du corrigé officiel** qui s'écartent d'une connaissance générale ou de la fiche (à retenir « version Médisup » pour le contrôle).

## 11. Calibrage par matière

Chaque fiche ne vaut que pour sa matière et **prime sur les règles générales** pour les points qu'elle traite ; pour tout le reste, les règles générales s'appliquent. Une matière sans fiche suit les règles générales. Quand une ligne précise **[Contrôle]** ou **[ECB]**, elle ne vaut que pour cette cible.

### ECB (examen commun d'un module) — règles communes
*Sources : ECB n°1 du module 1 (17 octobre 2026 : 55 questions en 1h30 — physiologie Q1–27, biophysique Q28–39, médicaments Q40–55) et ECB n°1 du module 2 (17 octobre 2026 : 59 questions en 1h30 — chimie Q1–22, biochimie Q23–49, BMI Q50–59).*
- Une seule épreuve pour tout le module, découpée en parties par matière, sans question transversale entre matières. Sur le site, le sujet et le corrigé officiels sont liés dans le bloc ECB de **chaque** matière, avec une fiche Tips par matière (`[Matiere]_ECB[n]_Medisup_tips.pdf`).
- **Rythme** : ≈ 1,5 à 1,6 min par question en moyenne sur l'épreuve. La durée d'un entraînement ECB se calcule sur ce rythme, sauf si la fiche de la matière en donne un autre.
- **Programme** : l'ECB couvre **tous** les cours du module depuis la rentrée, y compris ceux déjà tombés en contrôle de matière.
- Le nombre de questions de mes entraînements et la pondération par cours restent mon choix ; la fiche de chaque matière donne le poids observé pour information.
- Le style ECB d'une matière peut différer de celui de ses contrôles : se référer à la fiche de la matière.

### BMI — Biophysique du milieu intérieur (M2)
*Sources : contrôle officiel n°1 (15 questions en 30 min) et ECB n°1 du 17 octobre 2026 (10 questions : 6 QRM, 4 QRU), comparés à mes entraînements ECB 1 et 2.*
- **[Contrôle]** Les règles générales ont été calibrées sur ses contrôles ; rythme ≈ 2 min par question.
- **[ECB]** Rythme ≈ 1,5 min par question (mes entraînements à 2 min étaient trop généreux).
- **QRM/QRU** : ≈ 35-40 % de QRU. **[ECB]** Forme des QRU : **toujours une valeur numérique** (pH d'un tampon, hauteur de Jurin, exposants d'une analyse dimensionnelle, énergie).
- **Nombre de bonnes réponses par QRM** : de 2 à 4 (comme la règle générale) ; jamais 1 ni 5 à l'ECB.
- **[ECB] Calculs** : plus simples que mes entraînements. Données choisies pour un résultat rond (log 10 = 1, √81 = 9, puissances de 10), une seule aide donnée dans l'énoncé (ex. √2 = 1,4), aucun tableau log 2 / log 3. Une à deux étapes, une conversion au plus (mm → m). À éviter en préparation ECB : incertitudes sur un produit de puissances, débit à travers N pores, Jurin avec cos α, dérivée seconde de E<sub>p</sub>, dimensions à quatre grandeurs. Au plus un calcul avec aide numérique par entraînement ECB.
- **[ECB] Questions liées** : prévois un **énoncé commun à deux questions** (ECB : un satellite → énergie totale à l'entrée dans l'atmosphère, puis E<sub>p</sub>, E<sub>c</sub> et vitesse plus bas), au format « Énoncé commun aux deux questions suivantes ».
- **Mises en situation** : cas clinique court (hématies plongées dans NaCl + urée, gaz du sang d'une patiente qui vomit), questions de concept (propriétés colligatives, osmose passive, membrane hémiperméable), unités et dimensions.
- **Couverture observée à l'ECB** : grandeurs et unités 2, énergie 2, pH et acido-basique 2, colligatives 3, mécanique des solutions 1, **cinétique des solutions 0**. Ne supprime pas la cinétique (un seul ECB), mais n'y mets pas plus de poids qu'aux autres cours.
- **Point de cours à vérifier dans la fiche** : mon entraînement ECB n°2 (Q28 D) affirme qu'en mouillage parfait le ménisque est plat ; physiquement il est hémisphérique. Vérifie la formulation exacte du poly avant de réutiliser cette notion.

### Physiologie (M1)
*Sources : contrôle officiel n°2 (24 questions : 17 QRM, 7 QRU, 30 min) et ECB n°1 du 17 octobre 2026 (27 questions : 23 QRM, 4 QRU), comparés à mes entraînements ECB 1 à 6.*
- **Durée** : ≈ 1,3 à 1,6 min par question.
- **QRM/QRU** : ≈ 20 % de QRU (et non un tiers). Forme des QRU : moitié valeur numérique (calcul), moitié 5 affirmations dont une vraie.
- **Nombre de bonnes réponses par QRM : de 2 à 5** ; prévois de temps en temps une QRM à 5/5 (l'ECB en avait une, Q1).
- **Questions liées** : un scénario commun pour 2 ou 3 questions de calcul (ex. ECB : un cycliste → dépense de repos au sac de Douglas, bilan énergétique de régimes, travail au pédalier). C'est le format type des calculs de bioénergétique.
- **Calculs** : simples, nombres ronds, une à deux étapes, aucune aide numérique (log 10 = 1 dans Henderson-Hasselbalch). Garde le niveau intermédiaire de la règle générale, mais limite les aides numériques en physiologie.
- **Registre** : environ 80 % de restitution directe, énoncés courts (« À propos du cortisol : », « Concernant la filtration glomérulaire : »), items d'une ligne.
- **Pièges** : le mot unique inversé domine (couches/colonnes, préfrontal/occipital, cortico-/médullosurrénale, circadien/ultradien, négativement/positivement, augmente/diminue, ouverte/fermée, unidirectionnel/bidirectionnel, stocke/acquiert, lisse/strié, intérieur/extérieur).
- **Formulations à double lecture** : Médisup pose des items du type « est diminué en cas de… », « peut présenter… » — un « peut » valide l'item dès qu'un cas du cours le permet.

### BAM (M1)
*Sources : contrôle officiel n°1 (19 questions : 16 QRM, 3 QRU, 30 min) et ECB n°1 du 17 octobre 2026 (12 questions : 10 QRM, 2 QRU), comparés à mes entraînements ECB 1 à 4.*
- **Durée** : ≈ 1,6 min par question.
- **QRM/QRU** : ≈ 15 à 20 % de QRU (et non 25 %). Forme des QRU : une valeur numérique (calcul simple).
- **Nombre de bonnes réponses par QRM** : de 2 à 4 (comme la règle générale).
- **Calculs officiels très simples** : nombre entier de périodes (1/4 ⇒ 2 T), Q = mL avec une fraction ronde, PV = nRT avec des données rondes et R = 8, pression partielle = fraction × P. Aucune aide numérique. Garde le niveau intermédiaire, mais au plus un calcul avec aide numérique par entraînement.
- **Tableaux de données à interpréter** : prévois une question sur un tableau (ex. T1/T2 de plusieurs tissus → hypersignal/hyposignal selon la pondération).
- **Registre** : surtout restitution, chaque cours tiré par une question de généralités (quarks, transformations, écrans, effets, radioprotection, réfraction).
- **Pièges** : définitions croisées (somatique/héréditaire, déterministe/stochastique, Gy/Sv, gluon/graviton, β⁻/capture électronique, excès de neutrons/de protons, électrons/photons).

### Médicaments (M1)
*Source : ECB n°1 du 17 octobre 2026 (16 questions : 14 QRM, 2 QRU). Aucun entraînement encore fait dans cette matière.*
- **Durée** : ≈ 1,6 min par question.
- **QRM/QRU** : ≈ 12 % de QRU. Forme des QRU : 5 affirmations dont une vraie (raisonnement sur des K<sub>D</sub>, définition d'une forme pharmaceutique).
- **Nombre de bonnes réponses par QRM** : de 2 à 4.
- **Énoncés** : début de phrase à compléter (« Un antagoniste non compétitif », « La voie orale »), items d'une ligne. Pas de calcul ; au plus une question de lecture de valeurs (K<sub>D</sub>, CE50) qui se tranche par comparaison.
- **Contenu** : environ la moitié en pharmacologie des cibles (récepteurs canaux, RCPG, récepteurs-enzymes, transporteurs, enzymes, agonistes/antagonistes, K<sub>D</sub>/CE50), le reste en définitions réglementaires (définition du médicament, génériques, DCI, substances vénéneuses) et en dose/dosage/formes/voies.
- **Pièges** : mots absolus réfutés par un contre-exemple du cours (« toutes », « tout », « uniquement », « réservées » : Doliprane®/Efferalgan®, morphine, paracétamol), et mot inversé (dose/dosage, unitaire/multidose, vaginale/rectale, active/inhibe, PPSE/PPSI, augmente/diminue, OMS/laboratoire).

### Biochimie (M2)
*Sources : contrôle officiel n°2 du 7 octobre 2026 (22 questions : 18 QRM, 4 QRU, 30 min), comparé à mes entraînements 1 et 2 ; ECB n°1 du 17 octobre 2026 (27 questions : 21 QRM, 6 QRU), comparé à mes entraînements ECB 1 à 4.*
- **Durée** : ≈ 1,4 min par question (contrôle) ; ≈ 1,5 min **[ECB]**.
- **QRM/QRU** : ≈ 20-22 % de QRU. Forme des QRU : surtout 5 affirmations dont une vraie ; au plus une QRU à valeur numérique (type 20ⁿ) ou de classement (ordre d'élution).
- **Nombre de bonnes réponses par QRM** :
  - **[Contrôle]** de 1 à 5 : prévois au moins une QRM à 4 et, de temps en temps, une QRM à 5/5 (le contrôle n°2 en avait deux). Les consignes de la page de garde n'annoncent aucune fourchette (« QRM : une ou plusieurs propositions exactes »).
  - **[ECB]** de 2 à 4 seulement : les 21 QRM de l'ECB avaient 2, 3 ou 4 bonnes réponses (moyenne ≈ 2,8), aucune à 1 ni à 5/5. Mes entraînements ECB qui avaient des QRM à 5/5 ou à 1 réponse étaient hors cible.
- **Registre** : environ la moitié des questions en **restitution directe** (énoncé court du type « La liaison peptidique : », propositions brèves tirées du cours), le reste en application.
- **Fondamentaux d'abord** : chaque cours a ses questions de généralités (définitions, propriétés, classifications). En enzymologie en particulier : réaction spontanée, énergie d'activation, effet de la température, vitesse = pente, hypothèses de Michaelis-Menten, Km = concentration et affinité. Un cours ne doit pas être traité uniquement par des calculs. **[ECB]** L'enzymologie y était entièrement conceptuelle (allostérie, hypothèses de Michaelis-Menten, ce que donne la représentation de Lineweaver-Burk) : au plus un calcul d'enzymologie (kcat, intercepts) par entraînement ECB.
- **Détails pointus** (dates, auteurs, numéros de résidus, sous-types rares, valeurs chiffrées isolées comme un nombre de gènes ou une durée en années) : au plus une proposition par question.
- **Pièges** : surtout le **mot unique inversé** (transcription/traduction, avant/après, augmentée/diminuée, plus/moins, ω3/ω6, 6/8 atomes, 0°/180°, céramides/cérides, nucléoside/nucléotide, N-/O-glycosidique, intérieur/surface).
- **Structures dessinées** :
  - en lipides, une ou deux questions sur une formule topologique (glycérophospholipide, triglycéride, sphingomyéline) : compter les carbones et les doubles liaisons, identifier les liaisons ester, amide ou phosphoester, nommer les acides gras ;
  - **[ECB] molécule non nommée** : l'ECB pose « La molécule ci-dessous : » sans donner son nom (acide hyaluronique en motif répété, glutamine en Fischer zwitterionique, phosphatidyléthanolamine, sphingomyéline, galactose en Haworth simplifié sans OH écrits). Prévois au moins deux questions par entraînement ECB où il faut d'abord **reconnaître** la molécule ; ne donne pas le nom dans l'énoncé.
- **[ECB] Figures et données à lire** : prévois une question sur un tableau de pKa (dont chaînes latérales) avec un chromatogramme à interpréter (ordre d'élution sur échangeuse d'ions, à déduire des pHi), et, de temps en temps, une représentation 3D en ruban d'une protéine (hélices α, feuillets β, structure tertiaire).
- **[ECB] Calculs et raisonnements types** : combinatoire (20ⁿ), composition d'un ADN double brin (Chargaff, nombre de bases, **liaisons phosphodiester par brin = n − 1**), séquençage d'un peptide par enzymes et réactifs (aminopeptidase, carboxypeptidase, bromure de cyanogène, chymotrypsine).
- **Énoncés** courts : pas de longue mise en situation quand une phrase suffit.

### Chimie (M2)
*Sources : contrôle officiel n°1 du 7 octobre 2026 (14 questions : 9 QRM, 5 QRU, 30 min), comparé à mes entraînements 1 à 3 ; ECB n°1 du 17 octobre 2026 (22 questions : 12 QRM, 10 QRU), comparé à mes entraînements ECB 1 à 4.*
- **Durée** : ≈ 2 min par question **[Contrôle]** ; ≈ 1,5 min **[ECB]** (mes entraînements ECB à 2 min étaient trop généreux).
- **QRM/QRU** : ≈ 35 % de QRU **[Contrôle]**, ≈ 45 % **[ECB]**. Forme des QRU : **5 affirmations dont une seule vraie** ; aucune QRU à valeur numérique isolée. Les calculs se glissent dans une proposition.
- **Nombre de bonnes réponses par QRM** : de 2 à 4 ; **[ECB]** surtout 2 ou 3 (aucune QRM à 4 dans l'ECB n°1), jamais 1 ni 5.
- **Intitulés** : questions titrées par grand chapitre (« QRU. Atomistique. », « QRM. Thermodynamique. ») dont les propositions mêlent plusieurs notions du chapitre (atome + liaisons + VSEPR dans une même question). **[ECB]** Prévois aussi une ou deux questions **à cheval sur deux chapitres** (« QRU. Atomistique – Thermodynamique. » : ordre de liaison de B<sub>2</sub>, VSEPR, transformation cyclique, variable intensive, système fermé dans la même question).
- **Calculs** : les calculs officiels se résolvent par la **lecture des signes** (ΔH et ΔS → signe de ΔG ; convention de signe de W ; ΔU = Q + W avec des nombres ronds ; sens de déplacement selon Le Chatelier ; K > 1 ⇔ ΔG° < 0 ; Van't Hoff qualitatif). Garde le niveau intermédiaire de la règle générale, mais une bonne part des questions de thermodynamique doit se trancher sur les signes. **[ECB]** **Aucun calcul en atomistique** (rayon de Bohr, longueur d'onde, Heisenberg, quantité de matière) : au plus un calcul d'atomistique par entraînement ECB ; en thermodynamique, au plus un calcul chiffré, le reste en signes.
- **Atomistique** : couvre aussi les exceptions de configuration (Cu : 4s<sup>1</sup> 3d<sup>10</sup>), les ions d'éléments de transition (Zn<sup>2+</sup> : électrons retirés de 4s), le magnétisme d'ions diatomiques (O<sub>2</sub><sup>−</sup>, N<sub>2</sub><sup>+</sup>), l'électronégativité nulle des gaz rares.
- **Stéréochimie et nomenclature : uniquement sur des molécules dessinées.** Prévois sur ces cours :
  - une molécule d'intérêt médical en Cram (coins pleins et hachurés) : fonctions présentes, nombre de C*, R/S, Z/E, nombre de stéréoisomères, chiralité, (+)/(−), effet inductif d'un groupement, hybridation des carbones ;
  - un ose ou un acide aminé en Fischer : D/L, R/S d'un carbone, nombre de C*, piège (+)/lévogyre et énantiomère pur/racémique ;
  - une série de 4 à 5 petites molécules en formule topologique à nommer, avec les descripteurs (R/S, Z/E) dans le nom ;
  - des pièges de lecture : un coin dessiné sur un carbone qui n'est pas asymétrique (deux substituants identiques), un éther à ne pas confondre avec un ester, une amine à côté d'un ester ou d'une cétone, une double liaison terminale ou géminée diméthylée qui n'est ni Z ni E.
- **[ECB] Alcènes et alcynes : schémas dessinés.** L'ECB a posé ces cours sous trois formes, à reproduire :
  - « Parmi les enchaînements réactionnels suivants, lesquels conduisent majoritairement ou exclusivement aux produits proposés ? » : 5 réactions indépendantes, réactif + conditions → **produit dessiné** ;
  - une série de molécules dessinées et lettrées (F, G, H, I, J) avec des items du type « le traitement de F par … conduit majoritairement à G » ;
  - une séquence lettrée (prop-1-yne → G → H → I avec NaNH<sub>2</sub>, halogénoalcane, H<sub>2</sub>SO<sub>4</sub>/Hg<sup>2+</sup>) dont il faut identifier chaque intermédiaire et chaque type de réaction.
  Ne nomme pas le produit en toutes lettres quand il peut être dessiné.
- **[ECB] Pièges de conditions** : le produit est juste mais les conditions sont fausses (eau seule sans acide, H<sub>3</sub>O<sup>+</sup> au lieu d'une base forte pour la double déshydrohalogénation, KMnO<sub>4</sub> concentré à chaud dessiné comme donnant un diol, nickel de Raney donnant un alcène Z au lieu de l'alcane, hydrogénation d'un cycle benzénique à température et pression ordinaires), ou le produit est faux pour des conditions justes (alcynure + CO<sub>2</sub> dessiné en cétone, hydroboration dessinée en cétone).
- **Pièges** : le mot inversé domine (n / n + ℓ, période / famille, électronégativité / énergie d'ionisation, chlore / fluor, halogènes / gaz rares, Debye / London, −273 K / 0 K, ΔG / ΔG°, réversible / irréversible, pression / volume constant, lévogyre / dextrogyre, amine / amide, latéral / axial, émet / absorbe, catalytique / chimique).

## 12. Ma demande pour cette fois

**[Ex. : Génère les contrôles d'entraînement n°1 et n°2 de Chimie pour le contrôle Médisup n°3 sur le programme joint, puis ajoute-les à « Je m'entraîne ».]**
