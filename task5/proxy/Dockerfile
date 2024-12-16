# Utiliser Nginx comme base
FROM nginx:latest

# Copier la configuration du proxy
COPY ./proxy.conf /etc/nginx/conf.d/default.conf

# Exposer le port 80 pour les clients
EXPOSE 80
