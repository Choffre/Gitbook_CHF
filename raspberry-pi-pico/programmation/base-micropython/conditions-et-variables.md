# Conditions et variables

Les variables décrivent un endroit où l'on range des informations telles que des nombres, du texte, des listes de nombres ou de texte.  Elles peuvent être modifié à n'importe quel instant. On utilise des variables pour sauvegarder des données qui seront utilisées plus tard dans le code.&#x20;

{% hint style="info" %}
Contrairement à d'autre langage comme le C, les variables n'ont pas besoin d'être déclaré avant d'être utilisé.&#x20;
{% endhint %}

Les variables ont un **nom** qui identifie la variable et une **valeur** qui est enregistré dans la variable.

{% hint style="info" %}
En python, les variables n'ont pas besoin d'être déclarer avant d'être utilisé. Il suffit de leur assigner une valeur pour pouvoir les utiliser.
{% endhint %}

Créer un nouveau programme et taper la ligne suivante:

```python
nom = input("Quel est le meilleur joueur de tennis? ")
```

Exécuter le programme. Taper la réponse et puis appuyer sur Enter. Comme c’est l’unique ligne de code de votre programme, il ne se passe rien.

Ajouter les lignes suivantes pour utiliser le résultat.

```python
if nom == "Roger Federer":
    print("Vous avez raison")
else:
    print("Il y a meilleur que lui")
```

Si vous répondez autre chose que Roger Federer, le programme répondra « Il y a meilleur que lui ». Lorsque vous écrivez « Roger Federer », le programme répondra « Tu as raison ».

Le symbole `==` permet de faire une comparaison directe entre la variable nom et le texte qui a été répondu. Dans ce cas, nous comparons deux chaînes de caractères, ce que l’on appelle des strings.

Si l'on compare des nombres, il est possible d'utiliser les comparaisons suivantes:

| >  | est plus grand que         |
| -- | -------------------------- |
| <  | est plus petit que         |
| >= | est plus grand ou égale à  |
| <= | est plus petit ou égale à  |
| == | est égal à                 |
| != | est différent de           |

