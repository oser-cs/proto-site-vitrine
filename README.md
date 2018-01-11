# proto-site-vitrine

Ceci est le début d'implémentation avec [VueJS](http://vuejs.org) de la maquette de site vitrine. Pour l'instant, seule la page d'accueil est codée, et l'objectif n'est pas de la coder en entier.

## Installation

Vous aurez besoin de `npm` pour installer ce prototype en local.

```bash
# clonez le repo
$ git clone ...

# allez dans le dossier du proto
$ cd proto-site-vitrine

# installez les dépendances
$ npm install

# démarrez le serveur
$ npm run dev
# ou
$ npm start
```

Le serveur sera accessible à l'adresse [http://localhost:8080](http://localhost:8080).

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## Réutilisation pour d'autres usages

TL;DR : si vous cherchez à réutiliser le code de ce proto, regardez dans les fichiers `.vue` du dossier `src/components`. :+1:

Les pages sont décomposées en "composants" chacun définis dans un fichier `.vue`. Les composants se trouvent dans `src/components`. Un fichier `.vue` regroupe à la fois le template HTML, le code Javascript du composant (la déclaration des composants ressemble un peu à ce que fait React) et enfin le style. Pour le style, on utilise SASS, un pré-processeur CSS qui permet d'utiliser des styles imbriqués [et bien d'autres choses](http://sass-lang.com).
