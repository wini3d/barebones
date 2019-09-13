---
layout: default
title: NorthStack Example Blog
---
<!-- HTML elements for search -->
<input type="text" id="search-input" placeholder="Search blog posts..">
<ul id="results-container"></ul>

<div class="posts">
    {% for post in site.posts %}
        <article>
            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
            Published on {{ post.date | date_to_string }}
            {{ post.excerpt }}
        </article>
    {% endfor %}
</div>

<script src="https://cdn.rawgit.com/christian-fei/Simple-Jekyll-Search/master/dest/simple-jekyll-search.min.js"></script>
<script type="text/javascript">
      SimpleJekyllSearch({
        searchInput: document.getElementById('search-input'),
        resultsContainer: document.getElementById('results-container'),
        json: '/search.json',
        searchResultTemplate: '<li><a href="{url}" title="{desc}">{title}</a></li>',
        noResultsText: 'No results found',
        limit: 10,
        fuzzy: false
      })
</script>
