# Rapport sur la configuration de la zone demilitarisée 
## Introduction 
La DMZ est un segment de réseau qui se situe entre le réseau interne de confiance et l'internet non fiable. 
Elle héberge généralement des serveurs accessibles au public, tels que des serveurs Web ou des serveurs de messagerie, tout en les isolant du réseau interne.
## vue d'ensemble sur la configuration 
Dans notre conception, la DMZ contient un pare-feu Cisco ASA , un commutateur de couche 3  et un serveur DMZ.

## Configuration du Serveur 

### choix du serveur 
Windows Server est largement utilisé et compatible avec un large éventail de logiciels. ce pour il est  une cible privilégiée pour les pirates informatiques en raison de sa popularité.
On a donc choisit l'utilisateur d'Ubuntu car celui ci est plus sécurisé pour une DMZ en raison de:
Sa base de code plus petite et moins complexe, ce qui réduit la surface d'attaque.
Sa communauté active qui développe et publie rapidement des correctifs de sécurité.
Son architecture open source qui permet une inspection et une modification transparentes du code.

## Configuration du firewall 

## Configuration du switch 
