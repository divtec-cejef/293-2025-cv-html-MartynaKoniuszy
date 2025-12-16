## A) Corriger la structure du document (tout doit être dans `<body>`)
- Vous avez du contenu (image + menu) placé avant la balise `<body>`
- Veuillez déplacer ce contenu à l’intérieur du `<body>`

## B) Ajouter Normalize.css et Main.css (en local)
- Veuillez ajouter `normalize.css` en local dans `./css/normalize.css`
- Veuillez créer/utiliser `./css/main.css`
- Et les lier dans le `<head>` :
```
<link rel="stylesheet" href="./css/normalize.css">
<link rel="stylesheet" href="./css/main.css">
```

## C) Favicons : à la racine et référencés avec `./`
- Vos favicons sont dans `favicon_io/` et référencés sans `./`
- Veuillez mettre les favicons à la racine du projet et les référencer avec `./`
- Exemple :
```
<link rel="icon" href="./favicon.ico">
```

## D) Images : doivent être dans `img/`
- Votre image est dans `favicon_io/`
- Veuillez placer vos images dans `./img/` et corriger les chemins

## E) Navigation : corriger les ancres (`id`)
- Votre menu pointe vers `#experience`, `#competence`, `#formation`
- Mais vos titres n’ont pas ces `id`
- Veuillez ajouter les `id` sur les titres `<h2>` (ou sur des `<section>`)
- Exemple :
```
<h2 id="experience">Mon expérience</h2>
<h2 id="competences">Mes compétences</h2>
<h2 id="formation">Ma formation</h2>
```

## F) Footer
- Vous pouvez utiliser ce code pour avoir le logo Copyright `&copy;2025`
- Exemple :
```
<footer>
  &copy;2025 - Martyna Koniuszy |
  <a href="mailto:martyna.koniuszy@divtec.ch">martyna.koniuszy@divtec.ch</a>
</footer>
```

## Autres
- Description dans la balise `meta` dans `head`
- l'image doit être cliquable et ouvrable dans un nouvel onglet. Entourez une balise `<img>` d'une balise `<a>`, et spécificez l'attribut `target="_blank"` dans la balise `<a>`. N'oubliez pas de spécifiez aussi la source `src `de l'image dans la balise `<a>` (donc, le chemin vers l'image) 
