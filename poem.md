---
layout: page
title: Poem
---
<div class="category">
    <ul>
    {% for post in site.categories.poem %}
        <li>
            <h2>
            	<a href="{{ post.url }}">{{ poem.title }}</a>
            </h2>
            <span>{{ post.description }}</span>
        </li>
    {% endfor %}
    </ul>
</div><!-- .entry -->
