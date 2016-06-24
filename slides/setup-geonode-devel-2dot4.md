## Setup GeoNode 2.4 for development

Once you have entered the virtual environment then from your local versioned repository:

- First reset the setup of the master version:

```bash
(geonode)$ paver reset_hard
```

- Checkout to the branch of version 2.4

```bash
(geonode)$ git checkout -t origin/2.4.x
```

- Then run as before the following commands for dependencies:

```bash
(geonode)$ pip install -e .
(geonode)$ pip install pygdal==1.11.2.1
```
---
```bash
(geonode)$ paver setup
(geonode)$ paver sync
(geonode)$ python manage.py createsuperuser
```

