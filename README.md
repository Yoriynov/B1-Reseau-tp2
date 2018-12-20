B1-Reseau-tp2
# **I. Exploration locale en solo**
## **1. Affichage d'informations sur la pile TCP/IP locale**
### En ligne de commande
J’ai utilisé la ligne de commande « ipconfig /all » écrit sur powershell
#### Affichez les infos des cartes réseau de votre PC
•	nom, adresse MAC et adresse IP de l'interface WiFi

- Intel(R) Dual Band Wireless-AC 3168
- 30-E3-7A-E8-46-17
- 10.33.1.197/22

•	nom, adresse MAC et adresse IP de l'interface Ethernet
- Qualcomm Atheros AR8171/8175 PCI-E Gigabit Ethernet Controller
- 4C-CC-6A-DB-D9-A8
- Je n’ai pas d’IP dans Ethernet car je ne suis pas branché par câble Ethernet.

•	déterminer, pour chacune d'entre elles :

o	adresse de réseau : 

Conversions et étapes :

Ip : 10.33.1.197/22 => 0000 1010. 0010 0001. 0000 0001. 1100 0101
Masque : 255.255.252.0 => 1111 1111. 1111 1111. 1111 1100. 0000 000
Et donc : 0000 1010. 0010 0001. 0000 0000. 0000 0000 => 10.33.0.0

o	adresse de broadcast :

Et donc : 0000 1010. 0010 0001. 0000 0011. 1111 1111 => 10.33.3.255

#### Affichez votre gateway

•	trouvez sur internet une commande pour connaître

l'adresse IP de la passerelle de votre carte WiFi
L’adresse IP passerelle : 10.33.3.253

### En graphique (GUI : Graphical User Interface)
#### Trouvez comment afficher les informations sur une carte IP (change selon l'OS)


•	trouvez l'IP, la MAC et la gateway pour l'interface WiFi de votre PC :

- Pour ce faire vous devez faire un clique droit sur l’icône Wifi
- Cliquer sur « Ouvrir les paramètre réseaux et Internet »
- Une page s’ouvre et en bas de la page il y a « Centre Réseaux et partage »
- Une autre page s’ouvre et en haut a gauche cliquer sur « Modifier les paramètres de la carte »
- Sur cette page suivante faites un click droit sur votre carte Wi-Fi et cliquer sur « Statut » et ensuite « Details »  

#### Questions
•	à quoi sert la gateway dans le réseau d'Ingésup ? :

la gateway dans le réseau d’ingésup permet a tout les utilisateurs du réseau d’aller sur Internet.
## 2. Modifications des informations
### A. Modification d'adresse IP - pt. 1
Utilisez l'interface graphique de vorte OS pour changer d'adresse IP :

•	calculez la première et la dernière IP du réseau

-	La première Ip du réseau à été calculer auparavant et est : 10.33.0.0
-	La dernière Ip du reseau est donc 10.33.3.255

•	changez l'adresse IP de votre carte WiFi pour une autre (mais toujours dans le même réseau)
Pour changer l’adresse IP de votre carte Wifi, il faut donc l’IP que vous possédez actuellement, votre masque de réseau et votre passerelle par défaut avec la manipulation que je vous ai décrite plus haut, revenez sur clique droit de votre carte Wifi.
-	« Sur cette page suivante faites un click droit sur votre carte Wi-Fi et cliquer sur « Statut » et ensuite « Details » » ( Rappel )
-	Donc vous faites un clique droit sur votre carte Wifi et içi vous sélectionner « Propriétés » ensuite sur « Protocole internet version 4 »
-	Encore Propriétés et « Utiliser l’adresse IP suivante » içi il vous faut rentrer votre masque de sous réseau et   votre passerelle par défaut obtenue auparavant 
-	Et la vous rentrer votre nouvelle adresse IP
### B. Nmap
### C. Modification d'adresse IP - pt. 2

•	Modifiez de nouveau votre adresse IP vers une adresse IP que vous savez libre grâce à nmap :

Pour ce faire vous devez telecharger nmap. Une fois fait ouvrez votre invite de commande et faites "nmap -sn -PE "adresse réseau"" pour avoir toutes les adresses IP du réseau et donc prenez une adresse qui n'est pas prise et mettez votre nouvelle adresse Ip avec ce jai expliqué précédemment 

•	Modifiez votre adresse de gateway et essayez d'aller sur un site internet

Pour modifier son adresse gateway, rien de plus simple refaites le cheminement comme pour changer son adresse IP et changer votre passerelle par défaut

