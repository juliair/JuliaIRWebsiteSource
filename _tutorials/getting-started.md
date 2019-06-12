---
title: شروع کار با Julia
author: امیرعباس اسدی
desc: اجرای زبان جولیا در حالت Interactive Session و اجرای اسکریپ های نوشته شده در فایل مجزا
layout: tutorialLayout
---
برای نصب جولیا می توانید از فایل های باینری از قبل کامپایل شده یا سورس آن استفاده کنید که در هر دو صورت، روند سر راستی دارد.برای دانلود و نصب زبان Julia به [این لینک](https://julialang.org/downloads/) مراجعه کنید.  
آسان ترین راه امتحان و یادگیری زبان جولیا استفاده از یک Interactive Session است که به عنوان REPL هم شناخته می شود.می توانید آن را با اجرای فایل اجرایی جولیا و یا تایپ دستور `julia` در command line اجرا کنید.محیط Interactive Session به این شکل است:
<pre>
<code class="language-julia">

$ julia

               _
   _       _ _(_)_     |  Documentation: https://docs.julialang.org
  (_)     | (_) (_)    |
   _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 1.1.1 (2019-05-16)
 _/ |\__'_|_|_|\__'_|  |  
|__/                   |


julia> 1 + 2
3

julia> ans
3
</code>
</pre>
برای خروج از Interactive Session می توانید دستور `exit()` را تایپ کرده و یا از ترکیب `Ctr-D` استفاده کنید.  
در این حالت جولیا منتظر دریافت ورودی از کاربر است. زمانی که کاربر عبارتی مانند `1 + 2` را نوشته و کلید `enter` را فشار دهد، Interactive Session مقدار آن را محاسبه و نمایش می دهد. اگر عبارت وارد شده با `;` تمام شود، نتیجه آن عبارت نمایش داده نمی شود. متغیر `ans` همیشه حاوی مقدار آخرین عبارت اجرا شده است(حتی اگر آن عبارت با `;` تمام شده باشد).متغیر `ans` تنها در حالت Interctive Session قابل دسترسی بوده و هنگام اجرای جولیا با روش های دیگر، قابل استفاده نمی باشد.  
برای اجرای دستورت نوشته شده در یک فایل مثلا `file.jl` می توانید بنویسید:
<pre>
<code class="language-julia">
include("file.jl")
</code>
</pre>
برای اجرای کد یک فایل بدون استفاده از Interactive Session می توانید نام آن فایل را به عنوان ورودی به دستور `julia` بدهید:
<pre>
<code class="language-bash">
julia script.jl arg1 arg2...
</code>
</pre>
ورودی های داده شده در دستور بالا به عنوان command line arguments به `script.jl` داده شده و از طریق global constant `ARGS` قابل دسترسی هستند.نام فایل هم در یک ثابت به نام `PROGRAM_FILE` ذخیره خواهد شد.دستور `julia` می تواند مقدار یک عبارت را با تنظیم `-e` بدون اجرای Interactive Session نمایش دهد.در اینصورت ثابت `ARGS` قابل استفاده ولی ثابت `PROGRAM_FILE` خالی است.برای مثال دستور زیر ورودی های command line را نمایش خواهد داد:
 <pre>
<code class="language-bash">
julia -e 'println(PROGRAM_FILE); for x in ARGS; println(x); end' foo bar

foo
bar
</code>
</pre>
جولیا را می توان با استفاده از `-p` و یا `--machine-file` در حالت parallel اجرا کرد. تنظیم `-p n` به تعداد `n` worker process  برای اجرای جولیا، اجرا می کند. امادستور:
<pre>
<code class="language-bash">
julia --machine-file file
</code>
</pre>
برای هر ماشین تعریف شده در `file` یک worker ایجاد می کند. با هر یک از این ماشین ها باید بتوان از طریق یک ارتباط بدون password از نوع ssh ازتباط برقرار کرد و به علاوه در هر یک از آن ها زبان julia باید در مسیر مشابه با کامپیوتری که این فرمان را در آن اجرا می کنیم نصب شده باشد.در هر خط باید یک دستگاه به صورت زیر تعریف شده باشد:
<pre>
<code class="language-bash">
[count*][user@]host[:port] [bind_addr[:port]]
</code>
</pre>
مقدار پیشفرض `user` برابر با user است که از آن در حال استفاده اید.مقدار پیشفرض `port` برابر با پورت استاندارد `ssh` است.`count` نشان دهنده تعداد worker هایی که میخواهیم روی دستگاه مورد نظر اجرا شود و به طور پیشفرض برابر با 1 است.تنظیم `bind_addr[:port]` که نوشتن آن اختیاری است، آدرس IP که دیگر worker ها بتوانند با استفاده از آن به این worker متصل شوند را مشخص می کند.  

در صورتی که کدی دارید که می خواهید با هر بار اجرای Interactive Session اجرا شود، می توانید آن را در فایل `~/.julia/config/startup.jl` بنویسید.
