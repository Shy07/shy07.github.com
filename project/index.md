---
layout: home
---

<div class="index-content project">
    <div class="section">
        <ul class="artical-cate">
            <li><a href="/"><span>Paper</span></a></li>
            <li style="text-align:center"><a href="/poem"><span>Poem</span></a></li>
            <li class="on" style="text-align:right"><a href="/project"><span>Project</span></a></li>
        </ul>

        <div class="cate-bar"><span id="cateBar"></span></div>

        <ul class="artical-list">
        {% for post in site.categories.project %}
            <li>
                <h2>
                    <a href="{{ post.url }}">{{ post.title }}</a>
                </h2>
                <div class="title-desc">{{ post.description }}</div>
            </li>
        {% endfor %}
        </ul>
    </div>
    <div class="aside">
    </div>
</div>
<div id="footer">
    <div class="copyright">&copy; 2012 - 2014 Shy07. All Rights Reserved.</div>
    <div class="designed">Powered By <a href="http://pages.github.com/">Github</a> - Design By <a href="http://beiyuu.com">Beiyuu</a></div>
</div>
