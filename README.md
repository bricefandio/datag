# datag

1.	Se connecter en tant que développeur avec celui qui a le rôle de développeur.
2.	On créé un dossier test : dans le dossiers test la je met mes tests unitaires et test d’intégrations.
3.	Dans le terminal : taper : composer require –dev phpunit/phpunit :^10.5.20
Aller dans composer.json ajouter 


{
    "autoload": {
    "psr-4": {
        "App\\": "class/"
    }
},
"autoload-dev": {
    "psr-4": {
        "Tests\\": "tests/"
    }
},
    "require-dev": {
        "phpunit/phpunit": "^10.5.20"
    }
}


Taper la commande : composer dump-autoload
On ajoute un fichier .gitignore  et on écrit vendor


4.	Entrer sur gitlab en tant que root pour créer un nouveau projet
5.	Créer un nouveau projet et ajouter adams comme maintenir et guillaume comme developpeur
On pousse le projet sur la branche principale
On utilise les commandes de push an existing folder

Guillaume doit ajouter un test sur sa branche a lui.
On crée d’abord une branche develop pour les 2 developpeurs.
Se connecter avec guillaume sur developpeur
Git clone « lien » pour cloner le projet
On crée sa branche sur le terminal : git branch feature / addtowertest
Et               git checkout feature/addtowertest
Et après on pousse avec git push
6.	Après on se connecte sur git avec guillaume et on fait un create merge request
On fait un checkout-b develop     (ca crée une nouvelle branche et sa check up automatiquement)
Après on fait un git pull


On crée une nouvelle branche pour la pipeline git branch feature/create pipeline
Git checkout feature/create pipeline.


On crée un fichier .gitlab.ci.yml
A chaque fois qu’on pull le projet, on fait composer install
Commande pour voir si les tests passent :   
./vendor/bin/phpunit tests

Fait le pipeline. On rempli le données de gitlab.ci.yml
Et on fait un 	git add .
		Git commit -m « message »
		Git push

On ajoute les 3 fichiers php unit, et sonarprojet

Lien  pascal
https://github.com/victorwenji/
