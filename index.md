---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
<div class="grid-container">
    <div class="grid-x grid-padding-x align-center introduction">
      <div class="logo-holder cell small-10 medium-4">
        <img src="/assets/img/juliaIR-400-225.png" alt="مرجع فارسی زبان Julia" width="300" height="170">
      </div>
      <div class="project-desc cell medium-9">
        <p>
          جولیا یک زبان برنامه نویسی متن باز، سطح بالا  و چندمنظوره است که برای محاسبات علمی با کارایی بالا طراحی شده است. از این زبان برای برنامه نویسی سطح پایین سیستم ها هم می توان استفاده کرد.همچنین این زبان از پردازش همروند، موازی و توزیع شده هم پشتیبانی می کند. بهره‌مندی این زبان از کتابخانه های کارای محاسباتی در زمینه هایی مانند جبرخطی و همچنین کتابخانه های نوشته شده توسط جامعه‌ی فعال و پویای توسعه دهنده اش، آن را به یک انتخاب عالی برای کاربرد هایی مثل یادگیری ماشین، پردازش تصویر و ... تبدیل کرده است. وبسایت حاضر یک پروژه‌ی متن باز با هدف ترویج این زبان و تولید اسناد فارسی مفید برای آن است. اغلب این اسناد بر اساس <a href="https://julialang.org/" target="_blank">مستندات رسمی زبان Julia</a> نوشته شده اند.
        </p>
      </div>
    </div>
    <!-- Sections Start -->
    <div class="grid-x align-center sections">
      <div class="cell medium-9 grid-x grid-padding-x">
        <div class="cell medium-4">
          <div class="card">
            <div class="card-section">
              <h2 class="text-center">مطالب آموزشی</h2>
              <p>این بخش حاوی مطالبی برای آشنایی با قابلیت های اصلی زبان Julia است.در صورتی که قصد دارید با Julia آشنا شوید، از اینجا شروع کنید.</p>
              <a class="button primary" href="/tutorials">مطالب آموزشی</a>
            </div>
          </div>
        </div>
        <div class="cell medium-4">
          <div class="card">
            <div class="card-section">
              <h2 class="text-center">مثال های کاربردی</h2>
              <p>این بخش حاوی مثال هایی کاربردی از زبان Julia است.مطالعه این مثال ها می تواند به یادگیری بهتر این زبان و آشنایی با قابلیت ها و کاربرد های آن  کمک کند.</p>
              <a class="button primary" href="/examples">مثال های کاربردی</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Sections End -->
    <div class="grid-x grid-padding-x align-center">
      <div class="cell medium-9">
        <h2 class="text-center" id="about-us">درباره‌ این پروژه</h2>
        <p>پروژه‌ی <a href="/">مرجع فارسی زبان Julia</a> یک پروژه‌ی متن باز است که قصد دارد با تولید آموزش ها و اسناد فارسی مناسب برای زبان برنامه نویسی Julia ، استفاده از این زبان را برای اهداف علمی ترویج دهد.این پروژه در ۱۳۹۸ توسط هسته‌ی علمی یادگیری ماشین دانشگاه بوعلی سینا آغاز شده و از تمامی علاقمندان برای همکاری در گسترش آن دعوت به عمل می آید.</p>
        <h3>مشارکت کنندگان در این پروژه</h3>
        <ul class="no-bullet authors-list">
          {% for author in site.data.authors %}
          <li>
            <div class="author">
              <a href="{{ author.github }}">{{ author.name }}</a><br>
              <small>{{ author.desc }}</small><br>
              <small>ایمیل :‌ {{ author.mail }}</small>
            </div>
          </li>
          {% endfor %}
        </ul>
        <br/>
        <ul>
          {% for thank in site.data.thanks %}
            <li>{{ thank.text }}</li>
          {% endfor %}
        </ul>
        <h3>مشارکت در این پروژه</h3>
        <p>از تمامی علاقمندان برای تکمیل این مستندات دعوت می شود. برای مشارکت می توانید از طریق <a href="https://github.com/juliair">Github</a> اقدام کنید.</p>
      </div>
    </div>
</div>
<!-- Contents End -->
