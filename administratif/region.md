# Région

<https://bdtopoexplorer.ign.fr/region>

Les objets de la table BDTopo `Région` sont convertis en relation avec les tags suivants :

- `type` = `boundary`
- `boundary` = `administrative`
- `admin_level` = `4`

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en relation OSM

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nom officiel

Correspond au tag `name`.

### Code Insee de la région

Correspond au tag `ref:INSEE`.

### Code Siren

Correspond au tag `ref:FR:SIREN`.

### Date de création

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date de modification

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date d'apparition

Correspond au tag `start_date`.

### Date de confirmation

Correspond au tag `check_date`.

### Liens vers autorité administrative

Pas d'équivalent OSM (à recalculer par inclusion géométrique).
