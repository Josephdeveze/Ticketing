# LiteMVC - Système de Gestion de Tickets

## Description
LiteMVC est une application web PHP de gestion de tickets avec un système d'authentification. Elle permet aux utilisateurs de créer des tickets, aux techniciens de les traiter et aux administrateurs de les gérer.

## Fonctionnalités

### Authentification
- Inscription des utilisateurs
- Connexion/Déconnexion
- Gestion des rôles (Utilisateur, Technicien, Super Admin)

### Gestion des tickets
- Création de tickets
- Attribution de tickets aux techniciens
- Suivi du statut des tickets
- Génération de rapports sur les tickets

## Architecture Technique

### Technologies utilisées
- PHP 8.0+
- MySQL
- Twig Template Engine
- AltoRouter
- Bootstrap 5.3
- Composer

### Structure MVC
```
litemvc/
├── controllers/    # Contrôleurs de l'application
├── models/         # Modèles de données
├── views/          # Templates Twig
├── database/       # Configuration BDD
├── middlewares/    # Middleware d'authentification
└── vendor/         # Dépendances
```

## Installation

1. Cloner le projet
```bash
git clone [url-du-repo]
```

2. Installer les dépendances
```bash
composer install
```

3. Créer la base de données
- Importer le fichier `database/base.sql`
- Configurer les accès dans `database/Database.php`

4. Configurer le serveur web
- Point d'entrée: `index.php`
- URL de base: `/litemvc`

## Rôles utilisateurs

- **Utilisateur (role 0)**: Peut créer et voir ses tickets
- **Technicien (role 1)**: Peut gérer les tickets qui lui sont assignés
- **Super Admin (role 2)**: Peut assigner les tickets aux techniciens
