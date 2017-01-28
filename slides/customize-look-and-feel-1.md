## Customize look and feel

**Change homepage**

Override the index page by editing the HTML within the `template` folder:

```bash
$ cd ~/development/geonode/my_geonode/my_geonode/templates/
$ vi site_index.html
```

Change the main header with custom text

```html
<h1>{% trans "Welcome" %} al GeoNode Workshop of FOSS4G-IT 2017</h1>
```

Restart this custom application and open it up in the browser:

```bash
$ cd ~/development/geonode/my_geonode
$ python manage.py runserver 0.0.0.0:8000
```

