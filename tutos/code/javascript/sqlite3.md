# Sqlite3 en Jacascript

Il faut construire ce module natif avec les configurations de base d'Electron.

```
$ npm install electron-rebuild
$ ./node_modules/.bin/electron-rebuild -w sqlite3 -p

```

- [Electron app can't find sqlite3 module](https://stackoverflow.com/questions/38716594/electron-app-cant-find-sqlite3-module)
- [How to use Sqlite3 in electron](https://stackoverflow.com/questions/32504307/how-to-use-sqlite3-module-with-electron)

- [How does `db.serialize` work in `node-sqlite3`](https://stackoverflow.com/questions/41949724/how-does-db-serialize-work-in-node-sqlite3)
- [Promise with sqlite3](https://stackoverflow.com/questions/40691884/nodejs-sqlite-why-each-statement-return-no-results)

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
