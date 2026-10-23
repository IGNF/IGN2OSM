# Zone d'estran

<https://bdtopoexplorer.ign.fr/zone_d_estran>

Les objets de la table BDTopo `Zone d'estran` sont convertis en chemin fermé ou en relation multipolygone avec l'attribut `tidal` = `yes`.

TODO à vérifier

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en zone OSM (chemin fermé ou relation multipolygone)

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nature

Correspond au tag `natural` :

- `Graviers ou galets` devient `natural` = `shingle`
- `Rocher` devient `natural` = `bare_rock`
- `Sable` devient `natural` = `sand`

### Date de création

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date de modification

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date d'apparition

Correspond au tag `start_date`.

### Date de confirmation

Correspond au tag `check_date`.

### Hauteur

Correspond au tag `height`.

### Largeur

Correspond au tag `length`.

### Sources

Correspond au tag `source`.

### Identifiants sources

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:*` pour le conserver.

### Méthode d'acquisition planimétrique

Pas d'équivalent OSM.

### Précision planimétrique

Pas d'équivalent OSM.
