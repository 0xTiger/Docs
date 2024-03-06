{
  "date" : "2023-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "درباره فرمت فایل ECM و APIهایی که می‌توانند فایل‌های ECM را ایجاد و باز کنند، بیاموزید.",
  "title" : "فرمت فایل ECM - فرمت مدل ساز کد خطا (ECM).",
  "linktitle" : "ECM",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-ecm-fa",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-25"
}

## فایل ECM چیست؟

فایل ECM یک فایل تصویر دیسک است که با استفاده از ابزار Error Code Modeler (ECM) فشرده شده است. ابزار ECM برای کاهش اندازه تصاویر دیسک مانند تصاویر CD و DVD با حذف داده های اضافی و فشرده سازی داده های باقی مانده استفاده می شود. سپس فایل ECM به دست آمده را می توان از حالت فشرده خارج کرد و به عنوان یک درایو مجازی نصب کرد و به کاربر اجازه می دهد به محتویات تصویر دیسک اصلی دسترسی داشته باشد.

فایل های ECM را می توان با استفاده از ابزار ECM یا سایر برنامه های سازگار مانند ECMDecompress باز و از حالت فشرده خارج کرد. هنگامی که از حالت فشرده خارج شد، تصویر دیسک اصلی را می توان به عنوان یک درایو مجازی نصب کرد و به محتویات آن می توان به گونه ای که گویی روی یک دیسک فیزیکی قرار دارند، دسترسی داشت.

توجه به این نکته ضروری است که استفاده از فایل‌های ECM می‌تواند فضای زیادی را ذخیره کند و در برخی شرایط مفید باشد، اما این فرمت پرکاربرد نیست و همه ابزارها نمی‌توانند آن را باز کنند. همچنین، بسته به نوع تصویری که می‌خواهید باز کنید، فرمت‌های تصویر محبوب‌تری مانند ISO، BIN/CUE و NRG وجود دارند که به طور گسترده‌تری پشتیبانی می‌شوند.

## ارتباط با ECMDecompress

ECM یک فرمت فایل است که برای فشرده سازی و ذخیره تصاویر دیسک، مانند تصاویر CD و DVD، با حذف داده های اضافی و فشرده سازی داده های باقی مانده استفاده می شود. سپس فایل ECM به دست آمده را می توان از حالت فشرده خارج کرد و به عنوان یک درایو مجازی نصب کرد و به کاربر اجازه می دهد به محتویات تصویر دیسک اصلی دسترسی داشته باشد.

ECMDecompress ابزاری است که به طور خاص برای فشرده‌سازی فایل‌های ECM طراحی شده است، این یک نرم‌افزار رایگان و منبع باز است که می‌تواند برای تبدیل فایل‌های ECM به فرمت ISO یا BIN، که فرمت‌های تصویری به طور گسترده‌تری پشتیبانی می‌شوند، استفاده شود. همچنین می توان از آن برای استخراج فایل های موجود در تصویر دیسک اصلی استفاده کرد.

ECMDecompress ابزار رایجی است که برای باز کردن فایل‌های ECM استفاده می‌شود، یکی از محبوب‌ترین و پرکاربردترین ابزارها برای مدیریت فایل‌های ECM است. این یک ابزار ساده و آسان برای استفاده است که می تواند برای تبدیل فایل های ECM به فرمت های تصویری با پشتیبانی گسترده تر مانند ISO، BIN و NRG استفاده شود.

به طور خلاصه، ECM و ECMDecompress به این معنا مرتبط هستند که ECMDecompress ابزاری است که به طور خاص برای مدیریت فایل‌های ECM طراحی شده است و به کاربران اجازه می‌دهد فایل‌های ECM را از حالت فشرده خارج کرده و به فرمت‌های تصویری با پشتیبانی گسترده‌تر مانند ISO، BIN و NRG تبدیل کنند.

## چگونه فایل ECM را باز کنیم؟

برای باز کردن یک فایل ECM، باید از برنامه ای استفاده کنید که با فرمت ECM سازگار باشد، مانند ECMDecompress.

در اینجا مراحل باز کردن و از حالت فشرده کردن یک فایل ECM با استفاده از ECMDecompress آمده است:

1. ECMDecompress را از اینترنت دانلود کرده و بر روی کامپیوتر خود نصب کنید.
2. ECMDecompress را اجرا کنید و روی دکمه Open کلیک کنید یا به File -> Open بروید.
3. فایل ECM را که می خواهید از حالت فشرده خارج کنید انتخاب کنید و روی Open کلیک کنید.
4. بر روی دکمه Decompress کلیک کنید تا فرآیند رفع فشار شروع شود.
5. هنگامی که فرآیند رفع فشرده سازی کامل شد، یک فایل جدید با همان نام فایل ECM اما با پسوند .iso یا .bin در همان محل فایل ECM اصلی ایجاد می شود.
6. اکنون می توانید فایل .iso یا .bin را به عنوان یک درایو مجازی با استفاده از یک نرم افزار درایو مجازی مانند Daemon Tools، Alcohol 120% یا PowerISO مونت کنید و به محتویات تصویر دیسک اصلی دسترسی داشته باشید.

## منابع
* [چگونه فایل‌های ECM را از حالت فشرده خارج کنیم](https://www.freezenet.ca/guides/compatibility-and-emulation/how-to-decompress-ecm-files-ecm-tools/)

