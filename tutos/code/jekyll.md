# Jekyll sur votre machine

# Pré-requis

Installation de Bundler et Jekyll
```
sudo gem install bundler jekyll

```

## Pour créer un nouvel environnement jekyll
```

jekyll new monsite
cd my-awesome-site

```
## Pour créer un site Jekyll à partir d'un répertoire existant

Créer un fichier Gemfile et y placer les deux lignes suivantes:

```
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins

```

Puis exécuter la commande :

```
$ bundle install

```

## Pour lancer le site en local
Aller dans le répertoire du site

```
$ bundle exec jekyll serve
```
