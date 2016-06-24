## Troubleshooting and Logs

Run GeoNode application in DEBUG mode:

```bash
$ sudo vi /etc/geonode/local_settings.py
# edit systemwide settings
```
---
```python
DEBUG = TEMPLATE_DEBUG = True
# debug enabled. Need to restart Apache
```


GeoNode log is within apache log

```bash
$ sudo tail -f /var/log/geonode/apache.log
$ sudo tail -f /var/log/apache2/error.log
# apache logs
```

GeoServer log is usually within the data directory `GEOSERVER_DATA_DIR/logs/geoserver.log`

```bash
$ sudo tail -f /usr/share/geoserver/data/logs/geoserver.log
# geoserver logs
```

Tomcat log is useful for tracing any error in GeoServer

```bash
$ sudo tail -f /var/lib/tomcat7/logs/catalina.out
# tomcat logs
```
<!--
PostgreSQL log can be investigated here

```bash
sudo tail -f /var/log/postgresql/postgresql-9.3-main.log
# postgresql logs
``` -->
