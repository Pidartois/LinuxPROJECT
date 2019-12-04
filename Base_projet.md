# Descriptions des demandes :
*Contexte client à ne pas prendre en compte, nous sommes ici pour prendre du plaisir/s'entrainer sur des technos qui pourront
nous être utile*

## Entrée technique à prendre en compte 
_Infra en 2 partie LAN/WAN :_
* __Infra LAN :__
  * DNS : serveur ayant pour but de faire les résolution DNS sur le réseau Local entreprise
  * Web : Demande WordPress préconisation Léo : Wekan
  * BDD : à mettre en place pour gérer le service WEB
  * Serveur annuaire : permettra l'authentification sur le serveur
  * Serveur pour les sauvegardes
  * Reverse proxy pour accéder au service Web
  * Aucun serveur du réseau local n'a directement accès a internet, les dépots seront stockés sur un serveur qui gérera le cache ( à configurer dans les sources.list des différents serveurs)
  * Outil de provisionnement
* __Infra WAN :__
  * Passerelle de sortie vers itnernet
  * Serveur d'externalisation de sauvegarde (facultatif)
* __Supervision :__
  * Solution capable de superviser la partie LAN/WAN (pas des terminaux)
  * Métriques
  * Alertes
  * Automatisation d'actions mineures (facultatif) 
* __Sécurisation :__
  * _Mettre en place une solution permettant la sécurisation des éléments suivants :_
  * LDAP
  * DNS
  * HTTP
  * BDD

### Techno choisit pour à mettre en place pour le projet Linux

Ici je détail les différentes techno que nous allons étudier/mettre en place pour ce labo
* __Minimum attendu :__
  * OS : CentOS 7 1810
  * DNS  : [__PowerDNS__](https://doc.ubuntu-fr.org/pdns)
  * LDAP : [__OpenLDAP__](https://guide.ubuntu-fr.org/server/openldap-server.html)
  * DHCP :
  * IPAM : [__PHP IPAM__](https://phpipam.net/news/tag/guide/) ou [__NETBOX__](https://computingforgeeks.com/how-to-install-netbox-on-centos-7-with-apache-and-supervisord/)
  * BDD : [__MariaDB__](https://linuxize.com/post/install-mariadb-on-centos-7/), même si [__Postgre__](https://www.hostinger.com/tutorials/how-to-install-postgresql-on-centos-7/) est de plus en plus demandé en entreprise
  * WEB : [__Nginx__](https://www.cyberciti.biz/faq/how-to-install-and-use-nginx-on-centos-7-rhel-7/) avec [__Wekan__](https://computingforgeeks.com/install-wekan-kanban-on-centos-7-nginx-letsencrypt/)
  * NFS : NFS Utils 
  * SSH (serveur de rebond) :
  * Sauvegarde : Script créé en cours et si logiciel on peut utiliser [__Borgbackup__](https://borgbackup.readthedocs.io/en/stable/installation.html)
  * Gestion de configuration :

* __Services optionnels :__
  * FAil2ban
  * Reverse Proxy
  * OSSEC
  * Supervision/métrologie
  * Ansible
  * SpaceWalk
  * Docker
  
## Carac des VMs

Chaque VM contient 1 coeur, 1go de ram et 80go de DD
