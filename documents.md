---
layout: default
---

<div class="posts">
  {% for document in site.documents %}
    <article class="post">
      <a href="{{ site.baseurl }}{{ document.url }}">
        <h1>{{ document.title }}</h1>
        {% include post-author.html post = document %}

        {% include page-banner.html post=document %}

        <div class="entry">
          {{ document.excerpt }}
        </div>
        <div class="read-more">Read More</div>
      </a>
    </article>
  {% endfor %}
</div>