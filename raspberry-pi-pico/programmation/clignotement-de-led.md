# Clignotement de led

Voici un programme simple qui permet de faire clignoter la led qui se situe sur la carte.

```python
import machine 
import utime 

led_pin = machine.Pin(25, machine.Pin.OUT) #version pour Rapsberry Pico
#led_pin = machine.Pin('led', machine.Pin.OUT) #version pour Rapsberry Pico W

while True:
    led_pin.value(1) #allume la led
    utime.sleep(1) #attend 1 seconde
    led_pin.value(0) #éteint la led
    utime.sleep(1) #attend 1 seconde
```

Pour interagir avec le hardware, il y a besoin d’importer des librairies de code MicroPython afin de les rendre accessible. Pour faire clignoter une led, nous avons besoin des librairies `machine et utime`.

| `machine` | fournit les fonctions relative au hardware. Cette librairie contient la classe Pin qui permet de contrôler les pins I/O. |
| --------- | ------------------------------------------------------------------------------------------------------------------------ |
| `utime`   | fournit les fonctions relative au temps.                                                                                 |

{% hint style="info" %}
A la place de mettre `import machine` et puis d'utiliser `machine.Pin`(), il est possible d'importer directement la classe Pin en écrivant `from machine import Pin`. Ainsi, il est possible de remplacer `machine.Pin(...)` par uniquement `Pin(...)`&#x20;
{% endhint %}

La prochaine ligne assigne la classe `Pin` de la librairie `machine` à la variable `led_pin`. Ce nom de variable a été choisi. A savoir que l’on aurait pu choisir n’importe quel nom, mais il est toujours préférable d’utiliser un nom qui correspond au but de la variable.

Le premier argument, `25`, est le numéro de pin qui sera utilisé. Il correspond au GPIO de la led qui se situe sur la carte.&#x20;

{% hint style="warning" %}
Pour utiliser la led interne:

Il s'agit de la pin `25` sur la carte Pico sans wifi.&#x20;

Sur la carte avec wifi, la pin utilisé pour la led est également utilisé pour autre chose, il faut utiliser`'led' à la place de 25.`
{% endhint %}

Le second argument `machine.Pin.OUT` assigne cette pin comme sortie.

La ligne `while True :` défini une boucle infinie. Les lignes de code suivantes sont indentées ce qui signifie qu’elles font parties de la boucle.

L’objet `Pin` que contient la variable `led_pin` a une fonction `value()`. Cette fonction permet de mettre la sortie à 0 ou 1, respectivement 0V ou 3.3V.

La classe `sleep` de la libraire `utime` permet de faire des pauses dans le programme. Les lignes `utime.sleep(1)` permettent de faire des pauses de 1 seconde.

## Exercices

<details>

<summary>Exercice 1</summary>

Simplifier le code en utilisant la fonction toggle() au lieu de value().

Voici un lien sur la documentation de la librairie utime.&#x20;

[https://docs.micropython.org/en/v1.15/library/utime.html](https://docs.micropython.org/en/v1.15/library/utime.html)

</details>

<details>

<summary>Exercice 2</summary>

Faire différent essais en diminuant le delay. Quel est le plus petit délai qui permet de toujours voir le clignotement?

</details>

<details>

<summary>Exercice 3</summary>

Ajouter une led externe avec la résistance nécessaire et la faire clignoter.

</details>

<details>

<summary>Exercice 4</summary>

Ajouter une 2ème led externe et faire un programme qui les allument en alternance.

</details>

<details>

<summary>Exercice 5</summary>

Mettre 5 leds externes et faire un chenillard.&#x20;

</details>
