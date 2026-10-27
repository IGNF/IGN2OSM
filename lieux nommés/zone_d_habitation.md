# Zone d'habitation

<https://bdtopoexplorer.ign.fr/zone_d_habitation>

Les objets de la classe BDTopo `Zone d'habitation` peuvent être convertis en zone ou en noeud OSM. Les attributs Nature et Nature détaillée permettent de déterminer s'il faut convertir l'objet et quel tag principal à ajouter.

## Géométrie

Type de géométrie : MultiPolygone 2D

à convertir en zone OSM (chemin fermé ou relation multipolygone) ou en noeud OSM.

Si `Fictif` est `Vrai`, créer plutôt un noeud au centroïde de la géométrie fournie ?

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nature et Nature détaillée

TODO à vérifier / compléter

- `Nature` = `Château` + `Nature détaillée` = `Château fort` correspond à `historic` = `castle` + `castle_type` = `defensive`.
- `Nature` = `Château` + `Nature détaillée` = `Tour` ou sans valeur correspond à `historic` = `castle`.
- `Nature` = `Grange` n'a pas d'équivalent OSM. TODO regarder valeurs détaillées
- `Nature` = `Habitat temporaire` + `Nature détaillée` = `Carbet` correspond à `amenity` = `shelter`.
- `Nature` = `Habitat temporaire` + `Nature détaillée` sans valeur n'a pas d'équivalent OSM. L'objet est ignoré.
- `Nature` = `Lieu-dit habité` correspond à `place` = `*`. L'attribut `Importance` permet de déterminer la valeur du tag. À convertir en noeud, au centroïde de la géométrie fournie.
- `Nature` = `Moulin` TODO
- `Nature` = `Quartier` + `Nature détaillée` = `Quartier urbain` correspond à `place` = `suburb`. À convertir en noeud, au centroïde de la géométrie fournie.
- `Nature` = `Quartier` + `Nature détaillée` = `Chalet` ou `Hôtel particulier` ou `Immeuble` ou `Lotissement` ou `Résidence` ou sans valeur n'a pas d'équivalent OSM (il faudrait théoriquement positionner ces attributs sur le bâtiment déjà existant). L'objet est ignoré.
- `Nature` = `Ruines` correspond à `historic` = `ruins`.

TODO `Nature détaillée` = `Bergerie` ?
TODO `Nature détaillée` = `Cabane` ?

### Toponyme

Correspond au tag `name`.

### Statut du toponyme

Pas d'équivalent OSM.

### Importance

TODO à vérifier

L'attribut `Importance` est considéré uniquement quand `Nature` = `Lieu-dit habité` :

- `Importance` = `1` correspond à `place` = `town`.
- `Importance` = `2` ou `3` correspond à `place` = `village`.
- `Importance` = `4` correspond à `place` = `hamlet`.
- `Importance` = `5` ou `6` correspond à `place` = `isolated_dwelling`.

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

### Insee commune calculé

Pas d'équivalent OSM.

### Commune

Pas d'équivalent OSM.

### Identifiant voie BAN

Pas d'équivalent OSM.

### Id BAN Odonyme

Pas d'équivalent OSM.
