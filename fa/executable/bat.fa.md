{
  "date": "2021-06-24",
  "keywords": [
"فایل خفاش",
"فایل bat چیست",
"فایل",
"نمونه فایل bat",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل BAT و APIهایی که می‌توانند فایل‌های BAT را ایجاد و باز کنند، بیاموزید.",
  "title": "BAT - فرمت فایل دسته ای",
  "linktitle": "BAT",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ba-fat"
}
},
  "lastmod": "2021-06-24"
}

## فایل BAT چیست؟
یک فایل BAT به عنوان فایل دسته ای شناخته می شود که با DOS و تمام نسخه های ویندوز، تحت cmd.exe اجرا می شود. این شامل یک سری دستورات خطی در متن ساده است که توسط مفسر خط فرمان برای انجام کارهای مختلف مانند اجرای برنامه های تعمیر و نگهداری در ویندوز یا شروع برنامه های معمولی اجرا می شود. یک فایل دسته ای ممکن است شامل هر دستوری باشد که بتواند توسط مفسر به صورت تعاملی پذیرفته شود و از ساختار کدی استفاده کند که انشعاب شرطی و حلقه زدن را همانطور که در فایل دسته ای نوشته شده است، فعال می کند.
## فرمت فایل BAT
فرمت فایل BAT به سادگی یک اسکریپت است که برای خودکارسازی توالی دستورات که ماهیت تکراری دارند، گنجانده شده است. اصطلاح بچ برای پردازش دسته ای استفاده می شود، می توان آن را اجرای غیر تعاملی در نظر گرفت. بنابراین یک فایل دسته ای ممکن است دسته ای از چندین داده را پردازش نکند. در سیستم عامل دیسک قدیمی (DOS)، فایل دسته ای تحت رابط خط فرمان با تایپ نام فایل و پسوند bat اجرا می شد. سیستم عامل قبلی مبتنی بر رابط گرافیکی مایکروسافت مانند ویندوز مایکروسافت به DOS وابسته بود. کاربران مجبور بودند از DOS برای انجام عملیات معمولی مانند تعمیر، بهینه سازی یا نصب مجدد ویندوز استفاده کنند. بعداً مایکروسافت ویندوز NT را معرفی کرد که به سیستم عامل DOS وابسته نبود. بنابراین، فایل های دسته ای را می توان با استفاده از Command Prompt یا **cmd.exe** در سیستم عامل های امروزی مایکروسافت اجرا کرد.
### پارامترهای دسته ای فایل
Command Prompt از تعدادی متغیر خاص مانند **%0، %1 تا %9** پشتیبانی می کند تا به نام و مسیر کار دسته ای و 9 پارامتر فراخوانی از داخل کار دسته ای اشاره کند. پارامترهای غیر موجود با رشته ای با طول صفر جایگزین می شوند. اگرچه می توان آنها را مشابه متغیرهای محیطی استفاده کرد، اما در محیط ذخیره نمی شوند. مایکروسافت و IBM از این متغیرها به عنوان پارامترهای جایگزین یاد می کنند، در حالی که Novell، Digital Research و Caldera اصطلاح متغیرهای جایگزین را برای آنها معرفی کردند.

