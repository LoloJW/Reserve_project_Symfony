# 🍣 Sushi Factory
 
> Système de réservation de salles pour une grande entreprise.
> Application web full-stack développée avec **Symfony 7.4** et **Vue.js 3** — projet de fin de formation **DWWM** (Développeur Web et Web Mobile).
 
[![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?logo=php&logoColor=white)](https://www.php.net/)
[![Symfony](https://img.shields.io/badge/Symfony-7.4-000000?logo=symfony&logoColor=white)](https://symfony.com/)
[![Vue.js](https://img.shields.io/badge/Vue.js-3-4FC08D?logo=vuedotjs&logoColor=white)](https://vuejs.org/)
[![Doctrine](https://img.shields.io/badge/Doctrine-ORM%203-FC6A31?logo=doctrine&logoColor=white)](https://www.doctrine-project.org/)
 
---
 
## 📋 Présentation
 
Sushi Factory est une application permettant aux collaborateurs d'une entreprise de **réserver des salles**. Elle gère l'ensemble du cycle : création de compte sécurisée, authentification, et réservation des salles via une interface interactive.
 
Le projet couvre une stack web moderne de bout en bout : back-end Symfony, persistance via Doctrine, interface enrichie en Vue.js, et une chaîne qualité complète (tests, analyse statique, formatage automatique du code).
 
🔗 **Démo en ligne :** [https://...]  <!-- ⬅️ ajoute ton lien si l'appli est hébergée, sinon supprime cette ligne -->
 
## 🖼️ Aperçu
 
<!-- ⬅️ Ajoute 1 à 3 captures (accueil, réservation, espace utilisateur). -->
<!-- Place-les dans un dossier /docs et référence-les : ![Réservation](docs/reservation.png) -->
 
## ✨ Fonctionnalités
 
- **Authentification & gestion des rôles** — connexion sécurisée via le composant Security de Symfony.
- **Inscription avec vérification d'email** — confirmation du compte par lien (SymfonyCasts VerifyEmail).
- **Réinitialisation de mot de passe** — flux complet de récupération par email (SymfonyCasts ResetPassword).
- **Réservation de salles** — création et gestion des réservations par les utilisateurs.
- **Protection contre les abus** — limitation de débit (Symfony Rate Limiter).
- **Upload de fichiers** — gestion des images/avatars via VichUploader.
- **Interface interactive en Vue.js** — composants dynamiques côté front.
## 🛠️ Stack technique
 
| Couche | Technologies |
|---|---|
| **Back-end** | PHP 8.2+, Symfony 7.4, Doctrine ORM 3 |
| **Front-end** | Vue.js 3, Twig, SCSS, Webpack Encore, Symfony UX (Turbo, Stimulus) |
| **Base de données** | MySQL / MariaDB (via Doctrine ORM & Migrations) |
| **Qualité & tests** | PHPUnit, PHPStan, PHP CS Fixer |
| **Sécurité** | Symfony Security, Rate Limiter, vérification d'email, reset password |
 
## 🏗️ Architecture
 
- Le **back-end Symfony** gère l'authentification, les rôles, la logique de réservation et la persistance via **Doctrine ORM** (entités + migrations).
- Les vues sont rendues avec **Twig** et stylées en **SCSS**.
- Les parties interactives s'appuient sur **Vue.js**, compilé avec **Webpack Encore**.
- La qualité du code est outillée : tests unitaires **PHPUnit**, analyse statique **PHPStan**, et formatage **PHP CS Fixer**.
## 🚀 Installation locale
 
### Prérequis
 
- PHP 8.2 ou supérieur
- Composer
- Node.js & npm
- MySQL / MariaDB
- [Symfony CLI](https://symfony.com/download) (recommandé)
### Étapes
 
```bash
# 1. Cloner le dépôt
git clone https://github.com/LoloJW/Sushi_Factory_Project.git
cd Sushi_Factory_Project
 
# 2. Installer les dépendances back-end et front-end
composer install
npm install
 
# 3. Configurer l'environnement
# Copier .env vers .env.local puis renseigner :
#   - DATABASE_URL (connexion à ta base)
#   - MAILER_DSN  (envoi des emails de vérification / reset)
cp .env .env.local
 
# 4. Créer la base et appliquer les migrations
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
 
# 5. (Optionnel) Charger les données de démonstration
php bin/console doctrine:fixtures:load
 
# 6. Compiler les assets front-end
npm run dev        # build de développement
# ou
npm run build      # build de production
 
# 7. Lancer le serveur
symfony server:start
```
 
L'application est accessible sur `https://localhost:8000`.
 
### Outils qualité
 
```bash
vendor/bin/phpunit                 # tests
vendor/bin/phpstan analyse         # analyse statique
vendor/bin/php-cs-fixer fix        # formatage du code
```
 
## 🎯 Compétences mises en œuvre
 
Ce projet démontre :
 
- la conception d'une application **full-stack** Symfony de bout en bout ;
- la mise en place d'une **authentification sécurisée** (rôles, vérification d'email, reset password, rate limiting) ;
- la modélisation et la persistance de données avec **Doctrine ORM** (entités, migrations) ;
- l'intégration de **composants Vue.js** dans un projet Symfony via Webpack Encore ;
- l'application de **bonnes pratiques** : tests automatisés, analyse statique et formatage du code.
## 👤 Auteur
 
**Laurent Saint-Georges** — Développeur full-stack (Symfony / Vue.js), issu d'un parcours en infographie 3D.
 
- GitHub : [@LoloJW](https://github.com/LoloJW)
- LinkedIn : [https://linkedin.com/in/...]   <!-- ⬅️ à compléter -->
## 📄 Contexte
 
Projet réalisé dans le cadre de la formation **Développeur Web et Web Mobile** (Titre professionnel, niveau Bac+2). Code partagé à des fins de présentation de portfolio.
