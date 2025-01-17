{
  "date": "2019-10-11",
  "keywords": [
"mhtml",
"فایل mhtml",
"فرمت فایل mhtml",
"نوع فایل mhtml",
"فایل",
"نوع",
"فایل mhtml چیست"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHTML - MIME HTML فایل",
  "description": "درباره فرمت فایل MHTML و APIهایی که می توانند فایل های MHTML ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mhtm-fal"
}
},
  "lastmod": "2019-09-10"
}

## فایل MHTML چیست؟

فایل‌های با پسوند MHTML فرمت آرشیو صفحه وب را نشان می‌دهند که می‌تواند توسط تعدادی برنامه مختلف ایجاد شود. این قالب به عنوان فرمت آرشیو شناخته می شود زیرا کد **[HTML](/web/html/)** وب و منابع مرتبط را در یک فایل ذخیره می کند. این منابع شامل هر چیزی است که به صفحه وب مرتبط است مانند تصاویر، اپلت ها، انیمیشن ها، فایل های صوتی و غیره. فایل های MHTML را می توان در برنامه های مختلف مانند اینترنت اکسپلورر و مایکروسافت ورد باز کرد. مایکروسافت ویندوز از فرمت فایل MHTML برای ضبط سناریوهای مشکلات مشاهده شده در هنگام استفاده از هر برنامه کاربردی در ویندوز که مشکلاتی را ایجاد می کند استفاده می کند. فرمت فایل MHTML محتویات صفحه را شبیه به مشخصات تعریف شده در message/rfc822 که مشخصات مربوط به ایمیل متنی ساده است، رمزگذاری می کند. مشخصات واقعی قالب به شرح جزئیات [RFC 2557](https://tools.ietf.org/html/rfc2557) است.

## فرمت فایل MHTML

MHTML همچنین به عنوان MIME Encapsulation of Aggregate HTML اسناد شناخته می شود، زیرا می تواند صفحات وب HTML را به همراه منابع خود در یک آرشیو وب واحد رمزگذاری کند. طبق مشخصات RFC 2557، یک سند جمع‌آوری شده یک پیام رمزگذاری شده با MIME است که حاوی یک منبع ریشه (شیء) و همچنین منابع دیگری است که از طریق URI به آن پیوند داده شده‌اند. چنین منابع دیگری ممکن است نمایش تصاویر درون خطی، شیوه نامه ها، اپلت ها و غیره باشد. مشخصات سند کامل برای فرمت فایل MHTML به تفصیل در [RFC 2557](https://tools.ietf.org/html/rfc2557) است و باید برای هر نوع توسعه برنامه برای خواندن/نوشتن این فرمت فایل ارجاع داده شود. این استاندارد مشخص می‌کند که قسمت‌های بدنی که باید به آنها ارجاع داده شود، می‌توانند با Content-ID یا Content-Location شناسایی شوند.

### سرصفحه های محتوای MIME

یک هدر محتوای MIME، Content-Location، برای حل ارجاعات URI به منابع در سایر قسمت های بدن تعریف شده است. این هدر می تواند در هر عنوان پیام یا محتوایی وجود داشته باشد.

### سربرگ Content-Location

Content-Location نمایشی از یک URI است که محتویات قسمتی از بدن را که در آن قرار می گیرد برچسب گذاری می کند. مقدار آن می تواند یک URI مطلق یا نسبی باشد. می توان از آن برای برچسب زدن منبعی استفاده کرد که توسط برخی یا همه گیرندگان پیام قابل بازیابی نیست. یک پیام تنها مجاز است فقط یک سرصفحه Content-Location داشته باشد. مثالی از یک ساختار چندبخشی/مرتبط حاوی اجزای بدن با هر دو برچسب Content-Location و Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URIهای MHTML Aggregates

URI مجموع MHTML با URI ریشه آن متفاوت است. قسمت سرصفحه Content-Location اگر در عنوان یک عنوان چندبخشی/مرتبط استفاده می‌شود، باید برای کل مجموعه اعمال شود. به طور مشابه، مجموعه منابع بازیابی شده می تواند با مجموعه منابع بازیابی شده با استفاده از Content-Locations قسمت های آن متفاوت باشد، زمانی که URI اشاره به تجمع MHTML برای بازیابی این تجمع استفاده می شود. به عنوان مثال، بازیابی یک مجموعه MHTML ممکن است یک نسخه قدیمی را برگرداند، در حالی که بازیابی URI ریشه و اشیاء پیوند شده درون خطی آن ممکن است نسخه جدیدتر را بازگرداند.

## منابع

* [MIME کپسوله کردن اسناد مجموع - RFC 2557](https://tools.ietf.org/html/rfc2557)

* [فرمت فایل MHTML - توسط ویکی پدیا](https://en.wikipedia.org/wiki/MHTML)


