---
layout: home
---

<div class="index-content about">
    <div class="section">
        <ul class="artical-cate">
            <li><a href="/"><span>Blog</span></a></li>
            <li style="text-align:center"><a href="/opinion"><span>Opinion</span></a></li>
            <li class="on" style="text-align:right"><a href="/about"><span>About</span></a></li>
        </ul>

        <div class="cate-bar"><span id="cateBar"></span></div>

        <ul class="artical-list">
        {% for post in site.categories.about %}
            <li>
                <h2>
                    <!--a href="{{ post.url }}">{{ post.title }}</a-->
                    <div class="title-desc">{{ post.description }}</div>
                </h2>
                <div class="content">{{ post.content }}</div>
            </li>
        {% endfor %}
        </ul>
    </div>
    <div class="aside">
    </div>
</div>


