# Utiliser une image PHP officielle
FROM php:7.2-cli

# Installer les dépendances nécessaires (comme zip, unzip, etc.)
RUN apt-get update && apt-get install -y \
    git \
    unzip \
    libzip-dev \
    && docker-php-ext-install zip

# Installer Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Exposer le port 8000
EXPOSE 8000

USER root

# Créer un répertoire de travail pour le projet
WORKDIR /app

# Commande par défaut à exécuter dans le conteneur
CMD [ "php", "-a"]