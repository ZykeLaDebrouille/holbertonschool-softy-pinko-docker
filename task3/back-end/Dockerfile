# Base image
FROM ubuntu:latest

# Update APT
RUN apt-get update && apt-get upgrade -y

# Install Python and pip
RUN apt-get install -y python3 python3-pip

# Correct "EXTERNALLY-MANAGED" warning for pip
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask et le nécessaire flask
RUN pip3 install Flask Flask-Cors

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier le script Flask dans l'image
COPY ./api.py /app/api.py

# Commande pour lancer l'API
CMD ["python3", "api.py"]
