{
   "date":"2023-07-18",
   "keywords":[
"PAR",
"فایل PAR",
"نحوه باز کردن فایل par",
"فایل",
"پسوند فایل PAR",
"افزونه",
"فایل"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"فرمت فایل PAR - فایل فهرست پارشیو",
   "description":"درباره قالب PAR و API هایی که می توانند فایل های PAR را ایجاد و باز کنند، بیاموزید.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par-fa",
         "parent":"compression"
}
},
   "lastmod":"2023-07-18"
}

## فایل PAR چیست؟

در آرشیوهای Parchive (PAR)، یک فایل .par به یک فایل فهرستی اشاره دارد که شامل گروهی از حجم های برابری یا بلوک های برابری است. این فایل فهرست برای اهداف تشخیص خطا و بازیابی زمانی که یک یا چند فایل در بایگانی از بین رفته یا آسیب دیده استفاده می شود.

یک آرشیو Parchive معمولاً از هر دو فایل داده اصلی و حجم های برابری مربوطه تشکیل شده است. حجم های برابری با استفاده از الگوریتم های تصحیح خطا Reed-Solomon ایجاد می شوند. این حجم های برابری حاوی اطلاعات اضافی هستند که می توانند برای بازیابی فایل های داده اصلی استفاده شوند.

فایل .par که به عنوان مجموعه حجم برابری نیز شناخته می شود، حاوی اطلاعاتی در مورد ساختار و مکان حجم های برابری در بایگانی است. این به عنوان یک شاخص یا نقشه برای فرآیند بازیابی عمل می کند. با استفاده از فایل .par، نرم افزار تخصصی PAR می تواند تعیین کند که کدام حجم برابری مورد نیاز است و چگونه باید از آنها برای بازسازی فایل های گم شده یا آسیب دیده استفاده کرد.

هنگامی که یک یا چند فایل در بایگانی Parchive غیرقابل دسترسی یا خراب می شوند، می توان از فایل .par به همراه حجم های برابری موجود برای بازیابی داده های از دست رفته استفاده کرد. نرم افزار PAR فایل .par را می خواند، فایل های مفقود یا آسیب دیده را شناسایی می کند و از حجم های برابری برای بازسازی آنها استفاده می کند.

## چگونه یک فایل PAR را باز کنیم؟

برای باز کردن و استفاده از فایل های .par به نرم افزار تخصصی PAR نیاز دارید. در اینجا چند گزینه نرم افزار محبوب که می توانند فایل های .par را مدیریت کنند آورده شده است:

- **QuickPar:** QuickPar یک نرم افزار PAR پرکاربرد برای ویندوز است. این به شما امکان می دهد فایل های PAR را ایجاد، تأیید و تعمیر کنید. می‌توانید یک فایل .par را در QuickPar باز کنید تا یکپارچگی آن را تأیید کنید یا از آن برای تعمیر فایل‌های آسیب‌دیده یا گمشده در بایگانی Parchive استفاده کنید.

- **MultiPar:** MultiPar یکی دیگر از نرم افزارهای محبوب PAR است که برای ویندوز موجود است. از هر دو فرمت فایل PAR و PAR2 پشتیبانی می کند و ویژگی های پیشرفته ای را برای ایجاد، تأیید و تعمیر آرشیوها ارائه می دهد. MultiPar می تواند فایل های .par را باز کند و عملیات تشخیص و بازیابی خطا را بر اساس حجم های برابری ارائه شده انجام دهد.

- **MacPAR deLuxe:** MacPAR deLuxe یک نرم افزار PAR است که به طور خاص برای macOS طراحی شده است. از فرمت های فایل PAR و PAR2 پشتیبانی می کند و عملکردهای مشابه QuickPar و MultiPar را ارائه می دهد. MacPAR deLuxe می‌تواند فایل‌های .par را باز کند و به تأیید آرشیوها و بازیابی فایل‌های آسیب‌دیده یا مفقود کمک کند.

## فرمت فایل PAR - اطلاعات بیشتر

فرمت فایل PAR که معمولاً به آن Parchive گفته می شود، یک فرمت فایل خاص است که برای ایجاد داده های برابری و انجام تشخیص و بازیابی خطا در بایگانی فایل ها استفاده می شود. فرمت فایل PAR معمولاً از سه نوع تشکیل شده است: PAR، PAR2 و PAR3.

- **PAR:** فرمت اصلی فایل PAR که با نام PAR1 نیز شناخته می شود، توسط پروژه Parchive توسعه یافته است. این شامل داده های برابری تولید شده از فایل های داده اصلی است. فایل های PAR سطح پایه ای از تشخیص و بازیابی خطا را ارائه می دهند اما از نظر قابلیت های تصحیح خطا دارای محدودیت هایی هستند.

- **PAR2:** PAR2 نسخه بهبود یافته فرمت فایل PAR است. این قابلیت های پیشرفته تر تصحیح خطا و ویژگی های بهبود یافته را ارائه می دهد. فایل‌های PAR2 معمولاً برای ایجاد داده‌های برابری استفاده می‌شوند که می‌توانند فایل‌های از دست رفته یا آسیب‌دیده را در یک آرشیو بازیابی کنند. فایل‌های PAR2 محافظت بهتری در برابر خرابی داده‌ها ارائه می‌کنند و به طور گسترده برای اهداف آرشیو فایل استفاده می‌شوند.

- **PAR3:** PAR3 is the latest version of the PAR file format and provides further improvements in error correction and recovery. It offers even higher levels of redundancy and error correction capabilities compared to PAR2. فایل‌های PAR3 برای ارائه گزینه‌های حفاظت و بازیابی قوی‌تر برای داده‌های ذخیره‌شده در آرشیو طراحی شده‌اند.

هر دو فرمت فایل PAR2 و PAR3 به طور گسترده توسط نرم افزار PAR پشتیبانی می شوند و توانایی بررسی یکپارچگی فایل ها در یک آرشیو و بازیابی اطلاعات از دست رفته یا آسیب دیده را ارائه می دهند. فایل‌های PAR و PAR2 هنوز معمولاً مورد استفاده قرار می‌گیرند، در حالی که فایل‌های PAR3 به دلیل قابلیت‌های تصحیح خطای پیشرفته‌شان به تدریج مورد پذیرش قرار می‌گیرند.

## منابع
* [Parchive](https://en.wikipedia.org/wiki/Parchive)

