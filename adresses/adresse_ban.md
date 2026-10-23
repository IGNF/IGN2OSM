# Adresse BAN

<https://bdtopoexplorer.ign.fr/?id_classe=292>

Les objets de la table BDTopo `Adresse BAN` sont convertis en noeud isolés. Les attributs déterminent les tags à appliquer.

## Géométrie

Type de géométrie : Point 2D

à convertir en noeud OSM

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

### Numéro

Correspond à la première partie au tag `addr:housenumber`.

Ignorer l'objet si `Numéro`=`99999`.

### Suffixe

Correspond à la seconde partie au tag `addr:housenumber`.

Si présent, le préfixer d'un espace, puis le concaténer au `Numéro` pour constituer le tag `addr:housenumber`.

### Identifiant voie

Pas d'équivalent OSM.

### Nom voie

Correspond au tag `addr:street`.

### Insee commune

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Nom commune

Non recommandé dans OSM (à recalculer par inclusion géométrique).

Peut éventuellement être conservé via le tag `addr:city`

### Insee commune déléguée

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Nom commune déléguée

Pas d'équivalent OSM (à recalculer par inclusion géométrique).

### Type position

Pas d'équivalent OSM.

### Lieu-dit

Correspond au tag `addr:place`. (TODO à vérifier)

### Source adresse

Correspond au tag `source:addr`.

### Certification commune

Pas d'équivalent OSM.

### Parcelles cadastrales

Pas d'équivalent OSM.

### Identifiant adresse

Pas d'équivalent OSM.

### Clé d'interopérabilité

Pas d'équivalent OSM.
