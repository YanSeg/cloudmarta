# Proposition architecture d'un système.

Architecture Description Template :
===================================


General Description ofthe Service
What does this service do?

Software Architecture
What software blocks are there?

Servers or Services
Which servers (technical parameters) or services (APIs) do you need? How many of each?

SLA 
Wich 


Wich 
______________________________________________________________________

Vos besoins :
============= 
- Architecture à créer (on part de 0). 
- Vous enregistrez et recevrez de 10 à 40 Go par jour. Soit 25 Go par j en moyenne. 
- Ces données sont ensuite traiter avec Python par vos collaborateurs. 
- Les 60 derniers jours de données doivent être à la disposition des équipes.
- Les données anciennes (celà commencera dans deux mois) peuvent être stockée à faible coût (3j depusi la demenade).  À j+60 et ce jusqu' à n+2 (soit 2n -60j) soit une moyenne prévisionnelle de __ 9125 Go__  à stocker tout le temps. 


Architecture logicielle :
=========================
    - Module de réception des données :
    - 2 Système de stockage des données :
    - Système de traitement :
    - Contrôle d'accès et authentification :
    - Interface utilisateur :
    - ( Module d'archivage ou automatisation de l'archivage)

Serveurs et Services :
======================
    - Serveur de réception des données :
    - Service de traitement :
    - Service d'authentification :
    - Serveur d'archivage :
    - Service d'interface utilisateur :
    - Service de sauvegarde et de récupération :
    - ( Service de surveillance et de journalisation )

_________________________________________________________________


SLA Serveur OVH
===============  
SLA chez OVH page 5 https://storage.gra.cloud.ovh.net/v1/AUTH_325716a587c64897acbef9a4a4726e38/contracts/2fbf086-contrat_partDedie-FR-20.0.pdf

Temps de Disponibilité = 99.9 % = 1−Temps TotalTemps d’Arrêt​

Pour 99,9 % :

    Daily: 1m 26s
    Weekly: 10m 4.8s
    Monthly: 43m 28s
    Quarterly: 2h 10m 24s
    Yearly: 8h 41m 38s
_____________________________________________________________________________________________________

## Serveur de réception des données : (IaaS)


#### SLA, Objectif de Disponibilité : 99,9%

Gestion de l'infrastructure pour la réception et l'ingestion des données expérimentales.

Proche Grenoble pour diminuer la latence. 

## Serveurs de stockage des données : (IaaS)

#### SLA, Objectif de Disponibilité : 99,9%

    Fournit une infrastructure pour le stockage des données expérimentales.
    Implémente des mécanismes de redondance et de sauvegarde au niveau de l'infrastructure.

## Service de traitement : (PaaS)

SLA https://d1.awsstatic.com/legal/AmazonComputeServiceLevelAgreement/Amazon_Compute_Service_Level_Agreement_French_2022-05-25.pdf

Amazon EC2 car ` Les instances à la demande vous permettent de payer la capacité de calcul à l'heure, sans engagement à long terme`


#### SLA, Objectif de Disponibilité : 99,9%

    Infrastructure de calcul permettant l'exécution de scripts Python et la fourniture de ressources pour l'analyse des données.


## Deux Serveurs d'Archivage 1 (Stockage des données des deux dernières années - Disponible) :

#### SLA, Objectif de Disponibilité : 99,9%
    __Objectif__ : Stocker les données expérimentales des deux dernières années avec une disponibilité rapide.
    __Caractéristiques__ :
        Capacité de stockage élevée pour gérer les données des deux dernières années.
        Haute disponibilité pour un accès rapide.
        Performances optimisées pour la récupération rapide des données récentes.
    Politique de Rétention :
        Conserver les données des deux dernières années.
        Disponibilité immédiate pour la récupération.

## Serveur d'Archivage 2 (Stockage des données de plus de deux ans à moindre coût) :

#### SLA, Objectif de Disponibilité : 99%
    __Objectif__ : Stocker les données expérimentales de plus de deux ans à un coût réduit.
    __Caractéristiques__ :
        Capacité de stockage suffisante pour gérer les données archivées de plus de deux ans.
        Coûts d'exploitation réduits pour optimiser les dépenses.
        Performances acceptables, avec une priorité moindre sur la rapidité d'accès.
    Politique de Rétention :
        Archiver les données de plus de deux ans.
        Une disponibilité peut prendre jusqu'à 3 jours pour la récupération, en raison d'une priorité moindre sur la rapidité.






_________________________________________________________________________

PaaS (Platform as a Service) :
==============================

    Module de réception des données :
    =================================
        Abstraction de la gestion de l'infrastructure pour la réception et l'ingestion des données expérimentales.

    Système de stockage des données :
    =================================
        Abstraction de la gestion de l'infrastructure pour le stockage des données expérimentales avec des mécanismes de récupération.

    !!! Système de traitement : !!!
    ===============================

        Plateforme qui permet aux scientifiques d'écrire et d'exécuter des scripts Python sans se soucier de l'infrastructure sous-jacente.

    Contrôle d'accès et authentification :
    ======================================
        Service gérant l'authentification et l'autorisation des utilisateurs sans que ces derniers aient à gérer l'infrastructure.

    Interface utilisateur :
    =======================
        Plateforme fournissant une interface conviviale pour interagir avec le système, soumettre des travaux d'analyse de données et récupérer les résultats.

    Module d'archivage :
    ====================
        Service gérant le processus d'archivage des données plus anciennes que 60 jours avec un mécanisme de récupération.

    Service d'authentification :
    ============================
        Service gérant l'authentification et l'autorisation des utilisateurs sans gestion directe de l'infrastructure.

    Service d'interface utilisateur :
    =================================
        Plateforme fournissant une interface web sans nécessité pour les utilisateurs de gérer l'infrastructure sous-jacente.    


        Service de surveillance 
         Amazon CloudWatch Logs, Google Cloud Logging, ou Azure Monitor Logs 




______________________________________________________________________
Des Questions pour la fin :
 - Sécurité/Sensibilités de vos données?
 - Envisagez-vous un stockage des données disponibles en local? 
______________________________________________________________________


Questions Additionnelles :

    Sécurité/Sensibilités des Données :
        Comment la sécurité des données est-elle gérée pour chaque composant ?
        Y a-t-il des réglementations ou des normes spécifiques à respecter en matière de sécurité des données ?

    Stockage Local des Données :
        Envisagez-vous de stocker certaines données localement, et si oui, quelles sont les exigences de disponibilité pour ces données locales ?

    - En ce qui concerne le traitement des données :

        - Combien de licences utilisateurs pour le service de traitement ?

        - Quel puissance de calcul (rapidité) souhaité/nécessaire pour vos opérations ? 