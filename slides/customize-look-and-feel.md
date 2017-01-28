## Customize look and feel

**Change logo**

Override the stylesheet by editing the CSS within the `static` folder:

```bash
$ cd ~/development/geonode/my_geonode/my_geonode/static/css
$ vi site_base.css
```

```css
a.navbar-brand {
    background: transparent url("../img/foss4g_it.png") no-repeat scroll 20px -6px;
    margin: 30px;
    background-size: contain;
}
/* Add a rule for the logo */
```

**Download** the FOSS4G-IT 2017 logo within the `img` folder:

```bash
$ cd ~/development/geonode/my_geonode/my_geonode/static/img/
$ wget http://www.dicca.unige.it/geomatica/foss4git_2017/img/foss4g_it.png
```

**Restart** this custom application and open it up in the browser:

```bash
$ cd ~/development/geonode/my_geonode
$ python manage.py runserver 0.0.0.0:8000
```

