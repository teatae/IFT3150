# IFT3150

## Introduction

Gentlement est un éditeur de projection léger basé sur le Web qui vous permet de créer et de manipuler des modèles basés sur des concepts par projection.

### Motivation du drag-n-drop

Une bonne manipulation du visuel est cruciale pour un éditeur pour garantir une bonne expérience utilisateur. L'implémentation du *drag-n-drop* (glisser et déposer) permet d'améliorer l'expérience utilisateur.
Les intéractions telles que copier/couper/coller permet de faciliter l'expérience utilisateur.
Elle permet également de rendre plusieurs autres intéractions plus intuitives avec une visualisation plus évidente.

### Usage du drag-n-drop Gentleman

Le drag-nd

- Déplacement: Jusqu'à présent, glisser un concept par l'entête permet de le déplacer. Ensuite, déposer ce concept par dessus un autre permet d'interchanger leur emplacement dans l'éditeur.
- Copier/Coller: Glisser un concept par son contenu et non par son entête permet de copier le concept. Par la suite, déposer ce concept permet de le coller à la fin d'éditeur. Après la fonctionnalité de coller à l'intérieur d'un autre concept, il serait nécessaire d'implémenter un menu pour les déplacements, le copier/coller, ainsi que la possibilité d'annuler d'une action.

### Utilité du drag-n-drop

Le drag et drop n'est pas une technique nouvelle dans le monde des éditeurs, mais son implémentation est très importante.
Une bonne expérience utilisateur est ce qui fait la différence entre une application qui sera largement utilisé et une application obsolète.

## Application

Le drag-n-drop est implémenté à plusieurs niveaux dans Gentleman pour permettre différent comportements.

- Editor level
  - Upload: Ceci permet de glisser un fichier dans la zone de l'éditeur pour le charger et l'ouvrir. Cette application peut aussi être utilisé pour activer l'import de fichiers.
- Container level
  - Swap
  - Move
- Instance level
  - Copy
  - Move
- Set level
  - Swap
  - Move
