#EcoRide

**EcoRide** est une plateforme de covoiturage (autopartage) conçue pour promouvoir la mobilité écologique et économique. Ce projet comprend des fonctionnalités telles que l'enregistrement des utilisateurs, la connexion, la recherche de voyages, la création de voyages, etc.

## Table des matières

- [Description](#description)

- [Fonctionnalités](#fonctionnalités)

- [Prérequis](#prérequis)

- [Installation](#installation)

- [Utiliser](#utiliser)

- [Structure du projet](#project-structure)

- [Points de terminaison de l'API](#api-endpoints)

- [Technologies utilisées](#technologies utilisées)

- [Contributions](#contributions)

- [Licence](#licence)

---

## Description

EcoRide est une application web qui permet aux utilisateurs de :
- Inscrivez-vous et gérez votre profil.
- Recherchez et réservez des trajets partagés.
- Créez de nouveaux voyages en tant que conducteurs.
- Consulter l'historique des voyages effectués ou réservés.
- Contactez l'équipe d'assistance.

L’objectif principal est de réduire l’impact environnemental des déplacements et de promouvoir la mobilité durable.







---

## Caractéristiques

1. **Inscription des utilisateurs** : les utilisateurs peuvent s'inscrire en fournissant des informations personnelles et de contact.

2. **Connexion** : les utilisateurs peuvent se connecter avec leur e-mail et leur mot de passe.

3. **Recherche de voyages** : les utilisateurs peuvent rechercher des voyages en fonction de critères tels que la ville d'origine, la destination, la date et le nombre de sièges.

4. **Création de trajets** : les conducteurs peuvent créer de nouveaux trajets partagés.
5. **Historique des voyages** : les utilisateurs peuvent consulter leur historique des voyages effectués ou réservés.

6. **Gestion des véhicules** : les conducteurs peuvent enregistrer et mettre à jour les informations de leur véhicule.

7. **Assistance utilisateur** : les utilisateurs peuvent envoyer des messages à l'équipe d'assistance.

---

## Prérequis

Avant d'installer le projet, assurez-vous d'avoir les éléments suivants :

- **Serveur Web** : XAMPP, WAMP ou tout serveur compatible avec PHP et MySQL.

- **Node.js** : version 14 ou supérieure.

- **npm** : gestionnaire de packages Noeud.js.

- **React** : Framework pour le frontend.

- **MySQL** : Base de données pour stocker les informations.











---

##Installation

1. **Cloner le référentiel**
   ```bash
   DÉPÔT git clone
   cd écoride


2. Configurer la base de données
Importer le fichier BDD.sql sur votre serveur MySQL pour créer les tables nécessaires.
Assurez-vous que le fichier Interactiondb.php disposer des informations d'identification correctes pour vous connecter à la base de données.

3. Installer les dépendances :

	INSTALLATION DU NPM

4.- Démarrez le serveur de développement : 

	DÉBUT DU MNP

5.- Configurez le backend :

Placez le fichier Interactiondb.php dans le répertoire de votre serveur Web (par ex. htdocs un XAMPP).



Utiliser

1.- Enregistrer
Accès à /Inscription pour enregistrer un nouvel utilisateur.
2.- Connexion
Accès à /Rapport pour vous connecter.
3.- Rechercher des voyages
Accès à /Covoiturage pour rechercher les voyages disponibles.
4.- Créer des voyages
Accès à /Addcovoi pour créer un nouveau voyage en tant que conducteur.
5.- Consulter l'historique
Accès à /Historique pour consulter l'historique des voyages effectués ou réservés.
6.- Contacter l'assistance
Accès à /Contact pour envoyer un message à l'équipe d'assistance.




Structure du projet

/Applications/XAMPP/xamppfiles/htdocs/ECF0624/
├── exemple/
│ ├── src/
│ │ ├── Composants/
│ │ │ ├── [Addcovoi.js](http://_vscodecontentref_/0)
│ │ │ ├── [Connexion.js](http://_vscodecontentref_/1)
│ │ │ ├── [Contact.js](http://_vscodecontentref_/2)
│   │   │   ├── [Covoiturages.js](http://_vscodecontentref_/3)
│ │ │ ├── [Headeruser.js](http://_vscodecontentref_/4)
│   │   │   ├── [Historique.js](http://_vscodecontentref_/5)
│ │ │ ├── [listsearch.js](http://_vscodecontentref_/6)
│ │ │ ├── [qns.js](http://_vscodecontentref_/7)
│ │ │ ├── [Registration.js](http://_vscodecontentref_/8)
│ │ │ ├── [cf.js](http://_vscodecontentref_/9)
│ │ ├── DB/
│ │ │ ├── [BDD.sql](http://_vscodecontentref_/10)
│ │ │ ├── [Interactiondb.php](http://_vscodecontentref_/11)
│ │ ├── Images/
│ │ ├── [App.js](http://_vscodecontentref_/12)
│ │ ├── index.js
│ ├── public/
│ ├── package.json


Points de terminaison de l'API

Principaux paramètres

1.- Inscription des utilisateurs
POST /?adduser=1
Paramètres : { nom, prenom, pseudo, email, password_id, telephone, adresse, date_naissance }
2.- Se connecter
POST /?login=1
Paramètres : { e-mail, mot de passe }
3.- Rechercher des voyages
OBTENIR /?getCombinedData=1
Paramètres : { ville_départ, ville_arrivée, date_départ, nb_place }
4.- Créer un voyage
POST /?addCovoiturage=1
Paramètres : { ville_depart, ville_arrive, heure_depart, heure_arrive, date_depart, date_arrive, descrip, prix, nb_place, fumeur, animaux, voyeco, user_id, pseudo }
5.- Siège de réserve
POST /?reserveSeat=1
Paramètres : { user_id, covoiturage_id }
6.- Historique de l'utilisateur
GET /?getUserHistory=1
Paramètres : { ID de l'utilisateur }



Technologies utilisées


L'extrémité avant: Réagir.js

Back-end : PHP

Base de données : MySQL

Serveur Web : XAMPP

Styles : Amorçage


