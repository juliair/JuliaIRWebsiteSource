---
layout: default
permalink: /examples/
---
<div class="grid-container">
    <div class="grid-x grid-padding-x align-center">
        <div class="cell medium-9">
            <h1>مثال هایی از کاربرد های زبان Julia</h1>
            <small>این صفحه حاوی مثال هایی از زبان برنامه نویسی Julia است. مثال های جدید به مرور زمان افزوده خواهند شد</small>
        </div>
        <div class="cell medium-9 tutorials">
            <ul class="no-bullet">
                {% for example in site.examples %}
                <li>
                    <div class="tutorial grid-x">
                        <div class="cell">
                            <a href="{{example.url}}">{{ example.title }}</a>{% for label in example.labels %}<span class="label alert">{{ label }}</span>{% endfor %}
                        </div>
                        <div class="cell">
                            <p class="desc">{{ example.desc }}</p>
                            <span class="author">نویسنده یا مترجم : {{ example.author }} </span>
                        </div>
                    </div>
                </li>
                {% endfor %}
            </ul>
        </div>
    </div>
</div>
