# EPCI

<https://bdtopoexplorer.ign.fr/epci>

Les objets de la table BDTopo `EPCI` sont convertis en relation avec les tags suivants :

- `type` = `boundary`
- `boundary` = `local_authority`

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en relation OSM

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nom officiel

Correspond au tag `name`.

### Code Siren

Correspond au tag `ref:FR:SIREN`.

### Nature

Correspond au tag `local_authority:FR`.

La correspondance se fait suivant les règles suivantes :

- `Communauté d'agglomération` devient `CA`
- `Communauté de communes` devient `CC`
- `Communauté urbaine` devient `CU`
- `Etablissement public territorial` devient `EPT`
- `Métropole` devient `metropole`

### Date de création

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date de modification

Pas d'équivalent OSM (correspond plutôt à une métadonnée).

### Date d'apparition

Correspond au tag `start_date`.

### Date de confirmation

Correspond au tag `check_date`.

### Codes Insee des communes membres

Pas d'équivalent OSM.

### Codes Insee des départements membres

Pas d'équivalent OSM.

### Liens vers autorité administrative

Pas d'équivalent OSM (à recalculer par inclusion géométrique).
