---
title: متغیر ها در Julia
author: امیرعباس اسدی
desc: آشنایی با شیوه تعریف متغیر ها در Julia
layout: tutorialLayout
---
یک متغیر، در حقیقت یک نام مرتبط با یک مقدار است و هنگامی مفید است که لازم باشد مقداری را برای استفاده های بعدی ذخیره کنید. برای مثال:
<pre>
<code class="language-julia">
# انتساب مقدار 10 به یک متغیر
julia> x = 10
10

# انجام عملیات ساده ریاضی
julia> x + 1
11

# عوض کردن مقدار متغیر
julia> x = 1 + 1
2

# انتساب انواع دیگر مقدار مثل رشته
julia> x = "Hello World!"
"Hello World!"
</code>
</pre>

قواعد جولیا برای نام گذاری متغیر ها بسیار منعطف هستند.نام متغیر ها حساس به حروف کوچک و بزرگ نیست.
<pre>
<code class="language-julia">
julia> x = 1.0
1.0

julia> y = -3
-3

julia> Z = "My string"
"My string"

julia> customary_phrase = "Hello world!"
"Hello world!"

julia> UniversalDeclarationOfHumanRightsStart = "人人生而自由，在尊严和权利上一律平等。"
"人人生而自由，在尊严和权利上一律平等。"

julia> APerisianStatement = "مرجع فارسی زبان جولیا"
"مرجع فارسی زبان جولیا"


</code>
</pre>
برای نام گذاری متغیر ها می توان از تمام کاراکتر های یونیکد (UTF-8) استفاده کرد:
<pre>
<code class="language-julia">
julia> Ψ = 3.14
3.14
julia> مجموع = 52445
52445
julia> 안녕하세요 = "Hello"
"Hello"
</code>
</pre>
در محیط REPL می توانید با تایپ یک Backslash و سپس نام LaTeX یک نماد و فشردن Tab آن را تایپ کنید. مثلا `\delta` یا `\gamma` و .... حتی می توانید نمادی مانند $$\beta_2^3$$ را با ترکیب زیر تایپ کنید:
<pre>
<code class="language-julia">
\beta-tab-\_2-tab-\^3-tab
</code>
</pre>
همچنین اگر متغیری را جایی دیدید و خواستید بدانید که دستور تایپ آن چیست کافی است در REPL یک ؟ گذاشته و سپس کاراکتر موردنظر را آن جا paste کنید.  
جولیا همچنین اجازه می دهد ثابت ها  و توابع built-in آن را هم تعریف کنید(هر چند که این کار توصیه نمی شود).
<pre>
<code class="language-julia">
julia> pi = 3
3

julia> pi
3

julia> sqrt = 4
4
</code>
</pre>
البته اگر این ثابت ها یا توابع در حال استفاده باشند در صورت باز تعریف با خطا مواجه خواهید شد:
<pre>
<code class="language-julia">
julia> pi
π = 3.1415926535897...

julia> pi = 3
ERROR: cannot assign variable MathConstants.pi from module Main

julia> sqrt(100)
10.0

julia> sqrt = 4
ERROR: cannot assign variable Base.sqrt from module Main
</code>
</pre>
## اسامی مجاز برای متغیر ها
اسامی متغیر ها باید با یک حرف (a-z , A-Z) یا `_` یا مجموعه کاراکتر های یونیکد بزرگتر از 00A0 آغار شود. باقی حروف اسم می توانند شامل `!` و ارقام و دیگر کاراکتر های یونیکد باشد. از نام دستورات  built-in نمی تواند به عنوان نام متغیر استفاده کرد:
<pre>
<code class="language-julia">
julia> else = false
ERROR: syntax: unexpected "else"

julia> try = "No"
ERROR: syntax: unexpected "="
</code>
</pre>
## قرارداد های نام گذاری
علی رغم اینکه جولیا سخت گیری چندانی در مورد نام متغیر ها ندارد، بهتر است به منظور یکدست و استاندارد شدن برنامه های نوشته شده در نام گذاری آن ها از قواعد و قرارداد های زیر تبعیت کنید:  
- نام متغیر ها با حروف کوچک باشد.
- جداسازی کلمات می تواند با `_` انجام شود، اما بهتر است از استفاده از آن اجتناب کرد مگر اینکه بدون آن نام متغیر خوانا نباشد.
- نام `Type` ها و `Module` ها باید با یک حرف بزرگ آغاز شده و به جای استفاده از `_` جداسازی کلمات به شیوه Camel Case انجام شود.
- نام توابع و ماکرو ها باید متشکل از حروف کوچک و بدون `_` باشد.
- نام توابعی که ورودی خود را عوض می کنند باید با `!` پایان یابد. این توابع گاهی اوقات mutating و یا in-place نامیده می شوند چرا که علاوه بر بازگرداندن یک مقدار،‌ ورودی های خود را هم عوض می کنند.

برای کسب اطلاعات بیشتر در مورد قواعد و قرارداد های مربوط به ظاهر کدنویسی به [این](https://docs.julialang.org/en/v1/manual/style-guide/#Style-Guide-1) صفحه مراجعه کنید.
