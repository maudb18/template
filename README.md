# Template GRETA

## Description
Ce template a pour but de vous aider à démarrer un projet au GRETA. 
L'exemple est fait pour un projet Streamlit, mais vous pouvez l'adapter à vos besoins.

## Installation
Créer votre repository sur Github et cloner le en local.
Copier les fichiers de ce template dans votre repository local.
Travaillez sur votre projet depuis la branche `dev` et faites des pull request vers la branche `main` pour mettre à jour votre projet. (vous pouvez utiliser une branche intermédiaire si vous le souhaitez)

## Utilisation
Deux workflows de github actions sont disponibles:
- un workflow de publication de release qui créera une pull request vers la branche `main` à chaque fois que vous ferez un commit sur la branche main. **pensez à faire des commits conventionnels** *pensez à réglez les autorisation du workflow : paramètres > actions > read and write permissions + allow github action to create PR*
- un workflow de publication de docker qui créera une image docker, cette image sera publiée sur la registry github. (ce workflow est activable manuellement depuis l'onglet actions de votre repository, vous pouvez modifier le fichier `.github/workflows/docker-publish.yml` pour l'activer automatiquement à chaque push sur la branche `main`)

Vous pouvez en ajouter autant que vous voulez, par exemple :
- un workflow de test qui s'activera à chaque push sur la branche `dev`, pour vérifier que votre code est fonctionnel
- un workflow de publication de documentation qui s'activera à chaque push sur la branche `main`, pour publier votre documentation sur github pages
- un workflow d'analyse de secret, afin de vérifier qu'aucun secret n'a été commité dans votre repository (clé d'api, mot de passe, etc...)
- un workflow d'analyse statique de code, afin de vérifier que votre code est conforme aux bonnes pratiques
- un workflow d'analyse de votre container docker, afin de vérifier qu'il ne contient pas de faille de sécurité connue

Veillez à ne pas utiliser des actions "toute faites", non maintenus. Privilégiez les actions officielles, ou forgez la votre à partir de commandes shell. (voir m^me l'execution de scripts python ...)
La documentation des actions est disponible ici : https://docs.github.com/en/actions

La liste des variables d'environnement disponibles est disponible ici : https://docs.github.com/en/actions/reference/environment-variables 
