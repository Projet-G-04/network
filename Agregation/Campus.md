## Rapport  sur la partie d'agrégation d'un projet réseau avec 3 routeurs 

### Introduction

Ce rapport fournit une description détaillée de la partie d'agrégation d'un projet réseau composé de trois routeurs : VIOS-Core-1, VIOS-Core-2 et OpenSwitch-Acc-1. Le rapport couvre les aspects suivants :

* Topologie du réseau
* Adressage IP
* Routage
* VLAN
* Sécurité
* Qualité de service (QoS)
* Conclusion
* Recommandations
* Annexe

### Topologie du réseau

Le réseau est organisé en une topologie hiérarchique à trois niveaux, avec les routeurs VIOS-Core-1 et VIOS-Core-2 au niveau supérieur (noyau) et le routeur OpenSwitch-Acc-1 au niveau inférieur (accès). Les périphériques finaux, tels que les ordinateurs portables et les serveurs, sont connectés au routeur OpenSwitch-Acc-1.
## Définition des routeurs dans le projet réseau (Markdown)

### VIOS-Core-1 et VIOS-Core-2

Les routeurs VIOS-Core-1 et VIOS-Core-2 sont des routeurs de **noyau** (également appelés routeurs de distribution). Ils occupent une position centrale dans le réseau et assurent les fonctions suivantes :

* **Routage inter-VLAN:** Ils permettent la communication entre les différents VLANs configurés sur le réseau.
* **Liaison avec le réseau externe:** Ils assurent la connexion entre le réseau interne et le réseau externe, comme Internet.
* **Agrégation de liens:** Ils peuvent combiner plusieurs liaisons physiques en une seule liaison logique, augmentant ainsi la bande passante et la redondance.
* **Gestion du trafic:** Ils appliquent des politiques de qualité de service (QoS) pour prioriser le trafic en fonction de son type (voix, données, vidéo).
* **Sécurité:** Ils mettent en œuvre des mesures de sécurité pour protéger le réseau contre les accès non autorisés et les attaques malveillantes.

Ces routeurs sont généralement des équipements haut de gamme dotés de processeurs puissants et de fonctionnalités avancées, capables de gérer des volumes de trafic importants et de répondre aux exigences de performance élevées des réseaux modernes.

### OpenSwitch-Acc-1

Le routeur OpenSwitch-Acc-1 est un routeur d'**accès** (également appelé routeur de périphérie). Il se situe à la périphérie du réseau et assure les fonctions suivantes :

* **Connexion des périphériques finaux:** Il permet aux périphériques finaux, tels que les ordinateurs portables, les serveurs et les imprimantes, de se connecter au réseau.
* **Filtrage du trafic:** Il filtre le trafic entrant et sortant en fonction des règles de sécurité définies.
* **Gestion des adresses IP:** Il attribue des adresses IP aux périphériques finaux et gère les adresses IP dynamiques.
* **Support VLAN:** Il prend en charge les VLANs et permet de segmenter le réseau en différents domaines de diffusion.
* **Surveillance du réseau:** Il fournit des informations sur l'état du réseau et permet de détecter les éventuels problèmes.

Ce routeur est généralement un équipement économique et fiable, adapté aux réseaux de petite et moyenne taille.

### Tableau récapitulatif des caractéristiques des routeurs (Markdown)

| Caractéristique | VIOS-Core-1/VIOS-Core-2 | OpenSwitch-Acc-1 |
|---|---|---|
| Type | Routeur de noyau | Routeur d'accès |
| Fonction principale | Routage inter-VLAN, liaison avec le réseau externe, agrégation de liens, gestion du trafic, sécurité | Connexion des périphériques finaux, filtrage du trafic, gestion des adresses IP, support VLAN, surveillance du réseau |
| Performances | Élevées | Moyennes |
| Coût | Élevé | Faible |
| Complexité | Plus complexe | Plus simple |

**Remarque:**

* Les fonctionnalités spécifiques des routeurs peuvent varier en fonction du modèle et du fabricant.
* Ce rapport fournit une description générale des rôles et des fonctionnalités des routeurs dans un réseau. Des configurations et des fonctionnalités plus détaillées peuvent être nécessaires pour répondre aux besoins spécifiques d'un projet réseau particulier.

Les liaisons entre les routeurs sont des liaisons Ethernet Gigabit, offrant une bande passante élevée pour la transmission des données.

### Adressage IP

Chaque routeur et périphérique final se voit attribuer une adresse IP unique au sein du réseau. Le schéma d'adressage IP est le suivant :

* **VIOS-Core-1 :**
    * Interface e0 : 192.168.10.1/24 (réseau du noyau 1)
    * Interface el : 192.168.20.1/24 (réseau du noyau 2)
    * Interface e2 : 192.168.40.1/24 (réseau du noyau 3)
    * Interface mgmt : 10.0.0.1/24 (réseau de gestion)
* **VIOS-Core-2 :**
    * Interface e0 : 192.168.10.2/24 (réseau du noyau 1)
    * Interface el : 192.168.20.2/24 (réseau du noyau 2)
    * Interface e2 : 192.168.40.2/24 (réseau du noyau 3)
    * Interface mgmt : 10.0.0.2/24 (réseau de gestion)
* **OpenSwitch-Acc-1 :**
    * Interface e0 : 192.168.10.3/24 (réseau du noyau 1)
    * Interface e1 : 192.168.20.3/24 (réseau du noyau 2)
    * Interface e2 : 192.168.40.3/24 (réseau du noyau 3)
    * Interface mgmt : 10.0.0.3/24 (réseau de gestion)
* **PC_Linux-1 :** 192.168.10.10/24 (réseau du noyau 1)
* **PC_Linux-2 :** 192.168.20.10/24 (réseau du noyau 2)
* **PC_Linux-3 :** 192.168.40.10/24 (réseau du noyau 3)
* **PC_Linux-4 :** 192.168.40.20/24 (réseau du noyau 3)

Le masque de sous-réseau (/24) indique que chaque réseau peut accueillir jusqu'à 254 hôtes. Le réseau de gestion
