# Electron

Electron permet de développer des applications desktop à partir d'une application NodeJS.

Chaque page de l'application desktop est donc une page html faisant appel à du code javascript.

Des librairies propres à NodeJS permettent d'interagir avec le système d'exploitation de la machine,
notamment la gestion de fichiers.

[Debugging Electron application](https://www.sitepoint.com/debugging-electron-application/)

Sur Github, openlayers-electron montre une intégration d'une page
utilisant Openlayers dans une application Electron.
Note: Dans cet exemple, OpenLayers n'est pas accessible depuis le script index.js de l'application.


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

### Sqlite3
Il faut construire ce module natif avec les configurations de base d'Electron.

```
$ npm install electron-rebuild
$ ./node_modules/.bin/electron-rebuild -w sqlite3 -p

```

[How to build an Electron app](https://blog.alexdevero.com/electron-app-pt1/)

[Electron app can't find sqlite3 module](https://stackoverflow.com/questions/38716594/electron-app-cant-find-sqlite3-module)
[How to use Sqlite3 in electron](https://stackoverflow.com/questions/32504307/how-to-use-sqlite3-module-with-electron)

[How does `db.serialize` work in `node-sqlite3`](https://stackoverflow.com/questions/41949724/how-does-db-serialize-work-in-node-sqlite3)
[Promise with sqlite3](https://stackoverflow.com/questions/40691884/nodejs-sqlite-why-each-statement-return-no-results)


#### Prepared Statements
```
var sqlite3 = require('sqlite3').verbose();
var db = new sqlite3.Database('data.db');

db.serialize(function() {

  var stmt = db.prepare("INSERT INTO users VALUES (?,?)");
  for (var i = 0; i < 10; i++) {
      stmt.run("user " + i, "email " + i);
  }
  stmt.finalize();

  stmt = db.prepare("SELECT * FROM users WHERE id=?");
  stmt.each(userId, function(err, row) {
      console.log(row.name, row.email);
  }, function(err, count) {
      stmt.finalize();
  });
});
```

## Comment distribuer une application Electron?

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

### A propos des icones pour l'application
https://www.christianengvall.se/electron-app-icons/

### D'une machine à une autre
Passage d'un projet electron d'un environnement OSX à Windows 10

github clone

```
$ npm install
$ npm run build
```

Sur Windows, une erreur possible au début des commandes:
```
Openssl config failed: error:02001003:system library:fopen:No such process
Openssl config failed: error:02001003:system library:fopen:No such process
```
https://github.com/npm/npm/issues/17261

D:\dev\Fabloch\swail-electron>echo %OPENSSL_CONF%
C:\Program Files\PostgreSQL\psqlODBC\etc\openssl.cnf



```
> install-app-deps

   please use as subcommand: electron-builder install-app-deps
   electron-builder version=20.38.5
   rebuilding native production dependencies platform=win32 arch=x64
npm WARN ajv-keywords@3.4.0 requires a peer of ajv@^6.9.1 but none is install
 You must install peer dependencies yourself.

audited 2751 packages in 9.41s
found 0 vulnerabilities
```

npm install sqlite3
Error: "cannot find module node_sqlite3.node"
https://stackoverflow.com/questions/20221825/node-js-says-it-cant-load-sqlite3-module-but-does-anyway

npm install sqlite3 --build-from-source

```
> npm install sqlite3 --build-from-source

 ERR! configure error
 ERR! stack Error: Can't find Python executable "python", you can set the PYT
 env variable.

```


For Windows, you'll want to run in Powershell:
```
rm Env:\OPENSSL_CONF
```
Then remove any out-of-date references to OPENSSL_CONF from your profiles. Usually that's just $PROFILE:

```
edit $PROFILE
```
But you can get the full list with:

```
$PROFILE | select AllUsersAllHosts,AllUsersCurrentHost,CurrentUserAllHosts,CurrentUserCurrentHost | Format-list
```
https://github.com/npm/npm/issues/17261

https://medium.com/how-to-electron/a-complete-guide-to-packaging-your-electron-app-1bdc717d739f

https://github.com/felixrieseberg/windows-build-tools/issues/56
npm --add-python-to-path='true' --debug install --global windows-build-tools

Python 2.7.15
https://www.python.org/downloads/release/python-2715/

Run powershell as administrator

Error

https://github.com/felixrieseberg/windows-build-tools/issues/116
npm install --global --production --verbose windows-build-tools

npm --add-python-to-path='true' --debug install --global windows-build-tools

Error


Just add
%SystemRoot%/system32/WindowsPowerShell/v1.0
to your PATH and you should be good to go

npm --add-python-to-path='true' --debug install --global windows-build-tools

Error
https://github.com/felixrieseberg/windows-build-tools/issues/20
https://github.com/felixrieseberg/windows-build-tools/issues/110
https://github.com/felixrieseberg/windows-build-tools/blob/v2.3.0/src/constants.js#L3

Set Environment Variable
PYTHON_MIRROR=https://www.python.org/ftp/python

https://github.com/felixrieseberg/windows-build-tools/issues/47
https://github.com/felixrieseberg/windows-build-tools/issues/121

Pour installer les windowsbuildtools, il ne faut pas avoir Python 2.7 installé avant.




C:\Python27;C:\Program Files (x86)\NVIDIA Corporation\PhysX\Common;%SystemRoot%\system32;%SystemRoot%;%SystemRoot%\System32\Wbem;%SYSTEMROOT%\System32\WindowsPowerShell\v1.0\;C:\Program Files\dotnet\;D:\Program Files (x86)\Yarn\bin;C:\Program Files (x86)\dotnet\;C:\Program Files\Microsoft SQL Server\130\Tools\Binn\;C:\Program Files\Git\cmd;D:\Program Files\nodejs\;


### Menus

https://electronjs.org/docs/api/menu
Construire les menus d'une appli Electron
http://codaholic.sillo.org/2017/12/02/electron-les-menus/

### Boite de dialogue Fichiers
https://electronjs.org/docs/api/dialog

https://stackoverflow.com/questions/45849190/how-to-show-an-open-file-native-dialog-with-electron
