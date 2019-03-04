# Python 3

[Source](https://wsvincent.com/install-python3-mac/)

## Installation sur OSX

Prérequis:
- XCode
- Homebrew

### Installation des prérequis

#### Installation XCode

Il faut s'inscrire en tant que [développeur auprès d'Apple](https://developer.apple.com/).

```
$ xcode-select --install
```

#### Installation Homebrew

```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Pour vérifier l'installation de Homebrew
```
$ brew doctor
```

### Installation

```
$ brew install python3
```

## Environnements virtuels

Pour être propre dans la gestion de son installation php,
création d'environnements virtuels pour permettre plusieurs installations de python.

Création d'un répertoire pour recueillir les environnements virtuels
```
$ mkdir ~/.virtualenvs
```

Création d'un nouvel environnement virtuel
```
$ python3 -m venv ~/.virtualenvs/myvenv
```

Pour activer l'environnement virtuel
```
$ source ~/.virtualenvs/myvenv/bin/activate
(myvenv) $
```

Pour désactiver l'environnement virtuel
```
(myvenv) $ deactivate
$
```

Pour voir tous les logiciels installés dans cet environnement

```
$ pip freeze
$
```

[Source](https://wsvincent.com/install-python3-mac/)

## Sur PC
```
```

https://www.python.org/downloads/release/python-372/
