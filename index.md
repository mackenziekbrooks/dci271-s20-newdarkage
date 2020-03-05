---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

> Are we living in a "New Dark Age?” Artist and writer James Bridle argues that the abundance of information intended to enlighten the world has, in practice, darkened it. This course will take a big picture look at the interconnected impact of technology on the world around us.

Coming soon
{: .label .label-yellow }

# Blog 
   <div id='bump'>
        <section class="article archive">
          <article class="archive-wrap">
              <ul class="nobullet">
                 <lh><h2><span class="bb">{{ page.title }}</span></h2></lh>
                  {% for post in site.posts %}
                  <li>
                    <div class="deets" itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
                        <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>
                        <p class="date"><time datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">{{ page.date | date: "%b %d, %Y" }}</time></p>
                        <p class="">{% if post.description %}{{ post.description  | strip_html | strip_newlines | truncate: 120 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 120 }}{% endif %}</p>
                    </div>
                  </li>
                  {% endfor %}
              </ul>
          </article>
        </section>
    </div>

