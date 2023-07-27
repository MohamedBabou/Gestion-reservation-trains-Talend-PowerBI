# Gestion-reservation-trains-Talend-PowerBI
C'est un projet sur la gestion de réservations des trains constitue de 2 étapes : La première est la construction de base de données puis l'insertion de données en utilisant Talend. La deuxième est de faire de KPI avec Power BI
 # La Premiere partie de Gestion-reservation-trains-Talend-PowerBI
 ## Base de données
La base de données "train_donnees" est déjà incluse dans ce projet. Vous n'avez pas besoin de l'importer séparément, car elle est prête à être utilisée.
### Modèles conceptuel, logique et physique

Vous pouvez visualiser les modèles de la base de données à l'aide des fichier partagees. 
### Configuration de la base de données
Assurez-vous que vos paramètres de connexion MySQL (hôte, nom d'utilisateur, mot de passe, etc.) sont correctement configurés pour que votre projet puisse se connecter à la base de données "train_donnees".
N'hésitez pas à utiliser ces exemples comme point de départ pour interagir avec la base de données de ce projet.
## Importation des fichiers CSV dans Talend
Dans ce projet, nous utilisons Talend pour importer les données à partir de fichiers CSV dans la base de données "train_donnees". Suivez les étapes ci-dessous pour réaliser cette importation :

1. **Configuration de l'environnement :** Assurez-vous d'avoir installé Talend sur votre machine. Vous pouvez télécharger la version appropriée depuis le site officiel de Talend (https://www.talend.com/download/).
2. **Ouvrir le projet Talend :** Une fois Talend installé, ouvrez le logiciel et sélectionnez le projet associé à cette application de gestion.
3. **Créer une nouvelle tâche d'importation :** Dans le projet Talend, créez une nouvelle tâche (job) pour l'importation des données.
4. **Ajouter les composants nécessaires :** Dans le job d'importation, ajoutez les composants Talend requis pour la lecture des fichiers CSV et l'insertion des données dans la base de données. Les composants couramment utilisés sont "tFileInputDelimited" pour lire les fichiers CSV et "tMysqlOutput" pour insérer les données dans MySQL.
5. **Configurer les composants :** Configurez les composants "tFileInputDelimited" pour spécifier l'emplacement des fichiers CSV et les délimiteurs utilisés dans ces fichiers. Configurez également le composant "tMysqlOutput" pour établir la connexion à la base de données "train_donnees" et choisir la table de destination pour l'insertion des données.
6. **Exécuter le job :** Une fois la configuration terminée, exécutez le job pour importer les données à partir des fichiers CSV dans la base de données.
7. **Vérifier les résultats :** Vérifiez que l'importation s'est déroulée avec succès en consultant la base de données "train_donnees" pour vous assurer que les données ont été insérées correctement.
## Fichiers Talend
Dans ce projet, nous utilisons Talend pour gérer l'importation des données à partir de fichiers CSV dans la base de données "train_donnees". Voici une description des fichiers Talend utilisés dans le projet :

**InsertionNomTable.job :** Ce fichier Talend contient le job (tâche) pour l'importation des données. Il utilise le composant "tFileInputDelimited" pour lire les fichiers CSV et le composant "tMysqlOutput" pour insérer les données dans la base de données MySQL. Ce job est prêt à être exécuté une fois que vous avez configuré la connexion à la base de données.

**database_connection.properties :** Ce fichier Talend contient les informations de connexion à la base de données. Assurez-vous de configurer correctement ce fichier avec les paramètres de connexion appropriés avant d'exécuter le job d'importation. Vous pouvez modifier ce fichier en fonction de vos propres paramètres de connexion à MySQL.

## Connexion et déconnexion à la base de données
Dans le job Talend  **InsertionNomTable.job**, nous utilisons les composants InputDatabase.connect et InputDatabase.disconnect pour gérer la connexion à la base de données "train_donnees". Voici comment vous pouvez utiliser ces composants :

**InputDatabase.connect :** Ce composant est utilisé pour établir la connexion à la base de données avant d'effectuer l'importation des données. Assurez-vous que la configuration de connexion dans database_connection.properties est correcte avant d'utiliser ce composant.

**InputDatabase.disconnect :** Ce composant est utilisé pour fermer la connexion à la base de données une fois que l'importation des données est terminée. Il est important de libérer les ressources de connexion lorsque vous n'en avez plus besoin.

## Exécution du job d'importation
Pour importer les données depuis les fichiers CSV dans la base de données "train_donnees" :
Ouvrez Talend et sélectionnez le projet associé à cette application de gestion.
Localisez le fichier **InsertionNomTable.job** dans l'arborescence du projet.
Cliquez avec le bouton droit sur le fichier et choisissez "Run" (Exécuter) pour lancer le job d'importation.
Vérifiez la console Talend pour suivre le processus d'importation et vous assurer qu'il s'est déroulé avec succès.
Assurez-vous de configurer le fichier **database_connection.properties** avec les informations de connexion appropriées à la base de données "train_donnees" avant d'exécuter le job d'importation.
## Exemples de fichiers CSV
Vous pouvez utiliser des exemples de fichiers CSV pour tester l'importation. Des fichiers de démonstration sont disponibles dans le répertoire "examples/csv" de ce projet.
## Utilisation des types de SQL avec Talend
Dans ce projet, nous utilisons Talend pour gérer l'importation des données à partir de fichiers CSV dans la base de données "train_donnees". Lorsque vous configurez le job Talend pour l'insertion des données, il est essentiel de tenir compte des types de données utilisés dans la base de données, afin de garantir une correspondance appropriée entre les données du fichier CSV et les colonnes de la base de données.
Talend prend en charge un large éventail de types de données SQL, ce qui vous permet de choisir le type de données approprié pour chaque colonne lors de l'insertion des données. Voici comment vous pouvez utiliser les types de SQL avec Talend :
## Type de données de la base de données : 
Lors de la conception du modèle physique de la base de données, assurez-vous que les types de données de chaque colonne sont correctement définis en fonction des données que vous souhaitez stocker. Talend utilise ces types de données pour déterminer comment mapper les valeurs du fichier CSV aux colonnes de la base de données lors de l'insertion.
## Configuration du Serveur de Base de Données :
Dans ce projet, nous utilisons un serveur de base de données MySQL pour stocker les données de l'application. Plus spécifiquement, nous utilisons MySQL 5 fourni par WampServer.
## Installation de WampServer
Si vous n'avez pas encore installé WampServer, vous pouvez le télécharger à partir du site officiel de WampServer (https://www.wampserver.com/). Suivez les instructions d'installation pour configurer le serveur de base de données sur votre machine.
## Accès à MySQL
Pour accéder à la base de données MySQL via WampServer :
Assurez-vous que WampServer est en cours d'exécution et que le serveur MySQL est actif.
Utilisez le nom d'utilisateur et le mot de passe appropriés pour vous connecter à MySQL. Par défaut, le nom d'utilisateur est généralement "root" et il n'y a pas de mot de passe.
Si vous avez configuré un mot de passe pour l'utilisateur root, assurez-vous de l'utiliser lors de la connexion.
## Configuration de la Base de Données
Dans le fichier Talend **database_connection.properties**, vous devez spécifier les informations de connexion correctes pour accéder à la base de données MySQL. Assurez-vous que les paramètres de connexion correspondent à ceux de WampServer pour établir la connexion avec succès.
## Versions Prises en Charge
Ce projet a été développé et testé avec MySQL 5 fourni par WampServer. Bien que cela devrait fonctionner avec d'autres versions de MySQL, nous recommandons d'utiliser la version mentionnée pour une compatibilité optimale.

N'hésitez pas à personnaliser ces instructions en fonction de votre configuration spécifique et des versions que vous utilisez. Assurez-vous de fournir toutes les informations nécessaires aux utilisateurs pour configurer correctement leur serveur de base de données et établir la connexion avec succès pour utiliser l'application de gestion.
# Visualisation des Données avec Power BI
Dans ce projet, nous utilisons Power BI pour créer des visualisations à partir des données stockées dans la base de données "train_donnees". Pour faciliter la visualisation, nous fournissons les fichiers suivants :

 ## MyDB.xlsx :
 Ce fichier Excel contient les données que nous utilisons pour créer les visualisations dans Power BI. Il s'agit des données extraites de la base de données "train_donnees" et préparées spécifiquement pour cette étape de visualisation.

## fichier.pbix :
Ce fichier Power BI Desktop contient le rapport de visualisation que nous avons créé. Il est pré-configuré pour se connecter au fichier Excel mentionné ci-dessus et générer les visualisations correspondantes.

## fichier.pdf : 
Ce fichier PDF est une version statique du rapport Power BI. Vous pouvez l'utiliser pour visualiser les résultats sans avoir besoin d'installer Power BI Desktop.

## Visualisation des Données
Pour visualiser les données à l'aide du fichier Power BI :
Assurez-vous d'avoir installé Power BI Desktop sur votre machine. Si vous ne l'avez pas déjà, vous pouvez le télécharger à partir du site officiel de Power BI (https://powerbi.microsoft.com/desktop/).
Ouvrez Power BI Desktop et sélectionnez "Open" (Ouvrir) dans le menu pour ouvrir le fichier fichier.pbix.
Une fois le rapport ouvert, Power BI se connectera automatiquement au fichier Excel fichier.xlsx pour générer les visualisations. Si le fichier Excel est déplacé, assurez-vous de spécifier le nouveau chemin d'accès des données dans Power BI.
Explorez les différentes visualisations présentes dans le rapport pour obtenir des informations sur les données de "train_donnees". Vous pouvez interagir avec les graphiques, tableaux de bord et autres éléments pour obtenir des informations spécifiques.
  
Merci d'avoir utilisé ce projet de gestion ! Nous espérons que cela vous sera utile et que vous apprécierez l'utiliser dans vos projets. Si vous avez des questions ou des suggestions, n'hésitez pas à nous contacter.
