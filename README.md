*note de formation, enrichie par openai*

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

### USE NMAP & WIRESHARK

#### Permet de résoudre les problèmes sur de grands réseaux lorsque plusieurs chemins permettent d'atteindre le même point ou lorsque plusieurs composants intermédiaires (routeurs ou ponts) sont impliqués

#### L'utilitaire de diagnostic TRACERT détermine l'itinéraire vers une destination en envoyant des paquets d'écho ICMP (Internet Control Message Protocol) à la destination.


### Modèle OSI (VOIR NOTE)

#### BASE DU FONCTIONNEMENT D'UN  RÉSEAUX avec le soft Cisco.  [ex: de montage](https://github.com/berru-g/HDF-note/tree/main/Cisco)


##   Le protocole DNS (Domain Name System) 

Est utilisé pour convertir les noms de domaines en adresses IP. Il permet aux ordinateurs de trouver des sites web en utilisant des noms de domaines plutôt que des adresses IP numériques. STP (Spanning Tree Protocol) est un protocole de réseau qui empêche les boucles de se produire dans les réseaux étendus en créant un arbre qui couvre tous les éléments du réseau et en éliminant les liaisons en double. Il est utilisé pour éviter les boucles dans les réseaux Ethernet étendus en sélectionnant un chemin unique pour les données à suivre.

	Changer le fichier "host" = enlever les autorisations dans ce fichier host. 
	 C:\WINDOWS\system32\drivers\etc\hosts

### ICANN - Société pour l'attribution des noms de domaine.

	TLD = (Top-level domain)
	
Les TDL sont les derniers niveaux d'un nom de domaine, comme .com, .org, .edu, etc. Ils indiquent le type d'entité ou l'utilisation du domaine. Par exemple, les noms de domaine avec un TDL .com sont généralement utilisés pour les entreprises commerciales, tandis que les noms de domaine avec un TDL .edu sont réservés aux établissements d'enseignement.

La racine d'un nom de domaine est la partie la plus haute de l'arbre de nom de domaine. Il contient les TDL et les serveurs de nom racine qui sont responsables de l'enregistrement des noms de domaine et de la résolution des noms de domaine en adresses IP. Les serveurs de noms racine sont gérés par l'Internet Corporation for Assigned Names and Numbers (ICANN).


					Root (meme schéma avec chaque tdl)
									
                          .com
                        /    |   \ 
                    example  google  facebook
                      |
                 L2 - www.example.com
                      |
                 L3 - mail.example.com
                      |
                 L4 - support.mail.example.com


**  Ce schéma montre comment les noms de domaine peuvent être organisés en utilisant des niveaux de sous-domaine. Le niveau L2 (www) est ajouté pour créer un sous-domaine spécifique pour les pages web d'un site. Le niveau L3 (mail) est ajouté pour créer un sous-domaine pour les courriels. Enfin, Le niveau L4 (support) est ajouté pour créer un sous-domaine pour les pages d'aide ou de support. **

*Il est important de noter que les niveaux L2, L3, et L4 sont crées par les propriétaires de domaines et n'ont pas de règles strictes. Il est possible de les utiliser à sa guise en fonction de son besoin.*

### protocole DNS

                                Client
                                   |
                                   | Requête DNS pour "example.com"
                                   |
                                   V
                            +--------------+
                            |   Serveur DNS |
                            +--------------+
                                   |
                                   | Recherche de l'enregistrement A correspondant à "example.com"
                                   |
                                   V
                            +--------------+
                            |    TLD Server |
                            +--------------+
                                   |
                                   | Renvoi de l'adresse IP correspondante à "example.com"
                                   |
                                   V
                                Client

* Ce schéma montre comment un client envoie une requête DNS pour un nom de domaine spécifique (example.com) à un serveur DNS local. Le serveur DNS local recherche l'enregistrement A (adresse IP) correspondant à ce nom de domaine dans sa propre base de données ou en demandant à un serveur DNS de niveau supérieur (TLD Server) qui contient l'enregistrement A correspondant pour ce nom de domaine. Enfin, le serveur DNS de niveau supérieur renvoie l'adresse IP correspondante au client.

Il est important de noter que les requêtes DNS peuvent également être gérées par des serveurs de cache, qui mémorisent les réponses DNS récemment demandées pour accélérer les requêtes futures. *

## Exemples de consultation DNS

Pour vérifier l'association entre un nom et une adresse IP, plusieurs commandes sont disponibles suivant les systèmes d'exploitation utilisés.

