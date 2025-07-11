# Projet DevSecOps - Stack Docker Multi-Applications

## Description

Ce projet contient 5 applications Dockerisées :
- accueil (Nginx statique)
- kiacook (Nginx statique)
- frontend (Nginx statique)
- firstappnext (Next.js)
- rocket-ecommerce-v1.0.7 (Django + Gunicorn)

Chaque application est contenue dans son dossier avec son propre Dockerfile.

---

## Lancement rapide

1. Clone le projet :
https://github.com/arthur277/Docker/tree/master


2. Build et démarre tous les services :
docker compose up --build


3. Accède aux applications :
- Accueil : [http://localhost:8000](http://localhost:8000)
- KIA Cook : [http://localhost:8082](http://localhost:8082)
- Frontend : [http://localhost:8083](http://localhost:8083)
- FirstAppNext : [http://localhost:8080](http://localhost:8080)
- Rocket Ecommerce : [http://localhost:8084](http://localhost:8084)

---

## Structure du projet

/accueil
/kiacook
/frontend
/firstappnext
/rocket-ecommerce-v1.0.7
docker-compose.yml
README.md


---

## Variables d'environnement

Si besoin, crée un fichier `.env` à la racine pour y placer tes secrets ou variables Django.

---

## Publication Docker Hub

Les images sont disponibles sur Docker Hub :
- [accueil](https://hub.docker.com/r/arthurd277/accueil)
- [kiacook](https://hub.docker.com/r/arthurd277/kiacook)
- [frontend](https://hub.docker.com/r/arthurd277/frontend)
- [firstappnext](https://hub.docker.com/r/arthurd277/firstappnext)

---

## Schéma d'architecture

![Schéma d'architecture](chemin/vers/schema.png)

---

## Auteurs

- Arthur Deumeni Tsako


