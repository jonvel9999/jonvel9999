TP1_Construire un réseau Ethernet
*********************************

But
___
Installer et configurer un hôte pour qu'il puisse communiquer avec d'autres hôtes sur un réseau Ethernet commuté. 

Matériel
________

1. Un commutateur Ethernet avec son alimentation (commutateur), max 5 étudiants par commutateur
2. Son ordinateur personnel comme station Ethernet

Prérequis
_________
Chaque ordinateur personne est déconnecté d’internet, seule la liaison filaire ethernet est activée la carte wifi est mise hors service.

L’étudiant doit effectuer des recherches pour mettre en service son hôte sur le commutateur de groupe. Les résultats de ses recherches et des questions posées doivent se trouver dans un PDF depuis un le fichier de référence sphinx mis à disposition par l'enseignant.

Chaque groupe se voit attribuer une plage d’adresse IP

- Groupe 1 : 10.1.0.0 à 10.1.0.10
- Groupe 2 : 10.2.0.0 à 10.2.0.10
- Groupe 3 : 10.3.0.0 à 10.3.0.10
- Groupe 4 : 10.4.0.0 à 10.4.0.10
- Groupe 5 : 10.5.0.0 à 10.5.0.10

Théorie nécessaire 
__________________

En Ethernet, chaque carte réseau de votre station possède une adresse physique unique que le constructeur à paramétrer dans la mémoire ROM. C’est la fameuse adresse MAC.

On pourrait penser que seul l’adresse physique MAC de la couche « liaison de données » est suffisante pour que les stations puissent communiquer au travers du commutateur. C’est en partie vrai puisque seule l’adresse physique est comprise par la carte de éseau pour communiquer.  Mais dans ce TP je vous demande de pinger les stations, autrement dit d’utiliser une application de la plus haute couche « applicative » dont la couche inférieure TCP-IP exige une adresse IP. Aussi, vous devrez configurer une adresse IP fixe de manière manuelle dans votre station et désactiver les serveurs de distribution automatique d’adresses (DHCP)

Travail à effectuer
___________________

Etablissez un échange entre les différents hôtes de votre réseau afin de vérifier la communication entre hôtes. Pour cela, lancez la commande ping suivi de l'adresse IP de l'hôte distant et vérifiez que les paquets ont tous été reçus correctement.

.. code-block:: bash

    ping 10.1.0.0


Lorsque la communication fonctionne entre les stations, alors répondez aux questions.

Question 1
..........
Noter l’adresse IP choisie, relever l’adresse MAC de votre station et déterminer le constructeur de la carte (voire norme OUI)

Question 2
..........
Dans ce travail, vous paramétrez une adresse IP mais comment la station connaît-elle  l’adresse MAC de la station destination puisque le ping ne demande que l’adresse IP de destination ? par quel moyen, faites des recherches.

Question 3
..........
L’échange des informations entre couches est visualisable avec le logiciel « wireshark » Télécharger sur son ordi personnel et configurera le logiciel pour visualiser les échanges de trames ethernet.

+-----------+-----------+-----------+
| Heading 1 | Heading 2 | Heading 3 |
+===========+===========+===========+
| Hello     | World     |           |
+-----------+-----------+-----------+
| foo       |                       |
+-----------+          bar          |
| baz       |                       |
+-----------+-----------------------+
