!SLIDE
# Nova

Gère les VMs

Concurrent : Amazon EC2

!SLIDE full

![archi](../architecture/openstack-conceptual-arch-folsom.jpg)

!SLIDE full

![archi](../architecture/openstack-logical-arch-folsom.jpg)

!SLIDE
# Backend

Fonctionnel :

* Xen
* KVM
* Hyper-V

 En développement :

* LXC
* Citrix
* VMware

!SLIDE
# nova-api

Accepte et réponds aux utilisateurs.

Supporte OpenStack Compute API, EC2 API, admin API

Gère les activités d'orchestration et gère la politique.

!SLIDE
# nova-compute

Daemon qui gère la création / destruction des VMs via l'API de l'hyperviseur :

* XenAPI pour XenServer/XCP
* libvirt pour KVM / QEMU
* VMwareAPI pour VMware
* ...

!SLIDE
# nova-volume

Gère la création, attachement / détachement du volume persistent.

Note: Cinder le remplace

!SLIDE
# nova-network

Gère le réseau.

Note : Quantum le remplace.

!SLIDE
# nova-scheduler

Gère les requêtes d'une VM d'une file d'attente et détermine sur quelle machine cela doit tourner.

!SLIDE
# Queue

La file d'attente un hub central pour passer les messages entre les daemons :

* RabbitMQ
* Apache Qpid
* ZeroMQ

!SLIDE
# Base SQL

Gère les états de l'infrastructure :

* Les Type d'instance
* Les instances utilisées
* Les réseaux disponibles
* Les projets

Backend :

* sqlite3
* MySQL
* PostgreSQL

!SLIDE
# console

Nova fournit également une console :

* nova-console
* nova-vncproxy
* nova-consoleauth
