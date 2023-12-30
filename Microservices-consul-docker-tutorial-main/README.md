# Tutoriel sur l'utilisation des Microservices avec Consul et Docker

Ce tutoriel vous guide à travers la mise en place d'une architecture de microservices utilisant Consul pour la découverte de services et Docker pour le déploiement. Les quatre principaux services inclus sont :

### 1. Service Client
Ce service agit en tant que point d'entrée pour les demandes des utilisateurs. Il interagit avec d'autres services pour répondre aux requêtes.

### 2. Service Voiture
Ce service gère les informations relatives aux voitures, telles que la création, la modification et la suppression des données des véhicules.

### 3. Service de Découverte (Discovery)
Consul est utilisé comme serveur de découverte pour permettre aux services de trouver et de se connecter les uns aux autres de manière dynamique.

### 4. Service Passerelle (Gateway)
Ce service agit comme une passerelle pour rediriger les requêtes des utilisateurs vers les services appropriés.

## Comment Utiliser ce Tutoriel

### Prérequis
- Docker installé sur votre machine
- Compréhension de base des microservices et de Consul

### Simulation : 

https://drive.google.com/file/d/1lY-imwBT8Osj7J_YzKVTvAdK44i-O_4j/view?usp=sharing

### Étapes du Tutoriel
1. Cloner ce dépôt Git sur votre machine locale.
2. Accéder à chaque service individuellement pour comprendre son rôle et son fonctionnement.
3. Suivre les instructions de déploiement pour exécuter l'ensemble des services sur Docker.


## Instructions de Déploiement

1. Accédez au répertoire racine du projet.
2. Exécutez `docker-compose up` pour démarrer l'ensemble des services.
3. Consultez les logs pour vous assurer que tous les services se sont correctement démarrés.



## Endpoints API

### Dashboard Consul :
Consul: `http://localhost:8500/ui/dc1/services`

### PhpMyAdmin :
PhpMyAdmin: `http://localhost:8081/` (root:root)

### Service Client
- Récupérer tous les clients : `GET http://localhost:8888/SERVICE-CLIENT/clients`
- Ajouter un nouveau client : `POST http://localhost:8888/SERVICE-CLIENT/clients`
- Mettre à jour un client existant : `PUT http://localhost:8888/SERVICE-CLIENT/clients/{id}`
- Supprimer un client : `DELETE http://localhost:8888/SERVICE-CLIENT/clients/{id}`

### Service Voiture
- Récupérer toutes les voitures : `GET http://localhost:8888/SERVICE-VOITURE-V0/voitures`
- Ajouter une nouvelle voiture : `POST http://localhost:8888/SERVICE-VOITURE-V0/voitures`
- Mettre à jour une voiture existante : `PUT http://localhost:8888/SERVICE-VOITURE-V0/voitures/{id}`
- Supprimer une voiture : `DELETE http://localhost:8888/SERVICE-VOITURE-V0/voitures/{id}`


