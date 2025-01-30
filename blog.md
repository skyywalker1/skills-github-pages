---
layout: default
title: "Blog | Heartland Haven Farm"
---

# Heartland Haven Farm Blog
### Your Guide to Sustainable Living

<div class="blog-container">
    <h2>Latest Blog Posts</h2>

    <!-- Jekyll loop to display posts -->
    {% for post in site.posts %}
        <div class="blog-post">
            <h3 class="blog-post-title">
                <a href="#{{ post.url | split: '/' | last | remove: '.html' }}" class="blog-post-link">{{ post.title }}</a>
            </h3>
            <p class="blog-post-excerpt">{{ post.excerpt }}</p>
            <p><a href="#{{ post.url | split: '/' | last | remove: '.html' }}" class="blog-post-link">Read more...</a></p>
        </div>
    {% endfor %}
</div>

---

{% for post in site.posts %}
    <div id="{{ post.url | split: '/' | last | remove: '.html' }}" class="post-content">
        <h2>{{ post.title }}</h2>
        <p>{{ post.excerpt }}</p>
        {{ post.content }}
    </div>
{% endfor %}

<footer>
    <p>&copy; 2025 Heartland Haven Farm. All rights reserved.</p>
</footer>
