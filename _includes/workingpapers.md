<h2 id="publications" style="margin: 2px 0px 0px;">Working Papers</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.workingpapers.main %}

<li>
<div class="pub-row" style="margin-bottom: 30px;border: 1px solid transparent;">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px; margin: 0px 0px 0em;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% endif %}
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px; margin: 0px 0px 0em;">
      <div class="title"><a href="{{ link.pdf }}" target="_blank">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.abstract %} 
  <details>
    <summary style="cursor:pointer;">Abstract</summary>
    <blockquote style="font-size:16px; font-style:normal; margin-top:0; margin-bottom:0; border-left:4px solid #e5e5e5; border-top:0; border-bottom:0; padding-left:5px; width:100%;">
      <p style="margin-top:0; margin-bottom:0;">{{ link.abstract }}</p>
    </blockquote>
  </details>
      {% endif %} 
      
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}          
    </div>
  </div>
</div>
</li>


{% endfor %}

</ol>
</div>
