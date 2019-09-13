---
layout: home
title: NorthStack Example Blog
---

<!-- HTML elements for search -->
<input type="text" id="search-input" placeholder="Search blog posts..">
<ul id="results-container"></ul>

<!-- or -->
<script src="https://cdn.rawgit.com/christian-fei/Simple-Jekyll-Search/master/dest/simple-jekyll-search.min.js"></script>


<div class="posts">
    {% for post in site.posts %}
        <article>
            <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
            Published on {{ post.date | date_to_string }}
            {{ post.excerpt }}
        </article>
    {% endfor %}
</div>
