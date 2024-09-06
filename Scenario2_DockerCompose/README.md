# Docker Compose

*Mario et Marie travaillent ensemble sur un projet Laravel. Marie a des problèmes de compatibilité avec la version de PHP installée sur son système, ce qui entraîne des erreurs lors de l'exécution de Laravel. Mario a le même problème, mais avec sa version de MySQL.*

Ce scenario présente **Docker Compose**, un outil permettant de définir et de rouler plusieurs conteneurs sur un même réseau.

## Dans ce scénario...
- **docker-compose.yml** : Ce fichier de configuration permet de définir, gérer et orchestrer plusieurs conteneurs (services) de manière simplifiée en spécifiant les images, volumes, réseaux, et paramètres d'exécution.
- UnProjet : Un projet Laravel de base.
- nginx : Un fichier de configuration pour le serveur web nginx.
- php : Le Dockerfile du conteneur PHP dans lequel nous avons ajouté Composer.

## Pour lancer le scénario...
1. S'assurer d'être dans Scenario2 dans le terminal
3. `docker compose up -d`