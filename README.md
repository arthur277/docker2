# Projet DevSecOps - Stack Docker Multi-Applications

## Description

Ce projet contient 5 applications Dockerisées :
- accueil (Nginx statique)
- kiacook (Nginx statique)
- frontend (Nginx statique)
- firstappnext (Next.js)
- rocket-ecommerce-v1.0.7 (Django + Gunicorn)

Chaque application est contenue dans son dossier avec son propre Dockerfile.
Toutes les applications, sauf accueil, sont accessibles derrière un reverse proxy (à ajouter selon besoin).
Les images sont publiées sur Docker Hub et le code source est open-source.
---


Sommaire
Prérequis

Déploiement rapide

Accès aux applications

Variables d'environnement

Schéma d’architecture

Explications techniques

Répartition des tâches

Optimisations et sécurité

Liens utiles

Prérequis
Docker

Docker Compose

## Lancement rapide

1. Clone le projet :
https://github.com/arthur277/docker2


2. Build et démarre tous les services :

docker compose up --pull always --build



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
Explications techniques
Reverse Proxy : Toutes les apps sauf accueil sont derrière un reverse proxy pour centraliser l’accès et la sécurité.

accueil : Accessible directement pour permettre des pentests whitebox.

Images Docker Hub : Les images sont publiées pour garantir la reproductibilité et la rapidité du déploiement.

Stripe : Intégration de la passerelle de paiement Stripe dans l’app e-commerce, avec gestion sécurisée des clés API via variables d’environnement.

Optimisation Docker : Chaque Dockerfile est optimisé pour la légèreté et la sécurité (multi-stage build, user non-root, nettoyage des dépendances…).

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

Optimisations et sécurité
Images Docker minimales (alpine, multi-stage, suppression des caches)

Utilisation de variables d’environnement pour les secrets

Reverse proxy pour limiter la surface d’attaque

Un service exposé directement pour pentest approfondi

Publication open-source et sur Docker Hub pour la communauté

Liens utiles
Docker Hub - arthur277

Documentation Stripe

Docker Compose

## Schéma d'architecture

![Schéma d'architecture](chemin/vers/schema.png)

---

## Auteurs

- Arthur Deumeni Tsako


