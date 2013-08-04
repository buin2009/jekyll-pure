---
layout: default
---

<div class = "content">
    <h1 class="content-subhead">Recent Posts</h1>
    {% for post in site.posts limit: 5 %}
        <section class = "post">
            <header class = "post-header">
                <h2 class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></h2>
                <p class = "post-meta">
                    Post at {{ post.date | date:"%Y-%m-%d" }}
                </p>
            </header>
            <div class = "post-description">
                {{ post.content | split:'<!--more-->'| first }}
            </div>
        </section>
    {% endfor %}
</div>
