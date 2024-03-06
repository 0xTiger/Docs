{
  "date": "2021-04-08",
  "keywords": [
"فایل pkg",
"فرمت فایل pkg",
"فایل pkg چیست",
"فایل",
"pkg مثال",
"پسوند فایل pkg",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PKG - فرمت فایل بایگانی قابل توسعه",
  "description": "درباره فرمت فایل PKG و APIهایی که می‌توانند فایل‌های PKG را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "PKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pk-fag"
}
},
  "lastmod": "2021-04-13"
}

## فایل PKG چیست؟

یک فایل با پسوند pkg. یک فایل بسته نصب کننده است که برای نصب نرم افزار در macOS استفاده می شود. علاوه بر کامپیوترهای مکینتاش، در آیفون نیز استفاده می شود. برنامه نصب داخلی اپل را می توان برای نصب محتویات یک فایل PKG استفاده کرد. یک فایل PKG مشابه فایل MSI است که در سیستم عامل ویندوز برای نصب نرم افزار استفاده می شود. در حین نصب، این فایل‌های بسته می‌توانند پیام‌هایی را ثبت کنند که به شما این ایده را می‌دهد که چه چیزهای اضافی توسط این بسته نصب شده است.

## فرمت فایل PKG

PKR فایل های باینری هستند که برای کاهش حجم کلی فایل فشرده می شوند. از زمان OSX 10.5، بسته های مسطح با فایل های نصب تکی توسط اپل معرفی شده اند. این فرمت‌ها با قالب‌های بسته‌بندی قبلی که به‌جای فایل‌های منفرد به صورت بسته‌بندی عرضه می‌شدند، متفاوت هستند. این بسته های همراه حاوی یک سلسله مراتب دایرکتوری ساختاریافته بودند که فایل ها را به گونه ای ذخیره می کرد که بازیابی آنها را از طریق برخی از فایل های فهرست تسهیل می کند. فرمت فایل PKG مسطح در واقع یک آرشیو [XAR](/compression/xar/) است که دارای موارد زیر است:

 * Header - اندازه، چک جمع و اطلاعات نسخه را تعریف می کند
 * فهرست مطالب - یک سند XML که به صورت UTF-8 (و باید) کدگذاری شود و در ابتدای فایل ذخیره می‌شود، اسکن بایگانی را برای استخراج یک فایل آسان می‌کند.
 * Heap - پشته بدون ساختار داده که توسط TOC ارجاع شده است

## منابع

* [فرمت فایل بسته بسته](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)

* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

