# The Lone Conteneur 

*Mario et Marie réalisent un projet en Laravel pour un client. Les deux travaillent aussi chacun de leurs côtés sur des projets qui requierent des versions antérieures de php. Afin de ne pas devoir refaire l'installation complète de PHP à chaque fois qu'ils désirent changer de projet.*

Ce scenario présente un conteneur solitaire composé de php 8.2 et de Composer. Nous allons lier ce conteneur à notre projet sur notre machine locale grâce à un **volume lié** (bind mount).

## Dans ce scénario...
- **Dockerfile** : Ce fichier texte contient une série d'instructions pour automatiser la création d'une **image** Docker, en définissant le système de base, les dépendances, les fichiers, et les commandes à exécuter dans un conteneur.
- UnProjet : Un projet Laravel de base.
- scenario1.sh : Un script servant uniquement à la démonstration, il ne fait pas parti de l'architecture d'un projet Docker standard.

## Pour lancer le scénario...
S'assurer d'être dans Scenario1 dans le terminal
1. `docker build -t phpcegep .`
2. `docker run -it -p 8000:8000 -v CHEMIN/DU/PROJET/SUR/L'HÔTE:/app phpcegep bash`
3. `cd UnProjet`
4. `php artisan serve --host 0.0.0.0`

#### Pour aller plus loin...
- phpcegep est le nom de l'image (défini par le -t dans `docker build -t phpcegep .`).
- Le port 8000 du conteneur est bindé sur le port 8000 de la machine (`-p 8000:8000`).
- `CHEMIN/DU/PROJET/SUR/L'HÔTE:/app` bind votre répertoire de projet sur la machine à le conteneur afin de lui donner accès.