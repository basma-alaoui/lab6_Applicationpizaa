PizzaRecipes – Application Android Java
        
         Description

PizzaRecipes est une application Android développée en Java permettant d’afficher une liste de pizzas avec :

leur image 
leur nom
leur prix 
leur durée de préparation ⏱️

L’utilisateur peut cliquer sur une pizza pour consulter :

les ingrédients
la description
les étapes de préparation

Le projet suit une architecture organisée avec :

classes
dao
service
adapter
ui
 Aperçu de l’application
 Écran détail d’une pizza
5
               
                Technologies utilisées
Java
Android Studio
ListView
Custom Adapter
Intent
Splash Screen
POO (Programmation Orientée Objet)
📂 Structure du projet
com.example.pizzarecipes
│
├── classes
│   └── Produit.java
│
├── dao
│   └── IDao.java
│
├── service
│   └── ProduitService.java
│
├── adapter
│   └── PizzaAdapter.java
│
├── ui
│   ├── SplashActivity.java
│   ├── ListPizzaActivity.java
│   └── PizzaDetailActivity.java


                Modèle de données

Chaque pizza est représentée par la classe Produit contenant :

private long id;
private String nom;
private double prix;
private int imageRes;
private String duree;
private String ingredients;
private String description;
private String etapes;
         
         Interface DAO

Le projet utilise une interface générique IDao<T> :

public interface IDao<T> {
    T create(T t);
    T update(T t);
    boolean delete(long id);
    T findById(long id);
    List<T> findAll();
}

            Gestion des données

La classe ProduitService :

stocke les pizzas en mémoire
implémente le pattern Singleton
gère les opérations CRUD
 Écrans de l’application
 Splash Screen
Affiche le logo pendant 2 secondes
Redirige automatiquement vers la liste des pizzas
Liste des pizzas
Utilisation d’une ListView
Affichage image + nom + prix + durée
 Détails d’une pizza

Affiche :

image
ingrédients
description
étapes de préparation
 Lancer le projet
1️ Cloner le projet
git clone https://github.com/votre-compte/PizzaRecipes.git
2️ Ouvrir avec Android Studio
File → Open
Sélectionner le dossier du projet
3️ Exécuter l’application
Connecter un émulateur ou téléphone Android
Cliquer sur ▶ Run
 Minimum SDK
API 24 - Android 7.0
