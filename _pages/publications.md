---
title:
layout: default
permalink: /publications/
published: true
---

# Pre-prints
<ol>
{% assign sorted = site.publications | reverse %}
{% for pub in sorted %}
  {% unless pub.template%}
  {% unless pub.peerReview %}
  <li>
  <p> 
      <a href="{{ pub.url | prepend: site.baseurl | prepend: site.url }}">  {{ pub.title }} 
      </a> <br> 
      <span style="font-size:18px"> {{ pub.authors }} </span> <br> 
      <a href="{{ pub.arXivLink}}"> {{ pub.arXivId }} </a>
      
  </p>
  </li>
  {% endunless %}
  {% endunless %}
{% endfor %}
</ol>

# Published work

<ol>
{% assign sorted = site.publications | reverse %}
{% for pub in sorted %}
  {% unless pub.template%}
  {% if pub.peerReview %}
  <li>
  <p>
      <a href="{{ pub.url | prepend: site.baseurl | prepend: site.url }}">  {{ pub.title }} 
      </a> <br> 
      <span style="font-size:18px"> {{ pub.authors }} </span> <br>
      {% if pub.arXivLink %}
      	 <a href="{{ pub.pubLink}}"> {{ pub.pubName }} ({{ pub.pubYear }}) </a>  -- <a href="{{ pub.arXivLink}}"> {{ pub.arXivId }} </a> <br>
	 {% else %}
	 <a href="{{ pub.pubLink}}"> {{ pub.pubName }} ({{ pub.pubYear }}) </a>
	 {% endif %}
  </p>
  </li>
  {% endif %}
   {% endunless %}
{% endfor %}
</ol>

<sup>&dagger;</sup> These authors contributed equally to the work. 