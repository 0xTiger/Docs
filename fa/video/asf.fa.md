{
  "date": "2021-02-15",
  "keywords": [
"فایل asf",
"فرمت فایل asf",
"فایل asf چیست",
"فایل",
"به عنوان مثال",
"پسوند فایل asf",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASF - فرمت فایل سیستم های پیشرفته",
  "description": "درباره فرمت فایل ASF و APIهایی که می‌توانند فایل‌های ASF را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "ASF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-as-faf"
}
},
  "lastmod": "2021-02-16"
}

## فایل ASF چیست؟

یک فایل با پسوند asf. یک فرمت فایل چندرسانه ای برای ذخیره و پخش جریان های رسانه دیجیتال در شبکه است. این یک فرمت فایل کانتینری است که می تواند هم محتوای ویدیویی و هم صوتی برای پخش آنلاین داشته باشد. به ندرت فایل‌های ASF را پیدا می‌کنید، و احتمالاً با فایل‌های Windows Media Audio ([WMA](/audio/wma/)) و Windows Media Video ([WMV](/video/wmv/)) مواجه می‌شوید که هر دو فایل‌های ASF را مشخص می‌کنند که محتوای آن با کدک‌های مربوطه کدگذاری شده است. فایل های رسانه ای ویندوز را می توان با استفاده از Windows Media Format SDK ایجاد و خواند.

## فرمت فایل ASF

یک فایل ASF می تواند شامل چندین جریان مستقل یا وابسته باشد. این می‌تواند شامل جریان‌های صوتی چندگانه برای پخش‌های صوتی چند کانالی یا جریان‌های ویدیویی با نرخ بیت چندگانه باشد. نرخ بیت چندگانه، جریان ها را برای انتقال در پهنای باند مختلف مناسب می کند. علاوه بر این، جریان‌ها در یک فایل ASF می‌توانند به صورت فشرده یا غیرفشرده باشند. بهترین فشرده سازی با کدک های Microsoft Windows Media Audio و Video Series 9 حاصل می شود. مشخصات کامل فرمت فایل ASF در [Microsoft Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc) موجود است.

### ساختار فایل سطح بالای ASF

فایل های ASF به طور منطقی شامل سه نوع شی سطح بالا هستند:

* "Header Object" - اجباری است و باید در ابتدای هر فایل ASF قرار گیرد

* "Data Object" - اجباری است و باید از شی هدر پیروی کند

* "اشیاء(های) شاخص" - اختیاری است، اما برای ارائه دسترسی تصادفی مبتنی بر زمان به فایل‌های ASF مفید است.


تصویر زیر ساختار فایل های سطح بالای فایل های ASF را نشان می دهد.

![ASF File Structure](../asf.png "ASF File Structure")

#### شئ هدر سطح بالای ASF

شی Header یک توالی بایت شناخته شده را در ابتدای فایل های ASF ارائه می دهد و می تواند به صورت اختیاری حاوی ابرداده مانند اطلاعات کتابشناختی باشد. این شامل تمام اطلاعاتی است که برای تفسیر صحیح اطلاعات درون شی داده مورد نیاز است. شئ هدر ممکن است شامل چندین شی استاندارد باشد، از جمله، اما نه محدود به:

 * File Properties Object - حاوی ویژگی های فایل جهانی است.
 * Stream Properties Object - یک جریان رسانه دیجیتال و ویژگی های آن را تعریف می کند.
 * Header Extension Object - اجازه می دهد تا عملکردهای اضافی به فایل ASF اضافه شود در حالی که سازگاری با عقب را حفظ می کند.
 * شیء شرح محتوا - حاوی اطلاعات کتابشناختی است.
 * شیء دستور اسکریپت - شامل دستوراتی است که می توانند در خط زمانی پخش اجرا شوند.
 * Object نشانگر - نقاط پرش نامگذاری شده را در یک فایل ارائه می دهد.

شی هدر با استفاده از ساختار زیر نمایش داده می شود:

|نام فیلد |نوع فیلد |اندازه (بیت)|
---|---|---|
|شناسه شی| GUID| 128|
|اندازه شی| QWORD| 64|
|تعداد اشیاء سربرگ| DWORD| 32|
|رزرو شده1| BYTE| 8|
| رزرو شده2| BYTE| 8|

#### شی داده سطح بالای ASF

تمام داده های رسانه دیجیتال برای یک فایل ASF در شی داده موجود است و در قالب بسته های داده ASF ذخیره می شود. هر بسته داده دارای طول ثابت است و حاوی داده هایی برای یک یا چند جریان رسانه دیجیتال است.

#### اشیاء شاخص سطح بالای ASF

اشیاء شاخص سطح بالای ASF دو نوع زیر را دارند:

 * شیء فهرست ساده - حاوی یک شاخص مبتنی بر زمان از داده های ویدئویی در یک فایل ASF است. فاصله زمانی بین ورودی های ایندکس ثابت است و در Simple Index Object ذخیره می شود.
 * Index Object - به Index Object، Media Object Index Object و Timecode Index Object اشاره دارد که قالب های آنها مشابه است. مانند Simple Index Object، Index Object بر اساس زمان با یک بازه زمانی ثابت نمایه می شود، اما محدود به جریان های ویدیویی نیست.

## منابع

* [فرمت فایل ASF - مایکروسافت](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)

* [فرمت فایل QuickTime - ویکی پدیا](https://en.wikipedia.org/wiki/QuickTime_File_Format)


