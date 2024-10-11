Projet WordPress avec MySQL et phpMyAdmin via Docker Compose
Ce projet utilise Docker Compose pour configurer un environnement de développement WordPress complet, incluant une base de données MySQL et un outil de gestion de base de données phpMyAdmin.

Prérequis
Docker installé sur votre machine
Docker Compose installé
Contenu du fichier docker-compose.yml
Ce fichier définit trois services :

WordPress : Le CMS WordPress fonctionnant sur le port 8010.
MySQL : Base de données MySQL 8.0 pour stocker les données de WordPress.
phpMyAdmin : Un outil web pour gérer la base de données MySQL, disponible sur le port 8020.
Services
WordPress :

Utilise l'image officielle WordPress.
Exposé sur le port 8010 de l'hôte (accessible via http://localhost:8010).
Les variables d'environnement sont définies pour connecter WordPress à la base de données MySQL.
MySQL :

Utilise l'image officielle MySQL version 8.0.
Les variables d'environnement définissent la base de données exampledb et les informations de connexion (utilisateur et mot de passe).
phpMyAdmin :

Utilise l'image officielle de phpMyAdmin.
Accessible sur le port 8020 (via http://localhost:8020).
Permet de gérer la base de données MySQL via une interface graphique.
Volumes
Deux volumes sont définis pour persister les données :

wordpress : Stocke les fichiers WordPress.
db : Stocke les données de la base de données MySQL.
