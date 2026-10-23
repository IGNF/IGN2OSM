# Arrondissement

<https://bdtopoexplorer.ign.fr/arrondissement>

Les objets de la table BDTopo `Arrondissement` sont convertis en relation avec les tags suivants :

- `type` = `boundary`
- `boundary` = `administrative`
- `admin_level` = `7`

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en relation OSM

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nom officiel

Correspond au tag `name`.

### Code Insee de l'arrondissement

Correspond au tag `ref:INSEE`.

### Numéro de l'arrondissement

Pas d'équivalent OSM.

Envisageable d'utiliser la clef `ref`.

### Code Insee du département

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Code Insee de la région

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Liens vers autorité administrative

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Date de création

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date de modification

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date d'apparition

Correspond au tag `start_date`.

### Date de confirmation

Correspond au tag `check_date`.