Par exemple sur Windows la commande [nslookup](https://fr.wikipedia.org/wiki/Nslookup "Nslookup") est disponible via l'invite de commande :

> nslookup www.google.fr
Serveur : Livebox-6370
Address: 192.168.1.1

Réponse ne faisant pas autorité :
Nom : www.l.google.com
Addresses:
         209.85.229.104
         209.85.229.106
         209.85.229.103
         209.85.229.147
         209.85.229.105
         209.85.229.99
Aliases: www.google.fr
          www.google.com

###  TCP

	TCP (Transmission Control Protocol) et UDP (User Datagram Protocol) sont deux protocoles de transport de données utilisés pour établir une connexion de communication entre des ordinateurs sur un réseau.

La principale différence entre TCP et UDP est la manière dont les données sont transmises.

TCP est un protocole de transmission de données fiable qui garantit que les données transmises arrivent à destination dans l'ordre dans lequel elles ont été envoyées, et qu'il n'y a pas de paquets de données manquants ou endommagés. Il utilise des mécanismes de contrôle de flux et de correction d'erreur pour s'assurer que les données arrivent à destination en bon état. En raison de ces caractéristiques, les communications TCP sont généralement plus lentes, mais plus fiables.

UDP, d'autre part, est un protocole de transmission de données non fiable qui ne garantit pas que les données arrivent à destination dans l'ordre dans lequel elles ont été envoyées, ni qu'il n'y a pas de paquets de données manquants ou endommagés. Il ne fournit pas de mécanismes de contrôle de flux ou de correction d'erreur, ce qui signifie que les communications UDP sont généralement plus rapides, mais moins fiables.

**En résumé, TCP est utilisé pour les applications qui nécessitent une transmission fiable des données, tandis que UDP est utilisé pour les applications qui nécessitent une transmission rapide des données, même si cela signifie que certaines données peuvent être perdues.**

## Records resourcing

Les enregistrements de ressources définissent les types de données du système DNS. Les enregistrements de ressources ciblés par RFC 1035 sont stockés en format binaire à l’interne pour une utilisation par le logiciel DNS. [![icon_popup_short.gif](https://www.cisco.com/swa/i/icon_popup_short.gif)](https://www.cisco.com/swa/i/icon_popup_short.gif "icon_popup_short.gif") Ces enregistrements sont toutefois acheminés en format texte sur un réseau pendant qu’ils effectuent des transferts de zone. Ce document aborde certains types d’enregistrements de ressources parmi les plus importants.

### Début de l'autorité

Au niveau supérieur d'un domaine, la base de données de noms doit contenir un enregistrement de début d'autorité (SOA). Cet enregistrement SOA identifie la meilleure source d'informations pour les données du domaine. SOA contient la version actuelle de la base de données DNS, ainsi que divers autres paramètres qui définissent le comportement d'un serveur DNS particulier.

Il doit y avoir exactement un enregistrement SOA pour chaque domaine de serveur de noms (chaque sous-domaine). Cela s'applique aux sous-domaines de IN-ADDR.ARPA (domaines inversés). Une région d'espace de noms qui a une SOA distincte est appelée zone.

Le format de cet enregistrement est affiché dans cette sortie. La valeur indiquée pour les intervalles de temps dans cette SOA est celle recommandée par [RFC 1537](http://www.ietf.org/rfc/rfc1537.txt) [![icon_popup_short.gif](https://www.cisco.com/swa/i/icon_popup_short.gif)](https://www.cisco.com/swa/i/icon_popup_short.gif "icon_popup_short.gif").

> DOMAIN.NAME.    IN      SOA     Hostname.Domain.Name. Mailbox.Domain.Name. (
>                                 1        ;    serial number
>                                 86400    ;    refresh in seconds (24 hours)
>                                 7200     ;    retry in seconds (2 hours)
>                                 2592000  ;    expire in seconds (30 days)
>                                 345600)  ;    TTL in seconds (4 days)
> 
> 
> The SOA record for the fictional foo.edu might look something like this: 
> 
> FOO.EDU.        IN     SOA     FOO.EDU. Joe_Smith.Foo.EDU. (
>                                 910612   ;    serial number
>                                 28800    ;    refresh in 8 hours
>                                 7200     ;    retry in 2 hours
>                                 604800   ;    expire in 7 days
>                                 86400 )  ;    TTL is 1 day



#### Sécuriser un DNS.

Il existe plusieurs moyens de sécuriser un service DNS (Domain Name System), voici quelques-unes des principales méthodes :

1.  Utilisation de protocoles DNS sécurisés : Il existe des protocoles tels que DNS over HTTPS (DoH) et DNS over TLS (DoT) qui peuvent être utilisés pour sécuriser les communications DNS en chiffrant les données transmises.
    
2.  Configuration d'un serveur DNS sécurisé : Il est important de configurer correctement le serveur DNS en utilisant des stratégies de sécurité telles que la restriction de l'accès aux seuls utilisateurs autorisés, l'utilisation de mots de passe forts et la mise à jour régulière des logiciels.
    
3.  Utilisation d'un service de résolution de nom de domaine sécurisé : Il existe des services de résolution de nom de domaine qui peuvent offrir une sécurité supplémentaire en filtrant les demandes de résolution de nom de domaine pour éliminer les demandes malveillantes.
    
4.  Utilisation de la validation DNSSEC : DNSSEC est un protocole de sécurité pour DNS qui permet de vérifier l'intégrité des réponses DNS en utilisant des signatures numériques. Il protège contre les attaques de type cache poisoning.
    
5.  Utilisation d'un firewall : utiliser un firewall pour limiter l'accès à vos serveurs DNS aux seuls IPs nécessaires, cela empêchera les attaques de type amplification DDoS.
    

Il est important de noter que la sécurité ne repose pas sur une seule technique, il est donc important de combiner ces différentes techniques pour obtenir une sécurité optimale. Il est également important de surveiller les journaux de serveur DNS pour détecter les activités malveillantes et de mettre à jour régulièrement les logiciels pour corriger les vulnérabilités.




 


