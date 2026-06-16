# Application de Test Symfony CashNow

L'« Application de Test Symfony CashNow » est une application de référence créée pour tester votre
capacité à vous adapter à un nouvel environnement technique, basée sur l'architecture de notre projet
pour développer des applications en suivant les [Bonnes Pratiques Symfony][1].

Vous pouvez également en apprendre davantage sur ces pratiques dans [le livre officiel Symfony][5].

## Prérequis

* PHP 8.2.0 ou supérieur
* Extension PHP PDO-SQLite activée
* Et les [prérequis habituels d'une application Symfony][2]

## Installation

Installer notre projet « Application de Test Symfony » :

```bash
# Cloner le dépôt de code et installer ses dépendances
git clone git@github.com:CashNowMobile/cashnow_test.git cashnow_test
```

## Utilisation

Il n'est pas nécessaire de configurer quoi que ce soit avant de lancer l'application. Il existe
2 façons différentes de lancer cette application selon vos besoins :

**Option 1.** [Télécharger la CLI Symfony][4] et exécuter cette commande :

```bash
cd cashnow_test/
symfony serve
```

Accédez ensuite à l'application dans votre navigateur à l'URL indiquée (<https://localhost:8000> par défaut).

**Option 2.** Utiliser un serveur web comme Nginx ou Apache pour exécuter l'application
(lire la documentation sur [la configuration d'un serveur web pour Symfony][3]).

Sur votre machine locale, vous pouvez exécuter cette commande pour utiliser le serveur web intégré de PHP :

```bash
cd cashnow_test/
php -S localhost:8000 -t public/
```

## Tests et Tâches à Réaliser

* Installer le projet Symfony dans votre environnement local, en nommant le projet `cashnow_test`.
* Créer un dépôt git personnel (GitLab, GitHub, ...) avec le projet original. Créer une branche pour le test.
* Donner accès au dépôt à orey@cashnowmobile.com
* S'assurer que tout fonctionne et qu'il n'y a pas de fautes en testant soigneusement votre projet. Utiliser les tests unitaires pour vérifier et corriger les erreurs.
* Un utilisateur final a indiqué qu'il préférerait voir les articles les plus récents en premier. Pouvez-vous effectuer ce changement ?
* Une fonctionnalité existante déclenche un e-mail à l'auteur d'un article lorsqu'un commentaire est ajouté. Cette fonctionnalité ne fonctionne pas en mode développement. Pouvez-vous la corriger ?
* Si un utilisateur se connecte, il est redirigé vers la page d'administration, ce qui provoque une erreur si le rôle attribué est USER. Corrigez ce problème en redirigeant vers la page du blog après la connexion.
* La recherche ne prend pas en compte les tags assignés aux articles. Modifiez-la pour corriger ce problème.
* Ajouter la possibilité de téléverser un fichier dans l'objet article, basé sur un service (nous utiliserons également les commandes `make:entity` pour modifier l'entité Post, `make:migration` et `doctrine:migration:migrate` pour mettre à jour la base de données).
* Mettre à jour le README pour expliquer votre fonctionnalité.

```bash
cd cashnow_test/
./bin/phpunit
```

**Bonne chance !**

[1]: https://symfony.com/doc/current/best_practices.html
[2]: https://symfony.com/doc/current/setup.html#technical-requirements
[3]: https://symfony.com/setup/web_server_configuration.html
[4]: https://symfony.com/download
[5]: https://symfony.com/book
[6]: https://getcomposer.org/
