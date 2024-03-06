{
  "date": "2019-10-11",
  "keywords": [
"XPS",
"مشخصات کاغذ XML",
"فایل",
"افزونه",
"فرمت فایل",
"EMF",
"PDF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPS - فرمت فایل طرح بندی صفحه",
  "description": "درباره قالب فایل XPS و APIهایی که می‌توانند فایل‌های XPS را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "XPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xp-fas"
}
},
  "lastmod": "2021-04-23"
}

## فایل XPS چیست؟

یک فایل XPS فایل های طرح بندی صفحه را نشان می دهد که بر اساس مشخصات کاغذ XML ایجاد شده توسط مایکروسافت است. این به عنوان جایگزینی برای فرمت فایل EMF توسعه یافته است و شبیه فرمت فایل [PDF](/pdf/) است، اما از XML در طرح‌بندی، ظاهر و اطلاعات چاپ یک سند استفاده می‌کند. در واقع، توجیه بیشتری دارد که بگوییم XPS تلاشی برای PDF است، اما به دلایل بسیاری نتوانسته محبوبیت کافی را به عنوان متعلق به PDF بدست آورد. مایکروسافت XPS Document Writer را به طور پیش فرض از ویندوز 7 به بعد برای ایجاد فایل های XPS ارائه می دهد. فایل های XPS را می توان با انتخاب Microsoft XPS Document Writer به عنوان چاپگر هنگام چاپ سند ایجاد کرد.

بینندگان XPS به عنوان بخشی از ویندوز ویستا، ویندوز 7، ویندوز 8 و اینترنت اکسپلورر 6 یا جدیدتر ادغام می شوند. فایل های XPS پس از تولید فقط خواندنی می شوند. این امر به اطمینان کاربر نسبت به اسناد دریافتی ارسال شده به عنوان XPS برای صحت سند می افزاید. یک سند XPS می تواند حاوی یک یا چند صفحه باشد که از سند اصلی تبدیل شده است.

## تاریخچه مختصر ##

مایکروسافت مشخصات XPS را به Ecma International ارسال کرد. در ژوئن 2007، کمیته فنی Ecma 46 (TC46) برای توسعه استانداردی بر اساس مشخصات کاغذ OpenXPS راه اندازی شد. Ecma International استاندارد Ecma (ECMA-388) [XPS specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) را در ژوئن 2009 در مجمع عمومی 97 تصویب کرد.

## فرمت فایل XPS ##

فرمت XPS شامل نشانه گذاری XML است که ترکیب یک سند و ظاهر بصری هر صفحه را به همراه قوانین رندر برای نمایش یا چاپ سند تعریف می کند. تمام اطلاعات را برای ایجاد مجدد یک سند در هر سیستمی حفظ می کند که آن را مستقل از منابع موجود در آن سیستم می کند. این فرمت در اصل یک آرشیو ZIP است و اگر پسوند فایل را به ZIP تغییر نام دهید، فایل های تشکیل دهنده ای را خواهید دید که حاوی داده های سند هستند. این اسناد عبارتند از:

* فایل های صفحه سند (fpage.) - شامل محتوای سند و تنظیمات قالب سند است. هر صفحه در سند XPS یک فایل FPAGE دارد.

* فایل تنظیمات سند (fdoc.) - تنظیمات موجود در بایگانی XPS را ذخیره می کند.

* فایل های قطعه سند (frag.) - تنظیمات فایل XPS واقعی را تعیین می کند و هر صفحه در سند فایل .frag خود را دارد.


{{< figure src="../XPS-1.png" alt="فرمت فایل XPS" >}}

این فایل‌ها محتویات سند را به گونه‌ای حفظ می‌کنند که برای مثال، اگر شخصی فونت‌های مشابهی را روی دستگاه خود نصب نکرده باشد، نمایشگر XPS همچنان آن فونت‌های اصلی را ارائه می‌کند. این به معنای گنجاندن فایل نشانه گذاری XML برای هر یک است:

* صفحه

* متن

* فونت های تعبیه شده

* تصاویر شطرنجی

* گرافیک برداری 2 بعدی

* مدیریت حقوق دیجیتال


فرمت XPS Document شامل مجموعه ای از قطعات و روابط کاملاً تعریف شده است که هر کدام هدف خاصی را در سند انجام می دهند. این قالب همچنین ویژگی‌های بسته را گسترش می‌دهد، از جمله امضای دیجیتال، ریز عکس‌ها و interleaving.

یک سند معمولی XPS به شکل زیر است و می تواند در پرتو فرمت فایل XPS specifications تجزیه و تحلیل شود.

{{< figure src="../XPS-2.png" alt="فرمت فایل XPS" >}}


## منابع ##
* [مشخصات فرمت فایل XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - توسط Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

