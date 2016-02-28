---
layout: default
title: Blog
permalink: /blog/
---
{% include page_nav.html %}

<div class="container-wrapper grey-bg white-bottom-border">
  <div class="container">
    <div class="row">
      <div class="container-padding">
        <div class="col-xs-12 col-sm-12 col-md-8 col-lg-8">
          <div class="expertise-option">
            <div class="box">
              <div class="text-left">
                <h1 class="expertise-header">Recent Articles</h1>
                <hr/>
                <br/>
                <ul class="post-list">
                  {% for post in site.posts %}
                    <li>
                      <h2><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
                      <p>{{ post.excerpt }}</p>
                      <p class="meta padding-bottom-10">
                        {{ post.date | date: "%B %-d, %Y" }}
                        &middot;
                        {{ post.category }}
                        &middot;
                        <i class="fa fa-bookmark"></i> {{ post.minute_read_time }} minute read
                      </p>
                      <hr/>
                    </li>
                  {% endfor %}
                </ul>
                <br/>
                <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

              </div>
            </div>
          </div>
        </div>
        <div class="col-xs-12 col-sm-4 col-md-4 col-lg-4">
          {% include about.html %}
        </div>
      </div>
    </div>
  </div>
</div>
