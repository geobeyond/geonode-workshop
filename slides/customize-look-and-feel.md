## Customize look and feel

### Change logo

Override the stylesheet by editing the CSS within the `static` folder:

```bash
$ cd ~/devel/my_geonode/my_geonode/static/css
$ vi site_base.css
```

Add a rule for the logo

```css
.navbar-brand {
    width: 150px;
    height: 50px;
    background: transparent url("../img/nwwpy3.png") no-repeat scroll 15px 0px;
}
```

Download the GeoPython logo within the `img` folder:

```bash
$ cd ~/devel/my_geonode/my_geonode/static/img
$ wget http://www.geopython.net/assets/img/nwwpy3.png
```

Restart this custom application and open it up in the browser:

```bash
$ cd ~/devel/my_geonode
$ python manage.py runserver 0.0.0.0:8000
```

