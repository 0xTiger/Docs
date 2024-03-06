{
  "date": "2019-12-10",
  "keywords": [
"XLM",
"فایل",
"افزونه",
"فرمت فایل",
"فایل ماکرو اکسل مایکروسافت",
"صفحه گسترده"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "راهنمای فرمت فایل شما برای اینکه بدانید یک فایل ماکرو XLM و APIهایی که می‌توانند فایل‌های XLM را ایجاد و باز کنند چیست.",
  "title": "فایل XLM چیست؟",
  "linktitle": "XLM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-fam"
}
},
  "lastmod": "2019-12-10"
}

## فایل XLM چیست؟

XLM، برای Excel Macro، نوعی از فایل های صفحه گسترده است که برای ذخیره ماکروها استفاده می شود. از نقطه نظر کاربرد، ماکرو مجموعه ای از دستورالعمل هایی است که برای خودکارسازی فرآیندها استفاده می شود. ماکرو برای ضبط مراحلی که به طور مکرر برای قالب فایل [XLS](/spreadsheet/xls/) انجام می‌شود استفاده می‌شود و با اجرای مجدد ماکرو، انجام اقدامات را تسهیل می‌کند. ماکروها با ویژوال بیسیک مایکروسافت برای برنامه ها (VBA) از داخل کتاب کار اکسل با استفاده از ویرایشگر ویژوال بیسیک برنامه ریزی می شوند و می توانند مستقیماً از آنجا اجرا/اشکال زدایی شوند.

## تاریخچه مختصر ##

Microsoft Excel supported programming of macros since its first public launch. The features of macros remained the same through subsequent versions fo Excel with extension as per new features. XLM was the default macro language for Excel through Excel 4.0. Excel 5.0 ماکروها را در VBA به طور پیش فرض ضبط می کرد اما با نسخه 5.0 ضبط XLM همچنان به عنوان یک گزینه مجاز بود. بعد از نسخه 5.0 این گزینه متوقف شد. همه نسخه های اکسل، از جمله اکسل 2010، قادر به اجرای ماکرو XLM هستند، اگرچه مایکروسافت استفاده از آنها را منع می کند.

## ضبط ماکرو در XLM ##

اکسل مراحل آسان برای ضبط یک ماکرو را فراهم می کند. برای کار با ماکروها نیاز است که ابزارهای Developer را نصب کرده باشید. هنگامی که یک ضبط ماکرو در حال انجام است، هر اقدام کاربر را ضبط می کند تا بعداً پخش شود. ضبط ماکرو در واقع شامل تمام مراحلی است که کاربر پس از شروع ضبط انجام می دهد. بنابراین، اگر محتوای یک سلول را پررنگ، مورب بسازید و پس از شروع ضبط ماکرو، توجیه متنی آن را تنظیم کنید، همه این دستورات ثبت خواهند شد. به هر ماکرو ضبط شده می توان یک میانبر نیز برای پخش سریع در آینده اختصاص داد. ضبط ماکرو کد VBA را در قالب یک ماکرو تولید می کند که می تواند با استفاده از ویرایشگر ویژوال بیسیک (VBE) ویرایش شود.

## مدل شیء اکسل ##

ماکروها از روال های VBA در پشت خود استفاده می کنند و برای این منظور از [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model) پیروی می کنند. این مدل اشیاء یک صفحه‌گسترده را برای تعامل با صفحه‌گسترده از طریق نوار ابزار فرمان، نوار فرمان یا جعبه‌های پیام تعریف‌شده توسط کاربر شناسایی می‌کند. به عنوان مثال، دسترسی به ویژگی های کتاب کار با شی Workbook داده می شود. به طور مشابه، شی Worksheet در مدل وجود دارد تا به صورت برنامه‌نویسی با کاربرگ‌های کتاب کار کار کند.

## ماکروها و امنیت ##

VBA اجازه می دهد تا به تمام بخش های برنامه و همچنین سیستم فایل دسترسی داشته باشید و همچنین می تواند خطرناک باشد. این نگرانی در هنگام اشتراک‌گذاری کتاب کار با شخصی که بتواند فایل را در انتهای خود اجرا کند، ایجاد می‌کند. این است که مایکروسافت اکسل در مورد باز کردن چنین فایلی هشدار می دهد. ماکروها را می‌توان با امضای دیجیتال تأیید کرد تا سایر کاربران مطمئن شوند که قابل اعتماد هستند. بنابراین، ماکروها را می توان پس از تأیید منبع آنها فعال کرد.

## منابع ##

* [[MS-XLS] - ساختار قالب فایل باینری اکسل](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [برنامه نویسی ماکرو](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

