# Instructions séquentielles

## Process

Le PROCESS est un ensemble de logique exécuté séquentiellement. A l'intérieur du PROCESS, l'ordre des instructions est important.

La syntaxe de l'instruction d'un PROCESS est la suivante:

<pre class="language-vhdl"><code class="lang-vhdl"><strong>label:
</strong>PROCESS(sensitivity_list)
    --zone déclarative du process
    
BEGIN
    instruction sequentielle;
    instruction sequentielle;
    ..
    instruction sequentielle;
END PROCESS;
</code></pre>

La liste de sensibilité (sensitivity\_list) contient la liste de signaux qui vont réveiller un PROCESS en sommeil.&#x20;

La zone déclarative est privé au PROCESS, des variables peuvent être déclarés à cet endroit.

Entre BEGIN et END PROCESS se situe la zone d'instructions qui sont exécutées séquentiellement. On peut faire l'analogie entre cette zone et un boucle infinie en programmation.&#x20;

{% hint style="info" %}
**Séquentielles et concurrents**

Ce qui se trouve à l'intérieur d'un process se déroule donc de manière séquentiel. Le process dans sa globalité est concurrent à d'autre process ou d'autres instruction.&#x20;
{% endhint %}
