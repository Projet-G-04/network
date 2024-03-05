# Rapport sur la Configuration de la Couche d'Accès dans un Réseau d'Entreprise sur GNS3

## Introduction
Ce rapport traite de la configuration de la couche d'accès dans un réseau d'entreprise sur GNS3. La couche d'accès constitue la première étape de la connectivité réseau pour les utilisateurs finaux, et sa configuration est cruciale pour assurer un accès stable et sécurisé au réseau.

## Vue d'Ensemble de la Configuration
La couche d'accès est représentée par deux commutateurs OpenSwitch-Acc-I et OpenSwitch-Acc-II. Ces commutateurs sont des appliances OpenSwitch Qemu installées sur des disques VMware VMDK et exécutent le système d'exploitation réseau OpenSwitch version 0.4.0.

## Configuration des Ports et des VLANs
- Les ports Ethernet 3a et 4 des commutateurs sont configurés comme des ports d'accès, connectant les périphériques PC1 et PC4 au réseau d'entreprise.
- Les ports Ethernet 1 et Ethernet 2 sont configurés comme des liens montants, connectant les commutateurs d'accès aux commutateurs de distribution.
- Les VLANs 10, 20 et 999 sont configurés pour gérer le trafic des utilisateurs finaux et le trafic de gestion du réseau.

## Configuration des Interfaces de Gestion
- Les interfaces de gestion des commutateurs sont configurées avec des adresses IP statiques pour permettre l'accès à distance.
- Les ports Ethernet0 sont configurés comme des ports de gestion et sont connectés aux ports Ethernet6 des commutateurs de distribution.
- Les adresses IP et les masques de sous-réseau appropriés sont attribués à ces interfaces pour permettre la connectivité réseau.

## Configuration du Protocole NTP
- Les commutateurs d'accès sont configurés pour synchroniser leur horloge avec un serveur NTP situé dans le centre de données.
- Les adresses IP des serveurs NTP sont spécifiées dans la configuration des commutateurs pour faciliter la synchronisation de l'heure.

## Configuration de la Journalisation
- Les journaux des commutateurs d'accès sont envoyés à un serveur syslog-ng installé sur une appliance Server1 dans le centre de données.
- Les niveaux de gravité des journaux sont configurés pour collecter les messages pertinents.

## Sécurisation des Interfaces Inutilisées
- Les interfaces inutilisées des commutateurs sont sécurisées en les attribuant à un VLAN spécifique qui n'est pas utilisé pour le trafic utilisateur.

## Configuration des Mots de Passe
- Les mots de passe par défaut des comptes locaux sur les commutateurs sont modifiés pour renforcer la sécurité du réseau.
- Les mots de passe sont configurés en utilisant des procédures de changement de mot de passe sécurisées.

## Conclusion
La configuration de la couche d'accès dans un réseau d'entreprise sur GNS3 est une étape critique pour garantir un accès réseau fiable et sécurisé aux utilisateurs finaux. En configurant correctement les ports, les VLANs, les interfaces de gestion, les protocoles de synchronisation de l'heure et de journalisation, ainsi que les mesures de sécurité appropriées, il est possible de créer un environnement réseau robuste et stable pour l'entreprise.
