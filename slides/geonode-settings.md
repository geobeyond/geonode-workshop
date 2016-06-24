## GeoNode settings

Everything is configurable within the systemwide settings file `/etc/geonode/local_settings.py` and can override `/usr/local/lib/python2.7/dist-packages/geonode/settings.py`

```python
# -*- coding: utf-8 -*-
import os
import geonode

# Setting debug to true makes Django serve static media and
# present pretty error pages.
DEBUG = TEMPLATE_DEBUG = False

# Set to True to load non-minified versions of (static) client dependencies
# Requires to set-up Node and tools that are required for static development
# otherwise it will raise errors for the missing non-minified dependencies
DEBUG_STATIC = False

SITENAME = 'GeoNode'
SITEURL = 'http://localhost:8888/'

...
```
Please have a look!!
