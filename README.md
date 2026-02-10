Gestionnaire de Contacts Java (JDBC & MySQL)
--------------------------------------------

Description du projet
----------------------
Ce projet consiste en une application console développée en Java permettant de gérer un répertoire de contacts professionnels ou personnels. L'application communique avec une base de données MySQL pour assurer la persistance des données via l'API JDBC.

Note : Projet Collaboratif Ce projet a été réalisé en équipe dans le cadre de ma formation en Data Science. Il illustre notre capacité à concevoir une architecture logicielle modulaire (POO) et à manipuler des bases de données relationnelles.

Fonctionnalités
----------------
Connexion sécurisée : Authentification dynamique à la base de données par l'utilisateur.

CRUD Complet : Ajout, affichage, modification et suppression de contacts.

Recherche intelligente : Filtrage par mot-clé (nom, prénom, etc.).

Gestion de l'unicité : Vérification automatique des emails pour éviter les doublons.

Sécurité : Utilisation de PreparedStatement pour prévenir les injections SQL.

Stack Technique
----------------
Langage : Java
Base de données : MySQL 8.0
Connecteur : JDBC (Java Database Connectivity)
Outils : Scanner (entrées console), Script SQL de déploiement.

Structure du Code
------------------
L'architecture suit les principes de la programmation orientée objet :
Contact.java : Modèle de données (POO) représentant l'entité Contact.
GestionnaireContacts.java : Cœur logique contenant les requêtes SQL et la gestion de la connexion.
Main.java : Interface utilisateur (menu interactif) et point d'entrée du programme.

Mes Contributions Personnelles
-------------------------------
J'ai été responsable de la conception et du développement de la classe Contact.java, socle du projet. Mon travail s'est concentré sur les points suivants :
Conception du Modèle de Données : Définition de la structure de l'objet Contact (Nom, Prénom, Téléphone, Email, Catégorie) en respectant les principes d'encapsulation de la Programmation Orientée Objet (POO).

Validation des Données (Regex) : Implémentation de contraintes de saisie via java.util.regex.Pattern pour garantir la validité du format des adresses email avant leur stockage en base de données.

Persistance et Sérialisation : Intégration de l'interface Serializable pour permettre une évolution future vers une sauvegarde d'objets sur disque.
Optimisation de l'affichage : Redéfinition (Override) de la méthode toString() pour assurer un affichage console ergonomique et lisible, et création de méthodes utilitaires comme getNomComplet().

Installation et Utilisation
----------------------------
1. Prérequis
Avoir installé le JDK (Java Development Kit).
Un serveur MySQL actif.
Le driver JDBC MySQL (mysql-connector-java.jar) dans votre classpath.
2. Configuration de la base de données
Exécutez le script suivant dans votre client MySQL :
SQL
CREATE DATABASE Gestion_de_contacts;
USE Gestion_de_contacts;

CREATE TABLE Contact (
    id_contact INT PRIMARY KEY AUTO_INCREMENT,
    Nom VARCHAR(100),
    prenom VARCHAR(120),
    categorie VARCHAR(60),
    telephone VARCHAR(50),
    email VARCHAR(50) UNIQUE,
    adresse TEXT,
    date_creation TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
3. Exécution
Bash
# Compilation
javac *.java

# Exécution
java Main







