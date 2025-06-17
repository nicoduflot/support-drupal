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