# Lire un bouton

Connecter le Raspberry Pico sur une carte d'essai et connecter également un bouton poussoir. Relier une des pins du bouton poussoir au 3.3V et l'autre à une entrée GPIO (par exemple GP15).

Voici un schéma de la connexion interne d'un bouton poussoir.

<figure><img src="../../.gitbook/assets/button-connection-digram.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Afin de ne pas être flottante, une entrée a besoin d'une pull up ou d'une pull down pour fixer son état (0 ou 1). Dans le cas du Raspberry Pico, ces pull up/down sont directement contenu dans le microcontrôleur (uC). Par défaut, une pull down est utilisé.
{% endhint %}

&#x20; Voici ci-dessous le code qui permet de lire le bouton.

```python
import machine
import utime

bouton = machine.Pin(15, machine.Pin.IN)

while True:
    if bouton.value() == 1:
        print("Le bouton est pressé!")
        utime.sleep(2)
```

La variable `bouton` contient la classe `pin` qui dans ce cas est configuré en entrée pour la GP15.

Le programme va lire le bouton et lorsqu'il sera pressé, le message "Le bouton est pressé!" sera affiché. Si le bouton n'est pas pressé, il ne se passe rien.&#x20;

## Exercices

<details>

<summary>Exercice 1</summary>

Faire un programme qui allume une led lorsque l'on presse sur le bouton et qui s'éteint lorsque l'on relache le bouton.

</details>

<details>

<summary>Exercice 2</summary>

Modifier l'exercice 1 afin que le bouton fonctionne comme un interrupteur. On presse une première fois pour allumer, puis on presse à nouveau pour éteindre.

</details>
