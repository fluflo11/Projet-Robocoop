
# Engin Semi Autonome à Aile Fixe

Un projet de drone semi autonome permettant de passer d'un mode de 
commandes automatiques à un pilotage manuel.

L'objectif de ce repo est de présenter le projet ainsi que de centraliser les ressources nécessaires à la complétion de ce dernier.




## Présentation du projet

*Le choix des méthodes de planification de vol et de technologies embarquées, ainsi que le budget et de législation concernant ce projet seront abordés plus bas.*

L'intérêt principal serait de mobiliser et surtout de développer des compétences et techniques très diverses : Compétences en robotique et électronique, 
software engineering, conception de systèmes embarqués... tout ce qui touche de près ou de loin à la mécatronique. 

Ainsi, un des plus gros avantages de ce projet est qu'il permet à tous les profils d'apprendre et offre une grande part d'improvisation et de créativité.

## Budget et matériel

L'avantage avec l'aéromodélisme et la mécatronique sont les prix relativement bas fournis
pour des composants d'entrée/milieu de gamme. 

Chaque composant sera justifié et détaille dans la section suivante. 

Ci dessous une estimation des prix pour les composants essentiels : 


```
Mobilité : 
-moteur + variateur de vitesse : 75€ +- 20€
-chassis : DIY

Electronique :
-communication : 20€ +- 10€
-microcontrôleur : 30€ grand maximum, plus probablement 15€
-capteurs : 50€ +- 20€ selon le type de capteurs embarqués.
-batterie : 100€ +- 20€
-choses diverses difficiles à estimer (câblages, gaines en plastique, pièces de rechange) : +-50€
```

Il est également important de noter que les coûts peuvent être drastiquement réduits en raison des composants très facilement accessibles. 
## Détails techniques et problématiques

- Pour qu'un engin vole, il lui faut une structure aérondynamique appropriée(aussi appellée chassis).
Bien que certains de ces objets puissent être achetés, il est préférable de concevoir soi même le chassis, qui peut vite atteindre des coûts onéreux lorsqu'il s'agît de drones à aile fixe. 

De plus, l'aéromodélisme est sûrement l'une des parties les plus intéressantes du projet, il serait dommage de s'en priver :)

- Concernant la propulsion, le choix instictif est un moteur sans balais, puisque ces derniers sont très répandus, fiables et peu chers. 

Ici, le poids de l'engin jouera un rôle crutial. En effet, le prix du moteur nécessaire variera fortement en fonction de ce dernier. Un poids trop faible rendrait le drone moins stable et plus sujet aux turbulences. Cependant, un poids trop lourd forcerait à utiliser un moteur plus puissant, et donc plus coûteux. 

Le choix du moteur sera donc à discuter et à prévoir minutieusement avec l'ensemble des membres de l'équipe, en fonction du choix des autres caractéristiques. 

- L'alimentation (batterie) est le second choix le plus important. C'est elle qui permet au vol de se dérouler sans accroc. Il est donc nécessaire de correctement choisir sa batterie. Une batterie avec une grande capacité (par exemple 10A) pèsera plus du double d'une batterie moyenne capacité (5000mA). Elle influera donc fortement sur le choix du moteur, qui lui même dépend de la batterie.

Tout dépendra donc de la durée des vols envisagés et du poids estimé de l'engin.

- Arrive ensuite le microcontrôlleur. Ici, le choix est plutôt simple, les produits de type ARM Cortex sont peu chers et conçus spécialement pour de l'embarqué.

- Le choix des capteurs laisse en général une grande marge de manoeuvre. Cependant, certains capteurs sont nécessaires au bon fonctionnement de l'appareil. 

On trouvera les capteurs suivants :

```
-GPS (coordonnées)
-IMU (inclinaison)
-Compas (direction)
-Baromètre (altitude)
-Caméra (détection obstacles)
```

L'idéal pour mesurer l'altitude serait un système de télémètrerie LIDAR, qui donnerait une mesure précise de la distance au sol. 
Il en va de même pour la détection des obstacles, puisqu'un système LIDAR à 360° serait plus précis et couvrirait tous les angles. 

Mais les capteurs listés au dessus sont déjà largement suffisants, et la caméra peut être omise si l'on parie qu'aucun oiseau ou appareil ne sera sur notre chemin. 

- Enfin, le module de communication. En effet, il faut pouvoir envoyer les informations de l'appareil à un ordinateur au sol. 

Les solutions sont les suivantes : 

```
-LoRa : 
Avantages : Longue Portée (10km environ), peu cher
Inconvénients : Faible débit (pas de multimédia), latence, passe difficilement les obstacles.

-4G : 
Avantages : Portée quasi illimitée à basse altitude.
Inconvénients : Prix, Consommation, Dépendant de la couverture réseau.

-Radio : 
Avantages : Peut être DIY / modifié facilement, longue portée
Inconvénients : Configuration sensible, possibles interférences, le module prend de la place (antenne)
```

## Législation

Le drone devra être enregistré une fois terminé, puis ré-enregistré à la moindre modification. 

Il est interdit de survoler des zones à risque (centrales nucléaires, sites militaires, etc), des aérodromes. Une distance de 150m est à conserver avec les habitations et bâtiments. La hauteur de vol max des de 120m, sauf autorisation spéciale par la DGAC (drone équipé de fonctions de vol automatiques, pas de vol à vue, etc). 

D'autres pays, tels que la Suisse et la Norvège, permettent de faire voler très facilement un drone à haute altitude (+120m), avec des procédures simplifiées à l'extrême. 

Plus d'informations sur ce lien :
*https://www.service-public.fr/particuliers/vosdroits/F34630*
