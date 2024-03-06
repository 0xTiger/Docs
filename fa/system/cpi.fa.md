{
   "date":"2023-10-18",
   "keywords":[
"cpi",
"فایل cpi",
"فایل اطلاعات صفحه کد cpi",
"نحوه باز کردن فایل cpi",
"فایل",
"پسوند فایل cpi",
"افزونه",
"فایل"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"فرمت فایل CPI - فایل اطلاعات صفحه کد",
   "description":"درباره فرمت فایل اطلاعات صفحه کد صفحه CPI و APIهایی که می‌توانند فایل‌های CPI را ایجاد و باز کنند، بیاموزید.",
   "linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi-fa",
         "parent":"system"
}
},
   "lastmod":"2023-10-18"
}

## فایل CPI چیست؟

یک فایل «.cpi»، در زمینه سیستم‌عامل‌های مایکروسافت ویندوز و داس، معمولاً **«فایل اطلاعات صفحه کد» است.** این فایل‌ها حاوی اطلاعاتی درباره صفحات کد مورد استفاده برای رمزگذاری متن و نگاشت مجموعه کاراکترها هستند. صفحات کد برای نمایش و پردازش متن در زبان ها و مجموعه کاراکترهای مختلف ضروری هستند.

در زمینه ویندوز و داس، از صفحات کد برای تعریف نحوه نمایش و کدگذاری کاراکترها در زبان ها و مناطق مختلف استفاده می شود. این صفحات کد تعیین می کنند که چگونه کاراکترها در حافظه ذخیره شده و روی صفحه نمایش داده می شوند. هر صفحه کد دارای شناسه منحصربه‌فرد است و فایل‌های «.cpi» اطلاعات مربوط به این صفحات کد را ذخیره می‌کنند، از جمله جزئیاتی مانند نگاشت کاراکترها و اطلاعات فونت.

فایل‌های «.cpi» معمولاً در فهرست‌های سیستم‌های Windows یا DOS یافت می‌شوند و نقش مهمی در فعال کردن سیستم‌عامل برای نمایش صحیح متن برای مناطق مختلف و مجموعه کاراکترها دارند. آنها به سیستم کمک می کنند تا بفهمد چگونه کاراکترها را از زبان ها و رمزگذاری های مختلف تفسیر و ارائه کند.

## فایل های اطلاعات صفحه کد

اجازه دهید نگاهی دقیق‌تر به فایل‌های اطلاعات صفحه کد (.cpi) و نحوه عملکرد آنها در چارچوب MS-DOS و نسخه‌های قبلی مایکروسافت ویندوز بیندازیم:

1.  ** رمزگذاری کاراکتر و صفحات کد **: صفحات کد جزء مهمی از نحوه کدگذاری و نمایش متن در رایانه هستند. آنها رمزگذاری کاراکتر را برای زبان یا مجموعه کاراکترهای خاص تعریف می کنند. هر صفحه کد مقادیر عددی (نقاط کد) را به کاراکترها اختصاص می دهد و به رایانه اجازه می دهد آنها را نمایش و نمایش دهد. به عنوان مثال، صفحه کد 437 معمولاً در ایالات متحده و اروپای غربی استفاده می شود، در حالی که کد صفحه 850 برای رمزگذاری لاتین-1 استفاده می شود.
    
2.  **راه‌اندازی سیستم**: در طول راه‌اندازی سیستم (هنگامی که کامپیوتر بوت می‌شود)، MS-DOS و نسخه‌های قدیمی‌تر ویندوز فایل‌های «.cpi» را می‌خوانند تا تعیین کنند کدام صفحات کد را پشتیبانی می‌کنند. این اطلاعات برای رندر متن، ورودی صفحه کلید و تبدیل مجموعه کاراکتر بسیار مهم بود.
    
3.  **نمایشگر و پشتیبانی از صفحه کلید**: این فایل ها اطلاعاتی را در مورد نحوه نمایش کاراکترها بر روی صفحه و اینکه کدام مجموعه کاراکترها یا صفحات کد باید برای ورودی صفحه کلید پشتیبانی شوند، ارائه می دهند. صفحات کد مختلف مجموعه کاراکترهای متفاوتی را تعریف می کنند، بنابراین این فایل ها به سیستم عامل کمک می کنند تا بدانند چگونه ورودی کاربر را مدیریت کند و متن را به درستی نمایش دهد.
    
