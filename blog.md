---
layout: default
title: Blog
permalink: /blog/
mathjax: true
---
<form action="https://docs.google.com/forms/u/0/d/e/1FAIpQLSfQvCMl_txJj5gh831vnayGh0Ih-S24hd_rFp8SHHtu3WDv1Q/formResponse" method="post" class="subscribe-box" target="_blank">
  Subscribe via Email <br/>
  <input type="email" placeholder="Your email" name="entry.1686449738"/>
  <input type="submit" value="Subscribe" id="submit"/>
</form>

<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>
