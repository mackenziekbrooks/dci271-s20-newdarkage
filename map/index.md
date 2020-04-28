---
layout: default
title: Map
nav_order: 7
---

<iframe src="https://www.google.com/maps/d/embed?mid=14CyTp1hDCnNs7VJ-riSVpXYcY_Wy46KT" width="840" height="680"></iframe>

   <div id='bump'>
        <section class="article archive">
          <article class="archive-wrap">
              <ul class="nobullet">
                 <lh><h1>Hidden Landscapes Map</h1></lh>
                  {% assign mapposts = site.posts | where:"tags","map" %}
                  {% for post in mapposts %}            
                  <li>
                    <div class="deets" itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
                        <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }} - {{ post.author }}</a></h2>
                        <p class="date"><time datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">{{ page.date | date: "%b %d, %Y" }}</time></p>
                        <p class="">{% if post.description %}{{ post.description  | strip_html | strip_newlines | truncate: 120 }}{% else %}{{ post.content | strip_html | truncate: 120 }}{% endif %}</p>
                    </div>
                  </li>
                  {% endfor %}
              </ul>
          </article>
        </section>
    </div>
