---
layout: default
---

The following table is linked with:

- **Repo**: published website (from the gh-pages branch)
- **Status**: the Travis log summary of branches (draft and gh-pages)
- **Last Mod**: the Github repository, defaulting to the draft branch
- **Map**: the Github interactive map of the regions

{: #status_tbl .display}
| Repo | Study Area | Status | Last Mod | Map | Regions |
|------|------------|--------|----------|-----|---------|
{% for r in site.data.status %}| [{{ r.repo }}](http://ohi-science.org/{{ r.repo }}) | {{ r.study_area }} | {{ r.status }} | [{% if r.last_mod != "" %}{{ r.last_mod }}{% else %}---{% endif %}](http://github.com/OHI-Science/{{ r.repo }}) | [![]({{ r.map_url }})](https://github.com/OHI-Science/{{ r.repo }}/blob/draft/subcountry2014/spatial/regions_gcs.geojson) | {{ r.n_regions }} |
{% endfor %}

<script type="text/javascript">
$(document).ready(function(){
  $('#status_tbl').DataTable();
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
