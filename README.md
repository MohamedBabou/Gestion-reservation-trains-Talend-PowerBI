# Gestion-reservation-trains-Talend-PowerBI
C'est un projet sur la gestion de réservations des trains constitue de 2 étapes : La première est la construction de base de données puis l'insertion de données en utilisant Talend. La deuxième est de faire de KPI avec Power BI
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

### Exemples de fichiers CSV

Si vous souhaitez utiliser des exemples de fichiers CSV pour réaliser l'importation, vous pouvez trouver des fichiers de démonstration dans le répertoire "examples/csv" de ce projet. Ces fichiers sont utilisés pour tester l'importation et peuvent servir de modèle pour vos propres données CSV.
