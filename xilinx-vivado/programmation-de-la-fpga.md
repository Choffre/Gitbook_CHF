# Programmation de la FPGA

Une fois la description terminé. Il faut faire la synthèse du projet en cliquant sur le triangle vert ou en pressant F11. La fenêtre "Launch Runs" apparaît, cliquez sur "Ok".

<figure><img src="../.gitbook/assets/Launch_run.PNG" alt=""><figcaption></figcaption></figure>

Lorsque la synthèse s'est correctement passé, le message suivant apparaît.

<figure><img src="../.gitbook/assets/Synthes_completed.PNG" alt=""><figcaption></figcaption></figure>

Ensuite lancer l'implémentation en cliquant sur "Ok".

<figure><img src="../.gitbook/assets/ImplementationCompletedb.PNG" alt=""><figcaption></figcaption></figure>

Lorsque l'implémentation est faite, cliquer sur OK pour générer le bitstream.&#x20;

Puis cliquer sur Program Device,&#x20;

<figure><img src="../.gitbook/assets/prg.PNG" alt=""><figcaption></figcaption></figure>

Sélectionner le fichier .bit généré à l'étape précédente et programmer la FPGA.&#x20;

<figure><img src="../.gitbook/assets/prg_dev.PNG" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Bravo, la FPGA est maintenant programmer. Par contre, le programme sera effacer si vous éteignez la carte. Si vous désirez que le programme soit gardé en mémoire flash, veuillez suivre la procédure suivante.
{% endhint %}
