# Mesurer le temps

Nous avons utilisé précédemment la fonction`sleep()`de la librairie `utime`. Cette librairie comporte également la fonction ticks\_ms() qui retourne la valeur d'un compteur en milliseconde.

## Exercice 1: Test de réaction

Le but de cet exercice est de faire un montage qui mesure le temps de réaction d'une personne. Le montage comporte une led verte, une led rouge et 2 poussoirs.

Au démarrage les leds sont éteintes. Ensuite, on presse un des deux boutons pour démarrer le jeu. Les 2 leds clignotent une fois afin d'avertir l'utilisateur que le jeu commence. Ensuite, après un temps aléatoire entre 1 et 3 secondes, une deux leds s'allume (choix de la led aléatoire également). L'utilisateur doit ensuite presser le bouton correspondant à la couleur de la led le plus rapidement possible. Une fois le bouton pressé, la led s'éteint. Il est possible de recommencer un test en pressant à nouveau le bouton.

Mesurer le temps de réaction et l'afficher dans le shell.

