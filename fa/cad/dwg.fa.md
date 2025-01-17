{
  "date": "2020-03-16",
  "keywords": [
"DWG",
"فرمت فایل",
"CAD",
"باز کن",
"ايجاد كردن"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل DWG و APIهایی که می‌توانند فایل‌های DWG را ایجاد و باز کنند، بیاموزید.",
  "title": "فرمت فایل DWG",
  "linktitle": "DWG",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dw-fag"
}
},
  "lastmod": "2019-09-10"
}

## فایل DWG چیست؟

فایل‌های با پسوند DWG نشان‌دهنده فایل‌های باینری اختصاصی هستند که برای حاوی داده‌های طراحی دو بعدی و سه بعدی استفاده می‌شوند. مانند DXF که فایل‌های ASCII هستند، DWG فرمت فایل باینری را برای نقشه‌های CAD (طراحی به کمک کامپیوتر) نشان می‌دهد. این شامل تصویر برداری و ابرداده برای نمایش محتویات فایل های CAD است. بینندگان رایگانی برای مشاهده فایل‌های DWG در سیستم عامل ویندوز مانند DWG TrueView رایگان Autodesk وجود دارد. برنامه های شخص ثالث دیگری نیز وجود دارند که از دسترسی به فایل های DWG پشتیبانی می کنند. فایل های DWG حاوی اطلاعات ایجاد شده توسط کاربر و شامل موارد زیر است:

* طرح ها

* داده های هندسی

* نقشه ها و عکس ها


این قالب به طور گسترده توسط معماران، مهندسان و طراحان برای اهداف مختلف طراحی استفاده می شود.

## تاریخچه مختصر ##

DWG file format has evolved with the time since its formal introduction in 1982. مروری کوتاه بر وقایع گذشته از منظر تاریخ به شرح زیر است.

**1982:** Autodesk مجوز فرمت فایل DWG را که توسط مایک ریدل در سال 1970 ایجاد شد، به عنوان پایه اتوکد صادر کرد.

**1998:** با انتشار AutoCAD R14.01، Autodesk تأیید فایل را از طریق تابعی به نام DWGCHECK اضافه کرد که یک چک جمع رمزگذاری شده و کد محصول به نام WaterMark توسط Autodesk را در فایل های DWG ایجاد شده توسط برنامه جاسازی کرد.

**2006:** Autodesk AutoCAD 2007 را اصلاح کرد، تا تکنولوژی TrustedDWG را برای جاسازی رشته متن Autodesk DWG. این فایل یک DWG مورد اعتماد است که آخرین بار توسط یک برنامه Autodesk یا برنامه دارای مجوز Autodesk ذخیره شده است در فایل های DWG. هدف از این کار کمک به کاربران نرم افزار Autodesk بود تا اطمینان حاصل کند که این فایل ها توسط یک برنامه Autodesk یا RealDWG ایجاد شده اند، که قطعاً باید به کاهش خطر ناسازگاری کمک کند.

## ساختار فایل ##

DWG یکی از فرمت های فایلی است که به طور گسترده توسط طیف وسیعی از برنامه ها مورد استفاده قرار می گیرد و دارای ساختار فایل قوی است. از آنجایی که DWG یک فرمت فایل باینری است، مانند فرمت فایل ساده ASCII [DXF](/cad/dxf/) برای انسان قابل خواندن نیست. فایل‌های DWG معمولاً شامل اطلاعات مختصات تصویر و هرگونه ابرداده مرتبط با آن است. [specifications](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) کامل فرمت فایل DWG برای دانلود توسط OpenDesign در دسترس است. ساختار فایل فرمت فایل DWG به صورت زیر خلاصه شده است.

**Header**: هدر فایل شامل متغیرهای سربرگ DWG و اطلاعات مربوط به بررسی افزونگی چرخه ای (CRC) است که برای تشخیص خطا استفاده می شود. هر بخش فرعی یک بردار تخصصی است که در آن از طول های مختلف بیت ها برای نشان دادن برچسب های مختلف استفاده می شود. به عنوان مثال، 6 بیت اول متغیر DWG Header مخفف رشته نسخه است.

**تعریف کلاس:** یک فایل DWG ممکن است بسته به هدف خاص فایل .dwg دارای کلاس های متعددی باشد. اطلاعاتی مانند اندازه ابرداده کلاس منطقه داده کلاس، شماره کلاس و جمع کنترلی علاوه بر موارد دیگر.

**قالب**: این اختیاری است و برای نسخه های R15 و R15، این بخش در زیر قسمت Object Free Space قرار دارد.

**Padding**: متادیتا با تعداد مشخصی از بایت ها پسوند و پسوند می شود که باعث می شود نسخه های قدیمی نرم افزار اتوکد با فرمت فایل DWG جدید سازگار شوند.

**تصویر داده**: فراداده این بخش به نوع خاص dwg. بستگی دارد. برای کاربران R14 و R15، این بخش اختیاری است.

**داده های شی**: داده های شی شامل فهرست کاملی از موجودیت های جدول، مدخل های فرهنگ لغت و غیره مربوط به لیست اشیاء موجود است.

**نقشه شی**: محل هر شیء در فایل در این قسمت از فایل مشخص شده است. بیشتر ابرداده های این بخش، دسته های فایلی هستند که در شناسایی و رندر مجدد شی نقش دارند.

**فضای آزاد شی**: این بخش برای همه کاربران اختیاری است

**سرصفحه دوم**: تکراری از قسمت هدر فایل در انتهای فایل DWG

## منابع ##

* [مشخصات فرمت فایل DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)

* [مشخصات فایل DWG](https://www.scan2cad.com/blog/dwg/file-spec/)

* [DWG - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/.dwg)


