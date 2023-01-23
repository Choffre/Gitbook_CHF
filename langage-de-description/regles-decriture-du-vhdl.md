# Règles d'écriture du VHDL

### Commentaires

Les commentaires débutent par un double tiret et se prolonge jusqu'à la fin de la ligne.

<pre class="language-vhdl"><code class="lang-vhdl"><strong>a &#x3C;= b AND c ;  --en VHDL le symbole &#x3C;= effectue une assignation
</strong>                --a prend la valeur de l'operation logique (b and c)
</code></pre>

### Majuscules et minuscules

VHDL ne fait pas la différence entre les majuscules et les minuscules. `TESTENTREE` est identique à `testentree.`

### Identificateurs

Les identificateurs pour les objets utilisés en VHDL doivent suivre les règles de dénomination suivantes:

* Le premier caractère doit être une lettre.&#x20;
* Il peut comporter des lettres (les 26 lettre de l'alphabet uniquement, minuscules ou majuscules), chiffres ou underscore "\_".
* Il ne peut pas y avoir 2 "\__" qui se suivent et "\_" ne peut pas terminer le nom._
* _L'identificatuer ne pas être un nom réservé._

### Noms réservés

Le langage défini des mots clés qui ont une fonction définie et qui ne peuvent pas être utilisés comme identificateur. Vous trouvez la liste complète sur ce lien.&#x20;

{% embed url="https://www.gladir.com/CODER/VHDL/reservedword.htm" %}

### Fin d'instruction

Les instructions VHDL se terminent par le séparateur ";".&#x20;

### Espaces, sauts de lignes

Les espaces ne sont pas significatifs sauf dans les valeurs littérales et pour la séparation des identificateurs.

```vhdl
A <= B and C;
A<=B and C ;
```

Une instruction peut s'étendre sur plusieurs lignes.

```vhdl
A <= B when C='0' else D;
```

peut aussi s'écrire&#x20;

```vhdl
A <= B when C='0' 
else D;
```

###
