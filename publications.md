---
layout: default
title: Publications
permalink: /publications/
---

## Publications

<section class="publications-list">
  {% for publication in site.data.publications %}
    <article class="publication-entry">
        <em>{{ publication.title }}</em>
        <br/>
        {%- for author in publication.authors -%}
            {%- if author == "Brett Mullins" -%}
                <strong>{{ author -}}</strong>
            {%- else -%}
                {{ author -}}
            {%- endif -%}
            {% unless forloop.last %}, {% endunless %}
        {%- endfor %}
        <br/>
        <em>{{ publication.venue }}</em>{% if publication.venue and publication.year %},{% endif %} {{ publication.year }}
        <br/>
        {% if publication.pdf or publication.slides or publication.code or publication.link or publication.summary %}
            {% if publication.pdf %}
                <a href="{{ site.baseurl }}/papers/{{ publication.pdf }}" target="_blank" rel="noopener noreferrer">Paper</a>
            {% endif %}
            {% if publication.link %}
                <a href="{{ publication.link }}" target="_blank" rel="noopener noreferrer">Paper</a>
            {% endif %}
            {% if publication.slides %}
            {% if publication.pdf or publication.link %} | {% endif %}<a href="{{ site.baseurl }}{{ publication.slides }}" target="_blank" rel="noopener noreferrer">Slides</a>
            {% endif %}
            {% if publication.code %}
            {% if publication.pdf or publication.slides or publication.link %} | {% endif %}<a href="{{ publication.code }}" target="_blank" rel="noopener noreferrer">Code</a>
            {% endif %}
            {% if publication.summary %}
            {% if publication.pdf or publication.slides or publication.link or publication.code %} | {% endif %}<a href="{{ site.baseurl }}{% link {{publication.summary}} %}">Summary</a>
            {% endif %}
            {% if publication.video %}
            {% if publication.pdf or publication.slides or publication.link or publication.code or publication.summary %} | {% endif %}<a href="{{ publication.video }}" target="_blank" rel="noopener noreferrer">Video</a>
            {% endif %}
        {% endif %}
        <br/> <br/>
    </article>
  {% else %}
    <p>No publications listed yet.</p>
  {% endfor %}
</section>

See my [CV]({{ site.baseurl }}/images/cv.pdf) for a full list of publications, including those prior to 2020