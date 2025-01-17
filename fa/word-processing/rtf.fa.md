{
  "date": "2019-10-11",
  "keywords": [
"فایل rtf",
"فرمت فایل rtf",
"فایل rtf چیست",
"فایل",
"مثال rtf",
"پسوند فایل rtf",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RTF - قالب متن غنی",
  "description": "درباره فرمت فایل RTF و API هایی که می توانند فایل های RTF را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "RTF",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-rt-faf"
}
},
  "lastmod": "2019-09-10"
}

## فایل RTF چیست؟

Rich Text Format (**RTF**) که توسط مایکروسافت معرفی و مستند شده است، روشی برای رمزگذاری متن و گرافیک فرمت شده برای استفاده در برنامه ها است. این فرمت تبادل اسناد بین پلتفرمی با سایر محصولات مایکروسافت را تسهیل می‌کند و در نتیجه به هدف قابلیت همکاری کمک می‌کند. این قابلیت آن را تبدیل به استانداردی برای انتقال داده بین نرم افزارهای پردازش متن می کند و از این رو، محتویات را می توان از یک سیستم عامل به سیستم عامل دیگر بدون از دست دادن قالب بندی سند منتقل کرد. مشخصات فرمت فایل توسط مایکروسافت برای عمومی download در دسترس است و می توان از دیدگاه توسعه دهنده به آنها اشاره کرد.

## تاریخچه مختصر فرمت فایل RTF ##

RTF file format has underwent several revisions since its publication. Its official version for read/write was published as part of Microsoft Word 3.0 for Macintosh with version 1.0 specifications. The final version of specifications, 1.9.1 was published by Microsoft in Mar 2008. بعد از این دیگر هیچ پیشرفتی در مشخصات انجام نمی شود. در حال حاضر، تقریباً همه سیستم عامل ها دارای برنامه های کاربردی غنی از ویژگی های بیشتری هستند که استفاده از فرمت فایل RTF را به حداقل رسانده یا از بین برده اند.

## مشخصات فرمت فایل RTF ##

RTF serves as a standard of data transfer between word processing software and transfer of content from one operating system to another. This is achieved using control words that were introduced by Microsoft Office Word up through 2007. یک فایل RTF استاندارد شامل ASCII برای نمایش متن غنی و با کاراکترهای غیر ASCII است که به مقادیر کد مناسب تبدیل می شود. نسخه‌های جدیدتر Word می‌توانند فایل‌های RTF تولید شده با نسخه‌های قبلی را بخوانند، در حالی که نسخه‌های قدیمی‌تر کلمات کنترلی و گروه‌هایی را که نمی‌فهمند نادیده می‌گیرند.

### درک مبانی RTF ###

فایل های RTF از متن ساده 7 بیتی ASCII استفاده می کنند که شامل موارد زیر است:

* کلمات را کنترل کنید

* نمادهای کنترل، و

* گروه ها.


اینها به عنوان بلوک‌های ساختمانی برای نمایش داده‌های RTF به عنوان کدگذاری متن و کاراکتر قابل درک عمل می‌کنند.

#### کنترل ورد ####

این دستورات فرمت شده خاصی را نشان می دهد که برای علامت گذاری کاراکترها برای نمایش استفاده می شود و نمی تواند بیشتر از 32 حرف باشد. یک کلمه کنترلی به صورت زیر تعریف می شود:

\<ASCII Letter Sequence> //<//Delimiter//> //

هر کلمه کنترلی به حروف کوچک و بزرگ حساس است و با یک اسلش شروع می شود. دنباله حروف ASCII می تواند شامل الفبای ASCII (a تا z و A تا Z) باشد. این<Delimite> پایان نام کلمه کنترل را نشان می دهد و می تواند یکی از موارد زیر باشد:

* فضا. این فقط برای محدود کردن یک کلمه کنترل عمل می کند و در پردازش بعدی نادیده گرفته می شود.

