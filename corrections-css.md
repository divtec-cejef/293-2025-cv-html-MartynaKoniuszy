## A) Stockez vos fichiers css dans un dossier `/css`
C'est plus pratique pour organiser plusieurs fichiers CSS.

Dans le HTML vous avez actuellement :
```

<link rel="stylesheet" href="main.css">
```

Si le fichier est dans un dossier `css/`, il faut :
```

<link rel="stylesheet" href="./css/main.css">
```

---

## B) Favicon : chemin incorrect

Actuellement :
```

<link rel="icon" href="./favicon.ico/favicon-16x16.png">
```

Ça ressemble à un dossier “favicon.ico”, ce qui est bizarre (un `.ico` est normalement un fichier, pas un dossier).

À corriger (consigne : favicon à la racine avec `./`) :

* si vous avez `favicon.ico` à la racine :
```

<link rel="icon" href="./favicon.ico">
```

Ou si vous utilisez un PNG à la racine :
```

<link rel="icon" type="image/png" href="./favicon-16x16.png">
```

---

## C) Ajouter `em` et `rem` (exigence de l’exercice)

Vous avez déjà des tailles en `px` ✅
Il manque :

* une taille en `em`
* une taille en `rem`

Exemples :
```
body {
font-size: 1rem; /* rem */
}

nav a {
font-size: 1.1em; /* em */
}
```

💡 *L’exercice veut vous faire pratiquer les unités relatives.*

> *`em` dépend du parent, `rem` dépend de la racine.*

---

## D) Ajouter une image de fond (background-image)

Vous avez seulement une couleur de fond :
```
background-color: #f6f2f8;
```

À ajouter (exemple simple) :
```
body {
background-image: url("./img/background.jpg");
background-repeat: no-repeat;
background-size: cover;
background-position: center;
}
```

💡 *Une image de fond se met en CSS pour séparer contenu et décoration.*

> *HTML = structure, CSS = style.*

---

## E) Ajouter une police personnalisée avec `@font-face`

Vous utilisez `Roboto` et `Lato`, mais elles ne sont pas importées, et il n’y a pas de `@font-face`.

À corriger :

* télécharger une police (woff2) et la mettre dans `./fonts/`
* puis :
```
  @font-face {
  font-family: "MaPolice";
  src: url("../fonts/mapolice.woff2") format("woff2");
  font-weight: 400;
  font-style: normal;
  }

body {
font-family: "MaPolice", Arial, sans-serif;
}
```

💡 *Sans import, “Roboto/Lato” dépend de ce que l’ordinateur a déjà.*

> *Avec `@font-face`, vous garantissez le rendu partout.*

---

## F) Image dans `img/` : le logo doit respecter la consigne

Votre logo est dans :
```
./favicon_io/favicon-32x32.png
```

Consigne : les images dans `img/`.

À corriger :

* déplacer le logo dans `./img/`
* puis mettre à jour les chemins :
```

  <a href="./img/logo.png" target="_blank" rel="noopener noreferrer">
  <img src="./img/logo.png" alt="Logo" class="logo">

</a>
```

💡 *Un dossier `img/` clarifie où sont toutes les images.*

> *Organisation = plus simple à corriger et à relire.*
