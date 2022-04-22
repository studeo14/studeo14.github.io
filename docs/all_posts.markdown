---
layout: default
title: All posts
---

<h2><u>All Posts</u></h2>

<div class="pagination">
    <a href="{{ site.baseurl }}/" class="previous">
        View recent posts
    </a>
</div>


<!-- This loops through the paginated posts -->
{% for post in site.posts %}
<div class="post_section">
    <p class="listing_date">{{ post.date | date_to_long_string }}</p>
    <a href="{{ site.baseurl }}/{{ post.url }}">
        <h3 class="listing_title">{{ post.title }}</h3>
    </a>
    <!--
    <div class="tag_row">
    {% for category in post.categories %}
    <a href="{{ site.baseurl }}/categories/{{ category }}"><span class="pill_tag">{{ category }}</span></a>
    {% endfor %}
  </div>
-->
    <p>{{post.excerpt}} (<a href="{{ site.baseurl }}/{{ post.url }}">read more...)</a></p>
    <br>
    <hr>
</div>
{% endfor %}
