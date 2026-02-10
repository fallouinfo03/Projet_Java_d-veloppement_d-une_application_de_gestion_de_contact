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
Dans cette section, choisis les éléments que TU as principalement gérés (exemples ci-dessous) :
Développement de la logique métier : Implémentation de la classe GestionnaireContacts et des requêtes SQL.
Sécurisation : Mise en place de la vérification d'unicité des emails avant l'insertion.
Base de données : Conception du schéma relationnel et rédaction du script de création de la table.

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







