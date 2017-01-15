## How to customize GeoNode

Assuming we are using the current stable version **2.4** the customization can be started with the use of [GeoNode skeleton](https://github.com/GeoNode/geonode-project):

Create a new project based on the **same** branch version of your GeoNode:

```bash
(geonode)$ django-admin.py startproject my_geonode --template=https://github.com/GeoNode/geonode-project/archive/2.4.zip -epy,rst
```

Start the project that you have just created:

```bash
(geonode)$ pip install -e my_geonode
(geonode)$ cd my_geonode
(geonode)$ python manage.py syncdb
(geonode)$ python manage.py runserver 0.0.0.0:8000
```

> Remember you have to be in your virtual environment!!!

**If you load again the URL in the browser automagically *GeoNode* is up and running.**
Now it's time to change look and feel or inject new functionalities into GeoNode
