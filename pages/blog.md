---
layout: page
title: Blog
---

<div class="container">
  <ul class="post-list">
    {% for post in site.posts %}
    <article role="article" itemscope itemtype="http://schema.org/BlogPosting">
      <li>
        <time class="post-meta" itemprop="dateCreated" datetime="{{post.date}}">{{ post.date | date: "%B %-d, %Y" }}</time>
        <h2><a class="post-link" href="{{ post.url | prepend: site.baseurl }}" rel="bookmark" title="Permanent Link to {{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>            
        <p>{{ post.excerpt | strip_html }} <a href="{{ post.url | prepend: site.baseurl }}" class="more" title="read more">read more</a></p>
      </li>
    </article>
    {% endfor %}
  </ul>
</div>
