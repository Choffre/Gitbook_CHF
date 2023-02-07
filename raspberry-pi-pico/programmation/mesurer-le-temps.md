# Mesurer le temps

Nous avons utilisé précédemment la fonction`sleep()`de la librairie `utime`. Cette librairie comporte également la fonction `ticks_ms()` qui retourne la valeur d'un compteur en milliseconde.

## Exercice:&#x20;

Le but de cet exercice est de faire un montage qui mesure le temps de réaction d'une personne. Le montage comporte une LED verte, une LED rouge et 2 poussoirs.

Au démarrage les LEDs sont éteintes. Ensuite, on presse un des deux boutons pour démarrer le jeu. Les 2 LEDs clignotent une fois afin d'avertir l'utilisateur que le jeu commence. Ensuite, après un temps aléatoire entre 1 et 3 secondes, une des deux LEDs s'allume (choix de la led aléatoire également). L'utilisateur doit ensuite presser le bouton correspondant à la couleur de la LED le plus rapidement possible. Une fois le bouton pressé, la LED s'éteint. Il est possible de recommencer un test en pressant à nouveau le bouton.

Calculer le temps entre le moment de l'enclenchement de la LED et la pression du bouton poussoir. Afficher le résultat dans le Shell dans le format suivant:

`Votre temps de réaction est de: xxx ms`

Si le bouton n'a pas été pressé dans la seconde qui suit l'enclenchement. La LED s'éteint et le message suivant est affiché.

`Vous n'avez pas pressé sur le bouton.`

Si le mauvais bouton est pressé, le message suivant est affiché.

`Vous avez pressé le mauvais bouton.`

