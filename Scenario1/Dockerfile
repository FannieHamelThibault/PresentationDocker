# Utiliser une image PHP officielle avec Composer pré-installé
FROM php:8.2-cli

# Installer les dépendances nécessaires (comme zip, unzip, etc.)
RUN apt-get update && apt-get install -y \
    git \
    unzip \
    libzip-dev \
    && docker-php-ext-install zip

# Installer Composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

# Créer un répertoire de travail pour le projet
WORKDIR /app

# Commande par défaut à exécuter dans le conteneur
CMD [ "php", "-a" ]