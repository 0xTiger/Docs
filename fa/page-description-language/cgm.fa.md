{
  "date": "2019-10-11",
  "keywords": [
"CGM",
"متافایل گرافیک کامپیوتری",
"فایل",
"افزونه",
"فرمت فایل",
"گرافیک برداری",
"توصیفگر متافایل"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل CGM",
  "description": "درباره فرمت فایل CGM و APIهایی که می‌توانند فایل‌های CGM را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CGM",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-cg-fam"
}
},
  "lastmod": "2021-04-23"
}

## فایل CGM چیست؟ ##

متافیل گرافیکی کامپیوتری (CGM) فرمت متافایل رایگان، مستقل از پلتفرم و استاندارد بین المللی برای ذخیره و تبادل گرافیک های برداری (2 بعدی)، گرافیک های شطرنجی و متن است. CGM از یک رویکرد شی گرا و بسیاری از مقررات عملکرد برای تولید تصویر استفاده می کند. CGM از این ویژگی های شی گرا برای قالب بندی مجدد عناصر گرافیکی برای ارائه یک تصویر استفاده می کند. یک متافیل حاوی اطلاعات لازم است که فایل های دیگر را تعریف می کند. در CGM، یک فایل منبع مبتنی بر متن حاوی تمام عناصر گرافیکی است که بعداً می توانند در یک فایل باینری کامپایل شوند. اساسا، CGM راهی برای تسهیل تبادل داده های گرافیکی دو بعدی، مستقل از هر پلتفرم یا دستگاه خاصی است.

فرمت CGM عناصر مختلفی را برای انجام عملکردها و نشانه گذاری اشیا برای تنظیم اولیه هندسی و اطلاعات گرافیکی فراهم می کند. اگرچه CGM برای نمایش هنرهای گرافیکی در صفحات وب جایگزین فرمت های دیگر شده است، زیرا توسط صفحات وب به خوبی پشتیبانی نمی شود، اما همچنان در بین برنامه های صنعتی، هوانوردی و سایر برنامه های فنی بسیار محبوب است. اگرچه کنسرسیوم وب جهانی WebCGM را توسعه داده است، یک رویکرد جایگزین برای استفاده از CGM در وب. اجرای اولیه CGM تصویری از توالی عملیات اساسی سیستم هسته گرافیکی (GKS) بود. در طراحی های حرفه ای چندان مورد استفاده قرار نگرفته است، اما تا حد زیادی با فرمت های دیگری مانند DXF و SVG جایگزین شده است.

## تاریخ ##

CGM در سال 1987 یک استاندارد بین المللی شد (ISO 8632-1987) و همچنین به عنوان یک استاندارد ملی در بریتانیا توسط BSI و ایالات متحده توسط ANSI پذیرفته شد. پس از تعدادی اصلاحات در سال 1991، استاندارد تجدید نظر شده CGM در سال 1992 منتشر شد (ISO 8632:1992). در سال 2001، کنسرسیوم وب جهانی WebCGM را با قابلیت پیشرفته برای استفاده در صفحات وب توسعه داد. در سال 2007 نسخه دوم WebCGM و نسخه سوم در سال 2010 با قابلیت های پیشرفته منتشر شد.

## فرمت فایل CGM ##

متا فایل های گرافیکی کامپیوتری اساساً پایگاه داده ای برای اطلاعات گرافیکی هستند و ابزاری برای ضبط، ذخیره و انتقال داده های گرافیکی فراهم می کنند. در نتیجه، باید یک جزء سیستم گرافیکی برای ایجاد پایگاه داده به طور همزمان همراه با اجرای برنامه در قالب متافیل وجود داشته باشد. در بیشتر موارد، این مؤلفه مولد Metafile است. در کنار آن، به مؤلفه دیگری نیاز است که بتواند داده‌های گرافیکی را در یک متافیل واکشی، تفسیر و ارائه کند. این نیاز با حضور مترجم متافیل برآورده می شود. شکل زیر محیط کاری متافایل گرافیکی را نشان می دهد.

رابطه CGM با سایر اجزای یک سیستم گرافیکی معمولی در شکل بالا نشان داده شده است. همچنین از شکل مشخص است که عملکرد متافایل به خروجی دستگاه نهایی وابسته نیست.

Generally, there are two categories of metafile: **section capture** and **picture capture**. The primary functionality of picture capture metafile is the capturing of device-independent, multiple picture definitions. While session capture metafiles use the system interface to capture the output dialogue in a graphical system. CGM belongs to the category of static picture capture metafiles. CGM provides a well-organized arrangement of components with a two-level structure.

1. توصیف کننده متافیل
1. مجموعه ای از تصاویر منطقی مستقل

هر تصویر مجموعه ای از توصیفگرهای تصویر و بدنه تصویر شامل تعریف تصویر است. توصیفگر متافایل اطلاعات توصیفی را تعریف می کند که به طور یکسان برای همه تصاویر آن متافیل اعمال می شود. این اطلاعات به مفسر کمک می کند تا یک متافیل را به درستی تجزیه کند و منابعی را که برای رندر صحیح یک تصویر مورد نیاز است شناسایی کند. اگرچه توصیفگر تصویر نیز اطلاعات توصیفی را در بر می گیرد، اما تنها می تواند تصویری را که توصیفگر در آن قرار دارد تشخیص دهد. در این فرمت فایل، هر تعریف تصویر مستقل و منطقی است. آنها مستقل از تمام تعاریف تصویر دیگر در یک فایل هستند. درست پس از تفسیر متا توصیفگر، می توان به تصاویر به صورت تصادفی دسترسی پیدا کرد و تفسیر کرد. تغییر در وضعیت تصاویر قبلی هیچ تاثیری بر جانشینان آنها ندارد. این استقلال تصویر یکی دیگر از ویژگی‌های برجسته CGM است. CGM انتخاب مستقیم رنگ ها و انتخاب مبتنی بر شاخص را مشخص می کند. در حالت اول، مشخص کننده رنگ از یک RGB سه گانه تشکیل شده است در حالی که بعداً، مشخص کننده رنگ نمایه ای را در جدول رنگی نشان می دهد.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
