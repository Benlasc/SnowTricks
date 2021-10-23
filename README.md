SnowTricks est un site internet permettant aux internautes de consulter et enrichir un annuaire des figures de snowboard.

### Environnement de développement

## Pré-requis

PHP >= 7.2.5 
Composer

## Installer les dépendances

```bash
composer install
```

## Indiquer l'URL de votre base de données et le MAILER_DSN 

Créez un fichier « .env.local » à la racine du projet et indiquez les deux variables suivantes :

```bash
MAILER_DSN=smtp://...
DATABASE_URL="mysql://..."
```

## Installer la base de données et les tables

```bash
php bin/console doctrine:database:create
php bin/console doctrine:schema:update --force
```

## Charger les figures et le compte administrateur dans la base de donnnées

```bash
php bin/console doctrine:fixtures:load
```

## Lancer le serveur de développement

```bash
php bin/console server:run
```

## Se connecter en tant qu'administrateur ou utilisateur

Email : admin@domain.fr
Password : Azerty20

Email : user@domain.fr
Password : Azerty20
