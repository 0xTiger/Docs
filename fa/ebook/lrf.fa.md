{
  "date": "2019-12-12",
  "keywords": [
"LRF",
"فایل",
"افزونه",
"قالب",
"کتاب الکترونیکی",
"کتاب دیجیتال"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل LRF و APIهایی که می‌توانند فایل‌های LRF را ایجاد و باز کنند، بیاموزید.",
  "title": "فرمت فایل LRF - یک فایل خواننده قابل حمل سونی",
  "linktitle": "LRF",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-lr-faf"
}
},
  "lastmod": "2019-12-12"
}

## فایل LRF چیست؟

یک فایل با پسوند lrf. یک فایل کتاب الکترونیکی باند وسیع (BBeB) است که حاوی داده‌هایی برای BBeB سونی، از جمله متن، تصاویر و داده‌های صفحه‌بندی است. فایل در یک فرمت باینری فشرده که حاوی یک هدر، تعداد مشخصی از اشیاء و یک فهرست شی ذخیره می شود. فایل های LRF و LRX دو قالب کتاب BBeB موجود را در بر می گیرند. فایل های LRF رمزگذاری نشده اند و می توانند از فایل های [LRX](/ebook/lrf/) کامپایل شوند. فایل های LRF را می توان از چندین نوع فایل دیگر از جمله PDF و HTML تبدیل کرد. اگر رایانه شما نمی تواند فایل LRF را باز کند، احتمالاً نرم افزاری را برای باز کردن یا ویرایش فایل های LRF نصب نکرده اید. برنامه هایی که می توانند فایل های LRF را باز کنند عبارتند از Caliber، BookDesigner، Makelrf و Canon Book Creator برای ویندوز، Caliber برای لینوکس، Caliber و Sony Reader برای مکینتاش.

## تاریخچه مختصر

نوع فایل LRF قبل از هر چیز با Line Rider توسط [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment) مرتبط است. Line Rider یک اسباب بازی اینترنتی فیزیک است و در سپتامبر 2006 توسط یک دانشجوی اسلوونیایی به نام Boštjan Čadež اختراع شد. کتاب‌خوان‌های الکترونیکی برند سونی (مانند خواننده‌های PRS-500 سونی و سونی لیبری) از پسوند فایل LRF برای اسناد و متون خود استفاده می‌کنند. این نوع فایل اختصاصی و همچنین فایل های LRS و LRX مربوطه منسوخ شده است. این سه نوع فایل، BroadBand eBook (BBeB) را تشکیل می‌دهند که در سال 2010 زمانی که سونی شروع به فروش کتاب‌های الکترونیکی خود در قالب EPUB کرد، تولید آن متوقف شد.

## فرمت فایل LRF

مشخصات دقیق فرمت فایل LRF در [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat) موجود است. یک فایل LRF شامل موارد زیر است:
* یک هدر

* تعدادی اشیاء

* یک شاخص شی


همه این مقادیر به ترتیب اینتل (LSB اول) هستند.

### هدر LRF

|Offset (هگز) |اندازه (بایت) |نام/معنا| مقدار نمونه|
---|---|---|---|
|0 |8| امضای LRF| 4C 00 52 00 46 00 00 00 = LRF در یونیکد|
|8 |2| نسخه؟| 999 در اکثر فایل ها|
|A |2| Psuedo-Encryption |بایت کلید 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| NumberOfObjects |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| ناشناخته| 0|
|24 |1| پرچم ها| (16 - پشت به جلو، 1 = جلو به عقب) 16|
|25 |1| ناشناخته |(پر کردن؟) 0|
|26 |2| ناشناخته| 1600|
|28 |2| ناشناخته| (پدینگ؟) 0|
|2A |2| قد؟| 600|
|2C |2| عرض؟| 800|
|2E |1| ناشناخته| 24|
|2F |1| ناشناخته |(پر کردن؟) 0|
|30 |0x14| ناشناخته| صفر |
|44 |4| شناسه شی فقط شیء PlaneStream (0x1E)| 0x0042|
|48 |4| ناشناخته |0x1536|
|4C |2| XMLCompSize| 0x035C|


## منابع

* [فرمت فایل LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)

* [BBeB - توسط ویکی پدیا](https://en.wikipedia.org/wiki/BBeB)


