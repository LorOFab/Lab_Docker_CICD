# Lab_Docker_CICD

Intégration de Docker dans un workflow CI/CD avec Apache et PHP

Objectif : mettre en place un environnement conteneurisé pour une 
	application PHP utilisant Apache, puis configurer 
	un pipeline CI/CD pour automatiser les tests et le déploiement

--------------------------------------------------------------------------------------------

Étape 1 : préparation de l'application PHP

		Créez un dossier nommé workflow-apache-php contenant index.php :
		 
		 		$ mkdir workflow-apache-php
				$ cd workflow-apache-php
				$ nano index.php

-------------------------------------------------------------------------------------------

Étape 2 : création du Dockerfile

Le Dockerfile définira l'environnement Apache et PHP.

				$ cd workflow-apache-php
				$ nano Dockerfile 
				
-------------------------------------------------------------------------------------------

Étape 3 : test local de l'application avec Docker

	a- Construction de l'image Docker :

		$ docker build -t workflow-apache-php .

	b- Lançons le conteneur :

		$ docker run -d -p 8080:80 workflow-apache-php
		
	c- Une fois le conteneur lancé, vérifions. Pour ce faire, on lance :
	
		$ curl -f http://localhost:8080 | grep "Bonjour"
		
			 Le message dans la console est le contenu du fichier index.php

			 






