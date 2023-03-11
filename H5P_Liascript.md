
<!--

title: H5P et LiaScript, écrire des ressources éducatives libres

email: damien.belveze@univ-rennes1.fr 

language: fr 

@Jonas: French Male

comment: ce support a été présenté dans le cadre du Stretching Numérique (https://stretchingnumerique.fr) le 17 mars 2023

-->

# Stretching Numérique : H5P et Liascript

[![course badge](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://LiaScript.github.io/course/?https://raw.githubusercontent.com/damienbelveze/Liascript/main/H5P_Liascript.md#1)

## Introduction au H5P 




              --{{1 @Jonas}}--
H5P (HTML-5 Package) est un logiciel libre basé sur HTML5 et JavaScript développé depuis 2014

On peut éditer des activités avec H5P au moyen d'éditeurs téléchargeables ou bien à partir de Moodle (si le plugin pour H5P a bien été implémenté par votre gestionnaire Moodle)

Dans le cadre de cet atelier, nous vous proposons d'utiliser l'éditeur **Logiquiz** publié par le collectif La Digitale [^1]

[lien de téléchargement de Logiquiz](https://ladigitale.dev/logiquiz/)

- télécharger le logiciel et l'ouvrir
- observer la palette des activités H5P disponible

![console de Logiquiz](images/logiquiz1.PNG)

Toutes les activités H5P peuvent être exportées en format H5P ou en format HTML.

Le H5P, que ce soit à travers Moodle ou en dehors ne permet pas de collecter des **traces d'apprentissage**[^2]


[^1]:téléchargeable sans droit d'administrateur sur le poste. 
[^2]: Dans Moodle, pour collecter des traces d'apprentissage, il faut plutôt utiliser des activités 
comme les **tests**

**H5P apporte de l'interactivité, mais pas du suivi d'étudiant.**

### création d'un quiz avec H5P 

on va se limiter à des choses simples. 
Essayez de créer une question à choix multiple avec H5P

Exporter votre quiz en HTML et envoyez-le sous ce format dans [ce répertoire](https://uniren1-my.sharepoint.com/:f:/g/personal/damien_belveze_univ-rennes1_fr/EnxZV03hOENMi_mfQ8MkYLEB-YEjUczleP13rsgAYYGAoQ?e=Rsny3P)

### Charger un quiz dans Moodle 

!?[charge un quiz dans Moodle](images/video.mp4)

## Introduction à LiaScript

LiaScript est un logiciel qui s'inscrit dans le mouvement des OER (*Open Educational Resources*), ou REL (*Ressources éducatives Libres*) en français. 

![Ressources Educatives Libres](images/REL.png)

L'idée est de permettre à n'importe qui de créer un cours en ligne partageable seulement avec un éditeur de texte et un navigateur. Liascript interprête le texte pour qu'il s'affiche sous la forme de cours interactif dans le navigateur de la personne qui le consulte. 

LiaScript a été présenté par André Dietrich en [novembre 2019 à la conférence ELM Europe](https://youtu.be/w_CRABsJNKA), à la fois comme une alternative valable à Moodle et un outil complémentaire (et compatible avec les principaux LMS dont Moodle)

### Editer un texte pour l'interpréteur Liascript

              --{{2 @Jonas}}--
LiaScript interprête des textes en Markdown. La syntaxe de base de Markdown est très rapide à maîtriser.
Cet interpréteur a été pensé au départ pour des cours en informatique, il est donc possible d'exécuter du code à travers LiaScript. 

```javascript
var s = "Hello ";
alert(s)
s + "world";
```
<script>@input</script>

### Editer avec Visual Studio Code

Liascript est compatible originellement avec Atom et VS Code. Il a été ensuite adapté avec l'éditeur en ligne CodIMD [^3].

Télécharger Visual Studio Code si ce n'est pas déjà fait. 

Il faut ajouter deux extensions à VS Code : 

- LiaScript-preview

- Liascript-Snippet

Lorsqu'on a téléchargé LiaScript, il reste à modifier un paramétrage qui permettra d'activer l'extension LiaScript-Snippet

Dans VS Code faire la combinaison de touches "Ctrl-Shift-P" et entrer settings.
Dans le menu sélectionner **Préférences:Open user settings.json**

Ajouter au fichier le code suivant : 

````javascript
   "[markdown]": {
      "editor.tabCompletion": "on",
      "editor.quickSuggestions": true,
      "editor.snippetSuggestions": "top"
   },
````
Dès lors que ces extensions sont chargées et paramétrées, les menus lias devraient être accessibles

![](images/menu_lia.png)


### Editer en ligne 

Si pour tester la solution, vous reculez devant le fait de télécharger et de paramétrer un outil que vous ne connaissez pas, vous pouvez utiliser l'éditeur en [ligne de LiaScript](https://liascript.github.io/LiveEditor/)
Cliquer sur *New note*

### Commencer un cours sur LiaScript 

Pour être parsé correctement, un texte conçu pour LiaScript doit commencer par un titre 1, soit en markdown, un \# suivi d'une espace et du titre du cours. 

Avant ce titre 1, vous pouvez ajouter des métadonnées afin de décrire votre ressource ou d'orienter le traitement des informations. 
Cela se fait sous la forme d'un commentaire initial 

````html
<!-- 
commentaire 1
commentaire 2 
-->
````

### Créer des quiz avec LiaScript 

#### Questions à choix multiples

Pour créer un QCM, sélectionner Lia-quiz-multiple-choice :

Lesquels de ces volcans se trouvent en Amérique ?

\[[ ]] Stromboli  

\[[X]] Paricutin

\[[ ]] Erebus 

\[[X]] Cotopaxi 

(les bonnes réponses sont cochées)

cela donne :

[[ ]] Stromboli
[[X]] Paricutin
[[ ]] Erebus
[[X]] Cotopaxi

Pour ajouter des indices

\[[ ]] Stromboli

\[[X]] Paricutin

\[[ ]] Erebus

\[[X]] Cotopaxi

\[[?]] Cotopaxi signifie "le cou de la lune" en quechua

\[[?]] Stromboli est un film italien


[[ ]] Stromboli
[[X]] Paricutin
[[ ]] Erebus
[[X]] Cotopaxi
[[?]] Cotopaxi signifie "le cou de la lune" en quechua
[[?]] Stromboli est un film italien

[^3]: CodIMD permet de rédiger du texte en markdown en mode collaboratif. le CNRS a ouvert une instance à tous les établissements universitaires de France : https://codimd.math.cnrs.fr/


\[[ ]] Stromboli

\[[X]] Paricutin

\[[ ]] Erebus

\[[X]] Cotopaxi

\[[?]] Cotopaxi signifie "le cou de la lune" en quechua

\[[?]] Stromboli est un film italien

\****************************************

Le Paricutin est l'un des volcans les plus récemment apparus sur Terre, il est né au Mexique en 1943
Le volcan Cotopaxi se trouve en Equateur.

\****************************************

cela donne une fois interprété (parsé)

[[ ]] Stromboli
[[X]] Paricutin
[[ ]] Erebus
[[X]] Cotopaxi
[[?]] Cotopaxi signifie "le cou de la lune" en quechua
[[?]] Stromboli est un film italien
****************************************

- Le Paricutin est l'un des volcans les plus récemment apparus sur Terre, il est né au Mexique en 1943
- Le volcan Cotopaxi se trouve en Equateur.

****************************************

#### textes à trous

En 1610, rue de la Ferronnerie, un homme a poignardé à mort le roi Henri IV, quel était le nom de l'assassin ? 

[[Ravaillac]]




