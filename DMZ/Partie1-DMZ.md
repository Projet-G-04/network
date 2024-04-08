# Rapport sur la configuration de la zone demilitarisée 
## Introduction 
La DMZ est un segment de réseau qui se situe entre le réseau interne de confiance et l'internet non fiable. 
Elle héberge généralement des serveurs accessibles au public, tels que des serveurs Web ou des serveurs de messagerie, tout en les isolant du réseau interne.
## vue d'ensemble sur la configuration 
Dans notre conception on a les equipements suivants : 

### ASAv-DMZ-I : 
Ce pare-feu ASA contrôle le trafic entrant et sortant vers et depuis la DMZ. Il dispose de deux interfaces :
Gi0/0 : Cette interface est connectée à un routeur ou un commutateur menant à Internet.
Gi0/2 : Cette interface se connecte au commutateur multi-couche (vIOS-DMZ-I) au sein de la DMZ.

### vIOS-DMZ-I : 
Ce commutateur Cisco vIOS-L2 est responsable de la commutation de couche 2 au sein de la DMZ. Il dispose de trois interfaces :
Gi0/1 : Cette interface est connectée au pare-feu ASA (ASAv-DMZ-I).
e0 : Cette interface est connecté à Serv-DMZ-I (serveur Linux).
VLAN10 : Cette interface VLAN peut être utilisée pour connecter d'autres appareils au sein de la DMZ.



### Serv-DMZ-I : 
Ce serveur Linux exécute Ubuntu 16.04.3 LTS. Il fournit probablement ces services :
DNS (Domain Name System) : Convertit les noms de domaine en adresses IP pour les appareils de la DMZ.
NTP (Network Time Protocol) : Synchronise l'heure sur les appareils de la DMZ.
Syslog : Fournit un service de journalisation des événements provenant des appareils de la DMZ.
Serveur Web : Ce serveur semble également héberger un service Web public accessible depuis Internet.

## Configuration du Serveur 

### choix du serveur 
Windows Server est largement utilisé et compatible avec un large éventail de logiciels. ce pour il est  une cible privilégiée pour les pirates informatiques en raison de sa popularité.
On a donc choisit l'utilisateur d'Ubuntu car celui ci est plus sécurisé pour une DMZ en raison de:
Sa base de code plus petite et moins complexe, ce qui réduit la surface d'attaque.
Sa communauté active qui développe et publie rapidement des correctifs de sécurité.
Son architecture open source qui permet une inspection et une modification transparentes du code.

## Configuration du firewall 


## Configuration du switch 
