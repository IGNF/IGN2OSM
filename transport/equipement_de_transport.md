# Équipement de transport

<https://bdtopoexplorer.ign.fr/equipement_de_transport>

Les objets de la classe BDTopo `Equipement de transport` sont convertis en chemin fermé ou en relation multipolygone. Les attributs `Nature` et `Nature détaillée` permettent de définir le tag principal approprié.

Remarque : les objets avec `Nature` = `Autre équipement` n'ont pas assez de précision pour être convertis et devraient donc être ignorés.

## Géométrie

Type de géométrie : MultiPolygone 3D

à convertir en zone OSM (chemin fermé ou relation multipolygone)

Si `Fictif` est `Vrai`, créer plutôt un noeud au centroïde de la géométrie fournie ?

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nature et Nature détaillée

| Parking | Port | Péage | Service dédié aux véhicules | Service dédié aux vélos | Station de métro | Station de tramway | Tour de contrôle aérien

`Nature` = `Aire de repos ou de service` + `Nature détaillée` = `Aire de service` correspond à `highway` = `services`. TODO à vérifier

`Nature` = `Aire de repos ou de service` + `Nature détaillée` = `Aire de repos` correspond à `highway` = `rest_area`.

`Nature` = `Aire de triage` correspond à `landuse` = `railway` + `railway` = `yard`. TODO à vérifier

`Nature` = `Arrêt voyageurs` correspond à `train` = `yes` + `railway` = `halt` + `public_transport` = `station`.

`Nature` = `Autre équipement` n'a pas d'équivalent. Il est recommandé d'ignorer cet objet.

`Nature` = `Aérogare` correspond à `aeroway` = `terminal`.

`Nature` = `Carrefour` + `Nature détaillée` = `f` TODO
    Valeurs du champ « Nature détaillée » associées : Sans valeur | Echangeur | Echangeur complet | Echangeur partiel | Rond-point

    TODO vérifier la cohérence / redondance avec les classes décrivant le réseau routier.

`Nature` = `Gare fret uniquement` correspond à `railway` = `station` + `usage` = `freight`.

`Nature` = `Gare maritime` correspond à `public_transport` = `station` + `amenity` = `ferry_terminal`. TODO à vérifier

`Nature` = `Gare routière` correspond à `public_transport` = `station` + `amenity` = `bus_station`.

`Nature` = `Gare téléphérique` correspond à `public_transport` = `station` + `aerialway` = `station`. TODO à vérifier
    Valeurs du champ « Nature détaillée » associées : Sans valeur | Gare télécabine | Gare téléphérique intermédiaire TODO

`Nature` = `Gare voyageurs et fret` ou `Nature` = `Gare voyageurs uniquement` + `Nature détaillée` différent de `Gare funiculaire` correspond à `train` = `yes` + `railway` = `station` + `public_transport` = `station`.

`Nature` = `Gare voyageurs uniquement` + `Nature détaillée` = `Gare funiculaire` correspond à TODO

`Nature` = `Parking` + `Nature détaillée` = `Parking touristique` ou sans valeur correspond à `amenity` = `parking`.

`Nature` = `Parking` + `Nature détaillée` = `Aire de camping-cars` correspond à `tourism` = `caravan_site`. TODO à vérifier

`Nature` = `Parking` + `Nature détaillée` = `Aire de covoiturage` correspond à `amenity` = `parking` + `carpool` = `yes`. TODO à vérifier

`Nature` = `Parking` + `Nature détaillée` = `Parking couvert` correspond à `amenity` = `parking` + `covered` = `yes`.

`Nature` = `Parking` + `Nature détaillée` = `Parking relais` correspond à `amenity` = `parking` + `park_ride` = `yes`.

`Nature` = `Parking` + `Nature détaillée` = `Parking souterrain` correspond à `amenity` = `parking` + `parking` = `underground`.

### Toponyme

Correspond au tag `name`.

### Statut du toponyme

Pas d'équivalent OSM.

### Nom commercial

Correspond au tag `official_name`.

### Importance

Pas d'équivalent OSM.

### Numéro

Correspond au tag `ref`.

### Fictif

Pas d'équivalent OSM, mais peut-être utilisé pour simplifier la géométrie.

### Adresse postale

Non recommandé dans OSM.

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

### Méthode d'acquisition altimétrique

Pas d'équivalent OSM.

### Précision altimétrique

Pas d'équivalent OSM.

### Insee commune calculé

Pas d'équivalent OSM.

### Commune

Pas d'équivalent OSM.

### Identifiant voie BAN

Pas d'équivalent OSM.

### Id BAN Odonyme

Pas d'équivalent OSM.
