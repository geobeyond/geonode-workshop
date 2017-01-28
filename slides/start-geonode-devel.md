## Start GeoNode for development

#### Post setup for migrations

Make migrations and migrate the model if something has gone wrong with:

```bash
(geonode)$ python manage.py makemigrations
(geonode)$ python manage.py migrate
```

#### Run GeoNode application

```bash
# make sure you have stopped you systemwide installation by doing
$ sudo service apache2 stop
$ sudo service tomcat7 stop
(geonode)$ paver start -b 0.0.0.0:8000 # sudo apt-get install openjdk-8-jdk (if not present)
```

Development server is started within the VM at http://0.0.0.0:8000/. In order to access that on your host you have to add a new config line at your *vagrantfile* and reload:

```bash
config.vm.network "forwarded_port", guest: 8000, host: 8000
# forward to the host geonode development port
```
