---
layout: default
title: Dead Tech 
nav_order: 4
---

   <div id='bump'>
        <section class="article archive">
          <article class="archive-wrap">
              <ul class="post-list">
                 <lh><h2><span class="bb">{{ page.title }}</span></h2></lh>
                  {% assign deadposts = site.posts | where:"tags","deadtech" %}
                  {% for post in deadposts %}            
                  <li>
                    <div class="deets" itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
                        <h2><a href="{{ site.url }}{{ post.url }}">{{ post.title }} - {{ post.author }}</a></h2>
                        <p class="date"><time datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">{{ page.date | date: "%b %d, %Y" }}</time></p>
                        <p class="">{% if post.description %}{{ post.description  | strip_html | strip_newlines | truncate: 120 }}{% else %}{{ post.content | strip_html | truncate: 120 }}{% endif %}</p>
                    </div>
                  </li>
                  {% endfor %}
              </ul>
          </article>
        </section>
    </div>
