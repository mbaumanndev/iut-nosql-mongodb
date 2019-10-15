Cours de NoSQL sur Redis
========================

Ce dépôt contient du contenu déstiné à une utilisation pédagogique auprès des étudiants de seconde année du département informatique de l'IUT d'Amiens suivant le parcours orienté en bases de données.

Pré-requis
----------

Pour utiliser le contenu de ce dépôt, vous devez avoir un ordinateur équipé de :

- Docker 17.09.0+
- Docker Compose

Lancement de Docker
-------------------

Pour ce nouveau projet, nous allons de nouveau utiliser Docker avec l'utilitaire docker-compose. Notre infrastructure comporte trois conteneurs :
- Un conteneur mongodb en mode base de données,
- Un conteneur mongodb qui nous servira à avoir la ligne de commande,
- Un conteneur Mongo Express, un utilitaire en NodeJS + Express pour visualiser notre base comme on le ferait sur MySQL avec un phpMyAdmin.

> Avant de démarrer, si vous êtes sur des postes Linux ou Mac, vous pouvez retirer les `#` au début des lignes 7 et 8 du fichier `docker-compose.yml` pour activer la persistance sur disque.

Afin de démarrer notre infrastructure, nous allons éxécuter la commande suivante :

```
docker-compose up -d
```

Une fois l'infrastructure démarrée, vous pouvez vous pouvez ouvrir la ligne de commande avec la commande suivante :

```
docker-compose run mgcli
```

En fin de séance, n'oubliez pas d'éteindre l'infrastructure avec la commande appropriée :

```
docker-compose down
```

> Attention : Cette fois-ci, notre docker est configuré pour faire persister les données ! Si vous corrompez votre base, éteignez votre environement docker, et supprimez le contenu du répertoire `mongo-data`. De même, si vous changez de poste, pensez à copier votre répertoire `mongo-data`.
