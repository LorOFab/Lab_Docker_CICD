# Utiliser une image de base Apache avec PHP préinstallé
FROM php:8.2-apache

# Copier les fichiers de l'application dans le dossier racine web d'Apache
COPY . /var/www/html/

# Donner les permissions nécessaires
RUN chown -R www-data:www-data /var/www/html

# Exposer le port 80 pour le serveur Apache
EXPOSE 80
