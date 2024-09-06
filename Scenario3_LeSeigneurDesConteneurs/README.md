# Le Seigneur des conteneurs

*Marie et Mario travaillent ensemble sur un projet Laravel dockerisé. Marie a une extension qui formate le code selon des règles spécifiques, tandis que Mario en utilise une autre. Lorsqu'ils soumettent des modifications, le code peut apparaître différent en fonction des règles de formatage appliquées. Cela entraîne parfois des conflits lors de la fusion des branches ou des incohérences dans le style de code du projet.*

Ce scenario présente les **DevContainer**, un conteneur préconfiguré pour fournir un environnement de développement cohérent et isolé avec toutes les dépendances et outils nécessaires pour travailler sur un projet, souvent intégré dans un IDE comme Visual Studio Code.

## Dans ce scénario...
- **.devcontainer** et **devcontainer.json** : À la racine de PresentationDocker (à l'extérieur de Scenario3) se trouve un dossier .devcontainer contenant un devcontainer.json. Ce fichier configure les paramètres et les dépendances de l'environnement de développement.
- **docker-compose.yml** : Ce fichier de configuration permet de définir, gérer et orchestrer plusieurs conteneurs (services) de manière simplifiée en spécifiant les images, volumes, réseaux, et paramètres d'exécution.
- UnProjet : Un projet Laravel de base.
- nginx : Un fichier de configuration pour le serveur web nginx.
- php : Le Dockerfile du conteneur PHP dans lequel nous avons ajouté Composer.

## Pour lancer le scénario...
1. ctrl + shift + p
2. Devcontainer: Rebuild and Reopen in Container