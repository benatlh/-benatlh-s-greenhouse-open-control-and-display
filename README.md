# -benatlh-s-greenhouse-open-control-and-display
The purpose of the programm is to control greenhouse with raspberry pi pico w. The way to archieve it in the most energy efficient and affordable possible.

Le programme a plusieurs modes de fonctionnement:
- headless + wifi ap: on tout faire de la sauf l'envoi au cloud directe (qui n'est pas nécessaire à mon gout) + display e-paper 2 couleurs optionnel
- headless + wifi en mode routeur, donc il faut la box en permanence, ce n'est pas l'option souhaitable à mon sens + display e-paper 2 couleurs optionnel
- display e-paper 2 couleurs only



L’été : lucarnes ouvertes si pleut pas, grilles ventilation ouvertes, portes ouvertes, rideau tendu, communication maisin serre fermée
L’hivers:lucarnes fermées, grilles fermées, portes en aération le matin manuel, rideau rentré, communication on si hygronomie serre ok et t°C serre sup à t maison mais tmaison inférieur à 25°C. On a desréserves d’eau de la piere noire en forme de banc pour le déphasage. L’été on a de l’ombre au dessus de la serre avec arbre-lianne ? Et un rocket stove avec prise d’air extérieur. Alim systeme par panneau solaires. Affichage e-ink valeur capteurs+ evolution. Bloqueur de portes. Commandes débrayables facilement. Protection fusible si lucarnes ne se ferment pas facilement. Rigole de récupération de la condensation. Résistance poids verre 4 mm et vent 180hm/h*2. Étagères semis contre mur maison. Condensats dans arrosoir et trop plein arrosoir dans trop plein cuves. Capteur baromètrique.
Intersaison : varie selon température et hygronomie : grilles de ventilation ouvertes et potres aérées le mati puis refermées
	si t°C serre < 10  couche chaude au pied agrumes
	si T°C serre entre 15 et 24 on ne bouge pas
	si T°C serre > 24 on ferme le store
	si T°C serre > 25 on commence à ouvrir lucarnes
→ dans tous les cas si il pleut on ferme les lucarnes si sup a 24 on ferme le store. Il faut sortie vmc proche de lucarne pour évacuer l’été. Si nuit pas de courant donc on ferme les lucarnes au cas ou, on laisse le rideau. Si risque de glace ou canicule dans les cuves on vidange.


L'interface a été réfléchie pour disposer au mieux des informations tout en laissant de la lisibilité et un peu d'évolutivité. Il ne devrai pas y avoir trop de modif à faire d'ici la fin. On devrai pouvoir y configurer des vues.
