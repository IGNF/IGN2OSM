# Parc ou réserve

<https://bdtopoexplorer.ign.fr/parc_ou_reserve>

Les objets de la classe BDTopo `Parc ou réserve` sont convertis en chemin fermé ou en relation multipolygone avec le tag `boundary` = `protected_area`.

TODO à creuser

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en zone OSM (chemin fermé ou relation multipolygone)

Si `Fictif` est `Vrai`, créer plutôt un noeud au centroïde de la géométrie fournie ?

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nature et Nature détaillée

TODO

<https://wiki.openstreetmap.org/wiki/Key:protect_class>

Valeurs possibles pour Nature : Arrêté de protection | Bien inscrit sur la liste du patrimoine mondial de l'UNESCO | Géoparc mondial UNESCO | Parc national | Parc naturel marin | Parc naturel régional | Réserve biologique | Réserve de biosphère | Réserve nationale de chasse et de faune sauvage | Réserve naturelle | Site Natura 2000 | Site Ramsar | Site acquis ou assimilé des conservatoires d'espaces naturels | Terrain du Conservatoire du Littoral | Zone de silence | Zone naturelle

Valeurs possibles pour Nature détaillée : Sans valeur | Aire d'adhésion | Arrêté de protection de biotope | Arrêté de protection de géotope | Arrêté de protection des habitats naturels | Périmètre de protection d'une réserve naturelle nationale | Périmètre de protection d'une réserve naturelle régionale | Réserve biologique dirigée | Réserve biologique intégrale | Réserve intégrale | Réserve naturelle de Corse | Réserve naturelle nationale | Réserve naturelle régionale | Site inscrit au titre de la Directive Habitats | Site inscrit au titre de la Directive Oiseaux | Zone centrale | Zone cœur | Zone de transition | Zone protégée | Zone tampon

`Nature` = `Réserve nationale de chasse et de faune sauvage` correspond à `protect_class` = `4`.

`Nature` = ` ` + `Nature détaillée` = ` ` correspond à TODO

### Toponyme

Correspond au tag `name`.

### Statut du toponyme

Pas d'équivalent OSM.

### Fictif

Pas d'équivalent OSM, mais peut-être utilisé pour simplifier la géométrie.

### Etat de l'objet

TODO

Valeurs possibles : En construction | En projet | En service

### Date de création

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date de modification

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date d'apparition

Correspond au tag `start_date`.

### Date de confirmation

Correspond au tag `check_date`.

### Sources

Correspond au tag `source`.

### Identifiants sources

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:*` pour le conserver.

### Méthode d'acquisition planimétrique

Pas d'équivalent OSM.

### Précision planimétrique

Pas d'équivalent OSM.
