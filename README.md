# containers

Génération d'un environnement de developpement

## A quoi sert ?

Ce projet permet d'avoir une environnement de developpement dockerisé utilisant nginx - php 8.1 - mariadb - postgreSQL

Le developpeur aura le choit de choisir quel serveur de base de données à utiliser.

## Comment faire afin de lancer mon serveur ?

La première étape et de déclarer la configuration nginx liée à votre projet : `docker/nginx/config`
Ce dossier contient actuellement deux exemples de configuration : 
1. default.conf :
Cette configuration est transverse elle ne comporte pas une énorme configuration servant à faciliter l'initialisation de l'environnement.

2. drupal.conf:
Cette configuration est dédié au projet Drupal >= 7 contenant la configuration spécifique liée à la spécificité de Drupal.

Dans chaque configuration le developpeur à la main afin de choisir le host de sont projet (à ne pas oublié de déclarer le host dans votre host local)

## Comment choisir mon serveur BDD ?
Selon le besoin, les deux serveur sont running et le developpeur pourra créer et choisir la base de données à utiliser.
Les configurations de connexion sont indiquées au sein du fichier docker-compose.yml.

> Parmis les axes d'amélioration est de gérer les variables avec un fichier `.env` afin de les contextualiser
