!SLIDE
# Offres encore jeunes

Démarrage ~mi-2012.

!SLIDE
# Plusieurs fournisseurs disponibles

* Rackspace
* HP
* eNovance
* Metacloud
* Dreamhost (beta)

!SLIDE
# Exemple avec Rackspace

Facile et rapide

!SLIDE
# Création du compte

http://mycloud.rackspace.com 

!SLIDE
# Installation du client
```
$ sudo pip install rackspace-novaclient
```

!SLIDE
# Configuration

```
$ sudo pip install rackspace-novaclient
export OS_AUTH_URL=https://identity.api.rackspacecloud.com/v2.0/
export OS_AUTH_SYSTEM=rackspace
export OS_REGION_NAME=DFW
export OS_USERNAME=<username>
export OS_TENANT_NAME=<tenant_id>
export NOVA_RAX_AUTH=1
export OS_PASSWORD=<api_key>
export OS_PROJECT_ID=<tenant_id>
export OS_NO_CACHE=1
```

!SLIDE
# C'est parti !

```
$ nova credentials
$ nova image-list
```

!SLIDE
# Librairies Python

```
pip install pyrax

```

!SLIDE
# Utilisation

```python
import pyrax
pyrax.set_credential_file("/path/to/credential/file")
cs = pyrax.cloudservers
print cs.servers.list()
```
