{
  "date": "2021-03-08",
  "keywords": [
"RB",
"دستگاه کتاب الکترونیکی موشک Nuvo Media",
"فایل",
"افزونه",
"قالب",
"کتاب الکترونیکی"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره قالب فایل RB برای دستگاه و APIهای Nuvo Media's Rocket eBook که می‌توانند فایل‌های RB را ایجاد و باز کنند، بیاموزید.",
  "title": "RB - فایل کتاب الکترونیکی موشک",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-r-fab"
}
},
  "lastmod": "2021-03-08"
}

## فایل RB چیست؟

The file with extension .rb holds the Rocket eBook content. The Rocket eBook is actually a device made by Nuvo Media; they released this device in 1998. اگرچه Rocket eBook قادر به نمایش تصاویر است، اما فقط در نمایش سیاه و سفید. دارای صفحه نمایش 106 dpi یا 480 x 320 پیکسل در صفحه نمایش لمسی 4.5 x 3 اینچی. Rocket eBook از طریق یک پورت سریال به کامپیوتر متصل می شود تا کتاب های الکترونیکی را در قالب فایل RB دانلود کند. فایل‌های RB قادر به استفاده از DRM هستند، اما این فناوری در کتاب‌های الکترونیکی مدرن استفاده نمی‌شود. فایل RB به طور معمول شامل یک فایل HTML با تصاویر و یک فایل شبه OPF با تمام ابرداده ها (.info) است.

## مشخصات فنی فرمت فایل RB ##

یک عدد جادویی (به صورت هگزا) در 4 بایت اول فایل ظاهر می شود: B0 0C B0 0C.

به نظر می رسد که دو بایت بعدی یک شماره نسخه هستند، مانند 02 00 که مخفف نسخه اصلی 2 و نسخه کوچک 0 است.

چهار بایت بعدی حاوی متن NUVO و به دنبال آن 4 بایت 00h است.

The next 4-byte is the date when the book was created, encoded as an int16. این ما را در افست 0Eh قرار می دهد. نسخه قدیمی ORocketLibrary ارزش کامل سال را رمزگذاری می کرد (یعنی 1999 CF 07 بود، 2000 D0 07 بود). در نسخه اخیر، tm_year کلمه به کلمه ذخیره می شود، یعنی 100 برای سال 2000 (64 00). بعد از سال یک int8 می آید که نشان دهنده عدد 1 ماه نسبی است و یک int8 نشان دهنده روز ماه است.

6 بایت بعدی 00 ساعت است. برای تنظیم زمان، ممکن است این موارد رزرو شده باشند.

افست مطلق جدول مطالب در یک int32 در افست 18 ساعت موجود است.

بعد از این یک int32 حاوی طول فایل .rb است. این برای تعیین کامل بودن یا نبودن فایل ها استفاده می شود.

به نظر می رسد که کل این تکه بایت (20 ساعت تا 128 ساعت) فقط برای عنوانی که رمزگذاری شده است مورد نیاز باشد. در عناوین غیر رمزگذاری شده، آنها همیشه صفر هستند.

در بیشتر موارد، فهرست مطالب به شرح زیر است (در افست 128). با شمارش int32 تعداد ورودی های صفحه (بخش های فایل .rb) در ToC شروع می شود. هر ورودی شامل یک نام (صفر شده تا 32 بایت)، و به دنبال آن 3 int32 است: طول بخش داده، موقعیت در فایل .rb، و یک پرچم برای این ورودی. از امروز، مقادیر شناخته شده عبارتند از: 1 (رمزگذاری شده)، 2 (صفحه اطلاعات)، و 8 (ضعف شده). نام‌ها همگی در صورت لزوم طراحی شده‌اند تا اطمینان حاصل شود که همه آنها منحصر به فرد هستند.

## منابع

* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)


