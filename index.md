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
        <p>لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد. کتابهای زیادی در شصت و سه درصد گذشته، حال و آینده شناخت فراوان جامعه و متخصصان را می طلبد تا با نرم افزارها شناخت بیشتری را برای طراحان رایانه ای علی الخصوص طراحان خلاقی و فرهنگ پیشرو در زبان فارسی ایجاد کرد. در این صورت می توان امید داشت که تمام و دشواری موجود در ارائه راهکارها و شرایط سخت تایپ به پایان رسد وزمان مورد نیاز شامل حروفچینی دستاوردهای اصلی و جوابگوی سوالات پیوسته اهل دنیای موجود طراحی اساسا مورد استفاده قرار گیرد.</p>
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
        <p>لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد. کتابهای زیادی در شصت و سه درصد گذشته، حال و آینده شناخت فراوان جامعه و متخصصان را می طلبد تا با نرم افزارها شناخت بیشتری را برای طراحان رایانه ای علی الخصوص طراحان خلاقی و فرهنگ پیشرو در زبان فارسی ایجاد کرد. در این صورت می توان امید داشت که تمام و دشواری موجود در ارائه راهکارها و شرایط سخت تایپ به پایان رسد وزمان مورد نیاز شامل حروفچینی دستاوردهای اصلی و جوابگوی سوالات پیوسته اهل دنیای موجود طراحی اساسا مورد استفاده قرار گیرد.</p>
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
        <h3>با تشکر از</h3>
        <ul>
          {% for thank in site.data.thanks %}
            <li>{{ thank.text }}</li>
          {% endfor %}
        </ul>
        <h3>مشارکت در این پروژه</h3>
        <p>از تمامی علاقمندان برای تکمیل این مستندات دعوت می شود. برای مشاکت می توانید از طریق Github اقدام کنید.</p>
      </div>
    </div>
</div>
<!-- Contents End -->
