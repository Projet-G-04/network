# Configuration du Switch vIOS-Ser-I

Le choix du switch VIOS dans cette partie s'explique par ses capacités avancées de commutation Ethernet et sa parfaite intégration aux topologies de réseau virtuel de GNS3. Il offre un large éventail de fonctionnalités typiques des commutateurs Ethernet, telles que la gestion des VLAN, le STP (Spanning Tree Protocol), le trunking, etc. De plus, il peut être connecté à d'autres dispositifs réseau virtuels tels que des routeurs et des pare-feu pour simuler des réseaux complets. Cependant, bien qu'il soit capable de reproduire de nombreux aspects d'un commutateur Cisco réel, le switch VIOS dans GNS3 présente des limitations en termes de performances et de fonctionnalités avancées par rapport au matériel physique.

## AAA (Authentification, Autorisation et Comptabilité) : 
un cadre essentiel en matière de sécurité réseau. Examinons chaque composant :


- Authentification :

1. L’authentification garantit que les utilisateurs ou les appareils sont bien ceux qu’ils prétendent être avant d’accorder l’accès aux ressources réseau.
2. Les méthodes courantes d’authentification incluent :

-Nom d’utilisateur et mot de passe : L’utilisateur fournit un nom d’utilisateur et un mot de passe pour prouver son identité.
-Authentification basée sur des certificats : Les utilisateurs présentent des certificats numériques pour s’authentifier.
-Authentification biométrique : Utilisation des empreintes digitales, de la reconnaissance faciale ou d’autres données biométriques.

3. Une fois authentifiés, les utilisateurs obtiennent l’accès au réseau.

- Autorisation :

1.L’autorisation contrôle les actions ou les ressources auxquelles un utilisateur peut accéder après une authentification réussie.
2.Elle répond à la question : “Que peut faire cet utilisateur authentifié ?”
3.Les politiques d’autorisation définissent les permissions en fonction des rôles, des groupes ou d’attributs spécifiques.
Exemples :
Un utilisateur avec le rôle “administrateur” peut configurer les équipements réseau.
Un utilisateur invité peut uniquement accéder à Internet mais pas aux serveurs internes.

- Comptabilité :

1. La comptabilité enregistre l’activité des utilisateurs à des fins d’audit et de facturation.
2. Elle enregistre des détails tels que : quand un utilisateur se connecte ou se déconnecte, quelles ressources il a consultées et la quantité de données transférées.
3.Utile pour la conformité, le dépannage et la facturation.

## Le Spanning Tree Protocol (STP) :
un protocole utilisé par les commutateurs Ethernet pour éviter les boucles de commutation dans un réseau. Voici quelques points clés sur le fonctionnement du STP pour les commutateurs :

• Élection du commutateur racine : Le STP permet à tous les commutateurs d'un réseau de choisir un commutateur racine. Ce commutateur est au sommet de la hiérarchie et tous les chemins dans le réseau sont calculés par rapport à lui.

• Calcul des chemins sans boucle : Le STP désactive certains liens entre les commutateurs pour créer un arbre recouvrant qui garantit qu'il n'y a pas de boucles dans le réseau. Seuls les liens nécessaires pour connecter tous les commutateurs au commutateur racine sont activés.

• Utilisation des états de port: Les ports des commutateurs passent par différents états (bloqué, écoute, apprenant, et actif) en fonction de l'algorithme STP. Cela permet de s'assurer qu'aucun paquet n'est transmis sur un port tant que le réseau n'a pas convergé vers une topologie stable.

• Redondance et résilience : Le STP permet d'introduire de la redondance dans un réseau en activant des chemins de secours qui ne sont utilisés que si un lien principal échoue. Cela améliore la résilience du réseau.

• Versions du STP : Il existe plusieurs versions du STP, y compris le STP classique (802.1D), le Rapid Spanning Tree Protocol (RSTP - 802.1w) qui offre une convergence plus rapide, et le Multiple Spanning Tree Protocol (MSTP - 802.1s) qui permet de regrouper plusieurs VLANs dans un seul arbre recouvrant.

## Open Shortest Path First (OSPF) :
• Objectif et Fonctionnement :

1.OSPF est un protocole de routage à état de lien largement utilisé dans les réseaux IP.
2.Il appartient à la catégorie des protocoles de passerelle intérieure (IGP) et fait partie de la suite de protocoles Internet.
3.Son rôle est d’échanger des informations de routage au sein d’un système autonome (AS).

• Technologie à État de Lien :

1.Contrairement aux protocoles de vecteur de distance traditionnels tels que RIP, OSPF utilise la technologie à état de lien.
2.Il collecte des informations d’état de lien auprès des routeurs adjacents pour construire une carte topologique du réseau.
3.Cette carte permet à OSPF de calculer le chemin le plus court pour atteindre les destinations.

•Avantages et Subtilités :

1.OSPF propose des fonctionnalités telles que l’authentification des mises à jour de routage, le masque de sous-réseau de longueur variable (VLSM) et le résumé de route.
2.Il surmonte les limitations de RIP, comme la limite de 15 sauts.
3.OSPF convient particulièrement aux réseaux grands et complexes.
