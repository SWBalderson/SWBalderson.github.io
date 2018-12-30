---
layout: blog-front
title: Simon Balderson - Blog Posts
---

<div id="blog-grid">

  <section id="latest-post">
    {% for post in site.posts limit:1 %}
    <div class="spacer"></div>
    <article>
      <div class="latest-post-text">
        <h2><a href="{{post.url}}">{{post.title}}</a></h2>
        <p>{{post.summary}}</p>
        <p class="readmore"><strong><a href="{{post.url}}">READ MORE</a></strong></p>
      </div>
      <div class="latest-post-img" style="background: url('{{site.url}}/assets/img/{{post.image}}') no-repeat; background-size:cover; background-position: center center;">
      </div>
    </article>
    <div class="spacer"></div>
    {% endfor %}
  </section>

  <section id="blog-posts">
    <ul>
      {% for post in site.posts offset:1 %}
        <li>
          <a href="{{post.url}}">{{post.title}}</a>
        </li>
      {% endfor %}
    </ul>
  </section>

  <section id="blog-footer">
    <p>Footer</p>
  </section>

</div>
