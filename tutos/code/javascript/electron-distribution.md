# Comment distribuer une application Electron?

- [Officiel](https://electronjs.org/docs/tutorial/application-distribution)
- [Tutoriel en anglais](https://coursetro.com/posts/code/124/Electron-App-Deployment-Tutorial)

```
$ npm install electron-packager --save-dev
```

Modifier le fichier package.json
```
{
  // Other properties removed for brevity

  "scripts": {
    "start": "electron .",
    "package-mac": "electron-packager . --overwrite --platform=darwin --arch=x64 --icon=assets/icons/mac/icon.icns --prune=true --out=release-builds",
    "package-win": "electron-packager . electron-tutorial-app --overwrite --asar=true --platform=win32 --arch=ia32 --icon=assets/icons/win/icon.ico --prune=true --out=release-builds --version-string.CompanyName=<COMPANY NAME> --version-string.FileDescription=CE --version-string.ProductName=\"< YOUR PRODUCT NAME>\"",    
    "package-linux": "electron-packager . electron-tutorial-app --overwrite --asar=true --platform=linux --arch=x64 --icon=assets/icons/png/icon.1024x1024.png --prune=true --out=release-builds"   
  },

  // Other properties removed for brevity
  }
}
```

Puis pour chaque OS:
```
$ npm run package-win    (or package-mac, package-linux)
```

Une erreur comme ci-dessous?
```
CANNOT RUN WITH NODE 10.5.0
Electron Packager requires Node 4.0 or above.
```

Il s'agit d'un problème de comparaison de version dans la librairie.

La solution est ici:
[Cannot run with node 10.15.0](https://github.com/electron-userland/electron-packager/issues/863)
Modifier la version minimale de l'electron-packager dans le fichier package.json
