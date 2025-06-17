# Notes sur Drupal

## Extensions

### Extensions a récupérer et activer avant de commencer à créer la structure du contenu

* Media
* Media Library
* Admin Toolbar
* Admin Toolbar Extra Tools
* Admin Toolbar Search
* Token
* Pathauto
* Chaos Tools
* Configuration Translation
* Interface Translation
* Language

## Réglages préliminaires

### Ajouter la langue française dans l'interface utilisateur

* Accueil > Administration > Configuration > Régionalisation et langue > Langues >
**Ajouter une langue**
* Choisir Français et ajouter la langue
* Accueil > Administration > Configuration > Régionalisation et langue > 
**Langues**
* Mettre Français par défaut
* Accueil > Administration > Configuration > Régionalisation et langue > 
**Traduction de l'interface utilisateur**
importer
* Aller chercher le fichier de traduction sur [Localize.drupal](https://localize.drupal.org/translate/languages/fr)
* Choisir le fichier de la version majeur de drupal
* L'importer et laisser faire.

### Changer les réglages de saisie des Formats de texte et éditeurs
Accueil > Administration > Configuration > Rédaction de contenu >
**Formats de texte et éditeurs**

Pour HTML simple et HTML complet, choisir l'option Configurer

#### Configuration de la barre d'outils

* Il faut retirer le bouton Image et le remplacer par le bouton Media
* Une fois qu'on a mis le bouton Media, il faut aller cocher dans les réglages la case *Intégrer un Média*
* Une fois que cette case est cochée, il faut descendre jusqu'aux *paramètres de filtrage* et choisir les types de média qu'on autorise dans l'éditeur de texte

#### Remplacer le champ image dans le type de contenu *Article* par un champ *Media*

* Accueil > Administration > Structure > Types de contenu > Article >
**gérer les champs**
* Sur le drop down du champ *Image* Sélectionner *Supprimer*
* Valider la suppression dans la Modale
* Cliquer sur le bouton *Créer un nouveau champ*
Sélectionner *Media* et cliquer sur *Continuer*
* Donner un nom au champ et cliquer sur *Continuer*
* Vérifier que le type délément a référencer est bien *Media*
* Laisser la valeur limitée à 1
* Dans la partie *Type de référence*, laisser le mode de référence par défaut
* Cocher la case *Image* dans *Type de media*
* Ajouter si besoin une image par défaut, **ATTENTION** Il est préféreables qu'elle existe déjà dans la *Media  Library*, risque de bug.
* Il est possible d'enregistrer le champ sans valeur par défaut et de le modifier et l'ajouter par la suite
---
* Accueil > Administration > Structure > Types de contenu > Article >
**Gérer l'affichage du formulaire**
* Cacher le poids des lignes (lien en haut à droite)
* Aller chercher le champ créé
* En *drag-and-drop* attraper le champ sur l'icone à gauche du champ et le placer en dessous de *titre* par exemple
* Cliquer sur enregistrer
---
* Accueil > Administration > Structure > Types de contenu > Article >
**Gérer l'affichage**
* Même manipulation que pour l'affichage du formulaire

## Structurer les informations

il faut structurer les informations, en séparant ce qui sera un type de contenu particulier (comme *Articles* et *Pages*) ou une classification ou *Taxonomie* qui permettra de mettre en relation de façon pertinente le contenu du site

### Les types de contenu

Dans une médiathèque, les types de contenus peuvent être séparé de la façon suivante :

* Ce qui se lit : Roman, magazine, Nouvelle, Bande-dessiné
    **Champs pertinents :**
    * Couverture (Media Image limité 1)
    * Résumé
    **Taxonomie(s) possible :**
    * Support (Roman, magazine, Nouvelle, Bande-dessiné)
    * Genre Littéraire
    * Auteur(s) - Autrice(s)
    * Étiquettes (permettra d'ajouter des détails comme des protagonistes, des intervenants) etc.
* Ce qui se regarde : Film, Documentaire
    **Champs pertinents :**
    * Affiche (Media Image limité 1)
    * Galerie média (Media Image et vidéo illimité)
    * Résumé
    **Taxonomie(s) possible :**
    * Support (Dvd, Blu-ray)
    * Genre Vidéo
    * Créateur(s) - Créatrice(s)
    * Étiquettes (permettra d'ajouter des détails comme des protagonistes, des acteurs - actrices, etc)
* Ce qui s'écoute : Musique, livres Audio
    **Champs pertinents :**
    * Pochette (Media Image limité 1)
    * Tracklist
    **Taxonomie(s) possible :**
    * Support (Vinyl, Cd)
    * Genre Musical
    * Artiste(s) - Groupe(s)
    * Étiquettes (permettra d"ajouter des détails comme des protagonistes, des acteurs - actrices) etc.

### Créer les chemins pathauto des types de contenu existant - Page et Article

#### Créer un pathauto :
* Accueil > Administration > Configuration > Recherche et metadonnées > Alias d'URL >
**Patterns**
* *+ Add Pathauto pattern*
* Pattern type : Terme de taxonmie
* *Path pattern* support/[term:name]
* Libellé (pour cet exemple) : Pathauto pattern
* Cocher la case *Activés* pour la création automatique de l'alias d'url à chaque ajout de terme pour le vocabulaire

### Créer les taxonomies des types de contenu

Il est préférables de créer les taxonomies des types de contenu avant la création de ces types de contenu.
Les taxonomies seront ajoutées en tant que champs références dans les contenus.
Plutôt que de dréer un type de contenu, puis les taxonomies, puis modifier les types de contenus et d'ajouter les taxonomies, on prévoit à l'avance

**Une fois qu'une taxonomie est créée, ne pas oublier de créer le pattern pathauto correspondant afin d'automatiser la création des alias d'url pour chaque terme de la taxonomie**

#### Les taxonomies

* Accueil > Administration > Structure > Taxonomie >
**Ajouter un vocabulaire**
* Création de la taxonomie support qui sera générale aux types de contenu d'œuvre
* Le nom de la taxonomie, la description si besoin, et on clque sur *Enregistrer*
* On arrive sur la liste des termes, ce qui nous permet de préparer à l'avance des termes de taxonomie qui seront sûrement utilisés
* On clique sur *+ Ajouter un terme*
* On indique le nom du terme et on enregistre

### Créer les types de contenus

Maintenant que les champs existent pour les types de contenus, il faut créer chaque type de contenu en utilisant les nouveaux champs créés ou en réutilisant des champs existants

**Une fois qu'un type de contenu est créé, ne pas oublier de créer le pattern pathauto correspondant afin d'automatiser la création des alias d'url pour chaque contenu créé à partir de ce type de contenu**

#### Création des autres types de contenu

De la même façon que "ce qui se lit" : 

* on crée les champ nécéssaires au type de contenu
* On réutilise les champs quand cela est possible
* On vérifie les alias d'url automatique (pathauto pattern)
* on crée les alias manquant
* On ajoute ces champs dans le type de contenu
* on crée l'alias d'url du type de contenu