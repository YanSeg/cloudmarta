

Architecture logicielle :
=========================
    - Module de réception des données : (Trafic interne et public entrant compris dans l'offre ainsi que le trafic interne sortant)
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




| Serveur /Service          |        Détails de l'offre                                  | Tarifs                                                                  
|---                        |:-:                                                         |:-:
| Objetc storage OVH        | https://www.ovhcloud.com/fr/public-cloud/object-storage/   |   0,0013 € HT/mois/Go (avec 0,01 € HT/Go si besoin d'un trafic public sortant) (HT/mois/Go)
|                           |                                                            |   HT/mois/Go (avec 0,01 € HT/Go si besoin d'un trafic public sortant) (HT/mois/Go)
| Cold Archive OVH          | https://www.ovhcloud.com/fr/public-cloud/prices/#11500     |   0,0024 € (HT/mois/Go)
|  Compute Optimized        | https://www.ovhcloud.com/fr/public-cloud/prices/#13575     | De 0,6637 € à 1,48 € de l'heure. Grande variance, en fonction des besoins de rapidité (semaine/week-end)
|





SLA and Migration Possibilities
What is the SLA? Can we migrate the service to another provider or in-premise?

     Messages Envoyé :
    =================

      1.  " Cher Forunisseur,

          Afin de granatir la pérénité de notre angagement nous souhaiterions être informé par courrier des possbilités de migrations de nos données vers d'autres services en cas d'une éventuelles défaillance future de vos services (NB : https://www.channelnews.fr/google-sassocie-a-ovh-pour-combattre-aws-et-microsoft-99891) et/ou d'une solution hybride. 
          En effet il est possible qu'étant un organisme de recherche public ous envisagions d'éffectuer un backup au sein de notre propre serveur.

          Sincères salutations,
          xxxxxxxxxxx                           "



      2.   " Cher Fournisseur,

         A des fins de pérénités de nos données nous souhaitons nous assurers que nos données seront stockées dans différents lieux. 

         Sincères salutations,
         xxxxxxxxxxx "









           



|  Serveur / Service                                                                                                                                      | Détails de l'offre                                         | Tarifs                                                                                                                                                                                                                                                                                                  | Localisation                   |   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|---|
| Système de stockage des données ===============================                                                                                         |                                                            |                                                                                                                                                                                                                                                                                                         |                                |   |
| 1er choix  Object Storage Standard object storage - S3 API                                                                                              | https://www.ovhcloud.com/fr/public-cloud/object-storage/   | - 0,007 € HT/mois/Go - Inclus : Trafic interne et public entrant - Inclus : Trafic interne sortant                                                                                                                                                                                                     | France (Gravelines et Roubaix) |   |
| 2ème choix  Object Storage High Performance Object Storage - S3 API  (facturé en fonction de l'espace de stockage utilisé avec une granularité de 1 Go) |                                                            | - 0,018 € HT/mois/Go - Inclus : Trafic interne et public entrant - Inclus : Trafic interne sortant                                                                                                                                                                                                      | France (Gravelines)            |   |
| Serveur d'archivage, stockage des données à 2ans ================================================                                                       |                                                            |                                                                                                                                                                                                                                                                                                         |                                |   |
| 1er choix  Cold Archive                                                                                                                                 | https://www.ovhcloud.com/fr/public-cloud/prices/#11500     | - 0,0013 € (HT/mois/Go) - Avec 0,005 € pour la restauration des données                                                                                                                                                                                                                                 | France (Gravelines)            |   |
| 2ème choix    Cloud Archive                                                                                                                             | https://www.ovhcloud.com/fr/public-cloud/cloud-archive/    | - 0,0024 € (HT/mois/Go) - Avec 0,01                                                                                                                                                                                                                                                                     |                                |   |
| Volume Backup                                                                                                                                           | https://www.ovhcloud.com/fr/public-cloud/volume-backup/    | Stockage réplica x3- 0,011 € (HT/mois/Go)                                                                                                                                                                                                                                                               | France (Gravelines et Roubaix) |   |
| Système de traitement =====================                                                                                                             |                                                            |                                                                                                                                                                                                                                                                                                         |                                |   |
| 1er choix  Compute Optimized                                                                                                                            | https://www.ovhcloud.com/fr/public-cloud/prices/#13575     | De 0,0415 € à 1,3274 €de l'heure. Grande variance, en fonction des besoins de rapidité (semaine/week-end). Ces instances sont idéales pour les applications nécessitant des fréquences de calcul importantes ou de la parallélisation de tâches. Les vCores sont cadencés à 2,3 GHz et plus.            |                                |   |
| 2ème choix Memory Optimized                                                                                                                             | https://www.ovhcloud.com/fr/public-cloud/memory-optimized/ | De 0,0602 € à 1,9254 € de l'heure. Grande variance, en fonction des besoins de rapidité (semaine/week-end). Ces instances sont pensées pour les usages d'analyse des données et la datascience grâce à leurs ratios CPU/RAM optimisés et des IOPS accélérées. Les vCores sont cadencés à 2 GHz et plus. |                                |   |


Calcul des coûts annuel HT
==========================


1. Système de traitement 

Dans votre cas vous aurez besoin pour votre applicatif python du service Compute Optimized c3-64. Mémoire: 64Go,vCore: 32, Stockage: 400 Go NVMe, Réseau public: 8 Gbit/s, Réseau privé: 8 Gbit/s max.
Prix HT/heure: 1,3274 €
Vous recevez de 5 à 20 Go de données à traiter 2 fois par jours (soit une moyenne de 25 Go, à raison de 5 fois par semaine, sur 260j par an).
Sachant que le temps de calcul est d'environ 6h : 6 * 260 * 1,3274  € = 2070,744 € /ans


2. Stockage des données sur 60j

    - Environ 25Go/j _ 125 Go/semaines _ 1 To/2mois _ 6 To/ans.
    
    
    - Object Storage Standard object storage - S3 API:  6000 * 0,007 = 42 euros / mois  

    - Object Storage High Performance Object Storage - S3 API:  6000 * 0,018 = 108 euros /mois 

3. Stockage des données sur le long terme : 

    - 12 To strockées à l'année

    - Cold Archive: 12000 * 0,0013 = 15,6 euros / mois 

    - Cloud Archive: 12000 * 0,0024 = 28,8 euros / mois 

    - Volume Backup: 1200 * 0,011 = 132 euros / mois




Conclusions :
============

La solution Cloud Archive est plus sécurisé que la Cold Archive. Nous choisirons dans votre cas celle-ci en priorité. Néanmoins vu le degré d'importance de vos données la solution du Volume Backup qui concerve un triplicata de vos données est à privilégier.
Le côut est de 1584 euros HT. 345,6 HT à l'année pour le Cloud Archive.

Le système de traitement de vos données sera de 2070,744 € /ans

Le stockage de vos données à 2 mois coutera 504 euros à l'année.

L'estimation du coût total est de 4158,7 euros selon nos précaunisation. 
========================================================================