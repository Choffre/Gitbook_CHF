# Boucles et indentation

Un programme en MicroPython s'exécute du haut au bas de la page, comme les autres langages de programmation, de la même manière que si l’on écrivait chaque ligne une par une dans le Shell.&#x20;

Contrairement au langage c par exemple, le MicroPython n’utilise pas de {} pour contrôler les séquences mais l’indentation.

## Boucle finie

Créer un nouveau programme dans Thonny et commencer le programme par:

<pre class="language-python"><code class="lang-python">print("Start!")
for <a data-footnote-ref href="#user-content-fn-1">i </a>in range(10):
</code></pre>

La première ligne écrit un simple message dans le shell.

La seconde ligne est une boucle défini qui va s’exécuter 10 fois. Une variable `i` est assigné à la boucle et sera incrémenté automatiquement à chaque exécution. Dans ce cas, la variable `i` prendra les valeurs 0 à 9, ce qui correspond bien à 10 exécutions. Le symbole `:` indique a Micropython que la boucle commence à la prochaine ligne.

Une variable est un outil très puissant dans tous les langages de programmation. Ils ont une valeur qui peut changer dans le temps ou par le programme. Une variable a 2 aspects, son nom et les données qu’elle contient. Dans le cas de la variable `i`, son nom est i et sa valeur va s’incrémenter automatiquement (de 0 à 9) après chaque exécution du contenu de la boucle.

Pour ajouter une ligne de code à l'intérieur de la boucle il faut l’indenter (touche « tab », ou 4 espaces). Thonny ajoute automatiquement quand on presse Enter après les `:`.

Ajouter dans la boucle la ligne suivante.

```python
    print("Loop number", i)
```

En dehors de la boucle (donc non indenté, aligner avec le for) ajouter la ligne suivante:

```python
print("Loop finished!")
```

Le programme de démonstration est maintenant terminé. La première ligne est en dehors de la boucle et est exécuté une seule fois. La seconde ligne défini la boucle, la troisième sera exécuter 10x et la quatrième ligne est en-dehors de la boucle et sera exécuté une seule fois. Voici donc le code complet:

```python
print("Loop Starting!")
for i in range(10):
    print("Loop number", i)
print("Loop finished!")
```

Cliquer sur Run pour voir le résultat du programme dans le shell.

## Boucle infinie

La boucle infini renferme un code qui sera exécuté indéfiniment. Remplacer la boucle for par la boucle infini suivante:

```python
while True:
```

Si vous exécuter le code, vous obtiendrez une erreur disant que `i` n’est pas défini puisque l’on a supprimé la ligne qui créait et assignait une valeur à `i`. Pour corriger, modifier la ligne 3 par la suivante et exécuter le programme.

```python
 print("Loop running!")
```

{% hint style="info" %}
Dans les exemples ci-dessus, nous utilisons print() et range() qui sont deux fonctions prédéfinis. Le nom d'une fonction est suivi par des parenthèses dans lesquels il peut y avoir zéro, un ou plusieurs arguments.  &#x20;
{% endhint %}

## Exercices

{% tabs %}
{% tab title="Ex 1" %}
Faire un programme avec 2 boucles définis à la suite
{% endtab %}

{% tab title="Ex 2" %}
Faire un programme avec une boucle défini dans une boucle défini
{% endtab %}

{% tab title="Ex 3" %}
Faire un programme avec une boucle infini et compter le nombre de passage dans la boucle et l'afficher dans le shell.
{% endtab %}
{% endtabs %}



[^1]: 
