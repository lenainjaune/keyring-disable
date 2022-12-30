RO en attente de la fin de migration














































# keyring disable HOWTO
Tout ce qu'il faut savoir sur la désactivation du porte clé sous Linux

Contexte : quand on utilise l'autologin, le porte clé ne se déverrouille pas puisque c'est le mdp entré manuellement lors du login qui permet de déverrouiller. Il en résulte que le lancement de certaines applications "à risques" (telle remmina), afficheront cette demande de mdp pour déverrouiller avant d'utiliser l'application. Ce qui sera ennuyeux pour un utilisateur occasionnel qui ne connait pas le mdp et qui veut juste utiliser le PC.

Nota : pour une raison qui m'échappe apparemment on peut annuler cette demande de mdp pour accéder directement à l'application

La solution que j'ai trouvé par tests, c'est de supprimer (ou renommer) le dossier du porte clé :
```sh
user@host:~$ mv $HOME/.local/share/keyrings/ $HOME/.local/share/keyrings.bkp
```
