## Customize Metadata

**Second approach**

```python
CONNECTION_TYPES = (
    ('mdext', 'Metadata extension'),
)

NODE_TYPES = (
    ('mdext_o', 'Resource'),
    ('mdext_d', 'LayerExt')
)

class CustomMetadata(models.Model):
    object_id      = models.PositiveIntegerField()

    md_custom_f1  = models.CharField(_('f1'), max_length=3, choices=MY_CHOICES, default='xxx', help_text=_('something used for metadata'))
    md_custom_date = models.DateTimeField(_('metadata date'), default = datetime.now, help_text=_('metadata date'))

class MdextConnector(object):
    def __init__(self):
        self._registry = {'mdext_o': {},
                          'mdext_d': {},
                          }
    def get_ctype_pks(self, registry_name):
        pks = []
        for model in self._regitry[registry_name].iterkeys():
            pks.append(ContentType.objects.get_for_model(model))
            return pks

    def register(self, model, opts):
        for ntype in opts['node_types']:
            self._registry[ntype][model] = opts['node_types']
            setattr(model, '_post_save', True)
            if re_origin.search(ntype):
                model.add_to_class('mdext_connector_o',generic.GenericRelation(CustomMetadata,
                                    object_id_field='o_object_id')
                                   )
                if ntype == 'mdext_o':
                    signals.post_save.connect(mdext_post_save_o, sender=model)

            if re_destination.search(ntype):
                model.add_to_class('mdext_connector_d',generic.GenericRelation(Connection,
                                    object_id_field='object_id')
                                   )
                if ntype == 'mdext_d':
                    signals.post_save.connect(mdext_post_save_d, sender=model)

mdext_connector = MdextConnector()
...
from geonode.maps.models import Layer

mdext_connector.register(Layer, {'node_types': {'mdext_o': True,},})
```

