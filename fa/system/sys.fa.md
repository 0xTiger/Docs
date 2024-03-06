{
  "date": "2021-07-08",
  "keywords": [
"SYS",
"افزونه",
"فایل",
"قالب",
"سیستم",
"راننده",
"فایل سیستم",
"برنامه ها",
"کامپیوتر",
"کاربرد"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "SYS - فرمت فایل سیستم",
  "description": "با فرمت فایل SYS و APIهایی که می توانند فایل های SYS را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "SYS",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sy-fas"
}
},
  "lastmod": "2021-07-08"
}

## فایل SYS چیست؟ ##

فایل‌های SYS «فایل‌های سیستم» هستند که در برنامه‌های Windows OS و MS-DOS استفاده می‌شوند. این فایل ها مستقیماً باز نمی شوند و شامل درایور و پیکربندی دستگاه می شوند. فایل‌های SYS حاوی فایل‌های توابع اصلی سیستم عامل هستند. این فایل‌های حیاتی درایور دستگاه محسوب می‌شوند و همچنین می‌توانند برای حل هر مشکلی از راننده مسابقه استفاده شوند. اینها مسئول عملکرد صحیح یک سیستم کامپیوتری هستند و فایلهای .sys باید صحیح و کامل باشند.


## مشخصات فنی ##

فایل‌های .sys در واقع زیرمجموعه فرمت [BMP](/image/bmp/) هستند زیرا فقط ترکیب‌های خاصی را مجاز می‌دانند. فرمت معمول این فایل ها مانند LOGOS.SYS، LOGOW.SYS و LOGO.SYS است. هر فایل دیگری این فرمت را ندارد.

این فایل ها بیشتر در هنگام نصب در پوشه *C* ویندوز استفاده می شوند. اکثر مشکلاتی که حول محور درایورهای دستگاه می چرخند با به روز رسانی سیستم عامل ویندوز حل می شوند. جزئیات و اطلاعات این فایل ها با استفاده از برنامه های داخلی سیستم عامل ویندوز قابل مشاهده است. اینها همچنین شامل ارجاع به ماژول های مختلف در یک سیستم عامل هستند.
برخی از نمونه فایل های سیستم عبارتند از:

* IO.SYS (این درایورهای دستگاه سیستم عامل دیسک را ذخیره می کند)

* MSDOS.SYS (اینها حاوی هسته یا کد اصلی سیستم عامل هستند)

* CONFIG.SYS (اینها شامل گزینه های پیکربندی مختلف هستند)

* KEYBOARD.SYS (اینها حاوی اطلاعات مربوط به چیدمان صفحه کلید هستند) 

* COUNTRY.SYS (این اطلاعات مربوط به کشور و صفحه کد را شامل می شود)


## فرمت فایل SYS ##

مایکروسافت فایل ها را با پسوندهای .sys توسعه داده است. متغیرها و توابع در فایل های SYS گنجانده شده است. اینها بیشتر توسط سیستم عامل مایکروسافت استفاده می شود. این فایل ها عمدتا در دایرکتوری ریشه دیسک قرار دارند:

* C:\Windows\system32\drivers

* C:\Windows\WinSxS


برخی از هشدارهای رایج در مورد فایل های SYS به شرح زیر است:

* نام این فایل ها نباید تغییر کند زیرا این فایل ها وظیفه توابع و متغیرهای اصلی سیستم عامل را بر عهده دارند.
* این فایل ها نباید حذف شوند زیرا عدم وجود این فایل ها باعث ایجاد خطا می شود
* فایل های .sys نباید از اینترنت دانلود شوند تا زمانی که از مشروعیت منبع مطمئن شوید.
* نباید با این فایل ها سر و کار داشت زیرا تغییر آنها یا درهم ریختن آنها باعث خطاهای جدی سیستم می شود
* اگر این فایل‌ها توسط ویروس یا بدافزار خراب شدند، باید دوباره نصب شوند

## مثال SYS ##

نمونه زیر نمونه ای از یک فایل پیکربندی ساده سیستم SYS است:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```