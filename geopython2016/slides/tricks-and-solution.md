## Don't panic!

**Hints and tricks**

Take a look at browser console what is the problem

*Expose the port*

```bash
config.vm.network "forwarded_port", guest: 8080, host: 8080
# forward to the host another port
```

*Pass the cookie with the correct hostname to GeoServer*

```bash
$ sudo vi /usr/share/geoserver/data/security/auth/geonodeAuthProvider/config.xml
# edit the configuration of GeoServer authentication provider
```

Change with this value:

```xml
<baseUrl>http://localhost:8888/</baseUrl>
<!-- base url of geonode web server -->
```

Restart the server:

```bash
$ sudo service tomcat7 restart
# restart Tomcat
```

