# Ex 5: Convertisseur bin - 7 seg

A l’aide des boutons « SW0 » à « SW3 », créez un programme permettant de convertir les valeurs binaires reçues par ces 4 boutons pour les afficher sur l’un des afficheur 7 segments.

<figure><img src="../../.gitbook/assets/convertisseur_7seg.PNG" alt=""><figcaption></figcaption></figure>

Les valeurs à afficher sont en hexadécimal allant de 0 à F.

{% hint style="info" %}
Prenez le temps de bien observer le schéma électrique des afficheurs 7 segments. Notamment pour trouver comment le / les sélectionner (il s’agit d’une matrice).
{% endhint %}

Voici les codes à envoyer sur les digits pour afficher le nombre désiré :

* 0 : 1000000
* 1 : 1111001 &#x20;
* 2 : 0100100&#x20;
* 3 : 0110000&#x20;
* 4 : 0011001&#x20;
* 5 : 0010010&#x20;
* 6 : 0000010&#x20;
* 7 : 1111000&#x20;
* 8 : 0000000&#x20;
* 9 : 0010000&#x20;
* A(10) : 0001000&#x20;
* B(11) : 0000011&#x20;
* C(12) : 0100111&#x20;
* D(13): 0100001&#x20;
* E(14) : 0000110&#x20;
* F(15) : 0001110
