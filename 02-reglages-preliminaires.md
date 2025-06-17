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