---
layout: home
---

<div class="index-content article">
    <div class="section">
        <ul class="artical-cate">
            <li class="on"><a href="/"><span>Article</span></a></li>
            <li style="text-align:center"><a href="/poem"><span>Poem</span></a></li>
            <li style="text-align:right"><a href="/novel"><span>Novel</span></a></li>
        </ul>

        <div class="cate-bar"><span id="cateBar"></span></div>

        <ul class="artical-list">
        {% for post in site.categories.article %}
            <li>
                <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
                <div class="title-desc">{{ post.description }}</div>
            </li>
        {% endfor %}
        </ul>
    </div>
    <div class="foot">
        <div class="copyright">&copy; 2012 - 1013 Shy07. All Rights Reserved.</div>
        <div class="designed">Powered By <a href="">Github</a> - Design By <a href="http://beiyuu.com">Beiyuu</a></div>
    </div>
    <div class="aside">
    </div>
</div>
