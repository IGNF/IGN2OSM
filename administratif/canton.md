# Canton

<https://bdtopoexplorer.ign.fr/canton>

Les objets de la table BDTopo `Canton` sont convertis en relation avec les tags suivants :

- `type` = `boundary`
- `boundary` = `political`
- `political_division` = `canton`

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en relation OSM

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nom officiel

Correspond au tag `name`.

### Code Insee du canton

Correspond au tag `ref:INSEE`.

### Numéro du canton

Pas d'équivalent OSM.

Envisageable d'utiliser la clef `ref`.

### Code Insee du département

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Code Insee de la région

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Composition du canton

Pas d'équivalent OSM.

### Codes Insee des arrondissements

Pas d'équivalent OSM.

### Date de création

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date de modification

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date d'apparition

Correspond au tag `start_date`.

### Date de confirmation

Correspond au tag `check_date`.
