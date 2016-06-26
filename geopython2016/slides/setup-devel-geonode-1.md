## Setup GeoNode from sources

Download the code from [GitHub repo](https://github.com/GeoNode/geonode.git):

```bash
$ git clone https://github.com/GeoNode/geonode.git
```

Change the working directory into the **geonode** folder:

```bash
$ cd geonode
```

Install all required dependencies:

```bash
$ pip install -e .
```

```bash
$ pip install pygdal==1.11.2.1
```

Setup the custom build of [GeoServer](http://geoserver.org) for GeoNode:

```bash
$ paver setup
```

Create the schema and initialize the database:

```bash
$ paver sync
```

Create the superuser:

```bash
$ python manage.py createsuperuser
```
