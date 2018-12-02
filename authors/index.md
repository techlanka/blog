---
layout: page
current: authors
title: Authors
navigation: true
logo: 'assets/images/favicon.png'
class: page-template
subclass: 'post page'
---

<header class="site-header outer">
  <div class="inner">
    {% raw %}{{> "site-nav"}}
  </div>
</header>
{{#post}}
<main id="site-main" class="site-main outer" role="main">
  <div class="inner">
    <header class="post-full-header">
      <h1 class="post-full-title">{{title}}</h1>
    </header>
    {{#get 'users' limit='all' include='count.posts' order='count.posts desc'}}
      <div class="post-feed">
        {{#foreach users}}
          <article class="post-card {{#unless profile_image}} no-image{{/unless}}">
            {{#if profile_image}}
              <a class="post-card-image-link" href="">
                <div class="post-card-image" style="background-image: url({{profile_image}})"></div>
              </a>
            {{/if}}
            <div class="post-card-content">
              <a class="post-card-content-link" href="{% raw %}{{url}}">
                <header class="post-card-header">
                  <h2 class="post-card-title">{{name}}</h2>
                </header>
                <section class="post-card-excerpt">
                  <p>{{bio}}</p>
                </section>
              </a>
            </div>
          </article>
        {{/foreach}}
      </div>
    {{/get}}
  </div>
</main>
{{/post}}