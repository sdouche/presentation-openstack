!SLIDE
# Cinder

Fournit une unité de stockage persistente.

Concurrent : Amazon Elastic Block Store (EBS)

!SLIDE full

![archi](../architecture/openstack-conceptual-arch-folsom.jpg)

!SLIDE full

![archi](../architecture/openstack-logical-arch-folsom.jpg)

!SLIDE
# Cinder

Gestion des snapshots :

* Backup / restore
* Image pour un nouveau volume

!SLIDE
# cinder-api

Gère les requêtes vers cinder-volume

!SLIDE
# cinder-volume

Gère les états des volumes.

!SLIDE
# Support Horizon

- Création / effacement
- Liste

!SLIDE
# Backend

Abstraction de la technologie de stockage :

- LVM
- Ceph
- NetApp
- Nexenta
- SolidFire
- IBM Storwize
