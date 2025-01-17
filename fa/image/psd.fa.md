{
  "date": "2019-10-11",
  "keywords": [
"فایل psd",
"فرمت فایل psd",
"فایل psd چیست",
"فایل",
"نمونه psd",
"پسوند فایل psd",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSD - فرمت فایل تصویر فتوشاپ",
  "description": "درباره فرمت فایل PSD و API هایی که می توانند فایل های PSD را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "PSD",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-fad"
}
},
  "lastmod": "2019-09-10"
}

## فایل PSD چیست؟

PSD، Photoshop Document، فرمت فایل بومی Adobe Photoshop را نشان می‌دهد که برای طراحی و توسعه گرافیک استفاده می‌شود. فایل های PSD ممکن است شامل لایه های تصویر، لایه های تنظیم، ماسک لایه، حاشیه نویسی، اطلاعات فایل، کلمات کلیدی و سایر عناصر خاص فتوشاپ باشد. فایل های فتوشاپ دارای پسوند پیش فرض PSD هستند و حداکثر ارتفاع و عرض آن 30000 پیکسل و محدودیت طول آن دو گیگابایت است.

## مشخصات فرمت فایل PSD ##

داده ها در یک فایل PSD به ترتیب بایت اندیان بزرگ ذخیره می شوند. این به معنی تعویض اعداد صحیح کوتاه و بلند هنگام خواندن یا نوشتن در پلتفرم ویندوز است. فرمت فایل فتوشاپ به پنج بخش اصلی تقسیم می شود. این نشانگرهای طول زیادی دارد که می توان از آنها برای حرکت از یک بخش به بخش بعدی استفاده کرد. نشانگرهای طول معمولاً با بایت ها پوشانده می شوند تا به نزدیکترین فاصله 2 یا 4 بایت گرد شوند. پنج بخش عمده عبارتند از:

* سربرگ فایل

* داده های حالت رنگ

* منابع تصویری

* اطلاعات لایه و ماسک

* داده های تصویری


برای انطباق، داده ها باید در تمام این فیلدها در بخش نوشته شوند، زیرا فتوشاپ ممکن است سعی کند کل بخش را بخواند. همچنین به این معنی است که هنگام نوشتن روی یک فایل، صفرها در فیلدهای حذف شده نوشته می شوند. فیلد طول در بخش‌های مشخص شده با طول باید برای تصمیم‌گیری زمان توقف خواندن استفاده شود. در بیشتر موارد، فیلد طول تعداد بایت‌های زیر را نشان می‌دهد، نه رکوردها. نکات زیر را باید در هنگام خواندن یک فایل به خاطر بسپارید.

* مقادیر ستون "طول" در همه جداول بر حسب بایت است.

* تمام مقادیر تعریف شده به عنوان رشته یونیکد شامل موارد زیر است:

* یک فیلد به طول 4 بایت که نشان دهنده تعداد کاراکترهای رشته است (نه بایت).

* رشته ای از مقادیر یونیکد، دو بایت در هر کاراکتر.


### سربرگ فایل ###

هدر فایل حاوی ویژگی های اصلی تصویر است.

|طول|توضیحات
---|---|
|4|امضا: همیشه برابر با '8BPS' است. اگر امضا با این مقدار مطابقت ندارد سعی نکنید فایل را بخوانید.
|2|Version: always equal to 1. اگر نسخه با این مقدار مطابقت ندارد سعی نکنید فایل را بخوانید. (~*~*PSB~*~* نسخه 2 است.)
|6|رزرو شده: باید صفر باشد.
|2|تعداد کانال های موجود در تصویر، از جمله هر کانال آلفا. محدوده پشتیبانی شده 1 تا 56 است.
|4|ارتفاع تصویر بر حسب پیکسل. محدوده پشتیبانی شده 1 تا 30000 است.
|4|عرض تصویر بر حسب پیکسل. محدوده پشتیبانی شده 1 تا 30000 است.
|2|عمق: تعداد بیت در هر کانال. مقادیر پشتیبانی شده 1، 8، 16 و 32 هستند.
|2|حالت رنگ فایل. مقادیر پشتیبانی شده عبارتند از: Bitmap # 0; مقیاس خاکستری شماره 1; نمایه شماره 2; RGB # 3; CMYK # 4; چند کانال شماره 7; دوتون شماره 8; آزمایشگاه شماره 9.

### بخش داده های حالت رنگ ###

ساختار بخش داده های حالت رنگ به صورت زیر است:


|طول|توضیحات
---|---|
|4|طول داده های رنگ زیر
|متغیر|داده رنگ

داده‌های حالت رنگ فقط برای رنگ‌های نمایه‌شده و دوتونی که توسط فیلد حالت در بخش File Header تعریف شده‌اند، در دسترس هستند. برای همه حالت‌های دیگر، این بخش با مقادیر صفر شده 4 بایت نشان داده می‌شود. برای تصاویر رنگی نمایه‌شده، طول 768 است و داده‌های رنگی شامل جدول رنگی برای تصویر، به ترتیب غیر درهم می‌شوند. برای تصاویر Duotone، داده های رنگی حاوی مشخصات دوتون (که فرمت آن مستند نشده است) است. سایر برنامه‌هایی که فایل‌های فتوشاپ را می‌خوانند، می‌توانند یک تصویر دوگانه را به عنوان یک تصویر خاکستری در نظر بگیرند و فقط محتویات اطلاعات دوتون را هنگام خواندن و نوشتن فایل حفظ کنند.

