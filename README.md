# Mini-Projet Ansible

Automatisation du déploiement d’un serveur web statique et d’une application conteneurisée (Docker + Nginx Reverse Proxy).

# Objectif du projet

Ce projet automatise deux environnements :

# Partie 1 : Webserver + Page HTML

Installation automatique de Nginx

Détection de la distribution (CentOS / Ubuntu)

Déploiement d’une page HTML via Jinja2

Utilisation des facts Ansible

Activation et démarrage du service

# Partie 2 : Application Docker + Reverse Proxy

Installation de Docker

Installation de Docker Compose

Déploiement d’une application via docker-compose

Configuration d’un reverse proxy Nginx

Utilisation de deux rôles Ansible :

Rôle webapp

Rôle nginx



# Partie 1 — Déploiement Webserver
Objectifs

Installer les packages nécessaires

Installer et configurer Nginx

Déployer une page HTML basée sur un template

Activer et démarrer Nginx

Exécution
ansible-playbook -i hosts nginx_playbook.yml

# Partie 2 — Application Docker + Reverse Proxy
Rôle webapp

Installe Docker

Installe Docker Compose

Déploie docker-compose.yml

Lance l’application

Fichier associé :
webapp/templates/docker-compose.yml.j2

Rôle nginx

Installe Nginx

Déploie la configuration reverse proxy

Redémarre Nginx

Fichier associé :
nginx/templates/nginx.conf.j2

# Exécution
ansible-playbook -i hosts nginx_webapp_playbook.yml

# Résultat final attendu
- Serveur web statique automatisé

- Application Docker fonctionnelle

- Reverse proxy opérationnel

- Déploiement complet automatisé via Ansible


- Serveur web statique automatisé

- Application Docker fonctionnelle

- Reverse proxy opérationnel

- Déploiement complet automatisé via Ansible
