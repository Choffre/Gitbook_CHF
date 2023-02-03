# Architecture

Le description du fonctionnement interne d'un module se trouve dans l'architecture.&#x20;

## Niveau de description

Il existe plusieurs niveaux de description.

### **Description structurelle**

La fonctionnalité est décrite par l'utilisation et l'interconnexion de composants élémentaires. Il s'agit d'une transcription directe d'un schéma logique.&#x20;

### Description comportementale

Elle spécifie la fonctionnalité du circuit à l'aide de la syntaxe du langage VHDL. C'est le synthétiseur qui va ensuite interpréter la description et la traduire en logique concrète.&#x20;

{% hint style="info" %}
Nous allons utiliser la **description comportementale** dans ce cours et pour les exercices
{% endhint %}

## Syntaxe de l'architecture

L'architecture est divisée en deux parties : une zone déclarative et une zone d'instructions.&#x20;

Les instructions sont concurrentes, elles s'exécutent en parallèle. Les instructions d'une architecture peuvent donc être écrites dans un ordre quelconque, le fonctionnement ne dépend pas de cet ordre d'écriture.

```vhdl
ARCHITECTURE Behavorial OF ENTITY_NAME IS
    -- zone déclarative
BEGIN
    -- zone d'instructions
    instruction concurrente;
    instruction concurrente;
    ..
    instruction concurrente;
END Behavorial;
```

La zone déclarative permet de définir des types, des signaux ou des constantes qui seront utilisés dans les instructions suivantes. Elle permet également de déclarer des composants externes. &#x20;
