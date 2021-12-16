# TP-1

##### Installer Ansible

dnf install ansible

##### Installer le package Ansible POSIX

dnf install ansible-collection-ansible-posix

## Liste des Repository utilis�s

Repository initial fournit par l'intervenant :
 https://github.com/BastienBalaud/packer-course-bootstrap.git

Repository contenant l'utilitaire � install� sur la machine d�ploy� :
 https://github.com/BastienBalaud/golang-myip.git

Les cl�s SSH de l'intervenant, � ajouter � la machine d�ploy� :
 https://github.com/BastienBalaud.keys

## Les �tapes :

1. Installation GIT
2. Installation GOLANG
3. Installation MAKE
4. Clone du repo Golang-myip
5. Remplacement de la configuration de "server.go" (pour ouvrir le port 80 et non pas 8080)
6. Commande Shell "make" 
7. D�placement du fichier golang.service dans systemd
8. Passage de SElinux en "permissive"
9. Force le systeme � relire sa configuration
10. Configuration du lancement du service GOLANG au d�marrage
11. Ajout des cl�s SSH de l'intervenant

## Explication des �tapes :

[Etape 1-3] Installation des utilitaires n�cessaires � l'utilisation de Golang-myip.

[Etape 4] Installation de Golang-myip

[Etape 5] Remplacement de la configuration de "server.go" pour remplacer la ligne "args.Port = 8080" par "args.Port = 80".

[Etape 6] Utilisation d'une commande shell pour effectuer le "make" de golang-myip.

[Etape 7] Copie du fichier golang.service dans le r�pertoire /etc/systemd/system de la machine d�ploy�.

[Etape 8] Passage du SElinux en permissive pour permettre l'ex�cution du service.

[Etape 9] On force le systeme � relire la configuration pour que le service soit pris en compte.

[Etape 10] On configure le service pour qu'il d�marre en m�me temps que la machine (systemd).

[Etape 11] Ajout des cl�s SSH � la machine en clonant le repo github fournit.