* یک رقم عددی یا یک علامت منفی ASCII، که نشان می دهد یک پارامتر عددی با کلمه کنترل مرتبط است. سپس دنباله دیجیتال بعدی با هر کاراکتری غیر از یک رقم ASCII (معمولاً یک کلمه کنترلی دیگر که با یک اسلش شروع می شود) مشخص می شود. پارامتر می تواند یک عدد اعشاری مثبت یا منفی باشد. محدوده مقادیر برای عدد اسمی -32768 تا 32767 است، یعنی یک عدد صحیح 16 بیتی امضا شده است. تعداد کمی از کلمات کنترلی مقادیری در محدوده -2,147,483,648 تا 2,147,483,647 (اعداد صحیح امضا شده 32 بیتی) می گیرند. این کلمات کنترلی عبارتند از **\binN**، **\revdttmN//**، **\rsidN** کلمات کنترلی مرتبط و برخی ویژگی‌های تصویر مانند **\bliptagN**. در اینجا **N** مخفف پارامتر عددی است. یک تجزیه کننده RTF باید حداکثر تا 10 رقم را که به صورت اختیاری با علامت منفی جلوتر از آن قرار می گیرد، در نظر بگیرد. اگر جداکننده یک فاصله باشد، کنار گذاشته می‌شود، یعنی در پردازش بعدی گنجانده نمی‌شود.

* هر کاراکتری غیر از یک حرف یا یک رقم. در این حالت، کاراکتر تعیین کننده کلمه کنترل را خاتمه می دهد و بخشی از کلمه کنترل نیست. مانند علامت معکوس "\"، که به این معنی است که یک کلمه کنترلی جدید یا یک نماد کنترلی دنبال می شود.


#### نماد کنترل ####

یک نماد کنترل نشان دهنده یک رخداد خاص است که بسته به محتوای آن معنای خاصی دارد. این شامل یک بک اسلش و به دنبال آن یک کاراکتر خاص (غیر الفبایی) است و هیچ جداکننده ای ندارد.

#### گروه ####

یک گروه می تواند شامل متن، کلمات کنترلی یا نمادهای کنترلی باشد که در پرانتز قرار دارند (**{ }**). مهاربند باز (**{**) شروع گروه و مهاربند بسته شدن ( **}**) نشان دهنده پایان گروه است. هر گروه متن تحت تاثیر گروه و ویژگی های مختلف آن متن را مشخص می کند.

### ساختار فایل RTF ###

یک فایل RTF دارای نحو استاندارد زیر است:

Rich Text Format (**RTF**) که توسط مایکروسافت معرفی و مستند شده است، روشی برای رمزگذاری متن و گرافیک فرمت شده برای استفاده در برنامه ها است. این فرمت تبادل اسناد بین پلتفرمی با سایر محصولات مایکروسافت را تسهیل می‌کند و در نتیجه به هدف قابلیت همکاری کمک می‌کند. این قابلیت آن را تبدیل به استانداردی برای انتقال داده بین نرم افزارهای پردازش متن می کند و از این رو، محتویات را می توان از یک سیستم عامل به سیستم عامل دیگر بدون از دست دادن قالب بندی سند منتقل کرد. مشخصات فرمت فایل توسط مایکروسافت برای عمومی download در دسترس است و می توان از دیدگاه توسعه دهنده به آنها اشاره کرد.

#### سربرگ RTF ####

یک سربرگ RTF دارای نمایش زیر است.

|فیلد|توضیحات
---|---|
|\<header> |**\rtf1\fbidis**؟ \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

