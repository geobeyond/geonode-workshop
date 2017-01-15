## Site Base Template

Override the base page by editing the HTML within the `template` folder:

```html
{% extends "base.html" %}
{% block extra_head %}
      <link href="{{ STATIC_URL }}css/site_base.css" rel="stylesheet"/>
{% endblock %}
{% block extra_tab %}
{% comment %}
Add Tab for Third Party Apps
<li>
 <a href="{{ PROJECT_ROOT }}app">App</a>
</li>
{% endcomment %}
{% endblock %}
```

Remove the comment and see what is going to happen to Tab menu!!
