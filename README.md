# TP-1

##### Installer Ansible

dnf install ansible

##### Installer le package Ansible POSIX

dnf install ansible-collection-ansible-posix

## Liste des Repository utilisés

Repository initial fournit par l'intervenant :
 https://github.com/BastienBalaud/packer-course-bootstrap.git

Repository contenant l'utilitaire à installé sur la machine déployé :
 https://github.com/BastienBalaud/golang-myip.git

Les clés SSH de l'intervenant, à ajouter à la machine déployé :
 https://github.com/BastienBalaud.keys

## Les étapes :

1. Installation GIT
2. Installation GOLANG
3. Installation MAKE
4. Clone du repo Golang-myip
5. Remplacement de la configuration de "server.go" (pour ouvrir le port 80 et non pas 8080)
6. Commande Shell "make" 
7. Déplacement du fichier golang.service dans systemd
8. Passage de SElinux en "permissive"
9. Force le systeme à relire sa configuration
10. Configuration du lancement du service GOLANG au démarrage
11. Ajout des clés SSH de l'intervenant

## Explication des étapes :

[Etape 1-3] Installation des utilitaires nécessaires à l'utilisation de Golang-myip.

[Etape 4] Installation de Golang-myip

[Etape 5] Remplacement de la configuration de "server.go" pour remplacer la ligne "args.Port = 8080" par "args.Port = 80".

[Etape 6] Utilisation d'une commande shell pour effectuer le "make" de golang-myip.

[Etape 7] Copie du fichier golang.service dans le répertoire /etc/systemd/system de la machine déployé.

[Etape 8] Passage du SElinux en permissive pour permettre l'exécution du service.

[Etape 9] On force le systeme à relire la configuration pour que le service soit pris en compte.

[Etape 10] On configure le service pour qu'il démarre en même temps que la machine (systemd).

[Etape 11] Ajout des clés SSH à la machine en clonant le repo github fournit.
