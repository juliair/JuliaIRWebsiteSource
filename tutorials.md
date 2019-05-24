---
layout: default
permalink: /tutorials/
---
<div class="grid-container">
    <div class="grid-x grid-padding-x align-center">
        <div class="cell medium-9">
            <h1>آموزش های زبان Julia</h1>
            <small>فهرست آموزش های زبان برنامه نویسی Julia به صورت زیر است.مطالب جدید به مرور زمان افزوده خواهند شد.</small>
        </div>
        <div class="cell medium-9 tutorials">
            <ul class="no-bullet">
                {% for tutorial in site.tutorials %}
                <li>
                    <div class="tutorial grid-x">
                        <div class="cell">
                            <a href="{{tutorial.url}}">{{ tutorial.title }}</a>{% for label in tutorial.labels %}<span class="label alert">{{ label }}</span>{% endfor %}
                        </div>
                        <div class="cell">
                            <p class="desc">{{ tutorial.desc }}</p>
                            <span class="author">نویسنده یا مترجم : {{ tutorial.author }} </span>
                        </div>
                    </div>
                </li>
                {% endfor %}
            </ul>
        </div>
    </div>
</div>
