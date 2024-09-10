# Création Symfony LTS

```bash
Symfony new SymEntitiesG2 --webapp --version=lts
cd SymEntitiesG2
git remote add origin git@github.com:PommeDeuxTerre/SymEntitiesG2.git 
git push origin main
```

## Création du contrôleur

    php bin/console make:controller

2 fichiers sont créés, le contrôleur et la veu en `twig`

## Pour voir les routes

    php bin/console debug:route

#### Changement du chemin pour que ce soit dans le contrôlleur de notre accueil

Dans `src/Controller/PublicController.php`

on change

```php
#[Route('/public', name: 'app_public')]
# par
#[Route('/', name: 'homepage')]
```

## Copie de .env en .env.local
    cp .env .env.local

### Choix de la DB et modification du `.env.local`

### Création de la DB
    php bin/console doctrine:database:create

### Création de l'entité `Post`

    php bin/console make:entity Post

Création des fichiers
Avec l'id comme seul attribut

Si on veut le remplir on retape la même commande

    php bin/console make:entity Post
