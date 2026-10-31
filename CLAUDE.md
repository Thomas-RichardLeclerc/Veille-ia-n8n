# Veille IA automatisée

Workflow n8n de veille quotidienne : collecte RSS, filtrage, résumé par un modèle de langage, envoi sur Discord.

## Contraintes

* Aucun secret dans le dépôt. Les clés vivent dans les credentials n8n, l'URL du webhook dans une variable d'environnement.
* Le fichier `workflows/veille.json` est un export de n8n. Il ne se modifie pas à la main : on modifie dans n8n, on réexporte, on remplace.

## Workflow Git

* Jamais de commit direct sur `main`.
* Une issue, puis une branche, puis une pull request qui ferme l'issue avec `Closes #n`.
* Après le merge : supprimer la branche sur le serveur, en local, puis `git fetch --prune`.

## Langue

* Répondre en français. 
