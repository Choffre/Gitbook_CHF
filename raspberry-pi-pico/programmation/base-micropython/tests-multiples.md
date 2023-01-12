# Tests multiples

Les test multiples permettent de tester plusieurs conditions en même temps. Il est possible d'utiliser les opérateurs booléen `and`, `or` , `not`.

Voici un exemple:

```python
x = 1
y = 2
if x==2 and y==2:
    print("X et Y sont égal à 2")

elif x==2 or y==2:
    print("X ou Y égal à 2")
        
if not x==2:
    print("X n'est pas égal à 2")
```

{% hint style="info" %}
L'expression `if not x==2:` est équivalent à `if x!=2:`
{% endhint %}
