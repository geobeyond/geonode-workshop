## Setup GeoNode from sources

Download the code from [GitHub repo](https://github.com/GeoNode/geonode.git):

```bash
(geonode)$ git clone https://github.com/GeoNode/geonode.git
```

Change the working directory into the **geonode** folder:

```bash
(geonode)$ cd geonode
```

Install all required dependencies:

```bash
(geonode)$ pip install -e .
(geonode)$ pip install pygdal==1.11.2.1
```

Setup the custom build of [GeoServer](http://geoserver.org) for GeoNode:

```bash
(geonode)$ paver setup
```

Create the schema, initialize the database and then create the **superuser**:

```bash
(geonode)$ paver sync
(geonode)$ python manage.py createsuperuser
```
