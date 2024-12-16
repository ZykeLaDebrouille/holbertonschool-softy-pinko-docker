# Utiliser Nginx comme image de base
FROM nginx:latest

# Copier les fichiers du front-end dans le répertoire de travail de Nginx
COPY ./index.html /usr/share/nginx/html/index.html

# Copier le fichier de configuration de Nginx
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Exposer le port 9000 pour le front
EXPOSE 9000
