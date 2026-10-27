# Aérodrome

<https://bdtopoexplorer.ign.fr/?id_classe=73>

Les objets de la classe BDTopo `Aérodrome` sont convertis en chemin fermé ou en relation multipolygone. L'attribut `Nature` permet de définir le tag principal approprié.

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en zone OSM (chemin fermé ou relation multipolygone)

Si `Fictif` est `Vrai`, créer plutôt un noeud au centroïde de la géométrie fournie ?

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Catégorie

Correspond au tag `aerodrome:type` :

- `Autre` n'a pas de correspondance
- `Internationale` correspond à `aerodrome:type` = `international`
- `Nationale` correspond à `aerodrome:type` = `regional`

### Nature

`Nature` = `Altiport` ou `Aérodrome` ou `Hydrobase` correspond à `aeroway` = `aerodrome`.

`Nature` = `Héliport` correspond à `aeroway` = `heliport`.

### Usage

TODO `operator:type` ?

Valeurs possibles : Civil | Civil et militaire | Militaire | Privé

### Toponyme

Correspond au tag `name`.

### Statut du toponyme

Pas d'équivalent OSM.

### Fictif

Pas d'équivalent OSM, mais peut-être utilisé pour simplifier la géométrie.

### Etat de l'objet transport

TODO

Valeurs possibles : En construction | En projet | En service | Non exploité

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

### Altitude

Correspond au tag `ele`.

### Code ICAO

Correspond au tag `icao`.

### Code IATA

Correspond au tag `iata`.
