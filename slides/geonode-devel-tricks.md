## Start GeoNode for development

#### Tricks

If the version of Java is not upward compatible with GeoServer (i.e.: java7 vs java8):

```bash
(geonode)$ sudo apt-get purge --remove openjdk*
(geonode)$ sudo add-apt-repository ppa:webupd8team/java
(geonode)$ sudo apt-get update
(geonode)$ sudo apt-get install oracle-java8-installer
```
