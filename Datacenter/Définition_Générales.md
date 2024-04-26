# Définition:

Un centre de données, également appelé datacenter ou centre de données, est une installation physique qui regroupe un ensemble de ressources informatiques, telles que des serveurs, des dispositifs de stockage, des équipements réseau (commutateurs), et d'autres composants liés aux technologies de l'information (IT). Son rôle principal est de fournir un environnement centralisé pour la collecte, le traitement, le stockage, et la gestion de grandes quantités de données, ainsi que pour l'exécution d'applications informatiques et de services.
![Data Center](DC.png)

# Leur rôle:

Les data centers sont désormais des éléments essentiels dans les entreprises modernes et y jouent un rôle crucial:

    -Traitement et stockage des données:
        Ils hébergent des serveurs et des systèmes de stockage permettant aux entreprises de stocker et de traiter d'énormes quantités d'informations nécessaires à leurs opérations.

    -Redondance et Continuité de Service:
        Les data centers intègrent des dispositifs de redondance, tels que des systèmes d'alimentation de secours et des configurations réseau redondantes, afin d'assurer la continuité des opérations, même en cas de défaillance matérielle ou d'incidents.

    -Sécurité des données:
        Des mesures de sécurité physiques, telles que des contrôles d'accès, et des mécanismes de sécurité électroniques sont mis en place pour prévenir tout accès non autorisé.

    -Disponibilité:
        Les applications et les services informatiques essentiels à une entreprise, tels que les sites web, les bases de données, les applications métier, sont hébergés dans les data centers. Cela assure une disponibilité continue et des performances optimales.

# En quoi sont-ils importants ?

Dans le monde de l'informatique d'entreprise, les centres de données sont conçus pour prendre en charge les applications et les activités suivantes :

- Messagerie et partage de fichiers
- Applications de productivité
- Gestion de la relation client (CRM)
- Planification des ressources de l'entreprise (ERP) et bases de données
- Big data, intelligence artificielle et apprentissage automatique
- Postes de travail virtuels, services de communication et de collaboration

# Comment ça marche?

- Les données sont envoyées vers le data center via une connexion réseau sécurisée.
- Les serveurs traitent et stockent les données en fonction des instructions reçues.
- Les utilisateurs finaux accèdent aux données et aux services informatiques hébergés dans le data center via internet ou un réseau privé.

# Pourquoi le sécuriser ?

-Protection des données sensibles:
    - Fuite de données personnelles:
        - Risque de fraude, d'usurpation d'identité et de vol de données.
    - Perte financière:
        - Perte de données sensibles, interruption de l'activité et sanctions réglementaires.
    - Espionnage industriel:
        - Avantage concurrentiel pour les concurrents.

-Continuité des services:
    - Interruption de service:
        - Perte de productivité, perte de revenus et dommages à l'image de marque.

-Respect des réglementations:
    Sanctions financières en cas de non-conformité (ex: RGPD).

-Menaces croissantes:
     Cibles privilégiées pour les pirates informatiques.


# Types of data center

On considère 3 grands types de data centers. Un même organisme peut on utiliser plusieurs en fonction des ses besoins:

    -Data center d’entreprise (en premise):

        Ce modèle implique l'hébergement de l'infrastructure informatique et des données sur site, au sein de l'entreprise. De nombreuses organisations optent pour cette solution car elle leur offre un contrôle accru sur la sécurité de leurs informations et facilite la conformité à des réglementations telles que le RGPD. Cependant, l'entreprise assume l'entière responsabilité du déploiement, de la surveillance et de la gestion de son centre de données.

    -Data center de services managés:

        Dans un centre de données géré, l'entreprise cliente loue des serveurs, du stockage et du matériel réseau dédiés auprès d'un fournisseur. Ce dernier se charge de l'administration, de la surveillance et de la gestion de l'infrastructure pour le compte de l'entreprise. L'entreprise cliente a un accès exclusif au matériel, ce qui garantit un niveau élevé de confidentialité et de sécurité.

    -Data center en mode cloud:

        Les centres de données de cloud computing, également appelés data centers mutualisés, hébergent des ressources informatiques mises à la disposition de multiples clients. Le nombre de clients peut varier de quelques dizaines à plusieurs millions, selon la taille et la popularité du fournisseur de cloud.
        Les fournisseurs de services cloud les plus connus, tels qu'Amazon Web Services (AWS), Google Cloud Platform, IBM Cloud, Microsoft Azure et Oracle Cloud Infrastructure, gèrent les centres de données de cloud computing les plus importants. La plupart de ces fournisseurs disposent de plusieurs centres de données répartis à travers le monde, afin d'assurer une couverture géographique optimale et une meilleure résilience.


# Standard architecture
-Couche Physique
    -Alimentation électrique:
        L'alimentation électrique fournit l'énergie nécessaire au fonctionnement du data center.
    -Refroidissement:
        Le refroidissement évacue la chaleur générée par les serveurs.
    -Racks et serveurs:
        Les racks stockent les serveurs qui exécutent les applications et stockent les données.
    -Réseau:
        Le réseau permet la communication entre les serveurs et les utilisateurs externes.

-Architecture Spine-Leaf
![Spine-Leaf](Spine-leaf.png)
Les datacenters modernes utilisent l’architecture Spine-leaf. Cette dernière comprend deux types de commutateurs : les commutateurs "spine" et les commutateurs "leaf".

-Les commutateurs "spine" sont connectés entre eux et aux commutateurs "leaf".
-Les commutateurs "leaf" sont connectés aux serveurs.

Cette architecture s’est propagée avec la popularité du cloud et des conteneurs ce qui a causé l’augmentation du trafic est-ouest (entre serveurs) dans les data centers modernes. Spine-leaf est idéale pour ce trafic car :
    - Latence réduite et prévisible: Le chemin entre les serveurs est toujours le même, garantissant une performance optimale pour les applications sensibles au temps.
    - Capacité améliorée: ECMP remplace STP, permettant l'utilisation de tous les chemins disponibles et évitant la saturation des liens.
    - Meilleure évolutivité: Ajout simple de nouveaux commutateurs "spine" ou "leaf" sans reconfiguration du réseau.




