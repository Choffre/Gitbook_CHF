# Instructions concurrentes

Les instructions d'une architecture sont, sauf exception, évaluées en permence et toute simultanément. ce type de fonctionnement est appelé parallèle ou concurrent. L'ordre des instructions n'a donc pas d'influence.

## Assignation inconditionnelle

C'est la plus utilisée des instructions.

```vhdl
signal <= expression;
```

Exemple:

```vhdl
C <= A and B;
```

La sortie `C` prend la valeur du résultat de `A and B.`

L'affectation `std_logic` correspond à assigner un caractère:

```vhdl
signal_1bit <= '1';
```

L'affectation `std_logic_vector` correspond à assigner une chaîne de caractères:

```vhdl
vecteur_4bits <= "0101";
```

## Assignation conditionnelle

La forme générale:

```vhdl
signal <= expression1 when condition1 else
          expression2 when condition2 else
          ...
          expressionx when conditionx else expression_autre;
```

Exemple:

```vhdl
A <= B when (C='1') else 
     D when (E='1') 
     else '0';
```

A prend la valeur de B si C='1' sinon il prend la valeur de D si E='1' sinon il prend '0'.&#x20;

{% hint style="warning" %}
Il faut que les conditions listées soit exhaustives, elles ne doivent pas laisser de cas indéterminés. Dans le cas de l'exemple précédent, il faut absolument écrire la dernière ligne qui permet d'avoir une condition exhaustive.&#x20;
{% endhint %}

## Assignation sélective

La forme générale:

```vhdl
WITH selecteur SELECT
    signal <= expression1 WHEN valeur_selecteur1,
              expression2 WHEN valeur_selecteur2,
              ..
              expressionx WHEN OTHERS;
```

Voici un exemple:

```vhdl
architecture behavioral of mux is

signal ETAT : std_logic_vector(1 downto 0);
signal X,A,B,C,D : std_logic;

BEGIN
    with ETAT select
        X <= A when "00",
             B when "01",
             C when "10",
             D when others;
end ARCH_WITH;
```
