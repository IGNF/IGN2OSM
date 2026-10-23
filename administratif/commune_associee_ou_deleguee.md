# Commune associée ou déléguée

<https://bdtopoexplorer.ign.fr/commune_associee_ou_deleguee>

Les objets de la table BDTopo `Commune associée ou déléguée` sont convertis en relation avec les tags suivants :

- `type` = `boundary`
- `boundary` = `administrative`
- `admin_level` = `9`
- `disused:admin_level` = `8`

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en relation OSM

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nom officiel

Correspond au tag `name`.

### Code Insee de la commune associée ou déléguée

Correspond au tag `ref:INSEE`.

### Code Insee de la commune de rattachement

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Nature

Correspond au tag `admin_type:FR`.

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

### Code postal

Correspond au tag `postal_code`.

### Lien vers chef-lieu

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Liens vers autorité administrative

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Population

Correspond au tag `population`.
