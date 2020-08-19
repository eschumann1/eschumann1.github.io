---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---


<h2 class="archive__item-title"> Peer-Reviewed Conference Papers </h2>

{% for post in site.publications reversed %}
  {%if post.publication_type == 'es'%}
    {% include archive-single-publication.html %}
  {% endif %}
{% endfor %}
