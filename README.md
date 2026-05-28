# **Artemis II** : simulation numérique de la trajectoire

## Présentation

Les données fournies par le **JPL** donnent accès à la trajectoire suivie par le véhicule **Orion** dans le cadre de la mission **Artemis II**. On peut ainsi comparer cette trajectoire à celle obtenue par simulation numérique en appliquant les lois de Newton. La position et la vitesse initiale de cette simulation sont celles du véhicule **Orion** à une date initiale choisie.

Pour la simulation, on choisit le référentiel **ICRS** avec son origine placée au barycentre du système solaire. Les positions de la Terre, de la Lune et du Soleil sont donc données dans ce référentiel. On suppose que seuls ces astres influent sur l'accélération du véhicule. On vérifie ainsi ce que serait la trajectoire du véhicule  **sans aucun moyen de propulsion supplémentaire**. Par commodité, les résultats des simulations seront ensuite affichés dans le référentiel géocentrique écliptique.

## Descriptions et commentaires sur les essais menés

### Simulation juste après l'ITL (Injection Trans-Lunaire)

La date choisie pour fixer les valeurs initiales de position et de vitesse est le **3 avril 2026 à 00h00 UTC**, peu après qu'ait eu lieu la "grosse poussée" permettant le transit vers la Lune. La simulation se termine le **10 avril 2026 à 23h54 UTC**, car après cette date, les données sur la trajectoire d'Orion qui est alors tout près de la Terre, ne sont plus disponibles.

Après simulation numérique, on constate que le véhicule Orion sans moyen de propulsion aurait suivi une trajectoire très grossièrement comparable à la vraie trajectoire, avec cependant un écart d'environ **100000 km** à la date finale. Il est donc nécessaire de disposer d'un moyen de propulsion pour corriger la trajectoire.

### Simulation juste après la correction de trajectoire à proximité de la Lune

La date choisie pour fixer les valeurs initiales de position et de vitesse est le **6 avril 2026 à 03h30 UTC**, au moment où le véhicule s'approche de la Lune avant d'en faire le tour. Une correction a déjà été appliquée sous la forme d'un "delta V" d'environ 3 mètres par seconde.

Après simulation numérique, on obtient un bien meilleur suivi de la vraie trajectoire,  avec un écart d'environ **400 km** à la date finale.

### Simulation avec ajustement de la vitesse initiale

La date choisie pour fixer les valeurs initiales de position et de vitesse est le **3 avril 2026 à 00h00 UTC**, peu après l'injection trans-lunaire. On ajuste la vraie vitesse initiale du véhicule, de sorte que l'on suive aussi précisément que possible la vraie trajectoire jusqu'à la date finale du **10 avril 2026 à 23h54 UTC**. On réduit ainsi l'écart qui vaut alors **140 km** environ à la date finale.

On constate que le "delta V" qu'il aurait fallu appliquer est de l'ordre de **2,5 mètres par seconde** ! C'est l'ordre de grandeur des différentes corrections qui ont été appliquées durant la mission.

### Conclusion

Ces différentes situations simulées mettent en évidence le fait que la trajectoire est extrèmement sensible aux conditions initiales, notamment dès le début du transit vers la Lune. Il faut donc des moyens de propulsion pour réaliser des petites corrections ("delta V") tout au long de la mission. Il serait en effet illusoire de n'ajuster la vitesse qu'au début du transit, afin que l'ensemble du trajet s'effectue librement selon une trajectoire préétablie.

## Le notebook

Il est [ici](notebook/artemis2_simul.ipynb)

