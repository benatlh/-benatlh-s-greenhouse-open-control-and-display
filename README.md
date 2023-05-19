![Final interface white](https://github.com/benatlh/-benatlh-s-greenhouse-open-control-and-display/assets/37818231/77c905b1-291b-48d8-b730-f3a5a8982711)

# -benatlh-s-greenhouse-open-control-and-display
The purpose of the programm is to control greenhouse with raspberry pi pico w. The way to archieve it in the most energy efficient and affordable possible. The purpose of the greenhouse is to make vegetables and to warm the house during the intermediate seasons cause it is a lean to type greenhouse. The greenhouse is equiped with:

- roof windows
- retractable awning
- 2 sides manual doors
- 2 manual ventilation grid
- 2 concrete tanks
- 1 pump
- 1 lighting sensor i2c (bh1750 ? it should support the direct sunlight)
- 1 fan to supply hot air to the house powered by relay
- 3 temperature sensor (DHT22 ?)
- 1 soil moisture sensor (type Grove 101020008)
- e-motor for awning powered by relay
- e-motor for root top window powered by relay
- motorized damper RMVT160 / 1223  fan PF 32.000 11632853055 not decided yet witch NRV type BDD100 + carcoal filter + plug for winter + 
- return from kitchen hood and controlled mechanical ventilation into greenhouse
- atmospheric sensor (BMP280)
- matrix keypad with PCF8574T module.
- e-paper screen display waveshare 2.9inch e-paper module 296-128 px V3

-> first of all we have to make them interract with raspberry. We have to get and check the material is ok.

Then the coding:

Le programme a plusieurs configurations de fonctionnement:
- headless + wifi ap: on tout faire de la sauf l'envoi au cloud directe (qui n'est pas nécessaire à mon gout) + display e-paper 2 couleurs optionnel
- headless + wifi en mode routeur, donc il faut la box en permanence, ce n'est pas l'option souhaitable à mon sens + display e-paper 2 couleurs optionnel
- display e-paper 2 couleurs only

Le micro controleur agit si en auto ainsi;
L’été : lucarnes ouvertes si pleut pas, grilles ventilation ouvertes, portes ouvertes, rideau tendu, communication maisin serre fermée
L’hivers:lucarnes fermées, grilles fermées, portes en aération le matin manuel, rideau rentré, communication on si hygronomie serre ok et t°C serre sup à t maison mais tmaison inférieur à 25°C. On a desréserves d’eau de la piere noire en forme de banc pour le déphasage. L’été on a de l’ombre au dessus de la serre avec arbre-lianne ? Et un rocket stove avec prise d’air extérieur. Alim systeme par panneau solaires. Affichage e-ink valeur capteurs+ evolution. Bloqueur de portes. Commandes débrayables facilement. Protection fusible si lucarnes ne se ferment pas facilement. Rigole de récupération de la condensation. Résistance poids verre 4 mm et vent 180hm/h*2. Étagères semis contre mur maison. Condensats dans arrosoir et trop plein arrosoir dans trop plein cuves. Capteur baromètrique.
Intersaison : varie selon température et hygronomie : grilles de ventilation ouvertes et potres aérées le mati puis refermées
	si t°C serre < 10  couche chaude au pied agrumes
	si T°C serre entre 15 et 24 on ne bouge pas
	si T°C serre > 24 on ferme le store
	si T°C serre > 25 on commence à ouvrir lucarnes
→ dans tous les cas si il pleut on ferme les lucarnes si sup a 24 on ferme le store. Il faut sortie vmc proche de lucarne pour évacuer l’été. Si nuit pas de courant donc on ferme les lucarnes au cas ou, on laisse le rideau. Si risque de glace ou canicule dans les cuves on vidange.


L'interface a été réfléchie pour disposer au mieux des informations tout en laissant de la lisibilité et un peu d'évolutivité. Il ne devrai pas y avoir trop de modif à faire d'ici la fin. On devrai pouvoir y configurer des vues.
