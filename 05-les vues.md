## Les vues

Les vues permettent d'éxécuter des requêtes dans le contenu ou les taxonomie, afin de récupérer les information et de les afficher de manière personnalisée

Quand on crée une vue, on peut l'utiliser en tant que page, que bloc s'ajoutant au région du thème ou en flux XML

Ces variations de vues peuvent afficher les mêmes information sur les contenu ou des information différentes.

### Vue page et XML

#### Modifier une vue existante

##### La page d'accueil

La première vue que l'on va modifier est la vue de la page d'accueil. Par défaut, elle affiche tout le contenu promu en page d'accueil et publié, sous la forme d'un liste non mise en forme sur le contenu.

Le résultat est que la page d'accueil affiche chaque contenu référencé dans son entièreté, plus que d'afficher des petites section contenant les information principales et un lien pour accéder au contenu en entier dans son espace dédié.

* Accueil > Administration > Structure >
**Vues**
* On recherche *Page d'accueil* et on clique sur le bouton *modifier*
* Dans la première colonne on va pouvoir modifier :
    * Le titre de la vue, celui qui s'affiche en H1
    * Le format de la vue
        * Grille
        * Liste HTML
        * Grille réactive (responsive)
        * Tableau
        * Liste non mise en forme
    * Pour chaque format il existe des paramètre de mise en forme
    * le choix d'afficher les résultats sur le contenu ou sur les champs
    * le filtrage (quels sont les contenu que l'on récupère)
    * et les critères de tri

Quand on choisi d'afficher les champs, il faut ajouter les champs dans la partie *Champs* qui apparaît quand l'option est sélectionnée.

On peut choisir plusieurs champs d'un coup, et une fois qu'ils sont validé, une modale de paramétrage de chaque champs (affichage, etc) s'affichera pour chacun des champs choisis.

Si l'ordre prédéfini des champs généré par l'application ne convient pas, le dropdown de la partie champs permet de réordonner l'affichage.

Si le paramétrage d'un champsne convient pas, il suffit de cliquer sur le champ et de changer sa configuration, c'est aussi là qu'on peut le retirer de l'affichage.

##### La page des résultats des termes de taxonomie

Cette page permet d'afficher une vue des contenus correspondant au terme de taxonomie (Étiquettes, vocabulaires ajoutés par les utilisateurs).

Sa modification est la même que pour la page d'accueil

---

* vue page et xml
    * Modifier une vue existante
        * La page d'accueil
        * La page des résultat de terme de taxonomie
    * Créer une vue
        * Vu regroupant les type de contenu similaire
* vue block
    * Ajouter la vue bloc aux vues existante, avec un affichage différent
    * Créer une vue block sur les termes Étiquettes utilisés
* Modifier un thème de base
    * Réglages par défaut du thème Olivero
    * Modification avec CSS Editor
    * Ajout d'éléments au thème en utilisant le répertoire de fichier *\sites\default\files*