جداول سرصفحه در صورت وجود باید به این ترتیب ظاهر شوند. فایل RTF می‌تواند شامل گروه‌هایی برای فونت‌ها، سبک‌ها، رنگ صفحه، تصاویر، پاورقی‌ها، نظرات (حاشیه‌نویسی)، سرصفحه‌ها و پاورقی‌ها، اطلاعات خلاصه، فیلدها، نشانک‌ها، ویژگی‌های قالب‌بندی سند، بخش، پاراگراف و کاراکتر، ریاضیات، تصاویر و اشیاء اگر فونت، فایل، سبک، رنگ، علامت بازبینی، و گروه‌های اطلاعات خلاصه و ویژگی‌های قالب‌بندی سند در فایل گنجانده شده‌اند، باید در هدر RTF، که قبل از بدنه RTF است، ظاهر شوند. در صورت عدم استفاده از محتوای هر گروه، گروه را می توان حذف کرد. هر گروهی که از ویژگی های تعریف شده در گروه دیگر استفاده می کند باید بعد از گروهی که آن ویژگی ها را تعریف می کند ظاهر شود. به عنوان مثال، خواص رنگ و فونت باید قبل از گروه سبک باشد.

#### نسخه RTF ####

یک سند RTF باید با این شش کاراکتر شروع شود:

```
{\rtf1
```
که در آن عدد 1 شماره نسخه RTF را نشان می دهد.

#### مجموعه کاراکتر ####

بعد از {\rtf1، سند باید مشخص کند که از چه مجموعه کاراکتری استفاده می کند. روش اعلام مجموعه کاراکترها با یکی از این دستورات است:

`\ansi` - سند در مجموعه کاراکترهای ANSI است که به عنوان کد صفحه 1252 نیز شناخته می شود، مجموعه کاراکترهای معمول MSWindows.

`\mac` - سند در مجموعه کاراکتر MacAscii است، مجموعه کاراکترهای معمول در نسخه های قدیمی (قبل از 10) سیستم عامل Mac.

`\pc` - سند در کد DOS صفحه 437، مجموعه کاراکترهای پیش‌فرض برای MS-DOS است. تایپیست‌هایی که حافظه عضلانی خوبی دارند متوجه می‌شوند که این مجموعه کاراکتری است که هنوز برای تفسیر کدهای «عددی Alt» استفاده می‌شود—یعنی وقتی Alt را نگه می‌دارید و «130» را روی صفحه‌کلید عددی تایپ می‌کنید، یک é تولید می‌کند، زیرا کاراکتر 130 در CP437 یک é است. این تقریباً تنها کاربردی است که CP437 این روزها می بیند.

`\pca` - سند در صفحه کد DOS 850 است که به عنوان صفحه کد چند زبانه MS-DOS نیز شناخته می شود.

#### فرمان فونت ####

تعریف مجموعه کاراکتر با دستور \deffN دنبال می شود. این نشان می دهد که شماره فونت N فونت پیش فرض این سند است. شماره فونت N از جدول فونت ارجاع داده می شود. دستور '\deffN' از نظر فنی اختیاری است، اما باید در سمت امن به عنوان یک پرولوگ معمولی وجود داشته باشد، مانند انتخاب فونت 0 به عنوان فونت پیش‌فرض.

«{\rtf1\ansi\deff0».

#### جدول فونت ####

تمام فونت‌هایی که می‌توانند در یک سند استفاده شوند در یک جدول فونت فهرست شده‌اند که در آن هر فونت با یک شماره فونت نشان داده می‌شود. سند باید یک جدول فونت داشته باشد اگرچه برخی از برنامه ها بدون آن نیز کار می کنند.

نحو یک جدول فونت {\fonttbl //...declarations//...} است، که در آن هر اعلان این نحو اولیه را دارد:

`{\fnumber\familycommand Fontname;}`

یک جدول فونت با چهار اعلان به شرح زیر است:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

در سندی با آن جدول فونت، «{\f2 stuff}» «موارد» را در Courier New چاپ می‌کند. یک فونت تا زمانی که در جدول فونت فهرست نشده باشد را نمی توان در سند استفاده کرد.

### انتهای سند ###

هر سند RTF باید با یک } خاتمه یابد تا گروه باز شده توسط { که اولین کاراکتر سند است بسته شود. هیچ چیز نمی تواند از } نهایی پیروی کند، به جز احتمالاً یک خط جدید.

## منابع ##

* [قالب متن غنی](https://en.wikipedia.org/wiki/Rich_Text_Format)


