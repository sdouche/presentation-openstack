!SLIDE
# Glance

Stockage, découverte, enregistrement et distributions des images.

Concurent : Amazon AMI catalog

!SLIDE full

![archi](../architecture/openstack-conceptual-arch-folsom.jpg)

!SLIDE full

![archi](../architecture/openstack-logical-arch-folsom.jpg)

!SLIDE
# glance-api

Gère les requêtes de découverte, upload et download.

!SLIDE
# glance-registry

Gère les métadonnées des images.

!SLIDE
# Base de données

Enregistrement dans une SGBD :

* MySQL
* PostgreSQL
* ...

!SLIDE
# Format disque 

- raw
- vhd
- vmdk
- vdi
- iso
- qcow2
- aki, ari, ami

!SLIDE
# Backend

- Swift
- Cepth
- Amazon S3
- RADOS
- HTTP
