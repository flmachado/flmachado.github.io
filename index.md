---
layout: about
permalink: /
profile:
  align: right
  image: cara_2023.png
published: true
---

**Hello!** 👋 

My name is Francisco Machado and I am a Group Leader at <a href="http://www.qutech.nl">QuTech</a> in TU Delft.

My work explores what happens when many quantum systems are brought together, and how we can leverage this complexity to find novel ways to communicate, compute, sense, and simulate complex many-body phenomena.

See [research](research) for an overview of my research interests and [the publications below](publications) (or <a href="http://arxiv.org/a/machado_f_1">arXiv</a> or <a href="https://scholar.google.com/citations?user=P4aFRlUAAAAJ&hl=en">Google Scholar</a>) for a complete list of my publications.

If you are interested in exploring these directions for a Masters, PhD, or postdoc, reach out!

Originally from Portugal, Physics has taken me through many places:
- 2025-Present - **Group Leader** at the Quantum Internet Division of QuTech at TU Delft
- 2022-2025 - **ITAMP Fellow** at the Harvard-Smithsonian Center for Astrophysics
- 2016-2022 - **PhD** in Physics at UC Berkeley (advised by Prof. Norman Yao)
- 2013-2016 - **Bachelor of Science** in Physics at MIT
- 2012-2013 - Physics program at University of Coimbra

To contact me: flmachado42 at gmail dot com

(Updated website and email forthcoming!)


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
