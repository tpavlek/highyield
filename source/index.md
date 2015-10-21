---
layout: default
generator: pagination
pagination:
    max_per_page: 10
    provider: data.podcasts
use:
    - podcasts
---

{% for episode in page.pagination.items %}
    {% if page.pagination.page == 1 and loop.index0 == 0 %}
        {% include '_episode.html' %}
    {% else %}
        {% include '_episode-summary.html' %}
    {% endif %}
{% endfor %}
