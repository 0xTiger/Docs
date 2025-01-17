{
  "date": "2021-03-11",
  "keywords": [
"APNX",
"فهرست شماره صفحه آمازون",
"افزونه",
"فایل",
"قالب",
"کتاب الکترونیکی",
"کیندل آمازون"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل Amazon APNX و APIهایی که می توانند فایل های APNX را ایجاد و باز کنند، بیاموزید.",
  "title": "APNX - فهرست شماره صفحه آمازون",
  "linktitle": "APNX",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-apn-fax"
}
},
  "lastmod": "2021-05-28"
}

## فایل APNX چیست؟ ##

فایل فهرست شماره صفحه آمازون که از پسوند .apnx استفاده می کند یک نوع فایل کتاب الکترونیکی است. توسط آمازون کیندل استفاده شده است. این فایل ها در واقع به عنوان فایل های صفحه بندی مورد استفاده دستگاه های Kindle شناخته می شوند. بنابراین فایل‌های APNX معمولاً برای علامت‌گذاری صفحات کتاب‌های الکترونیکی Kindle ایجاد می‌شوند. ویژگی صفحه بندی در دستگاه های Kindle آمازون از زمان سیستم عامل 3.1 آن شروع شده است. به فایل APNX برای نمایه‌های صفحه نگاه می‌کند و سپس آن را با شماره‌های صفحه در کتاب چاپی اصلی ترسیم می‌کند. این فایل‌ها به همراه فایل‌های کتاب الکترونیکی آمازون در دستگاه‌های Kindle ذخیره می‌شوند. شما نمی توانید فایل های APNX را باز یا ویرایش کنید.

## مشخصات فرمت فایل APNX ##

### چیدمان

| بایت | محتوا| نظرات|
---|---|---|
|4 |00010001 | شناسه فرمت. ارزش 65537 little-endian.|
|4 |شروع بعدی | آفست پس از پایان مکان هدر اول. دنباله جدیدی از اطلاعات سرصفحه|
|4 |طول| طول هدر اول|
|N |سربرگ اول | رشته حاوی هدر محتوا. دنباله بعدی شروع می شود|
|2 |ناشناخته | همیشه 1|
|2 |طول | طول هدر دوم|
|2 |تعداد صفحات | تعداد کل بایت ها بعد از هدر دوم که صفحات را نشان می دهد. این کل شامل بایت هایی است که توسط pageMap نادیده گرفته می شوند.|
|2 |ناشناخته | همیشه 32|
|N |سربرگ دوم | رشته حاوی هدر نقشه برداری صفحه|
|4*N |بالشتک | اولین عدد داده شده در هدر نگاشت صفحه، تعداد 0 بایت را نشان می دهد.|
|4*N |لیست صفحه ||

### سربرگ محتوا

هدر محتوا از یک رشته محصور شده در {} تشکیل شده است که شامل جفت های کلید و مقادیر است:

| محتوا| نظرات|
---|---|
|contentGuid| راهنما.|
|آسین | شناسه آمازون برای نسخه Kindle کتاب.|
|cdeType | MOBI cdeType. همیشه باید EBOK برای کتاب‌های الکترونیکی باشد.|
|fileRevisionId | بازبینی این فایل.|

#### مثال
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### سرصفحه نقشه برداری صفحه
سرصفحه نگاشت صفحه شامل یک رشته محصور در {} است که شامل جفت های کلید و مقدار است.

| محتوا | نظرات|
---|---|
|آسین | ISBN 10 برای کتاب کاغذی که صفحات مربوط به| است
|pageMap| سه مقدار تاپل. به نظر می رسد: (N,N,N)\
1) تعداد بایت ها بعد از هدر که دنباله شماره گذاری صفحه را شروع می کند\
2) ناشناخته
3) ناشناخته\|
#### مثال
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### فهرست صفحات

فهرست صفحات دنباله ای از آفست ها در HTML خام است. هر یک
مقدار شروع یک صفحه جدید است. هر ورودی یک اندیان بزرگ 4 بایتی است
بین المللی



## منابع

* [فرمت فایل آمازون APNX](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)

* [APNX - توسط MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)


