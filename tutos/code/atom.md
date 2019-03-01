# Atom.io

sudo apt-get install linuxbrew-wrapper

```
On Linux, we rely on libsecret to remember this token (via [keytar](https://github.com/atom/node-keytar)). Do you have a keyring manager installed?
```

git --version
Version 2.17.1

@marcosdsanchez's answer is for Arch (which answers the original question) but I'm on Ubuntu. For git >= 2.11:
```
sudo apt-get install libsecret-1-0 libsecret-1-dev
cd /usr/share/doc/git/contrib/credential/libsecret
sudo make
git config --global credential.helper /usr/share/doc/git/contrib/credential/libsecret/git-credential-libsecret
```

Fait sur ordi de Julien, reboot pour tests, négatif
Appel de la palette de commandes
Recherche de github:Logout
(Comme remarqué dans [Add command and UI to clear saved GitHub token](https://github.com/atom/github/pull/1180/commits/f5a2d6d83349622e6b0218d140f9410078eaa7f0))
Entrée à nouveau de son compte et mot de passe.
Le push marche. 



For git < 2.11:
```
sudo apt-get install libgnome-keyring-dev
cd /usr/share/doc/git/contrib/credential/gnome-keyring
sudo make
git config --global credential.helper /usr/share/doc/git/contrib/credential/gnome-keyring/git-credential-gnome-keyring
```
