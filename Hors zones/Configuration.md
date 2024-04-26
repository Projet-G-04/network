# Configuration du Routeur-vIOS-EDGE
Choisir le routeur vIOS offre une solution pratique pour les besoins de simulation et de test réseau.
En déployant le vIOS, les administrateurs peuvent rapidement créer et tester des topologies réseau complexes dans des environnements virtualisés, ce qui permet de réduire les coûts et les efforts liés à la mise en place de configurations matérielles physiques.

## Protocole NAT (Network Address Translation)
est un protocole qui permet de traduire les adresses IP et les ports d'un réseau privé en adresses IP publiques ou en d'autres adresses privées, et vice versa, lorsqu'ils accèdent à Internet ou à d'autres réseaux. 

- Fonctionnement : Le routeur NAT remplace les adresses IP privées des périphériques par une adresse IP publique pour accéder à Internet, en utilisant une table de traduction pour rediriger les paquets.

- Avantages : Économie d'adresses IP publiques, sécurité renforcée en masquant les adresses IP internes, compatibilité IPv4/IPv6, contrôle du trafic réseau.

## Protocole eBGP (exterior Border Gateway Protocol)
est un protocole de routage utilisé entre différents systèmes autonomes (AS) sur Internet.

- Fonctionnement : Le eBGP échange des routes entre des routeurs de systèmes autonomes différents en annonçant des préfixes IP et en mettant à jour les tables de routage en conséquence.

- Avantages : Connectivité inter-domaine pour Internet, flexibilité des politiques de routage, redondance et tolérance aux pannes.

- Sécurité : Le eBGP propose des fonctionnalités telles que l'authentification des voisins BGP et le filtrage des annonces de routage pour prévenir les attaques telles que le détournement de trafic ou les attaques DDoS, renforçant ainsi la sécurité du réseau.

## Protocole NTP (Network Time Protocol)
est un protocole utilisé pour synchroniser les horloges des périphériques sur un réseau.

- Fonctionnement : Le NTP synchronise les horloges des périphériques en utilisant des serveurs de temps de référence.

- Avantages :
1.Précision de la synchronisation : Assure une synchronisation précise des horloges.
2.Cohérence des événements : Maintient la cohérence des horaires dans les journaux et les transactions.
3.Sécurité renforcée : Contribue à renforcer la sécurité du réseau en assurant une meilleure traçabilité des événements.

## DNS (Domain Name Serice ):
- Fonctionnement :
Le DNS convertit les noms de domaine en adresses IP pour permettre la navigation sur Internet.

- Avantages :
-Simplifie l'accès aux ressources en utilisant des noms de domaine.
-Permet la scalabilité et améliore la disponibilité des services.

# Configuration des Routeurs ISP
Choisir un routeur ISP garantit une connectivité rapide et fiable, avec un support professionnel et des fonctionnalités avancées pour une évolutivité et une sécurité optimales.

Pour sa configuration, les mêmes protocoles cités précédemment ont été utilisés.

# Configuration du Firewall Cisco ASAv
ASA-v est la version virtuelle du pare-feu et dispositif de sécurité réseau ASA de Cisco. Il offre les mêmes fonctionnalités de sécurité avancées que les appareils physiques, mais dans un environnement virtuel, ce qui permet une protection efficace des réseaux et des applications dans des environnements virtualisés.

## Protocole FTP (File Transport Protocol)
Protocole de transfert de fichiers utilisé pour échanger des fichiers entre un client et un serveur. 
- Fonctionnement: en deux modes principaux; actif et passif.
- Avantages : Permet le transfert de fichiers de manière efficace et sécurisée sur les réseaux. 
- Sécurité : Peut être sécurisé en utilisant des protocoles comme FTPS (FTP sécurisé) ou SFTP (SSH File Transfer Protocol) pour chiffrer les données.

## Protocole OSPF:
Protocole de routage interne utilisé pour échanger des informations de routage entre les routeurs au sein d'un même système autonome.
- Fonctionnement: en échangeant des messages de routage et en calculant les chemins les plus courts vers les réseaux. 
- Avantages : Offre une convergence rapide du routage et une utilisation efficace de la bande passante. 
- Sécurité : Peut être sécurisé en utilisant des mécanismes d'authentification comme les clés MD5 pour empêcher les attaques d'altération de routage.

## SSH (Secure Shell ): 
Protocole de connexion sécurisée utilisé pour accéder à distance à des équipements réseau. Permet d'établir une connexion chiffrée entre un client et un serveur. 
- Avantages : Protège les communications sensibles contre l'interception et la manipulation. Sécurité : Utilise des techniques de chiffrement pour garantir la confidentialité et l'intégrité des données échangées.

## ACL (Access List): 
Listes de contrôle d'accès utilisées pour filtrer le trafic réseau en fonction de critères tels que l'adresse source, l'adresse de destination et le type de protocole. 
- Avantages : Permet de contrôler précisément le flux de trafic en autorisant ou en refusant spécifiquement certains types de trafic
- Sécurité : Un outil essentiel pour limiter l'accès non autorisé aux ressources réseau en définissant des politiques de sécurité personnalisées.

## Protocole NTP
Comme vu precédemment.

