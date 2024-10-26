# nautilusSrcDoc

Dépot contenant les sources de la documentation du projet Nautilus : https://github.com/gaelle8278/SpringAngularNautilus

Ces sources sont produites grâce au framework Material For MkDocs https://squidfunk.github.io/mkdocs-material/ 

## Publication

Le site produit est publié sur la page Github du projet.

2 possibilités : 

- soit faire un workflow github utilisant la commande `mkdocs gh-deploy`, fournit par MkDocs pour publier le site sur une page GitHub
=> cela build les sources et les  pousse le site produit sur la branche gh-pages du dépot. 
Il faut donc une branche gh-pages dédiée dans le dépot et il faut que le dépot soit configuré pour que la page GitHub du projet soit publiée à partir de la branche gh-pages
Sources :
	- https://squidfunk.github.io/mkdocs-material/publishing-your-site/#github-pages
	- https://www.mkdocs.org/user-guide/deploying-your-docs/#project-pages

- soit faire un workflow github qui publie le site directement sur l'environnement github-page à partir des sources présentes sur la branche main du dépot (option choisit)
=> tout est "transparent" = le site est build sur un runner/vm GitHub puis directement publié sur le serveur des GitHub Pages

NB: la branche gh-pages existe suite au test de la première option. Elle est gardée pour exemple de ce que produit la commande `mkdocs build`

Voir les fichiers de workflow pour exemple des 2 options : 
- doc-deployment.yaml utilise la commande fournit par mkdocs
- direct-deploy-to-pages.yaml utilise des actions github pour construire le site et le publier directement en tant que Page GitHub du projet
