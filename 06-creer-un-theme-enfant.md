## Les thèmes enfants

Créer un thème enfant permet de s'appuyer sur l'intelligence d'un thème stable et maintenu, et on a la possibilité de modifier les éléments de ce thème.

Pour créer une thème enfant, il suffit d'ajouter un dossier dans le répertoire *\themes*

Les thèmes sont en fait des modules, mais leur fonction est un peu différente

### Création des fichiers nécessaires

De base, deux fichiers sont nécessaire : 

myTheme.info.yml
myTheme.libraries.yml

```
themes
    |_myTheme/
        |_myTheme.info.yml
        |_myTheme.libraries.yml

```

#### Fichier .info.yml

C'est le fichier qui permet de définir, entre autre :
* Le nom du thème / module
* Le type de module : theme
* La description du thème
* la / les versions de base de drupal avec lesquelle le theme est compatible
* le thème parent sur lequel notre thème s'appuie
* Le logo du thème
* les librairies (les fonctionnalité externe comme un datepicker js, jquery, chartjs, etc)
* Les régions du thème (les partie principales du thème comme header, hero, content, sidebar, etc.)

```myTheme.info.yml```

```yml
name: myTheme
type: theme
description: Thème enfant de starterkit_theme
core_version_requirement: ^10 || ^11
base theme: starterkit_theme
logo: images/nicolas-duflot-avatar.svg
libraries:
    - myTheme/general
regions:
    header: 'Header'
    primary_menu: 'Primary menu'
    secondary_menu: 'Secondary menu'
    highlighted: 'Highlighted'
    custom_region: 'Custom region'
    help: 'Help'
    breadcrumb: 'Breadcrumb'
    content: 'Content'
    sidebar_first: 'Left sidebar'
    sidebar_second: 'Right sidebar'
    footer: 'Footer'
```

#### Fichier .libraries.yml

les lirairies correpondent :
* Les fichiers CSS du thème
* les fichiers js du thème
* les polices du thème
* des widget js / css comme chartJs
* etc

```myTheme.libraries.yml```

```yml
general: 
    header: true
    css:
        theme:
            # Il est possible de préciser à quel type d'affichage, screen ou print par exemple, sera utilisé la bibliothèque nommé
            css/bootstrap.css: {media: screen}
            css/bootstrap-icon.css: {}
            css/style.css: {media: screen}
            css/print.css: {media: print}
    js:
        js/bootstrap.bundle.js: {}
        js/scripts.js: {}
```
### Activer le débuggage de thème dans drupal

Il faut activer le débug de twigg et arrêter les caches d'affichage afin de voir dans l'inspecteur d'éléments les fichiers twig utilisés dans le thème, connaître le nom des fichiers a créer pour surcharger des parties ciblées du thème et connaîte l'arborescences des fichiers twig dans le thème

```
html.html.twig (<html>)
|   |_page.html.twig (div class layout-container)
|   |   |_region.html.twig (class region region header)
|   |   |   |_block.html.twig (id block-mytheme-page-title)
|   |   |   |   |_page-title.html.twig 
|   |   |   |_block.html.twig (id block-mytheme-syndicate)
|   |   |   |   |_feed-icon.html.twig
|   |   |   |_block--system-branding-block.html.twig (id block-mytheme-site-branding)
|   |   |
|   |   |_(etc)
|   |   |
|   |   |
|   |   |
|   |   |_region.html.twig (class region region-help)
|   |   |   |_ (etc)
|   |
|   |   
|

```

* Accueil > Administration > Configuration > Développement >
**Paramètres de développement**
* Cocher toutes les cases

### Surcharger les fichiers de thème

Les thèmes dans drupal sont gérés par le moteur de thème twig

Un thème enfant s'appuie sur tous les fichiers twig du thème parent, quand il est nécessaire de modifier l'apparence d'un des éléments, il faut reproduire dans le thème enfant l'arborescence des fichiers twig du thème parent et reprende soit le fichier exact(dans le cas d'une modification générique) soit créer un fichier twig avec le nom suggéré par le débug qui s'affiche en commentaire html dans le code de la page.

``` html
<!-- THEME DEBUG -->
<!-- THEME HOOK: 'page' -->
<!-- FILE NAME SUGGESTIONS:
   ▪️ page--front.html.twig
   ▪️ page--node.html.twig
   ✅ page.html.twig
-->
<!-- 💡 BEGIN CUSTOM TEMPLATE OUTPUT from 'themes/myTheme/templates/layout/page.html.twig' -->
```

*page.html.twig* est noté comme étant le fichier utilisé, les nom de fichier possible pour une surcharge particulière sont donc 
* page--front.html.twig
* page--node.html.twig

