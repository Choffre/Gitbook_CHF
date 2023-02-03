# Entité

L'entité représente donc la vue externe d'un circuit. Dans la rubrique PORT, on y trouve la définition des entrées et sorties du composant.&#x20;

Voici la syntaxe de la déclaration d'entité.

```vhdl
ENTITY ENTITY_NAME IS
    PORT (
        A,B : mode type;
        C : mode type
    );
END ENTITY_NAME;
```

## Mode

Le mode précise le sens du signal. Les principaux modes définis en VHDL sont:

* **IN**: applicable à un signal d'entrée (monodirectionnel)
* **OUT**: applicable à un signal de sortie. Ne peut pas être relu dans l'architecture.
* **INOUT**: applicable à un signal bidirectionnel

## Type

Il existe plusieurs types prédéfinis comme `integer, natural, positive, bit, bit_vector, boolean, real, time`.&#x20;

Pour la synthèse de circuit logique, nous allons utiliser principalement les types complémentaires **`std_logic`** et **`std_logic_vector`**. &#x20;

Le type `std_logic` peut prendre 9 valeurs décrivant tous les états d'un signal électronique numérique. Dans un premier temps, nous allons utiliser les états suivants:

* `'0'` niveau 0&#x20;
* `'1'` niveau 1
* `'Z'` haute impédance&#x20;
* `'-'` quelconque (indifférent)

Le type std\_logic est défini par le paquetage normalisé IEEE.std\_logic\_1164, il est donc obligatoire de déclarer celui-ci au début de son fichier VHDL.&#x20;

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;
```

Voici un exemple de déclaration d'un signal de type `std_logic_vector`:&#x20;

```vhdl
DATA : in std_logic_vector(15 downto 0);  --  DATA est un vecteur d'entrée de 16 bits
```

`DATA` est donc un vecteur qui contient les 16 signaux de type `std_logic` suivants: `DATA(15), DATA(14), ..., DATA(1), DATA(0)`

## Exemple

Voici la déclaration de l'entité correspondant à l'exemple de la [page précédente](./).

<pre class="language-vhdl"><code class="lang-vhdl"><strong>ENTITY Fonction1 IS
</strong>    PORT (
        A,B : IN std_logic;
        C : OUT std_logic
    );
END Fonction1;
</code></pre>
