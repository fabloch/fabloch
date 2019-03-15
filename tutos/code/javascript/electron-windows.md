# Electron dans un environnement Windows

## Windows, gestion de l'openssl
Sur Windows, une erreur possible au début des commandes:
```
Openssl config failed: error:02001003:system library:fopen:No such process
Openssl config failed: error:02001003:system library:fopen:No such process
```
https://github.com/npm/npm/issues/17261

```
> echo %OPENSSL_CONF%
```


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

Pour installer les windowsbuildtools, il ne faut pas avoir Python 2.7 installé avant.


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
```
npm --add-python-to-path='true' --debug install --global windows-build-tools
```

Python 2.7.15
https://www.python.org/downloads/release/python-2715/

Run powershell as administrator

Error

https://github.com/felixrieseberg/windows-build-tools/issues/116
npm install --global --production --verbose windows-build-tools

npm --add-python-to-path='true' --debug install --global windows-build-tools

Error

Just add %SystemRoot%/system32/WindowsPowerShell/v1.0 to your PATH and you should be good to go

npm --add-python-to-path='true' --debug install --global windows-build-tools

Error
https://github.com/felixrieseberg/windows-build-tools/issues/20
https://github.com/felixrieseberg/windows-build-tools/issues/110
https://github.com/felixrieseberg/windows-build-tools/blob/v2.3.0/src/constants.js#L3

Set Environment Variable
PYTHON_MIRROR=https://www.python.org/ftp/python

https://github.com/felixrieseberg/windows-build-tools/issues/47
https://github.com/felixrieseberg/windows-build-tools/issues/121