4.  **محلی سازی**: فایل های `.cpi` برای بومی سازی سیستم عامل ضروری هستند. آنها سیستم را قادر می سازند تا با زبان ها، مناطق و مجموعه کاراکترهای مختلف سازگار شود و این امکان را برای کاربران در سراسر جهان فراهم می کند که از MS-DOS یا Windows به زبان های دلخواه خود استفاده کنند.
    
5.  **چندین فایل «.cpi»**: در رایانه با پشتیبانی چند زبانه، ممکن است چندین فایل «.cpi» مربوط به صفحات کد مختلف پیدا کنید. برای مثال، سیستم ممکن است «437.cpi» برای ایالات متحده، «850.cpi» برای Latin-1، «852.cpi» برای اروپای مرکزی و غیره داشته باشد. فایل مناسب بر اساس محلی کاربر یا صفحه کد انتخاب شده بارگذاری می شود.
    
6.  **اطلاعات قلم**: علاوه بر نگاشت کاراکترها، این فایل ها ممکن است حاوی اطلاعات فونت باشند و مشخص کنند که از کدام فونت برای هر صفحه کد استفاده شود. این برای رندر متن در سبک و اندازه مناسب مهم است.
    
7.  **سیستم‌های قدیمی**: فایل‌های «.cpi» در نسخه‌های قدیمی‌تر MS-DOS و Windows رایج‌تر بودند. نسخه های مدرن ویندوز (مانند ویندوز 10 و جدیدتر) معمولاً از یونیکد برای رمزگذاری متن استفاده می کنند که از طیف گسترده ای از کاراکترها و زبان ها پشتیبانی می کند. یونیکد پردازش متن را برای محیط های چند زبانه ساده می کند و برای نرم افزارهای مدرن استاندارد است.

## چگونه فایل CPI را باز کنیم؟

باز کردن فایل .CPI (اطلاعات صفحه کد) یک اقدام معمولی کاربر نیست و این فایل ها معمولاً قرار نیست به صورت دستی باز شوند. آنها توسط سیستم عامل برای مدیریت رمزگذاری متن و مجموعه کاراکترها استفاده می شوند و محتوای آنها به طور خودکار توسط سیستم قابل دسترسی و استفاده است.

با این حال، اگر علاقه مند به مشاهده محتوای فایل .CPI برای اهداف اطلاعاتی هستید، می توانید آن را با ویرایشگر متن یا نمایشگر هگزا دسیمال باز کنید. در اینجا نحوه تلاش برای باز کردن فایل .CPI آمده است:

1.  **ویرایشگر متن**: می توانید از ویرایشگر متن مانند Notepad (در ویندوز) یا هر ویرایشگر متن ساده در سایر سیستم عامل ها برای باز کردن و مشاهده فایل .CPI استفاده کنید. به خاطر داشته باشید که محتویات فایل‌های .CPI قرار نیست برای انسان قابل خواندن باشد و ممکن است مجموعه‌ای از کاراکترها را ببینید که تفسیر آنها دشوار است.
    
2.  **نمایشگر هگزادسیمال**: از یک نمایشگر هگزا دسیمال یا ویرایشگر هگزا می توان برای باز کردن و بازرسی محتوای فایل .CPI به شکل باینری خام آن استفاده کرد. ویرایشگرهای Hex نمای دقیق تری از داده های فایل ارائه می دهند که اگر سعی در درک ساختار آن دارید می تواند مفید باشد. نمونه هایی از این نرم افزارها عبارتند از HxD، Hex Fiend (برای macOS) و 010 Editor.

## سایر فایل های CPI

در اینجا انواع فایل دیگری وجود دارد که از پسوند فایل **.cpi** استفاده می کنند.

**ویدیو و سیستم**
- [CPI - AVCHD Video Clip Information](/video/cpi/)
- [CPI - Codepage Information File](/system/cpi/)

## منابع
* [صفحه کد](https://en.wikipedia.org/wiki/Code_page)

