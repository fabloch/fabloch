# Electron

Electron permet de développer des applications desktop à partir d'une application NodeJS.

Chaque page de l'application desktop est donc une page html faisant appel à du code javascript.

Des librairies propres à NodeJS permettent d'interagir avec le système d'exploitation de la machine,
notamment la gestion de fichiers.

[Debugging Electron application](https://www.sitepoint.com/debugging-electron-application/)

[How to build an Electron app](https://blog.alexdevero.com/electron-app-pt1/)

Sur Github, openlayers-electron montre une intégration d'une page utilisant Openlayers dans une application Electron.
Note: Dans cet exemple, OpenLayers n'est pas accessible depuis le script index.js de l'application.

- [Distribuer une application Electron](electron-distribution.md)

## Tips and Tricks

[La doc complète](https://electronjs.org/docs/all)

### couldn't set selectedTextBackgroundColor from default ()
Parfois, la console peut afficher le message suivant:
```
Electron Helper[1944:91412] Couldn't set selectedTextBackgroundColor from default ()
```
[Couldn't set selectedTextBackgroundColor from default()](https://github.com/electron/electron/issues/4420)
En placant le code suivant dans le HTML, le message n'apparait plus.
```
<style> ::selection { background: white; /* WebKit/Blink Browsers */ } </style>
```

### A propos des icones pour l'application
https://www.christianengvall.se/electron-app-icons/

### Menus

https://electronjs.org/docs/api/menu
Construire les menus d'une appli Electron
http://codaholic.sillo.org/2017/12/02/electron-les-menus/

### Boite de dialogue Fichiers
https://electronjs.org/docs/api/dialog

https://stackoverflow.com/questions/45849190/how-to-show-an-open-file-native-dialog-with-electron

### D'une machine à une autre
Passage d'un projet electron d'un environnement OSX à Windows 10

github clone

```
$ npm install
$ npm run build
```

### Electron dans un environnement Windows
Avec sqlite, l'installation d'un environnement de développement pour une application Electron sous Windows est un peu plus sport. De multiples tentatives ont rempli pas mal d'heures avant d'arriver à une solution convaincante.
[Tout le détail d'une préparation de l'environnement Windows pour Electron](electron-windows)
