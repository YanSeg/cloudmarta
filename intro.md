Infra as a service : IASS
=========================

- Loueur un serveur virtuel
- Louer un espace de stockage 
- Louer de la capacité réseau


' If you’re a startup or a business giant and require a “pay-as-you-go” cloud computing model, IaaS is the right choice. '

Plateform as a service : PASS (permet d obtenir des services plus évolués qu'un simple serveur virtuel)
==============================

- Des services plus évolués 
    - Deployer une base de donées (sans avoir en IASS à louer un serveur et installer la bdd)
    - Communication inter aplllications
    - Chiffrement
    - ML
    - 175 services dans AWS
- Permet de construire une apllication très rapiedement    
- Ces services s'adaptent en fonction de la demande 


Software as a service : SAAS
============================
En utilisant IAAS et PASS de dfaçon très combiné on eput construire des applications très abouties. On parle alors de Software as a service : SAAS

- Des logiciels que l'on utilise en tant que service 
    - Rien à installer 
    - Pas de gestion des mises à jour 
    - ex : Gmail, Netflix, airbnb, achat en ligne

    Campus skills : SAAS
    Scaleway : IASS
    Discord : SAAS
    Google Drive : SASS
    AWS EC2 (Elastic Compute Cloud) : IAAS
    Google Translate API (https://cloud.google.com/translate) : PASS








Architecture d'un réseau cloud :

    L'architecture d'un réseau cloud implique la conception de la structure et de la disposition des ressources informatiques dans le cloud. Cela inclut la mise en réseau, le stockage, la sécurité, la redondance, et d'autres éléments essentiels.



Principes de la réversibilité :

    La réversibilité concerne la capacité à migrer facilement d'une plateforme cloud à une autre ou à revenir à un environnement sur site. Il est important de concevoir des systèmes qui permettent une migration sans heurts.


Contrats de niveaux de service (SLA) :

    Les SLA définissent les garanties de performance, de disponibilité, et d'autres aspects du service cloud. Il est important de comprendre ces contrats pour s'assurer que les besoins de l'entreprise sont satisfaits.

Configuration des serveurs à déployer :

    Cela implique la spécification des ressources nécessaires pour exécuter les applications, y compris les capacités de calcul, de stockage, et de réseau.    


Architecture système à déployer :

    La conception de l'architecture système implique la planification et la disposition des composants logiciels et matériels pour répondre aux besoins du système, en tenant compte de la scalabilité, de la sécurité, et de la performance.





 Avantage du cloud =>
 - Tolérance aux problèmes (Grosse capacité de stocka   ge et de réplication replication, sécurité)
 - Scalabilité  (pay-as-you-go)
 - Globalistaion (ressources près de leur marché: performation/réglementation)
 - Agilité (s'adapate aux cnagement, aux besoins => RAPIDIDTÉ)
 - coût


______________________________________________________________
 NB : CLOUD PRIVE
 Créer un cloud privé nécessite quelques étapes fondamentales. Voici une explication simple du processus :

    Infrastructure Matérielle :
        Obtenez le matériel nécessaire, comme des serveurs et du stockage, qui sera utilisé pour créer votre cloud privé. Cela peut être sur site dans votre propre centre de données ou chez un fournisseur d'hébergement.

    Virtualisation :
        Utilisez des logiciels de virtualisation tels que VMware, Hyper-V ou KVM pour créer des machines virtuelles à partir de votre matériel physique. Cela permet de maximiser l'utilisation des ressources matérielles.

    Gestion des Ressources :
        Installez un logiciel de gestion de ressources, comme OpenStack, pour orchestrer et gérer les ressources virtuelles. Cela inclut la création, la suppression et la surveillance des machines virtuelles.

    Réseau :
        Configurez un réseau interne pour connecter toutes les machines virtuelles. Assurez-vous de mettre en place une sécurité appropriée pour protéger votre cloud privé.

    Stockage :
        Mettez en place un système de stockage pour héberger les données de vos machines virtuelles. Des solutions telles que Ceph ou GlusterFS peuvent être utilisées pour le stockage distribué.

    Sécurité :
        Mettez en place des mesures de sécurité robustes, y compris des pare-feu, des mécanismes d'authentification et des politiques de contrôle d'accès pour protéger votre cloud privé.

    Accès à Distance :
        Configurez un moyen d'accéder à distance à votre cloud privé, généralement via une interface web ou des outils de ligne de commande.

    Sauvegardes :
        Établissez des procédures de sauvegarde régulières pour garantir la sécurité de vos données en cas de problème.

    Maintenance et Mises à Jour :
        Planifiez des périodes de maintenance régulières et assurez-vous de mettre à jour les logiciels et les systèmes d'exploitation pour garantir la sécurité et la stabilité.

    Documentation :

    Documentez soigneusement la configuration de votre cloud privé pour faciliter la gestion continue et pour aider en cas de besoin de dépannage.

Il est important de noter que la mise en place d'un cloud privé peut varier en fonction de la taille de l'entreprise, des besoins spécifiques et des ressources disponibles. Il peut être utile d'obtenir l'aide de professionnels de l'informatique pour s'assurer que la configuration est robuste et sécurisée.
_________________________________________________________________________________________




Pour un institut scientifique enregistrant et traitant des données expérimentales, une solution qui combine à la fois PaaS (Platform as a Service) et IaaS (Infrastructure as a Service) pourrait être appropriée. Voici quelques suggestions en fonction des besoins spécifiques décrits :

    Stockage des Données :
        IaaS : Utilisez une solution de stockage cloud, comme Amazon S3 ou Azure Blob Storage, pour stocker les données expérimentales. Choisissez un emplacement de stockage en fonction de la proximité géographique du site d'expérimentation (Grenoble) pour minimiser la latence.

    Traitement des Données :
        PaaS : Utilisez des services PaaS pour le traitement des données. Par exemple, vous pouvez déployer des environnements de traitement Python sur des plateformes telles que Google Cloud AI Platform, Azure Machine Learning, ou AWS SageMaker.

    Base de Données pour les Données Historiques :
        IaaS : Pour conserver toutes les données des deux dernières années, vous pourriez utiliser une base de données cloud, telle que AWS RDS, Azure SQL Database, ou Google Cloud SQL. Cela vous donne le contrôle sur la gestion de la base de données.

    Archivage des Données Anciennes :
        IaaS : Pour l'archivage des données anciennes, envisagez l'utilisation de services de stockage à faible coût et à long terme, comme Amazon Glacier, Azure Blob Storage - Cool Tier, ou Google Cloud Storage Nearline.

    Gestion de l'Évolutivité :
        PaaS/IaaS : Utilisez des solutions qui permettent une évolutivité facile, surtout pendant les périodes d'expérimentation intensive. Vous pouvez ajuster la capacité de stockage et de traitement en fonction des besoins avec des solutions cloud.

    Sécurité et Conformité :
        IaaS/PaaS : Assurez-vous de mettre en place des politiques de sécurité robustes. Certains services PaaS et IaaS offrent des fonctionnalités de sécurité avancées, comme le chiffrement des données au repos et en transit.

    Accès aux Données Historiques :
        IaaS : Pour garantir un accès rapide aux données historiques, conservez une copie dans un stockage à accès rapide et basculez vers des solutions d'archivage à la demande. Par exemple, vous pourriez utiliser un service IaaS de stockage à faible latence.

En combinant PaaS pour le traitement des données en temps réel et IaaS pour le stockage, l'archivage, et la gestion des bases de données, vous pouvez construire une infrastructure cloud qui répond efficacement aux besoins de l'institut scientifique. Cette approche offre la flexibilité et la scalabilité nécessaires pour gérer les exigences variées de stockage et de traitement des données.