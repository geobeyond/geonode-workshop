## Start GeoNode for development

#### Post setup for migrations

Make migrations

```bash
(geonode)$ python manage.py makemigrations
```

Migrate with:

```bash
(geonode)$ python manage.py migrate
```

#### Run GeoNode application

```bash
(geonode)$ paver start -b 0.0.0.0:8000
```

Development server is started within the VM at http://0.0.0.0:8000/. In order to access that on your host you have to add a new config line at your vagrantfile and reload:

```bash
config.vm.network "forwarded_port", guest: 8000, host: 8000
# forward to the host geonode development port
```
