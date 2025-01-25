# PROJET DE PIPELINE CI/CD 
Pour le projet nous avons 02 applications dont nous voulons automatiser les taches d'integration et de deploiement.

# Description des apps
  *l'app_1, API REST en python (FLASK)* : une API REST simple qui renvoie un message de bienvenue et accepte une entree utilisateur 
  pour renvoyer une reponse.
  *l'app_2, une application web statique en HTML/CSS avec un backend simple en Node.js* : Une page web affichant une liste de taches ou un backend Node.js 
  gere les ajouts de taches via un formulaire.
 Les differents codes sources se trouvent en local, nous avons travaille sur VS code 

 # LES DIFFERENTES ETAPES DU PROJETS 

   # Etape 1: Definition des objectifs et choix des outils 
     Pour assurer un déploiement automatisé et fiable de nos applications, nous avons mis en place
     un pipeline CI/CD en utilisant GitHub Actions pour l'intégration continue et Docker pour le déploiement sur un serveur 
     Ubuntu.
   # Etape 2: DEVELOPPER LES APPLICATIONS ET PUSH
   
  * Nous avons developpe nos appli sur Vs code ensuite nous avons creer un depot Git dans lequel nous avons pousser (push) nos differents code sources. 
    Ces applications sont organisées dans des branches GitHub distinctes:
       -main, pour l'application Flask.
       -app2, pour l'application Node.js.

    # Etape 3. Configuration des fichiers Docker
  Pour chaque application, nous avons créé un fichier Dockerfile permettant de définir l'environnement d'exécution de l'application.

   # Etape 4. Configuration de GitHub Actions

  Nous avons mis en place des workflows CI/CD dans GitHub Actions pour automatiser les étapes suivantes :

    -Clonage du dépôt.

    -Installation des dépendances.

    -Exécution des tests automatisés (unitaires et d'intégration).

    -Génération d'un rapport de tests en PDF.

    -Construction et publication des images Docker sur Docker Hub.

    -Déploiement automatique sur un serveur Ubuntu via SSH.

  # Etape 5. Implémentation des tests automatisés

Nous avons intégré des tests unitaires et de performance pour chaque application.

Pour Flask (Python) : Tests unitaires avec unittest.
 Génération de rapports HTML et conversion en PDF via wkhtmltopdf.

Pour Node.js :
Tests unitaires et d'intégration avec Jest.
Génération de rapports HTML et conversion en PDF via Puppeteer.


# ETAPE 6. Déploiement avec AWS EC2


