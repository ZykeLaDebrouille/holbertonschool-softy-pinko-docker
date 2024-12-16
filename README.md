# **Softy Pinko - Docker Project**

## **Description**

Ce projet met en place une architecture complète et scalable pour une application composée de plusieurs services (backend, frontend, et proxy) en utilisant **Docker** et **Docker Compose**. 🚀

- **Backend** : Serve une API Flask accessible via `/api/hello`.
- **Frontend** : Une interface utilisateur statique servie avec Nginx.
- **Proxy Nginx** : Centralise les accès et gère le load balancing entre plusieurs instances du backend.

---

## **Architecture**

### Services Docker

1. **Backend** :
   - Framework : Flask (Python).
   - Route principale : `/api/hello`.
   - Scalable avec plusieurs répliques via Docker Compose.

2. **Frontend** :
   - Serveur : Nginx.
   - Contenu statique accessible à [http://localhost](http://localhost).

3. **Proxy** :
   - Serveur : Nginx.
   - Centralise les accès et effectue un load balancing automatique entre les instances backend.

---

## **Prérequis**

- Docker installé : [Docker Desktop](https://www.docker.com/products/docker-desktop)
- Docker Compose installé (inclus avec Docker Desktop).

---

## **Installation**

1. Clonez le dépôt :

   ```bash
   git clone https://github.com/zykeladebrouille/holbertonschool-softy-pinko-docker.git
   cd holbertonschool-softy-pinko-docker
   ```

2. Construisez et démarrez les services avec Docker Compose :

   ```bash
   docker-compose up --build
   ```

3. Accédez à l'application :
   - **Frontend** : [http://localhost](http://localhost)
   - **Backend API** : [http://localhost/api/hello](http://localhost/api/hello)

---

## **Structure du Projet**

```plaintext
holbertonschool-softy-pinko-docker/
├── back-end/
│   ├── api.py                # Application Flask
│   ├── Dockerfile            # Dockerfile pour le backend
├── front-end/
│   ├── index.html            # Page HTML statique
│   ├── softy-pinko-front-end.conf  # Config Nginx pour le frontend
│   ├── Dockerfile            # Dockerfile pour le frontend
├── proxy/
│   ├── proxy.conf            # Config Nginx pour le proxy
│   ├── Dockerfile            # Dockerfile pour le proxy
├── docker-compose.yml        # Orchestration des services
└── README.md                 # Documentation
```

---

## **Fonctionnalités**

1. **Backend :**
   - Serve une API Flask accessible via `/api/hello`.
   - Gestion du CORS avec `Flask-CORS`.

2. **Frontend :**
   - Héberge une interface utilisateur statique avec Nginx.

3. **Proxy :**
   - Load balancing entre plusieurs instances backend.
   - Redirection des requêtes API via `/api`.

4. **Scalabilité :**
   - Ajout de plusieurs instances backend configuré dans `docker-compose.yml`.

---

## **Utilisation des commandes Docker**

### Lancer les services

```bash
docker-compose up --build
```

### Arrêter les services

```bash
docker-compose down
```

### Voir les logs des services

```bash
docker-compose logs
```

### Accéder à un conteneur en ligne de commande

```bash
docker exec -it <container_name> bash
```

---

## **Améliorations Futures**

- Ajouter un certificat SSL avec **Let's Encrypt** pour sécuriser l'application.
- Déployer l'application sur un service cloud (AWS, Azure, DigitalOcean).
- Monitoring des performances avec des outils comme **Prometheus** et **Grafana**.

---

## **Contributeurs**

- **Enes** : Développeur en pleine ascension ! 🚀
- **Mentorat** : Guidé par mon fidèle copilote. 🤖
