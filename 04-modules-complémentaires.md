## Modules Complémentaires

### Book

Book était historiquement un module présent dans le coeur de Drupal, mais il a été retiré à l'arrivée de la version 11

Il est toujours possible de l'installer en module contribué

Book permet de créer des livre, ces livres permettent de regrouper différents type de contenus, dans un ordre précis, et permet de profiter d'une pagination et d'une table des matière représentant la hiérarchie des contenus regroupés.

Permet donc un regroupement transverse de contenu n'yany pas de champs similaire mais des thèmes associés très forts

#### Gérer les droits de Book

Une fois l'exention Book installée, il faut activer book et aussi l'extension book olivero qui permet de l'utiliser correctement avec le thème par défaut de drupal "Olivero"

Book ajoute un nouveau type de contenu *Book page*, il faut gérer tout de suite le droit de gestion de ce type de contenu pour les utilisateurs

#### Gérer les types de contenus pouvant utiliser le principe de livre

Depuis les extensions, ouvrir l'accordéon de book et on clique sur *configurer*

Il est possible d'ajouter des type contenu existant pour utiliser le principe de *book*

#### Alias d'url pour les pages de livre

Pour pouvoir profiter des alias d'url automatique, comme pour les types de contenus que l'on a créé soit-même, la création d'un pathauto permettra un meilleur référencement du contenu regroupé

Dans le cas où les pages enfants sont des pages de livre, la pagination fonctionnera correctement car les alias d'url seront correctement associés au type de contenu *book page*, en revanche, si du contenu extérieur (autre que *book page*) est ajouté, la pagination ne fonctionnera pas car on est redirigé vers l'affichage du type de contenu de la page et non pas d'une *book page* enfant.

Mais le fil d'ariane précisera, sur le contenu extéieur, les éléments *parents* liés à la hiérarchie imposée par la page principale (*page de garde*) du livre.