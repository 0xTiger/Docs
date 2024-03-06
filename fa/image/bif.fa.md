{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "فایل BIF - فرمت تصویر کامل اسلاید Ventana",
  "description":"با فرمت فایل BIF و APIهایی که می توانند فایل های BIF را ایجاد و باز کنند آشنا شوید.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-fa",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## فایل BIF چیست؟

یک فایل BIF یک فایل تصویر شطرنجی است که حاوی تصویر نمونه اسلاید است. این شامل چندین تصویر TIFF است که توسط برنامه های مشاهده اسلاید در یک تصویر ترکیبی واحد ترکیب می شوند. فایل‌های BIF توسط اسکنر اسلاید دیجیتال Ventana Medical Systems ایجاد شده‌اند و کاملاً با نوع BigTIFF تعریف [TIFF](/image/tiff/) v 6.0 مطابقت دارند.

## فرمت فایل BIF

یک فایل BIF به عنوان فایل تصویری باینری ذخیره می شود و از 200000 x 200000 پیکسل تشکیل شده است. این می تواند به اندازه فایل های بزرگ منجر شود و محدودیت اندازه 4 گیگابایتی اعمال شده توسط نشانگرهای فایل 32 بیتی تعریف شده توسط استاندارد TIF را بشکند. با این حال، با اشاره گرهای فایل 64 بیتی، این مانع اندازه فایل توسط نوع BigTIFF استاندارد TIFF برطرف می شود.

### چه کسی از فایل BIF استفاده می کند؟

فایل های BIF توسط اسکنرهای اسلاید دیجیتال برای اسکن و ایجاد کپی های دیجیتالی از نمونه های اسلاید استفاده می شود. اگر شما یک آسیب شناس هستید، می توانید این فایل های BIF را در برنامه های مشاهده اسلاید باز کنید. با سطح بالایی از جزئیات و داده های با وضوح بالا، می توانید یک تصویر اسلاید را بزرگنمایی و کوچکنمایی کنید تا بخش های نمونه را با جزئیات بیشتر یا کمتر مشاهده کنید. فایل فوق داده [XML](/web/xml/) موجود در این فایل‌ها، نحوه ترکیب تصاویر و تصویری را که باید به عنوان تصویر کوچک فایل استفاده شود، مشخص می‌کند.

## چگونه فایل BIF را باز کنیم؟

شما می توانید فایل های BIF را با:

 * OpenSlide (کراس پلت فرم)
 * ImageJ (کراس پلتفرم)
 * نمایشگر NetScope (ویندوز)

## منابع ##

 * [Roche Digital Pathology BIF Paper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)
