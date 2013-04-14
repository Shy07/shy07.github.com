---
layout: page
---
<h1 class="entry-title">
    <a href="http://www.shy07.com/2013/02/love-whisper-p1-217.html">Love Whisper Novel Version 第一部分</a>
</h1>
<div class="post-info">
    On 2013/02/23 by <a href="http://www.shy07.com/author/shy07">Shy07</a> With - <a href="http://www.shy07.com/category/novel" title="查看 Novel 中的全部文章" rel="category tag">Novel</a>
</div>
<div class="index-artical">
    <ul class="index-left">
    {% for post in site.categories.article %}
        <li>
            <h2>
            	<a href="{{ post.url }}">{{ post.title }}</a>
            </h2>
            <span class="title-desc">{{ post.description }}</span>
        </li>
    {% endfor %}
    </ul>

    <ul class="index-mid"> </ul>

    <ul class="index-right">
    {% for post in site.categories.poem %}
        <li>
            <h2>
            	<a href="{{ post.url }}">{{ post.title }}</a>
            </h2>
            <span class="title-desc">{{ post.description }}</span>
        </li>
    {% endfor %}
    </ul>
</div>

<script type="text/javascript">
$(function(){
    var height = $('.index-artical').height();
    $('.index-mid').height(height-90);
});
</script>
