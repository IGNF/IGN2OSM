# Tronçon de route

<https://bdtopoexplorer.ign.fr/troncon_de_route>

Les objets de la classe BDTopo `Tronçon de route` sont convertis en chemins, principalement `highway` = `*`.

Les attributs suivants permettent de définir plus précisément la valeur du tag `highway` :

- Nature
- Importance
- Nature de la restriction
- CPX_Classement administratif
- etc

TODO définir plus précisément l'ordre et les règles à considérer et reformuler les paragraphes correspondants (ne pas hésiter à les regrouper si nécessaire)

## Géométrie

Type de géométrie : Ligne 3D

à convertir en chemin OSM

## Attributs

### Cleabs

Pas d'équivalent OSM.

Envisageable de créer une clef `ref:FR:BDTopo` pour le conserver.

### Nature

TODO à reformuler quand les règles seront claires :

- `Nature` = `Bac ou liaison maritime` correspond à `route` = `ferry` (pas de tag `highway` dans ce cas).
- `Nature` = `Bretelle` correspond à `highway` = `trunk_link`. TODO à vérifier (peut-être aussi motorway_link / primary_link / secondary_link / tertiary_link. Voir aussi `Importance`)
- `Nature` = `Chemin` correspond à `highway` = `track` + `surface` = `unpaved`.
- `Nature` = `Escalier` correspond à `highway` = `steps`.
- `Nature` = `Rond-point` correspond à `junction` = `roundabout`. Dans ce cas, le tag `highway` est déterminé à partir de l'attribut `Importance`.
- `Nature` = `Route empierrée` correspond à `highway` = `unclassified` + `surface` = `unpaved`.
- `Nature` = `Sentier` correspond à `highway` = `path`.
- `Nature` = `Route à 1 chaussée` ou `Route à 2 chaussées` ou `Type autoroutier` ne permettent pas de déterminer seul le tag principal. À compléter avec `Importance` / `CPX_Classement administratif` / `Urbain` ? TODO

### Nom collaboratif gauche

TODO à comparer avec `Nom voie BAN gauche` ?

remplir `name` ou `name:left`

### Nom collaboratif droite

TODO

### Importance

TODO à affiner (surement à combiner avec `Nature` ou autre)

- `Importance` = `1` correspond à `highway` = `trunk`
- `Importance` = `2` correspond à `highway` = `primary`
- `Importance` = `3` correspond à `highway` = `secondary`
- `Importance` = `4` correspond à `highway` = `tertiary`
- `Importance` = `5` correspond à `highway` = `unclassified` / `residential` ?
- `Importance` = `6` correspond à `highway` = `service`

### Fictif

TODO

### Position par rapport au sol

TODO à vérifier :

- `Position par rapport au sol` = `-1` ou `-2` ou `-3` ou `-4` correspond à `tunnel` = `yes`. En complément, la valeur de l'attribut est ajouté dans le tag `layer`.
- `Position par rapport au sol` = `1` ou `2` ou `3` ou `4` correspond à `bridge` = `yes`. En complément, la valeur de l'attribut est ajouté dans le tag `layer`.
- `Position par rapport au sol` = `Gué ou radier` correspond à `fjord` = `yes`.

### Etat de l'objet

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

### Nombre de voies

Correspond au tag `lanes`.

Cas particuliers : ne pas créer de tag `lanes` lorsque `Nombre de voies` = 0 ou sans objet.

### Largeur de chaussée

Correspond au tag `width`.

TODO vérifier si arrondi nécessaire, et si des valeurs 0 sont présentes (à ignorer).

### Itinéraire vert

TODO

### Privé

`Privé` vrai correspond à `access` = `private`.

TODO à confirmer (la définition BD Topo peut-être différence de celle OSM)

### Sens de circulation

- `Sens de circulation` = `Sens direct` correspond à `oneway` = `yes`.
- `Sens de circulation` = `Sens inverse` correspond à `oneway` = `-1`.
- `Sens de circulation` = `Double sens` correspond à `oneway` = `no` mais peut être ignoré car c'est la valeur par défaut dans OSM.
- `Sens de circulation` sans objet peut être ignoré.

TODO vérifier comment sont gérés les sens uniques sur rond-point

### Réservé aux bus

TODO à vérifier

semble correspondre à `lanes:bus` / `lanes:bus:forward` / `lanes:bus:backward`

### Urbain

TODO

Si `Nature` = `Route à 1 chaussée` (?) et `Urbain` vrai, alors `highway` = `residential` ?

renseigner `maxspeed` à partir de ça également ?

### Vitesse moyenne VL

Pas d'équivalent OSM.

### Accès véhicule léger

TODO à vérifier

