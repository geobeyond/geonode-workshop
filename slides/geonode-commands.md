## GeoNode commands

**List** all available commands by typing in the shell:

```bash
$ geonode help
# commands are divided in subcommands
```

**Import layers** from folders or files. Supported formats are *Shapefile* and *GeoTiff*:

```bash
$ geonode importlayers --user=geopython --keywords=milan,italy --category=environment,elevation --regions=lombardia --title=tubestops ./data
# in case of massive import these settings will be used for all layers
```

**Update** layers information from GeoServer into GeoNode application:

```bash
$ geonode updatelayers --user=geopython --skip-geonode-registered --store=geopython --workspace=workshop
# update geonode with layer still not registered and from specific workspace and store of GeoServer
```

**Update IP** of local map layers in one command:

```bash
$ geonode updatemaplayerip
# update geonode with layer still not registered and from specific workspace and store of GeoServer
```

**Update Map baselayers** of local maps in one command:

```bash
$ geonode shell
```

```python
>>>from geonode.maps.models import MapLayer
>>>MapLayer.objects.filter(name='osm').update(visibility=False)
>>>MapLayer.objects.filter(name='mapnik').update(visibility=True)
```

