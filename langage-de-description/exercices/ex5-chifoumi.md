# Ex5: Chifoumi

Réaliser un système permettant de jouer à deux à « papier-caillou-ciseaux » ou « chifoumi ».

Pour rappel, chaque joueur nomme en même temps un des trois objets. Le papier l'emporte sur la pierre, la pierre l'emporte sur la paire de ciseaux, la paire de ciseaux l'emporte sur le papier.

Chaque joueur dispose de 3 boutons poussoirs (Pa1,Ca1,Ci1 pour le joueur 1 et Pa2, Ca2, Ci2 pour le joueur 2) correspondant respectivement à papier, pierre et ciseaux.

Un témoin lumineux par joueur (J1 et J2) indique à celui-ci qu'il doit jouer. Lorsqu'un joueur a enfoncé un des trois boutons poussoirs, son témoin lumineux Jx s'éteint. Le système détermine qui l'emporte par l'allumage des lampes G1 (si le joueur 1 a gagné) ou G2 (si le joueur 2 a gagné).

En cas de coup nul, une lampe N s'allume. Pour chaque joueur, l'enfoncement simultané de plusieurs des boutons de commande (Pa, Ca ou Ci) fait gagner le concurrent ; on introduit deux fonctions « tricheurs » T1 et T2 qui sont à 1 si un joueur enfonce plusieurs boutons à la fois.

Pour pouvoir jouer le coup suivant, il suffit que les poussoirs Pa, Ca et Ci des deux joueurs soient tous relâchés.

Le système électronique à réaliser possède donc 6 entrées logiques et 7 sorties logiques.

IMPORTANT:

* les lampes G1 et G2 indiquant le gagnant ne doivent s’allumer qu’une fois que les deux joueurs ont joués.
* si un seul joueur triche, l’autre joueur gagne mais la lampe Tx du tricheur ne doit s’allumer qu’une fois que les deux joueurs ont joués.
* si les deux joueurs trichent simultanément alors il y a coup nul et aucun joueur ne gagne.

### 1ère étape

* Dresser et compléter la table de vérité correspondant au fonctionnement du système.
* Rechercher et réduire les équations logiques des sorties J1, J2, T1 et T2 en fonction des entrées Pa1, Ca1, Ci1, Pa2, Ca2 et Ci2.
* Rechercher et réduire les équations logiques des sorties G1, G2 et N en fonction de J1, J2, T1,T2, Pa1, Ca1, Ci1, Pa2, Ca2 et Ci2.&#x20;

### 2ème étape

Réaliser le système en VHDL dans Vivado et tester sur la carte Basys 3.

