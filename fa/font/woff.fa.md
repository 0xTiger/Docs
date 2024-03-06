{
  "date": "2020-08-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF - قالب فایل باز وب",
  "description": "فایل WOFF یک فرمت فونت باز است که در قالب فونت باز وب ایجاد شده است.",
  "linktitle": "WOFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-wof-faf"
}
},
  "lastmod": "2020-09-30"
}

## فایل WOFF چیست؟

یک فایل با پسوند .woff یک فایل فونت وب مبتنی بر قالب فونت باز وب (WOFF) است. دارای محفظه فشرده با فرمت خاص بر اساس انواع فونت TrueType (.TTF) یا OpenType (OTT). WOFF با هدف تفاوت فونت های وب از فایل های فونت های مورد استفاده در برنامه های دسکتاپ معرفی شد. علاوه بر این، فرمت برای کاهش تأخیر انتقال فونت ها از سرور به رایانه مشتری از طریق شبکه هدف قرار گرفته است. چندین ابزار موجود است که می تواند فایل های WOFF را به TTF و سایر فرمت های فایل فونت تبدیل کند.

## فرمت فایل WOFF

فرمت فونت WOFF جداول داده فونت ساختارهای sfnt مبتنی بر جدول را فشرده می کند که در انواع فونت های مختلف مانند TrueType، OpenType و Open Font Format استفاده می شود. مانند محفظه ای برای این نوع فونت ها است و همچنین دارای اتاقی برای گنجاندن فراداده های قلم و داده های استفاده خصوصی برای گنجاندن در ظرف است. مبدل‌ها از فایل‌های sfnt به یک فایل با فرمت WOFF استفاده می‌کنند و عامل‌های کاربر فایل کدگذاری‌شده را برای استفاده با سند وب بازیابی می‌کنند. لازم به ذکر است که داده های فونت بازیابی شده دقیقاً از همه جنبه ها با فرمت فونت ورودی مطابقت دارد.

برنامه های کاربردی فایل WOFF اغلب شامل ویژگی های اضافی مانند زیرمجموعه علامت، اعتبارسنجی یا افزودن ویژگی فونت هستند اما ضروری نیست. هم سازنده و هم عامل استفاده کننده باید اطمینان حاصل کنند که اعتبار داده های فونت زیرین حفظ می شود.

### ساختار فایل WOFF

ساختار فایل WOFF شبیه به فونت های sfnt است. بر اساس دایرکتوری جدولی است که شامل طول و افست جداول داده هر فونت است. تمام جداول بعد از این اطلاعات اولیه دنبال می شوند. فایل حاوی پایگاه داده فونت است که مانند فونت های اصلی است. ترتیب جداول نیز یکسان است اما ممکن است هر کدام فشرده شوند. دایرکتوری جدول WOFF جایگزین دایرکتوری جدول اصلی می شود.

یک فایل WOFF شامل موارد زیر است:

 * WOFFHeader - هدر فایل با نوع فونت و نسخه اصلی، همراه با افست به ابرداده و بلوک های داده خصوصی.
 * TableDirectory - دایرکتوری جداول فونت که اندازه اصلی، اندازه فشرده و مکان هر جدول را در فایل WOFF نشان می دهد.
 * FontTables - جداول داده فونت از فونت sfnt ورودی، فشرده شده تا پهنای باند مورد نیاز را کاهش دهد.
 * ExtendedMetadata - یک بلوک اختیاری از ابرداده توسعه یافته، که در قالب XML نمایش داده شده و برای ذخیره در فایل WOFF فشرده شده است.
 * PrivateData - یک بلوک اختیاری از داده های خصوصی برای طراح فونت، ریخته گری یا فروشنده برای استفاده.

### WOFF هدر
هدر WOFF شامل یک امضای شناسایی است که نوع داده های موجود در فایل را نشان می دهد. هدر WOFF به همراه فیلدهای آن به شرح زیر است.

|نوع|نام فیلد|توضیحات|
---|---|---|
|UInt32|امضا |0x774F4646 'wOFF' |
|UIint32| flavor | نسخه sfnt فونت ورودی.|
|UIint32| طول |اندازه کل فایل WOFF.|
|UIint16| numTables |تعداد ورودی های فهرست فونت جداول.|
|UIint16| رزرو شده | رزرو شده; روی صفر تنظیم کنید.|
|UIint32| totalSfntSize |اندازه کل مورد نیاز برای داده های فونت فشرده نشده، از جمله هدر sfnt، فهرست راهنمای و جداول فونت (شامل padding).|
|UIint16| majorVersion |نسخه اصلی فایل WOFF.|
|UIint16| minorVersion |نسخه کوچک فایل WOFF.|
|UIint32| metaOffset |Offset به بلوک فراداده، از ابتدای فایل WOFF.|
|UIint32| metaLength | طول بلوک ابرداده فشرده.|
|UIint32| metaOrigLength |اندازه فشرده نشده بلوک ابرداده.|
|UIint32| privOffset |Offset به بلوک داده خصوصی، از ابتدای فایل WOFF.|
|UIint32| privLength |طول بلوک داده خصوصی.|

## منابع

 * [فرمت فایل w3 WOFF](https://www.w3.org/TR/WOFF/)
