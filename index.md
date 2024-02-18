---
layout: about
permalink: /
profile:
  align: right
  image: cara_2023.png
published: true
---

**Hello!** 👋 

My name is Francisco Machado and I am a theoretical physicist working at the intersection of atomic physics and condensed matter.

Originally from Portugal, Physics has taken me through many places:
- 2022-present - **ITAMP Fellow** at the Harvard-Smithsonian Center for Astrophysics
- 2016-2022 - **PhD** in Physics at UC Berkeley (advised by Prof. Norman Yao)
- 2013-2016 - **Bachelor of Science** in Physics at MIT
- 2012-2013 - Physics program at University of Coimbra



See [research](research) for an overview of my research interests and [the publications below](publications) (or <a href="http://arxiv.org/a/machado_f_1">arXiv</a>) for a complete list of my publications.

To contact me: fmachado at cfa dot harvard dot edu


# Pre-prints
<ol>
{% assign sorted = site.publications | reverse %}
{% for pub in sorted %}
  {% unless pub.template%}
  {% unless pub.peerReview %}
  <li>
  <p> 
      <a href="{{ pub.url  }}">  {{ pub.title }} 
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
      <a href="{{ pub.url  }}">  {{ pub.title }} 
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
