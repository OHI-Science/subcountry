---
layout: default
---

**Note**: this page is out of date. 


The [subcountry:status.csv](https://github.com/OHI-Science/subcountry/blob/gh-pages/_data/status.csv) table is displayed below with the following links:

- **Assessment Area**: the assessment and website  (from the gh-pages branch)
- **Repository**: the Github repository, defaulting to the draft branch
- **Map**: the Github interactive map of the regions
- **Regions**: the number of regions in the assessment area

{: #status_tbl .display}
| Assessment Area | Repository | Map | Regions |
|-----------------|------------|-----|---------|
{% for r in site.data.status %}| [{{ r.study_area }}](http://ohi-science.org/{{ r.repo }}) | [{{ r.repo }}](http://github.com/OHI-Science/{{ r.repo }}) | [![]({{ r.map_url }})](https://github.com/OHI-Science/{{ r.repo }}/blob/draft/subcountry2014/spatial/regions_gcs.geojson) | {{ r.n_regions }} |
{% endfor %}

<script type="text/javascript">
$(document).ready(function(){
  $('#status_tbl').DataTable({
    "paging":   false
  });
});
</script>
<!-- original from jekyll new
  <h1 class="page-heading">Posts</h1>

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
-->
