# CMW---TheSimpleWhite

Thème pour craftmywebsite 2.0 

Ce thème fonctionne sous le Framework Tailwindcss.

Réaliser par Zomblard imaginé par PinglsDzn

https://craftmywebsite.fr/

## ----------

# Installation de tailwind

## 1 - Commandes
**Run** : `npm init -y `

**Run** : `npm install -D tailwindcss postcss-cli autoprefixer`

**Run** : `npx tailwindcss init -p`

## 2 - Créer dossier et fichiers
public => index.html

src => tailwind.css

## 3 - Dans tailwind.css
**Ajouter** 
```
@tailwind base;
@tailwind components;
@tailwind utilities;
@layer base {
}
@layer components {
}
```

## 3 - Build
**Ajouter** dans le package.json : script => 
``"build": "postcss -w src/tailwind.css -o public/assets/style.css"``

**Run** : ``npm run build``

## 4 - Configuration de tailwind
**Ajouter** dans tailwind.config.js : 

```
module.exports = {
  content: [
    './public/*.{html,js}',
  ],
```

**Run** : `npm run build`

## 5 - Installation des component daisyui
**Run** :``npm i daisyui``

dans tailwind.conf.js rajouter >

```
module.exports = {
  //...
  plugins: [require("daisyui")],
}
```

## 6 - Page index de test

```
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title></title>
    <meta name="description" content="">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="assets/style.css">
    <script src="https://kit.fontawesome.com/eced519d56.js" crossorigin="anonymous"></script>

</head>

<body>
    <div class="text-green-900 uppercase text-center font-extrabold">Si ce texte est centré vert et gras alors </div>
    <div class="text-green-900 uppercase text-center font-extrabold">TailWinds est pret !</div>
</body>
</html>
```
