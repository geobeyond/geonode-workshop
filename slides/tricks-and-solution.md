## Don't panic!

**Security hints and tricks**

Security in GeoServer is hugely changed with the introduction of **[OAuth2](http://docs.geonode.org/en/master/tutorials/admin/geoserver_geonode_security/)**

*Firstly expose the port to your host machine*

```bash
config.vm.network "forwarded_port", guest: 8080, host: 8080
# forward to the host another port
```

*Set security with the correct GeoNode Base Url to GeoServer*

```bash
$ sudo vi /usr/share/geoserver/data/security/role/geonode\ REST\ role\ service/config.xml
# edit the configuration of geonode REST role service
```

Change with this value:

```xml
<baseUrl>http://localhost:8888/</baseUrl>
<!-- base url of geonode web server -->
```

