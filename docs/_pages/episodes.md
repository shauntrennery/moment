---
layout: default
title: "Episodes from Just a Moment News"
summary: Recent news, powered by AI. This computer-generated daily podcast covers the most important stories in easy-to-digest 3-minute episodes.
permalink: /episodes
---

<p><strong>Just a Moment News</strong> brings you today's news, powered by AI. This computer-generated daily podcast covers the most important stories in easy-to-digest 3-minute episodes</p>

<div class="card-grid">
<!--     -->
    
    {% assign first_post = site.posts.first %}
    <div class="cards first">
        <h1 class="label reversed">Latest Episode</h1>
        <div class="center-content">
            <div class="seven columns">
                <h2><a class="post-link" href="{{ first_post.url | prepend: site.baseurl }}">{{ first_post.title }}</a></h2>
                
                <p class="meta">{{ first_post.date | date: "%b %-d, %Y" }}</p>
                <p>{{ first_post.summary }} </p> 
            </div>
            <div class="four columns center-content">
                <a href="{{ first_post.file }}" class="button button-primary" download="{{ first_post.title }}">Download Now</a>    
            </div>
        </div>            
        </div>
    
    {% for post in site.posts offset:1 %}
        <div class="cards">
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <p class="meta">{{ post.date | date: "%b %-d, %Y" }}</p>
        <p>{{ post.summary }} </p>
        </div>
    {% endfor %}
    
</div>
