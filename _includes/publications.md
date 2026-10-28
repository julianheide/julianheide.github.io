<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}
<li>
  <div class="pub-row">
    <div class="col-sm-12" style="position: relative;padding-right: 15px;padding-left: 15px;">
      <div class="title">
        {% if link.doi %}
        <a href="{{ link.doi }}" target="_blank" rel="noopener">{{ link.title }}</a>
        {% elsif link.page %}
        <a href="{{ link.page }}" target="_blank" rel="noopener">{{ link.title }}</a>
        {% else %}
        {{ link.title }}
        {% endif %}
      </div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <div class="links">
        {% if link.doi %}
        <a href="{{ link.doi }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">DOI</a>
        {% endif %}
        {% if link.pdf %}
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">PDF</a>
        {% endif %}
        {% if link.code %}
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Code</a>
        {% endif %}
        {% if link.page %}
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Link</a>
        {% endif %}
        {% if link.bibtex %}
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">BibTeX</a>
        {% endif %}
        {% if link.notes %}
        <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
        {% endif %}
        {% if link.others %}
        {{ link.others }}
        {% endif %}
      </div>
    </div>
  </div>
</li>
<br>
{% endfor %}

</ol>
</div>
