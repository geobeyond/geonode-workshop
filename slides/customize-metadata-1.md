## Customize Metadata

**First approach**

```python
from annoying.fields import AutoOneToOneField

class MdExtension(models.Model):
    resource     = AutoOneToOneField(ResourceBase, primary_key=True)

    md_custom_f1  = models.CharField(_('f1'), max_length=3, choices=MY_CHOICES, default='xxx', help_text=_('something used for metadata'))
    md_custom_date = models.DateTimeField(_('metadata date'), default = datetime.now, help_text=_('metadata date'))

    contacts     = models.ManyToManyField(Profile, through='MultiContactRole')
    ...

@property
def complete(self):
# your code here

ResourceBase.complete = complete
```

