# Lire une valeur analogique

Au chapitre précédent, nous avons lu un bouton qui est une entrée digitale (0 ou 1). A présent, nous allons lire une tension analogique.&#x20;

L'une des principales caractéristiques d'un convertisseur analogique digital (ADC) est sa résolution. La résolution sur le Pico est de 12 bits, donc chaque conversion donne une valeur entre 0 et 4095.

{% hint style="info" %}
La résolution du Pico est de 12 bits mais lorsque l'on va lire le résultat d'une conversion, il convertit la valeur en 16 bits, soit entre 0 et 65535.
{% endhint %}

Le Pico a 3 pins qui peuvent être utilisé comme ADC. Il s'agit de GP26\_ADC0, GP27\_ADC1, GP28\_ADC2, respectivement channel 0, 1 et 2. Un 4ème channel est utilisé pour le capteur de température interne au Pico.

Voici un code qui lit la valeur analogique de GP26 qui affiche la tension sur le shell. Utiliser un potentiomètre pour générer la tension analogique.&#x20;

```python
import machine
import utime

potentiometer = machine.ADC(26)

while True:
    value = potentiometer.read_u16() 
    print(value)
    utime.sleep(2)
```

La variable `potentiometer` contient l'objet ADC initialisé avec le numéro de pin GP26.

Le lecture du channel ADC se fait avec la fonction `read_u16()`. Le _u16_ veut simplement dire que cette fonction retourne un _unsigned 16bit integer_, ce qui veut dire une valeur entre 0 et 65535.

Si l'on veut afficher la valeur de la tension au lieu de la valeur binaire entre 0 et 65535. Il faut utiliser un facteur de conversion comme dans l'exemple ci-dessous.&#x20;

```python
import machine
import utime

potentiometer = machine.ADC(26)

conversion_factor = 3.3 / (65535)

while True:
    voltage = potentiometer.read_u16() * conversion_factor
    print(voltage)
    utime.sleep(2)
```

Le facteur de conversion correspond à la tension par incrément. Dans notre cas, un incrément d'un bit correspond à 0.5 uV/ incrément. Ainsi, lorsque l'on multiplie la valeur lu par l'ADC et le facteur de conversion, on obtient une tension. Vous pouvez vérifier le résultat avec un multimètre.

<details>

<summary>Exercice</summary>

Faire un chenillard avec 5 leds dont la vitesse varie à l'aide d'un potentiomètre.

</details>
