{
  "date": "2021-06-29",
  "keywords": [
"تاکسی",
"افزونه",
"فایل",
"قالب",
"سیستم",
"فایل کابینت ویندوز",
"مایکروسافت",
"نصاب",
"برپایی",
"AdvPak"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CAB - فایل کابینت ویندوز",
  "description": "درباره فرمت فایل CAB و APIهایی که می‌توانند فایل‌های CAB را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CAB",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ca-fab"
}
},
  "lastmod": "2021-06-29"
}

## فایل CAB چیست؟ ##

یک فایل با پسوند cab. متعلق به فایل کابینت ویندوز است که به دسته فایل های سیستم تعلق دارد. این فایلی است که در قالب فایل بایگانی در نسخه‌های مایکروسافت ویندوز که از الگوریتم‌های داده‌های فشرده‌شده پشتیبانی می‌کنند، مانند [LZX](/compression/lzx/)، Quantum و [ZIP](/compression/zip/) ذخیره می‌شود. زمانی که کاربر یا توسعه‌دهنده می‌خواهد داده‌ها و فایل‌های نصب نرم‌افزار را داشته باشد، از این فایل استفاده حیاتی می‌کند. ویژگی‌های فشرده‌سازی داده‌های بدون تلفات و گواهی دیجیتال موجود در این فایل‌ها، این فایل را برای ذخیره و اشتراک‌گذاری چنین فایل‌هایی ایده‌آل می‌کند. این برنامه از نصب کننده های مختلف مایکروسافت مانند Device Installer، SetUp API و AdvPak پشتیبانی می کند.

## تاریخچه مختصر ##

فایل CAB یک نوع فایل فشرده سازی داده است که توسط مایکروسافت توسعه یافته است. در ابتدا الماس نامیده می شد، اما سپس به عنوان فایل CAB، مخفف کلمه Cabinet شناخته شد.

## مشخصات فنی ##

یک فایل CAB معمولاً می‌تواند حداکثر تا 65535 پوشه داشته باشد که به نوبه خود می‌تواند حداکثر شامل 65536 فایل باشد. مکانیسم ذخیره سازی فایل CAB از نظر زمان و مکان کارآمد است زیرا به جای فشرده سازی و ذخیره هر فایل به طور جداگانه، هر پوشه را به عنوان یک بلوک فشرده ذخیره می کند. پوشه های خالی را نمی توان در پوشه های بایگانی CAB ذخیره کرد. فایل CAB اولین بار توسط مایکروسافت توسعه داده شد و در نصب کننده های مختلفی مانند InstallShield با فرمت کمی متفاوت استفاده می شود. فایل های CAB معمولاً به برنامه های خود استخراج کننده متصل می شوند. فایل های مایکروسافت CAB به دلیل نشانگر منحصر به فردشان که به شناسایی فرمت کمک می کند، به راحتی قابل تشخیص هستند. نشانگر منحصربه‌فرد برای همه فایل‌های Microsoft CAB یک پیشوند چهار کلمه‌ای، MSCF است. با دیدن این کد، کاربر به راحتی می تواند یک فایل CAB مایکروسافت را از سایر فایل ها تشخیص دهد و از آن در کمپرسورها یا نسخه ها استفاده کند. فایل‌ها را می‌توان با داده‌های نصب نرم‌افزار بیشتر فشرده کرد، یا داده‌های موجود را می‌توان با استفاده از نرم‌افزار مناسب از حالت فشرده خارج کرد.


## مثال CAB ##

مثال زیر رابطه بین فایل ها و پوشه ها را در ساختار فایل CAB نشان می دهد:

{{< figure src="../cab.png" alt="فرمت فایل CAB" >}}

## ارجاع ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))