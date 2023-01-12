# Opérations sur les variables numériques

Pour mieux comprendre comment utiliser les variables exécuter les codes suivants et analyser le résultat:

```python
a=3
a=a+2
print(a)
a=a+a
print(a)
```

Voici les opérations de base que l'on peut effectuer en python sur des nombres.

```python
a=5
b=3
print(a+b)
print(a-b)
print(a*b)
print(a/b)
```

Pour les puissances, on double la multiplication. On obtient donc `x**n`.&#x20;

Pour la racine carrée qui est équivalent au nombre puissance 0.5, on utilise la même notation.&#x20;

```python
print(2**3) # Affiche le résultat de 2 puissance 3
print(3**2) # Affiche le résultat de 3 puissance 2
print(9**0.5) # Affiche la racine carrée de 9
print(2**0.5) # Affiche la racine carrée de 2
```

On peut réaliser également des divisions euclidiennes. Le quotient d'une division s'obtient avec `//` et le reste avec `%.`

```python
a=22
b=3
print(a//b) # Affiche le quotient de la division euclidienne de a par b
print(a%b) # Affiche le reste de la division euclidienne de a par b
```
