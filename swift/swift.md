!SLIDE
# Swift 

Système de stockage évolutif & redondant

Accessible uniquement avec une API (pas un FS)

Les données sont des objets

Concurrent : Amazon S3

!SLIDE full

![archi](../architecture/openstack-conceptual-arch-folsom.jpg)

!SLIDE full

![archi](../architecture/openstack-logical-arch-folsom.jpg)

!SLIDE
# Objectif

Disposer d'un stockage redondant (écriture sur plusieurs
disques / machines).

!SLIDE
# Elasticité

Par ajout de serveurs (matériel standard).

!SLIDE
# En cas d'erreur

Swift gère la réplication.

!SLIDE
# proxy-server

Gère les demandes via l'API ou HTTP.

Accpète les upload, modification ou création de conteneur.

!SLIDE
# Cache externe

Peut utiliser memcache.

!SLIDE
# replication services

* auditor
* updater
* reaper
