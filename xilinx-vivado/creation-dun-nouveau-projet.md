# Création d'un nouveau projet

Veuillez suivre la procédure suivante pour créer un nouveau projet.

Dans le menu **Files**, cliquez sur **New project**.

{% hint style="info" %}
Ne pas mettre d'espace dans le nom du projet
{% endhint %}

<figure><img src="../.gitbook/assets/NewProject.PNG" alt=""><figcaption></figcaption></figure>

Sélectionner "RTL Project" et décocher "Do not specify sources at this time"

<figure><img src="../.gitbook/assets/project_type.PNG" alt=""><figcaption></figcaption></figure>

Créer une source en cliquant sur le +, puis "Create file".&#x20;

<figure><img src="../.gitbook/assets/add_source.PNG" alt=""><figcaption></figcaption></figure>

Sélectionner le type VHDL et donner un nom au fichier. Vous pouvez donner le même nom que pour le projet.

<figure><img src="../.gitbook/assets/create_source.PNG" alt=""><figcaption></figcaption></figure>

Cliquez sur Next et ensuite ajouter le fichier de contrainte correspondant à la carte Basys 3 (Basys-3-Master.xdc). Ce fichier se trouve dans le dossier digilent-xdc-master que vous avez copier dans vos documents pendant la procédure d'installation. Cochez "Copy constraints files into project" et cliquez sur Next.

<figure><img src="../.gitbook/assets/contraintes.PNG" alt=""><figcaption></figcaption></figure>

Rechercher et choisir la carte Basys 3 dans l'onglet "Boards".

<figure><img src="../.gitbook/assets/part.PNG" alt=""><figcaption></figcaption></figure>

Puis cliquez sur **Next** et puis **Finish**. Le projet est maintenant créé.

Vivado ouvre à présent une fenêtre pour définir les entrées et sorties du projet. Pour l'exercice 1, il y a 1 entrée SW0 et 1 sortie LD0 comme dans l'exemple ci-dessous.

<figure><img src="../.gitbook/assets/define_module (1).PNG" alt=""><figcaption></figcaption></figure>

Voici une vue du projet que vous devez obtenir.

<figure><img src="../.gitbook/assets/sources.PNG" alt=""><figcaption></figcaption></figure>