در اینجا چند دستور مفید فایل دسته ای وجود دارد:
| فرمان | توضیحات |
------|------------|
| VER | این دستور دسته ای نسخه MS-DOS مورد استفاده شما را نشان می دهد. |
|ASSOC| این یک دستور دسته‌ای است که یک پسوند را با یک نوع فایل (FTYPE) مرتبط می‌کند، پیوندهای موجود را نمایش می‌دهد یا یک ارتباط را حذف می‌کند. |
|CD| این دستور دسته ای به ایجاد تغییرات در یک دایرکتوری دیگر یا نمایش دایرکتوری فعلی کمک می کند. |
|CLS| این دستور دسته ای صفحه را پاک می کند. |
|کپی| این دستور دسته ای برای کپی فایل ها از یک مکان به مکان دیگر استفاده می شود. |
|DEL| این دستور دسته ای فایل ها و نه دایرکتوری ها را حذف می کند. |
|DIR| این دستور دسته ای محتویات یک دایرکتوری را فهرست می کند. |
|تاریخ| این دستور دسته ای به یافتن تاریخ سیستم کمک می کند. |
|ECHO| این دستور دسته‌ای پیام‌ها را نمایش می‌دهد یا بازتاب فرمان را روشن یا خاموش می‌کند. |
|خروج| این دستور دسته ای از کنسول DOS خارج می شود. |
|MD| این دستور دسته ای یک دایرکتوری جدید در مکان فعلی ایجاد می کند. |
| حرکت | این دستور دسته ای فایل ها یا دایرکتوری ها را بین دایرکتوری ها جابجا می کند. |
| مسیر| این دستور دسته ای متغیر مسیر را نمایش می دهد یا تنظیم می کند. |
|مکث| این دستور دسته ای از کاربر درخواست می کند و منتظر می ماند تا یک خط ورودی وارد شود. |
| PROMPPT| از این دستور دسته ای می توان برای تغییر یا تنظیم مجدد دستور cmd.exe استفاده کرد. |
|RD| این دستور دسته ای دایرکتوری ها را حذف می کند، اما دایرکتوری ها قبل از حذف باید خالی باشند. |
|REN| تغییر نام فایل ها و دایرکتوری ها |
|REM| این دستور دسته ای برای اظهار نظر در فایل های دسته ای استفاده می شود و از اجرای محتوای اظهارنامه جلوگیری می کند. |
|شروع| این دستور دسته ای یک برنامه را در پنجره جدید شروع می کند یا یک سند را باز می کند. |
| زمان| این دستور دسته ای زمان را تنظیم یا نمایش می دهد. |
|نوع| این دستور دسته ای محتوای یک فایل یا فایل ها را در خروجی چاپ می کند. |
|VOL| این دستور دسته ای برچسب های حجم را نمایش می دهد. |
|ATTRIB| ویژگی های فایل ها را در دایرکتوری Curret نمایش می دهد یا تنظیم می کند
|CHKDSK| این دستور دسته ای دیسک را برای هر گونه مشکل بررسی می کند. |
|انتخاب| این دستور دسته ای لیستی از گزینه ها را در اختیار کاربر قرار می دهد. |
|CMD| این دستور دسته ای نمونه دیگری از خط فرمان را فراخوانی می کند. |
|COMP| این دستور دسته ای 2 فایل را بر اساس اندازه فایل مقایسه می کند. |
|تبدیل| این دستور دسته ای حجم را از سیستم فایل FAT16 یا FAT32 به سیستم فایل NTFS تبدیل می کند. |
|DRIVERQUERY| این دستور دسته ای تمام درایورهای دستگاه نصب شده و ویژگی های آنها را نشان می دهد. |
|گسترش| این دستور دسته ای فایل ها را از فایل های فشرده کابینت cab استخراج می کند. |
|پیدا کردن| این فرمان دسته ای یک رشته را در فایل ها یا ورودی جستجو می کند و خطوط منطبق را خروجی می دهد. |
|FORMAT| این دستور دسته ای دیسک را برای استفاده از سیستم فایل پشتیبانی شده از ویندوز مانند FAT، FAT32 یا NTFS فرمت می کند و در نتیجه محتوای قبلی دیسک را بازنویسی می کند. |
|HELP| این دستور دسته ای لیستی از دستورات ارائه شده توسط ویندوز را نشان می دهد. |
|IPCONFIG| این دستور دسته ای تنظیمات IP ویندوز را نمایش می دهد. پیکربندی بر اساس اتصال و نام آن اتصال را نشان می دهد. |
|LABEL| این دستور دسته ای یک برچسب دیسک را اضافه، تنظیم یا حذف می کند. |
|بیشتر| این دستور دسته ای محتویات یک فایل یا فایل ها را در یک صفحه نمایش می دهد. |
|NET| بسته به دستور مورد استفاده، خدمات شبکه مختلفی را ارائه می دهد. |
|پینگ| این دستور دسته ای بسته های ICMP/IP echo را از طریق شبکه به آدرس تعیین شده ارسال می کند. |
|خاموش شدن| این دستور دسته ای یک کامپیوتر را خاموش می کند یا کاربر فعلی را از سیستم خارج می کند. |
|SORT| این دستور دسته ای ورودی را از یک فایل منبع می گیرد و محتویات آن را بر اساس حروف الفبا، از A به Z یا Z به A مرتب می کند. خروجی را روی کنسول چاپ می کند. |
|SUBST| این دستور دسته‌ای یک حرف درایو را به یک پوشه محلی اختصاص می‌دهد، تکالیف فعلی را نمایش می‌دهد یا یک تخصیص را حذف می‌کند. |
|SYSTEMINFO| این دستور دسته ای پیکربندی یک کامپیوتر و سیستم عامل آن را نشان می دهد. |
|TASKKILL| این دستور دسته ای به یک یا چند کار پایان می دهد. |
|فهرست وظایف| این دستور دسته ای وظایف، از جمله نام کار و شناسه فرآیند (PID) را فهرست می کند. |
|XCOPY| این دستور دسته ای فایل ها و دایرکتوری ها را به روشی پیشرفته تر کپی می کند. |
|درخت| این دستور دسته ای درختی از همه زیرشاخه های دایرکتوری فعلی را به هر سطحی از بازگشت یا عمق نمایش می دهد. |
|FC |این دستور دسته ای تفاوت های واقعی بین دو فایل را فهرست می کند. |
|DISKPART |این دستور دسته ای ویژگی های پارتیشن های دیسک را نشان می دهد و پیکربندی می کند. |
|TITLE |این دستور دسته ای عنوان نمایش داده شده در پنجره کنسول را تنظیم می کند. |
|SET | لیستی از متغیرهای محیطی را در سیستم فعلی نمایش می دهد. |

## نمونه فایل BAT
اسکریپت های دسته ای معمولاً به صورت فایل های متنی ساده ذخیره می شوند. شامل دستوراتی است که به صورت متوالی اجرا می شوند. این فایل ها با پسوند bat ذخیره می شوند. با استفاده از نرم افزار **Command Interpreter** شناسایی و اجرا می شود. این نرم افزار به صورت بومی در ویندوز مایکروسافت با نام **cmd.exe** موجود است.

در اینجا یک نمونه اسکریپت دسته ای وجود دارد که تمام فایل های موجود در فهرست فعلی را حذف می کند:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## منابع 

* [دسته اسکریپت - راهنمای سریع](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)

* [فایل دسته ای - توسط Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


