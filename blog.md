---
layout: default
title: Blog
permalink: /blog/
mathjax: true
---
<form action="https://getsimpleform.com/messages?form_api_token=bf9ee17b64768467ab777087bbbbbdd8" method="post" class="subscribe-box">
  Subscribe via Email <br/>
  <input type="email" placeholder="Your email" id="email"/>
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
