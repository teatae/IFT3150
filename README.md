# IFT3150

## Introduction

Gentlement est un éditeur de projection léger basé sur le Web qui vous permet de créer et de manipuler des modèles basés sur des concepts par projection.

### Motivation du drag-n-drop

Une bonne manipulation du visuel est cruciale pour un éditeur pour garantir une bonne expérience utilisateur. L'implémentation du *drag-n-drop* (glisser et déposer) permet d'améliorer l'expérience utilisateur.
Les interactions telles que copier/couper/coller permet de faciliter l'expérience utilisateur.
Elle permet également de rendre plusieurs autres interactions plus intuitives avec une visualisation plus évidente.

### Usage du drag-n-drop Gentleman

- Déplacement: Jusqu'à présent, glisser un concept par l'entête permet de le déplacer. Ensuite, déposer ce concept par-dessus un autre permet d'interchanger leur emplacement dans l'éditeur.
- Copier/Coller: Glisser un concept par son contenu et non par son entête permet de copier le concept. Par la suite, déposer ce concept permet de le coller à la fin d'éditeur. Après la fonctionnalité de coller à l'intérieur d'un autre concept, il serait nécessaire d'implémenter un menu pour les déplacements, le copier/coller, ainsi que la possibilité d'annuler d'une action.

### Utilité du drag-n-drop

Le drag et drop n'est pas une technique nouvelle dans le monde des éditeurs, mais son implémentation est très importante.
Une bonne expérience utilisateur est ce qui fait la différence entre une application qui sera largement utilisée et une application obsolète.

## Application

Le drag-n-drop est implémenté à plusieurs niveaux dans Gentleman pour permettre différents comportements.

### Éditeur

> Fonctions: Upload

Au niveau de l'éditeur (fenêtre d'édition), le drag-n-drop permet d'ajouter (upload) des fichiers en les glissant dans la zone de l'éditeur. Cette application peut aussi être utilisée pour activer l'import de données.

### Conteneur

> Fonctions: Swap, Move

Dans la zone d'édition, plusieurs conteneurs peuvent être activés. Ceci est pratique pour donner une vue d'ensemble et manipuler plusieurs instances durant une session de travail. Dans ce cadre, le drag-n-drop permet d'organiser les conteneurs d'instances. L'utilisateur peut donc permuter deux conteneurs ou simplement déplacer un conteneur à une autre position.

### Instance

> Fonctions: Copy, Cut, Paste, Clone

Au niveau d'une instance (contenu du conteneur), le drag-n-drop permet principalement de manipuler les valeurs de l'instance. En glissant le contenu d'une instance `A` vers une autre instance `B`, l'utilisateur peut copier le contenu de `A` dans `B`. Si une instance est glissée dans un espace vide de la zone d'édition, une nouvelle instance est créé avec la même valeur.

### Collection

> Fonctions: Swap, Move, Duplicate

Une collection ou liste regroupe un ensemble d'éléments (nombre variable). Elle se porte bien au genre de manipulation permis par le drag-n-drop. Ainsi, le drag-n-drop permet, comme pour les conteneurs, d'organiser les éléments par des permutations ou déplacement. Similaire aux instances, un élément peut aussi être cloné en le glissant dans un espace vide de la liste.

### Options

Les fonctionnalités décrites plus haut sont parfois ambiguës lors d'une manipulation. Par exemple, dans le cas d'une liste, Un utilisateur pourrait glisser un élément dans un espace vide pour le déplacer ou pour le dupliquer. De manière similaire, il est difficile de distinguer les actions *copier-coller* et *couper-coller*. Pour éviter un choix arbitraire, lorsque l'élément glissé est relaché, un menu d'options (3 options max) est présenté à l'utilisateur pour choisir l'action a réalisé.
