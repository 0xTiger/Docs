{
  "date": "2019-10-11",
  "keywords": [
"فایل dcm",
"فرمت فایل dcm",
"فایل dcm چیست",
"فایل",
"نمونه dcm",
"پسوند فایل dcm",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل DCM - فایل اطلاعات پزشکی دیجیتال",
  "description": "درباره فرمت فایل DCM و APIهایی که می‌توانند فایل‌های DCM را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "DCM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dc-fam"
}
},
  "lastmod": "2021-07-03"
}

## فایل DCM چیست؟

فایل‌های با پسوند .dcm تصویر دیجیتالی را نشان می‌دهند که اطلاعات پزشکی بیماران مانند MRI، سی‌تی اسکن و تصاویر اولتراسوند را ذخیره می‌کند. فایل‌های DCM از فرمت فایل تصویری [DICOM](/image/dicom/) (تصویربرداری دیجیتال و ارتباطات در پزشکی) استفاده می‌کنند و می‌توانند شامل اطلاعات بیمار برای مرجع باشند. این توسط [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) توسعه داده شد و به منظور استاندارد کردن فرمت فایل تصویربرداری برای توزیع و مشاهده تصاویر پزشکی بود.

## فرمت فایل DCM

فایل های DCM اطلاعات را در قالب تصویر DICOM ذخیره می کنند. این فایل‌ها مجموعه داده‌ها را ذخیره می‌کنند، که اطلاعات دنیای واقعی است، که یک نمونه SOP مربوط به DICOM IOD را نشان می‌دهد. اطلاعات متا فایل DICOM در فایل و به دنبال آن جریان بایت مجموعه داده واقعی ذخیره می شود.

### اطلاعات متا فایل DICOM ##

هر فایل DICOM شامل یک هدر اطلاعات شناسایی برای مجموعه داده کپسوله شده است که شامل موارد زیر است:
   * یک مقدمه فایل 128 بایتی
   * 4 بایت پیشوند DICOM
   * عناصر متا فایل

این هدر برای هر فایل DICOM ضروری است.

### عناصر متا فایل ###
|نام ویژگی|برچسب|نوع| شرح صفت
---|---|---|---|
|پرمبل فایل|بدون برچسب یا فیلدهای طول|1|یک فیلد 128 بایتی ثابت برای نمایه برنامه یا استفاده مشخص شده در پیاده سازی موجود است. اگر توسط یک Application Profile یا یک پیاده سازی خاص استفاده نشود، همه بایت ها باید روی 00H تنظیم شوند. خوانندگان یا به‌روزرسانی‌کننده‌های مجموعه فایل برای تعیین اینکه این فایل یک فایل DICOM است یا نیست، به محتوای این مقدمه تکیه نمی‌کنند.
|پیشوند DICOM|بدون برچسب یا فیلدهای طول|1|چهار بایت حاوی رشته کاراکتر DICM. این پیشوند برای تشخیص اینکه این فایل یک فایل DICOM است یا نه استفاده می شود.
|طول گروه اطلاعات متا فایل|(00020000)|1|تعداد بایت های بعد از این متا عنصر فایل (انتهای فیلد مقدار) تا آخرین متا عنصر فایل از اطلاعات متا فایل گروه 2
|File Meta Information Version|(0002,0001)|1|This is a two byte field where each bit identifies a version of this File Meta Information header. In version 1 the first byte value is 00H and the second value byte value is 01H.Implementations reading Files with Meta Information where this attribute has bit 0 (lsb) of the second byte set to 1 may interpret the File Meta Information as specified in this version of PS3.10. تمام بیت های دیگر نباید بررسی شوند.
| UID کلاس SOP ذخیره سازی رسانه|(0002,0002)|1|کلاس SOP مرتبط با مجموعه داده را به طور منحصر به فرد شناسایی می کند. UIDهای کلاس SOP مجاز برای ذخیره سازی رسانه در PS3.4 - نمایه های برنامه ذخیره سازی رسانه مشخص شده اند.
UID نمونه SOP Storage Media|(0002,0003)|1|به طور منحصر به فرد نمونه SOP مرتبط با مجموعه داده قرار داده شده در فایل و به دنبال اطلاعات متا فایل را شناسایی می کند.
|Transfer Syntax UID|(0002,0010)|1|به طور منحصربفرد نحو انتقال مورد استفاده برای کدگذاری مجموعه داده زیر را مشخص می کند. این نحو انتقال برای اطلاعات متا فایل اعمال نمی شود.
|کلاس پیاده‌سازی UID|(0002,0012)|1|پیاده‌سازی که این فایل را نوشته و محتوای آن را به‌طور منحصربه‌فرد شناسایی می‌کند. در صورت بروز مشکلات مبادله ای، شناسایی واضحی از نوع پیاده سازی که آخرین بار فایل را نوشته است، ارائه می دهد.
|نام نسخه پیاده‌سازی|(0002,0013)|3|نسخه‌ای را برای UID کلاس پیاده‌سازی (0002,0012) با استفاده از حداکثر 16 کاراکتر از مجموعه مشخص می‌کند.
| عنوان نهاد برنامه منبع|(0002,0016)|3|عنوان DICOM Application Entity (AE) AE که محتوای این فایل را نوشته (یا آخرین بار آن را به روز کرده است). در صورت استفاده، امکان ردیابی منبع خطا را در صورت بروز مشکلات تبادل رسانه فراهم می کند.
|UID ایجاد کننده اطلاعات خصوصی|(0002,0100)|3|UID خالق اطلاعات خصوصی (0002,0102).
|اطلاعات خصوصی|(0002,0102)|1C|حاوی اطلاعات خصوصی قرار داده شده در اطلاعات متا فایل. ایجاد کننده باید در (0002,0100) مشخص شود. در صورت وجود UID ایجاد کننده اطلاعات خصوصی (0002,0100) الزامی است.

### کپسوله کردن مجموعه داده ###

یک فایل DICOM شامل یک مجموعه داده واحد است که نشان دهنده یک نمونه SOP منفرد مربوط به یک کلاس SOP منفرد است. UID نحو انتقال اطلاعات متا فایل DICOM باید نحو انتقال مورد استفاده برای رمزگذاری مجموعه داده را تعریف کند.

### پشتیبانی از اطلاعات مدیریت فایل ###

لایه فرمت رسانه اطلاعات مدیریت فایل زیر را در صورت لزوم برای نمایه برنامه DICOM ارائه می دهد.

  * شناسایی مالک محتوای فایل

  * آمار دسترسی به فایل (به عنوان مثال، تاریخ و زمان ایجاد)

  * کنترل دسترسی به فایل برنامه

  * کنترل دسترسی به رسانه فیزیکی (مثلاً محافظت از نوشتن)

## منابع ##
  * [استاندارد DICOM](https://www.dicomstandard.org/current/)
  * [فرمت فایل DICOM](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

