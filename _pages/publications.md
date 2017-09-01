---
layout: archive
permalink: /publications/
author_profile: flase
---

## Publications

{% assign sorted = (site.publications | sort: 'path') | reverse %}
{% for pub in sorted %}
  * [{{ pub.title }}]({{ pub.url }})  
  *{{ pub.authors }}*
{% endfor %}