- `Accès véhicule léger` = `A péage` correspond à `toll` = `yes`.
- `Accès véhicule léger` = `Libre` peut être ignoré (correspond à `access` = `yes`, qui n'est pas recommandé dans OSM).
- `Accès véhicule léger` = `Physiquement impossible` correspond à `access` = `no`.
- `Accès véhicule léger` = `Restreint aux ayants droit` correspond à `access` = `destination`.

### Accès piéton

TODO à vérifier

- `Accès piéton` = `A péage` correspond à `foot` = `yes` + `fee` = `yes`. (TODO)
- `Accès piéton` = `Libre` correspond à `foot` = `yes`.
- `Accès véhicule léger` = `Passage difficile` TODO
- `Accès piéton` = `Restreint aux ayants droit` correspond à `foot` = `destination`.

TODO ne pas renseigner sur escalier / déjà renseigné par ailleurs sur voie verte

### Période de fermeture

TODO condition restrictions (mapping à faire)

### Nature de la restriction

TODO vérifier vis à vis de `Nature` :

- `Nature de la restriction` = `Piste cyclable` correspond à `highway` = `cycleway`.
- `Nature de la restriction` = `Voie verte` correspond à `highway` = `path` + `foot` = `designated` + `bicycle`= `designated` + TODO le tag du panneau voie verte

Valeurs possibles : Sans valeur | Aménagement mixte hors voie verte | Chaussée à voie centrale banalisée | Double sens cyclable non matérialisé | Entrée avec gardien | Interdit à la descente | Passage barré | Piste cyclable | Plot amovible | Voie de tramway utilisable par les véhicules de secours | Voie verte | Vélorue

### Restriction de hauteur

TODO à vérifier

Correspond au tag `maxheight`.

Cas particulier : ignorer si `Restriction de hauteur` = 0.

### Restriction de poids total

TODO à vérifier

Correspond au tag `maxweightrating`.

Cas particulier : ignorer si `Restriction de poids total` = 0.

### Restriction de poids par essieu

TODO à vérifier

Correspond au tag `maxaxleload`.

Cas particulier : ignorer si `Restriction de poids par essieu` = 0.

### Restriction de largeur

TODO à vérifier

Correspond au tag `maxwidth`.

Cas particulier : ignorer si `Restriction de largeur` = 0.

### Restriction de longueur

TODO à vérifier

Correspond au tag `maxlength`.

Cas particulier : ignorer si `Restriction de longueur` = 0.

### Matières dangereuses interdites

`Matières dangereuses interdites` vrai correspond à `hazmat` = `no`.

### Borne début gauche

Pas d'équivalent OSM.

### Borne début droite

Pas d'équivalent OSM.

### Borne fin gauche

Pas d'équivalent OSM.

### Borne fin droite

Pas d'équivalent OSM.

### Insee commune gauche

Pas d'équivalent OSM.

### Insee commune droite

Pas d'équivalent OSM.

### Alias gauche

TODO alt_name ?

### Alias droit

TODO alt_name ?

### Date de mise en service

Correspond au tag `opening_date`.

### Liens vers route nommée

Pas d'équivalent OSM.

### Liens vers itinéraire autre

Pas d'équivalent OSM.

### CPX_Numéro

Correspond au tag `ref`.

### CPX_Numéro route européenne

Correspond au tag `int_ref`. TODO à vérifier

### CPX_Classement administratif

TODO voir si permet d'affiner `highway` ?

### CPX_Gestionnaire

Correspond au tag `operator`. TODO vérifier si retraitement nécessaire

### CPX_Toponyme route nommée

Pas d'équivalent OSM.

### CPX_Toponyme itinéraire cyclable

Pas d'équivalent OSM.

### CPX_Toponyme voie verte

Pas d'équivalent OSM.

### CPX_Nature itinéraire autre

Pas d'équivalent OSM.

### CPX_Toponyme itinéraire autre

Pas d'équivalent OSM.

### Délestage

TODO

### Source voie BAN gauche

Pas d'équivalent OSM.

### Source voie BAN droite

Pas d'équivalent OSM.

### Nom voie BAN gauche

TODO

### Nom voie BAN droite

TODO

### Lieux-dits BAN gauche

Pas d'équivalent OSM.

### Lieux-dits BAN droite

Pas d'équivalent OSM.

### Identifiant voie BAN gauche

Pas d'équivalent OSM.

### Identifiant voie BAN droite

Pas d'équivalent OSM.

### Sens aménagement cyclable gauche

TODO

### Sens aménagement cyclable droit

TODO

### Aménagement cyclable gauche

TODO cycleway:left

### Aménagement cyclable droit

TODO cycleway:right

### Aire de retournement DFCI

TODO

### Gabarit DFCI

TODO

### Impasse DFCI

TODO

### Nature détaillée DFCI

TODO surface ?

### Ouvrage d'art limitant DFCI

TODO

### Pente maximale DFCI

TODO incline ?

### Piste DFCI

TODO

### Piste DFCI débroussaillée

TODO

### Piste DFCI fossés

TODO

### Sens de circulation DFCI

TODO

### Tout terrain DFCI

TODO

### Vitesse moyenne DFCI

TODO

### Zone de croisement DFCI

TODO

### Catégorie DFCI

TODO

### Vitesse collaborative

Pas d'équivalent OSM.

### Id BAN Odonyme droite

Pas d'équivalent OSM.

### Id BAN Odonyme gauche

Pas d'équivalent OSM.
