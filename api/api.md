!SLIDE
# 2 formats

* JSON
* XML

!SLIDE
# Exemple

```
$ curl -d '{"passwordCredentials": {"username": "joe",
                                    "password": "shhh"}}'
       -H "Content-type: application/json"
       http://localhost:5000/v2.0/tokens
```

!SLIDE

```
{
  "auth": {
    "token": {
      "expires": "2015-02-05T00:00:00", 
      "id": "999888777666"
    }, 
    "serviceCatalog": {
      "glance": [
        {
          "adminURL": "http://10.0.2.15:9292/v1", 
          "region": "RegionOne", 
          "internalURL": "http://10.0.2.15:9292/v1", 
          "publicURL": "http://10.0.2.15:9292/v1"
        }
      ], 
      "nova": [
        {
          "adminURL": "http://10.0.2.15:8774/v1.1/openstack", 
          "region": "RegionOne", 
          "internalURL": "http://10.0.2.15:8774/v1.1/openstack", 
          "publicURL": "http://10.0.2.15:8774/v1.1/openstack"
        }
      ], 
      "identity": [
        {
          "adminURL": "http://10.0.2.15:5001/v2.0", 
          "region": "RegionOne", 
          "internalURL": "http://10.0.2.15:5000/v2.0", 
          "publicURL": "http://10.0.2.15:5000/v2.0"
        }
      ]
    }
  }
}
```

!SLIDE

```python
import httplib
import json

url = "192.168.10.1:5000"

osuser = "joe"
ospassword = "shhh"

params = '{"auth":{"passwordCredentials":{"username": "admin", "password":"openstack"},
                   "tenantId":"YourTenantIdGoesHere"}}'
headers = {"Content-Type": "application/json"}

conn = httplib.HTTPConnection(url)
conn.request("POST", "/v2.0/tokens", params, headers)

response = conn.getresponse()
data = response.read()
dd = json.loads(data)

conn.close()

apitoken = dd['access']['token']['id']
print "Your token is: %s" % apitoken
```

!SLIDE
# OpenStack API Reference

http://api.openstack.org/api-ref.html

http://docs.openstack.org/api/api-specs.html

!SLIDE
# Python

Tous les services sont écrits en Python, il est donc facile de scripter avec.

!SLIDE
# Binding

* Ruby https://github.com/ruby-openstack/ruby-openstack
* Java https://github.com/woorea/openstack-java-sdk
