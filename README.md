## Commandes de base utiles :

### Sous Win, Linux donc powershell:

    ping : vérifie la connectivité réseau avec une adresse IP ou un nom d'hôte
    tracert : trace le chemin d'un paquet à travers les différents routeurs jusqu'à sa destination
    nslookup : affiche les informations DNS pour un nom d'hôte spécifique
    ipconfig : affiche la configuration IP de l'ordinateur
    netstat : affiche les statistiques de connexion réseau actuelles
    tasklist : affiche la liste des processus en cours d'exécution
    taskkill : termine un processus en cours d'exécution en utilisant son nom ou son ID de processus.
    net user : permet de gérer les comptes utilisateurs sur un ordinateur ou un domaine.
    net group : permet de gérer les groupes d'utilisateurs sur un ordinateur ou un domaine.
    net share : permet de gérer les partages réseau sur un ordinateur.
	
### Sous Linux:

	top: affiche les processus utilisant le plus de ressources en temps réel
	free: affiche la mémoire libre et utilisée sur le système
	df: affiche l'utilisation de l'espace disque
	du: affiche l'utilisation de l'espace disque pour un répertoire spécifique
	tail: affiche les dernières lignes d'un fichier
	grep: recherche des chaînes de caractères dans un fichier ou dans la sortie d'une commande.
	

## Automatiser l'installation d'un logiciel sous Linux. Voici quelques exemples :

    Utiliser un script d'installation : vous pouvez créer un script qui automatise toutes les étapes d'installation, comme télécharger les fichiers nécessaires, configurer les paramètres, etc.

    Utiliser un gestionnaire de paquet : les systèmes d'exploitation Linux ont généralement un gestionnaire de paquet intégré, comme apt pour Ubuntu ou yum pour Red Hat, qui peut automatiser le processus d'installation.

    Utiliser Ansible : Ansible est une plate-forme de gestion de configuration open source qui permet de gérer et automatiser les déploiements de logiciels sur plusieurs serveurs.

Les gestionnaires de paquet sont des outils intégrés à la plupart des systèmes d'exploitation Linux qui permettent d'installer, désinstaller et mettre à jour des logiciels de manière automatisée. Les commandes de base pour utiliser un gestionnaire de paquet sont généralement similaires entre les différents systèmes d'exploitation. Voici quelques exemples courants :

    Pour installer un logiciel :

    Sur Ubuntu et Debian, utilisez la commande apt install <nom_du_paquet>
    Sur Red Hat et Fedora, utilisez la commande yum install <nom_du_paquet>

    Pour mettre à jour un logiciel :

    Sur Ubuntu et Debian, utilisez la commande apt update puis apt upgrade
    Sur Red Hat et Fedora, utilisez la commande yum update

    Pour désinstaller un logiciel :

    Sur Ubuntu et Debian, utilisez la commande apt remove <nom_du_paquet>
    Sur Red Hat et Fedora, utilisez la commande yum remove <nom_du_paquet>

Il est important de noter que les noms des paquets peuvent varier.


## Installer une machine virtuelle dans [VirtualBox](https://www.virtualbox.org/) sur un PC Windows:

    Téléchargez et installez VirtualBox sur votre PC Windows.

    Créez une nouvelle machine virtuelle en cliquant sur "Nouveau" dans le menu principal de VirtualBox.

    Sélectionnez le système d'exploitation que vous souhaitez installer sur la machine virtuelle, puis cliquez sur "Suivant".

    Allouez la quantité de mémoire vive (RAM) que vous souhaitez utiliser pour la machine virtuelle, puis cliquez sur "Suivant".

    Créez un disque dur virtuel pour la machine virtuelle, puis cliquez sur "Suivant".

    Sélectionnez le fichier d'installation de votre système d'exploitation, puis cliquez sur "Démarrer" pour lancer l'installation.

    Suivez les instructions à l'écran pour installer le système d'exploitation sur la machine virtuelle.

Il est important de noter que vous aurez besoin d'une copie légale de système d'exploitation pour installer dans la virtualbox.

Si vous rencontrez des problèmes lors de l'installation, vous pouvez consulter la documentation de VirtualBox. Chercher sur le net ou la solution à toute vos question, [Openai](https://chat.openai.com/), le chat intelligent.



## Réseaux (notes)

    cisco packet tracer

### Les réseaux sous WIN 10

#### 5 Classes [de A à E](https://learn.microsoft.com/fr-fr/troubleshoot/windows-client/networking/tcpip-addressing-and-subnetting)

 - Tester un réseaux sur plusieurs machines virtuel et vérifier leurs connexion via ping.

### Ping
| net id | host id |
|--|--|
|192.168.1.  |  44  |

### CMD

#### Lister les interfaces sur le réseaux

    netsh interface ipv4 show interface
    
#### Voir la Configuration pour l'interface

    netsh interface ipv4 show config 5
    
#### Attribuer une nouvelle adress ipv4

     netsh interface ipv4 set address name=6 static 10.0.1.3 255.255.255.0


#### Redonner l'adresse de base

    netsh interface ipv4 set address name=6 dhcp


####  Voir ses ID et son réseaux
	ipconfig

#### Voir les IP sur son wifi
	arp -a

#### Envoie un mess sur un PC de son réseaux
	msg */server:192.168.1.19 tu_recoit_ce_message

#### Server adress
	nslookup

#### Permet tout d'abord de connaître l'état des ports et des connexions sur votre machine. (fermer tte fenetre sur son pc)
	netstat 

### NMAP

#### Permet de résoudre les problèmes sur de grands réseaux lorsque plusieurs chemins permettent d'atteindre le même point ou lorsque plusieurs composants intermédiaires (routeurs ou ponts) sont impliqués

#### L'utilitaire de diagnostic TRACERT détermine l'itinéraire vers une destination en envoyant des paquets d'écho ICMP (Internet Control Message Protocol) à la destination.


### Modèle OSI

#### BASE DU FONCTIONNEMENT D'UN [RÉSEAUX](https://github.com/berru-g/HDF-note/tree/main/Cisco) avec le soft Cisco. (voirpdf oyokai)


##  DNS

#### protocole permettant les échanges avec autorisation

	Changer le fichier "host" = enlever les autorisations dans ce fichier host. 

#### C:\WINDOWS\system32\drivers\etc\hosts















