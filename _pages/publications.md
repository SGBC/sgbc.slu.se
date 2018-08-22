---
layout: archive
permalink: /publications/
author_profile: false
---

## Publications

{% assign sorted = (site.publications | sort: 'path') | reverse %}
{% for pub in sorted %}
  * [{{ pub.title }}]({{ pub.url }})  
  *{{ pub.authors }}*
{% endfor %}
