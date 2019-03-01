# javascript

Mesurer le temps
- [How to measure time](https://stackoverflow.com/questions/313893/how-to-measure-time-taken-by-a-function-to-execute)

## Chaîne de caractères
Un classique, le remplacement d'une chaine de caractères
- [string.replace all occurrences](https://stackoverflow.com/questions/21162097/node-js-string-replace-doesnt-work)

https://stackoverflow.com/questions/41298164/how-to-remove-single-and-double-quotes-at-both-ends-of-a-string


## Les tableaux et les dictionnaires
L'objet javascript, un tableau, un dictionnaire
- [How to create dictionary](https://stackoverflow.com/questions/7196212/how-to-create-dictionary-and-add-key-value-pairs-dynamically)
- [How to do associative array hashing](https://stackoverflow.com/questions/1208222/how-to-do-associative-array-hashing-in-javascript)

Accéder à une partie d'un tableau
https://stackoverflow.com/questions/7538519/how-to-get-subarray-from-array

Itérer sur un dictionnaire
https://stackoverflow.com/questions/34913675/how-to-iterate-keys-values-in-javascript

Tester la longueur d'un dictionnaire {}
https://stackoverflow.com/questions/3337367/checking-length-of-dictionary-object
```
var length = Object.keys(dictionary).length
```

https://stackoverflow.com/questions/12623272/how-to-check-if-a-string-array-contains-one-string-in-javascript
https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Objets_globaux/Set/entries
https://stackoverflow.com/questions/1042138/how-to-check-if-function-exists-in-javascript
https://stackoverflow.com/questions/43642729/calling-a-method-from-another-method-in-the-same-class?rq=1
https://stackoverflow.com/questions/32556299/call-javascript-prototype-method-from-another
https://stackoverflow.com/questions/1098040/checking-if-a-key-exists-in-a-javascript-object
https://stackoverflow.com/questions/34913675/how-to-iterate-keys-values-in-javascript
https://stackoverflow.com/questions/3010840/loop-through-an-array-in-javascript
https://stackoverflow.com/questions/175739/built-in-way-in-javascript-to-check-if-a-string-is-a-valid-number
https://stackoverflow.com/questions/281264/remove-empty-elements-from-an-array-in-javascript

## Graphes

### algorithmes de référence
- [Javascript algorithms](https://github.com/trekhleb/javascript-algorithms)

### npath, fast path finding
[Path finding library](https://www.reddit.com/r/javascript/comments/71k0nr/i_made_a_very_fast_path_finding_library_what_do/)

- [ngraph.graph](https://github.com/anvaka/ngraph.graph)
- [ngraph.path](https://github.com/anvaka/ngraph.path)


### node-dijkstra

Installation
```
npm install node-dijkstra
```

Utilisation
```
const Graph = require('node-dijkstra')

const route = new Graph()

route.addNode('A', { B:1 })
route.addNode('B', { A:1, C:2, D: 4 })
route.addNode('C', { B:2, D:1 })
route.addNode('D', { C:1, B:4 })

route.path('A', 'D')
```
