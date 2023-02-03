# Signaux, constantes

Ces éléments peuvent être déclarés dans la **partie déclarative** de l'architecture.&#x20;

## Signaux

Il est souvent nécessaire de faire appel à des signaux internes dans la description d'architecture. Ces signaux internes sont équivalents à un signal d'entité, à deux exceptions près:

* un signal interne n'a pas de mode ( pas de sens). Voici un exemple de déclarations de signaux internes:

<pre class="language-vhdl"><code class="lang-vhdl"><strong>SIGNAL BUS_LOCAL : std_logic_vector(23 DOWNTO 0);
</strong>SIGNAL CARRY_IN, CARRY_OUT : std_logic;
</code></pre>

* Un signal interne peut disparaître lors de la synthèse du circuit en fonction de l'optimisation.&#x20;

## Constante

Une constante peut être assimilée à un signal interne auquel est associé une valeur fixe et définitive. La déclaration d'une constante est rarement une nécessité, elles sont utilisées pour une meilleures lisibilité et une meilleure compréhension.&#x20;

L'affection de valeur pour les constantes s'effectue avec l'opérateur ':=', voici quelques exemples:

```vhdl
CONSTANT ZERO : std_logic_vector(l DOWNTO 0) := "00";
CONSTANT HUIT_OU_PLUS : std_logic_vector(3 DOWNTO 0) := "1---";
CONSTANT HAUTE_IMPED : std_logic_vector(7 DOWNTO 0) := "ZZZZZZZZ"
```

Lorsqu'il est nécessaire de mettre tous les bits d'un vecteur à la même valeur, il est possible d'utiliser l'écriture simplifiée suivante:

```vhdl
CONSTANT HI_Z : std_logic_vector(15 DOWNTO 0) := (OTHERS => 'Z');
```

##

