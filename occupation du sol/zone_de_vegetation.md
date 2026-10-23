# Zone de végétation

<https://bdtopoexplorer.ign.fr/?id_classe=330>

Les objets de la table BDTopo `Zone de végétation` sont convertis en chemin fermé ou en relation multipolygone. Les tags principaux sont définis à l'aide de l'attribut `Nature`.

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en zone OSM (chemin fermé ou relation multipolygone)

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Date de création

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date de modification

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date d'apparition

Correspond au tag `start_date`.

### Date de confirmation

Correspond au tag `check_date`.

### Nature

TODO : `landuse`= `heath` ou `natural`=`scrub` pour Lande ligneuse

- `Bananeraie` correspond à `landuse`= `orchard` + `trees`= `banana_plants`
- `Bois` correspond à `landuse`= `forest`
- `Canne à sucre` correspond à `landuse`= `farmland` + `crop`= `sugarcane`
- `Cocoteraie` correspond à `landuse`= `orchard` + `trees`= `coconut_palms`
- `Forêt fermée de conifères` correspond à `landuse`= `forest` + `leaf_type`= `needleleaved`
- `Forêt fermée de feuillus` correspond à `landuse`= `forest` + `leaf_type`= `broadleaved`
- `Forêt fermée mixte` correspond à `landuse`= `forest` + `leaf_type`= `mixed`
- `Forêt ouverte` correspond à `natural`= `wood`
- `Haie` correspond à `barrier`= `hedge`
- `Houblonnière` correspond à `landuse`= `orchard` + `trees`= `hop_plants`
- `Lande herbacée` TODO <http://bdtopoexplorer.ign.fr/?id_classe=330#attribute_value_1102>
- `Lande ligneuse` correspond à `landuse`= `heath`
- `Mangrove` correspond à `natural`= `wetland` + `wetland`= `mangrove`
- `Peupleraie` correspond à `landuse`= `forest` + `leaf_type`= `broadleaved`
- `Rizière` correspond à `landuse`= `farmland` + `crop`= `rice` + `natural`= `wetland`
- `Verger` correspond à `landuse`= `orchard`
- `Vigne` correspond à `landuse`= `vineyard`
- `Zone arborée` correspond à `natural`= `wood`

Remarque : des haies sont également présentes sous forme linéaires, dans la classe `Haie`. Une déduplication peut être nécessaire.

Remarque : Dans OpenStreetMap, il existe deux tags pour représenter la forêt :

- `natural` = `wood` pour les forêts primaires, sans exploitation
- `landuse` = `forest` pour les forêts entretenues ou exploitées

Cette information n'est pas toujours explicitement fournie par l'attribut `Nature` donc des imprécisions demeurent

### Sources

Correspond au tag `source`.

### Identifiants sources

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:*` pour le conserver.

### Méthode d'acquisition planimétrique

Pas d'équivalent OSM.

### Précision planimétrique

Pas d'équivalent OSM.
