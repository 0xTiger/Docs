{
  "date": "2021-07-29",
  "keywords": [
"فایل md5",
"فرمت فایل md5",
"فایل md5 چیست",
"فایل",
"نمونه md5",
"پسوند فایل md5",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فایل MD5 - MD5 Checksum",
  "description": "درباره فایل MD5 و APIهایی که می‌توانند فایل‌های MD5 را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MD5",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-md-fa5"
}
},
  "lastmod": "2021-07-29"
}

## فایل MD5 چیست؟

فایل MD5 یک فایل چک‌سوم است که برای تأیید صحت یک فایل استفاده می‌شود. این شبیه به اثر انگشت برای فایل مرتبط است و به طور منحصربه‌فرد با استفاده از الگوریتمی که از تعداد بیت‌های موجود در فایل استفاده می‌کند، تولید می‌شود. برای تأیید فایل با نرم افزارهایی مانند [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html) استفاده می شود. یکی از مزایای استفاده از فایل‌های MD5 این است که تأیید کنید فایل‌های دانلود شده خراب نیستند.

## فرمت فایل MD5 - اطلاعات بیشتر

معمولاً یک فایل MD5 با همان نام فایل اصلی اما با پسوند md5. ذخیره می شود. برای مثال، اگر نام فایل مرتبط «abc_987_123456.grb» باشد، نام فایل MD5 مربوطه «abc_987_123456.grb.md5» خواهد بود. فایل‌های MD5 به شناسایی اینکه فایل دریافتی یا دانلود شده آسیب‌دیده یا تحت تأثیر محتوای مخرب نیست، کمک می‌کند. به طور خلاصه، فایل های MD5 کامل بودن یک فایل را تضمین می کنند.


## چگونه MD5 Checksum را بررسی کنیم؟

با استفاده از ابزار [md5sum](https://en.wikipedia.org/wiki/Md5sum) به شرح زیر می توان یک فایل را برای MD5 بررسی/تأیید کرد.

```
md5sum -c abc_987_123456.grb.md5
```

## منابع

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)


