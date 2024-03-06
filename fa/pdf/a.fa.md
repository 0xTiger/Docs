{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل PDF/A",
  "description": "درباره فرمت فایل PDF/A و APIهایی که می‌توانند فایل‌های PDF/A را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "PDF/A",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf--faa"
}
},
  "lastmod": "2019-09-10"
}

# PDF/A چیست؟ #

PDF/A یک فرمت استاندارد ISO برای بایگانی اسناد الکترونیکی در قالب PDF است. دلیل اصلی به وجود آمدن آن، برآوردن الزامات بایگانی طولانی مدت بود. این استاندارد باز شدن فایل‌های بایگانی‌شده را حتی پس از مدت‌زمان طولانی با اعمال محدودیت‌های خاصی بر روی بخش‌های جدایی‌ناپذیر سند برای دستیابی به انطباق تضمین می‌کند. این قالب در حال حاضر به طور گسترده در تمام صنایع پذیرفته شده است. بینندگان PDFA/A مانند Adobe Acrobat Reader، اطمینان حاصل کنند که فایل های ذخیره شده با این فرمت حتی در آینده مطابق با اطلاعات به اشتراک گذاشته شده توسط این استاندارد باز می شوند.

## نسخه PDF/A ##

PDF/A was accepted as ISO Standard in October 2005. از آن زمان به بعد، به طور مداوم بهبود یافته و چندین استاندارد دیگر با گذشت زمان توسعه یافته است. اطلاعات مربوط به استانداردهای PDF/A منتشر شده با گذشت زمان و جزئیات آنها به شرح زیر است:

* **PDF/A-1:** منتشر شده در اکتبر 2005 به عنوان ISO 19005-1 و بر اساس PDF 1.4 است.

* **PDF/A-2:** منتشر شده در ژوئن 2011 به عنوان ISO 19005-2 و بر اساس PDF 1.7 (ISO 32000-1:2008)

* **PDF/A-3:** منتشر شده در اکتبر 2012 به عنوان ISO 19005-3 و بر اساس PDF 1.7 (ISO 32000-1:2008)


## PDF/A-1 ##

استاندارد PDF/A-1 بر اساس نسخه اصلی PDF 1.4 بود. استاندارد PDF/A-1 دو سطح انطباق را برای فایل های PDF تعریف می کند.

### PDF/A-1a ###

مطابق با سطح A است و تمام الزامات استاندارد PDF/A-1 را برآورده می کند. PDF/A-1a تضمین می کند که متن از سند قابل استخراج است. همچنین تضمین می کند که روند طبیعی خواندن متن یکپارچه دست نخورده باقی بماند. PDF/A الزامی برای توانایی نمایش متن بر روی صفحه نمایش های کاهش یافته با تغییر ساختار که به عنوان PDF برچسب گذاری شده شناخته می شود، تحمیل می کند. هدف از آن افزایش دسترسی به فایل های منطبق برای کاربرانی که از نظر جسمی ضعیف هستند با اجازه دادن به نرم افزارهای کمکی بود.

### PDF/A-1b ###

PDF/A-1b سطح پایین تری از انطباق است و با ظاهر بصری اسناد الکترونیکی با توجه به استاندارد ISO 19005 سروکار دارد. این تضمین می کند که متن و سایر مطالب در صفحات به طور یکنواخت بازتولید می شوند. این انطباق سطح B حداقل انطباق را نشان می دهد تا اطمینان حاصل شود که ظاهر بصری ارائه شده یک فایل منطبق در طولانی مدت قابل حفظ است.

## PDF/A-2 ##

PDF/A-2 was released by ISO Standard in July 2011 as a new standard known as ISO 32001-1. این استاندارد جدید نه تنها از تمامی امکانات نسخه های PDF تا 1.7 بهره می برد، بلکه به عنوان یک استاندارد جدید معرفی شد. PDF/A-2 شامل ویژگی های زیر به عنوان بخشی از این استاندارد جدید است.

* PDF/A-2 با پشتیبانی از [JPEG2000](/image/jp2/) ارائه می شود که در مورد اسناد اسکن شده مفید است.

* از تعبیه مجموعه های PDF/A پشتیبانی می کند که می توان از آنها برای ایجاد یک PDF کانتینری با فایل های مشابه دیگر استفاده کرد.

* از ویژگی شفافیت فایل‌های PDF در کل در مقایسه با PDF/A-1 که تا حدی پشتیبانی می‌شد، پشتیبانی می‌کند.

* PDF/A-2 از محتوای اختیاری پشتیبانی می کند که برای نقشه برداری برنامه ها و نقشه های مهندسی مفید است. اینها همچنین به عنوان لایه‌هایی شناخته می‌شوند که می‌توانند بر اساس نیازهای فرد بیننده قابل مشاهده یا پنهان شوند.

* الزامات فوق داده XMP سفارشی را مشخص می کند

* برخی از انواع نظرات جدیدتر را به لیست انواع حاشیه نویسی ممنوع اضافه می کند. علاوه بر این، برخی از انواع نظرات جدیدتر مانند نظرات ویرایش متن به لیست موارد قابل قبول اضافه شد.


## PDF/A-3 ##

PDF/A-3 شامل تمام الزامات انطباق سطح 2 است و امکان جاسازی فرمت های فایل اضافی (مانند XML، [CSV](/spreadsheet/csv/)، [CAD](/cad/)، [word-processing](/word-processing/)، [spreadsheet](/spreadsheet/) و موارد دیگر را می دهد. ) در اسناد منطبق با PDF/A.

## منابع ##

* [PDF/A - توسط ویکی پدیا](https://en.wikipedia.org/wiki/PDF/A)

* [White Paper: PDF/A – The Basics](https://www.pdf-tools.com/public/downloads/whitepapers/whitepaper-pdfa.pdf)

