# TP 3 - Formulaires Symfony 

**Nom :** Doha ElAkrouchi
**Date :** 26 Décembre 2025

## Description du projet

Création d'un formulaire Symfony pour ajouter un produit au panier.

Le formulaire permet de :
- Sélectionner la quantité (de 1 à 10)
- Choisir la couleur parmi 3 options 

## Structure des fichiers créés

### 1. Form Type
**Fichier :** `src/Form/Type/ProductType.php`

Définit les deux champs du formulaire :
- `quantity` (IntegerType) : Nombre entier avec validation min=1, max=10
- `color` (ChoiceType) : Liste déroulante avec 3 choix

### 2. Contrôleur
**Fichier :** `src/Controller/ProductController.php`

Route `/product` qui :
- Crée le formulaire avec `createForm()`
- Gère la soumission avec `handleRequest()`
- Valide les données avec `isValid()`
- Affiche les données soumises (debug avec `dd()`)

### 3. Vue Twig
**Fichier :** `templates/product/index.html.twig`

Affiche :
- Image du produit
- Informations (prix, description, caractéristiques)
- Formulaire personnalisé avec fonctions Twig : `form_start()`, `form_widget()`, `form_end()`

### 4. Template de base
**Fichier :** `templates/base.html.twig`

Template parent avec :
- Import de Bootstrap 5.3 (CSS + JS)
- Blocks Twig pour l'héritage de templates


## Ce que j'ai appris

### Les Form Types Symfony
- Comment créer un Form Type avec `AbstractType`
- Utiliser `IntegerType` pour les nombres
- Utiliser `ChoiceType` pour les listes déroulantes
- Ajouter des attributs HTML personnalisés 

### Le pattern MVC
- **Model :** Form Type (définition des données)
- **View :** Twig (affichage)
- **Controller :** ProductController (logique métier)

### Twig et les formulaires
- Fonctions `form_start()`, `form_widget()`, `form_label()`, `form_errors()`, `form_end()`
- Personnalisation des attributs CSS avec Bootstrap
- Héritage de templates avec `{% extends %}`

### Git et GitHub
- Workflow : add → commit → push
- Importance de commits clairs et descriptifs
- Convention de nommage des fichiers 