### بخش منابع تصویر ###

بخش سوم فایل حاوی منابع تصویری است. با یک فیلد طول شروع می شود و به دنبال آن مجموعه ای از بلوک های منبع قرار می گیرد.


|طول|توضیحات
---|---|
|4|طول بخش منبع تصویر. طول ممکن است صفر باشد.
|متغیر|منابع تصویر (بلوک های منبع تصویر)

منابع تصویر برای ذخیره داده های غیر پیکسلی مرتبط با تصاویر مانند مسیرهای ابزار قلم استفاده می شود. آنها به عنوان بلوک های منبع شناخته می شوند زیرا آنها داده هایی را که در نسخه های اولیه فتوشاپ در منبع مکینتاش ذخیره شده بود نگهداری می کنند. ساختار اصلی بلوک های منبع تصویر به شرح زیر است:


|طول|توضیحات
---|---|
|4|امضا: '8BIM
|2|شناسه منحصر به فرد برای منبع. شناسه منابع تصویر حاوی لیستی از شناسه های منابع مورد استفاده فتوشاپ است.
|متغیر|نام: رشته پاسکال، برای یکنواخت کردن اندازه (نام پوچ شامل دو بایت 0) است.
|4|اندازه واقعی داده های منبع که در ادامه آمده است
|متغیر|داده های منبع، که در بخش های مربوط به انواع منابع منفرد توضیح داده شده است. برای یکنواخت شدن سایز آن بالشتک شده است.

منابع تصویر از چندین شماره شناسه استاندارد استفاده می کنند.

### اطلاعات لایه و ماسک ###

بخش چهارم یک فایل فتوشاپ حاوی اطلاعاتی در مورد لایه ها و ماسک ها مانند تعداد لایه ها، کانال های موجود در لایه ها، محدوده های ترکیبی، کلیدهای لایه تنظیم، لایه های افکت ها و پارامترهای ماسک است. اگر هیچ لایه یا ماسکی وجود نداشته باشد، این بخش با فیلد 4 بایتی صفر نشان داده می شود. در حین خواندن این بخش به دلیل مقادیر صفر شده باید به طول بخش ها توجه ویژه ای شود. چینش بخش لایه و ماسک به شرح زیر است:


|طول|توضیحات
---|---|
|4|طول لایه و قسمت اطلاعات ماسک. (طول PSB 8 بایت است.)
|متغیر|اطلاعات لایه
|متغیر|اطلاعات ماسک لایه جهانی
|متغیر|سری بلوک های برچسب گذاری شده حاوی انواع مختلف داده ها.

#### اطلاعات لایه ####

جدول زیر سازماندهی سطح بالای اطلاعات لایه را نشان می دهد.


|طول|توضیحات
---|---|
|4|Length of the layers info section, rounded up to a multiple of 2. (طول PSB 8 بایت است.)
|2|تعداد لایه ها. اگر عددی منفی باشد، مقدار مطلق آن تعداد لایه‌ها است و اولین کانال آلفا حاوی داده‌های شفافیت برای نتیجه ادغام شده است.
|متغیر|اطلاعات مربوط به هر لایه. رجوع کنید به رکوردهای لایه ساختار این اطلاعات را برای هر لایه توضیح می دهد.
|متغیر|داده های تصویر کانال. شامل یک یا چند رکورد داده تصویر برای هر لایه است. لایه ها به همان ترتیبی هستند که در اطلاعات لایه وجود دارد

### داده های تصویر ###

داده های پیکسل تصویر در بخش Image Data فایل موجود است. ترتیب داده ها در بخش Image Data به ترتیب مسطح است یعنی ابتدا تمام داده های قرمز، سپس همه داده های سبز و غیره. هر صفحه به ترتیب خط اسکن و بدون بایت پد ذخیره می شود. همانطور که در جدول زیر نشان داده شده است.

|طول|توضیحات
---|---|
|2|Compression method: *0 = Raw image data * 1 = RLE فشرده شده، داده های تصویر با تعداد بایت ها برای تمام خطوط اسکن (ردیف * کانال ها) شروع می شود و هر تعداد به عنوان یک مقدار دو بایت ذخیره می شود. داده‌های فشرده‌شده RLE با هر خط اسکن جداگانه فشرده می‌شوند. فشرده‌سازی RLE همان الگوریتم فشرده‌سازی است که توسط PackBits روتین رام مکینتاش و استاندارد TIFF استفاده می‌شود. *2 = ZIP بدون پیش بینی *3 = ZIP با پیش بینی.
|متغیر|داده های تصویر. ترتیب مسطح = RRR GGG BBB و غیره

## منابع ##

* [مشخصات فرمت فایل PSD - توسط Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)

* [فرمت فایل Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


