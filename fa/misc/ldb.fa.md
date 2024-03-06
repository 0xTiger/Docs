{
  "date": "2023-04-20",
  "keywords": [
"فایل ldb",
"فایل ldb چیست",
"ldb شامل چه اطلاعاتی است",
"هدف از فایل ldb چیست؟",
"پسوند ldb",
"فایل",
"افزونه"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل LDB - فایل قفل Microsoft Access",
  "description": "در مورد فرمت LDB و اطلاعاتی که در آن وجود دارد بیاموزید.",
  "linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb-fa",
      "parent": "misc"
}
},
  "lastmod": "2023-04-20"
}

## فایل LDB چیست؟

یک فایل LDB یک فایل قفل است که توسط مایکروسافت اکسس برای جلوگیری از ویرایش همزمان یک پایگاه داده توسط چندین کاربر استفاده می شود. هنگامی که کاربر یک پایگاه داده Access را باز می کند، Access یک فایل LDB مربوطه را در همان فهرست پایگاه داده ایجاد می کند. این فایل حاوی اطلاعاتی درباره افرادی است که در حال حاضر از پایگاه داده استفاده می کنند و چه رکوردهایی را ویرایش می کنند.

فایل LDB با باز شدن پایگاه داده به طور خودکار توسط Microsoft Access ایجاد می شود و با بسته شدن پایگاه داده حذف می شود. توجه به این نکته ضروری است که فایل LDB هرگز نباید به صورت دستی حذف شود زیرا این امر می تواند باعث ایجاد مشکل در پایگاه داده شود.

اگر در پایگاه داده مایکروسافت اکسس با مشکل مواجه شدید، یک راه حل بالقوه این است که سعی کنید فایل LDB مرتبط با آن پایگاه داده را حذف کنید. با این کار هرگونه قفلی که ممکن است مانع از دسترسی شما به پایگاه داده شود، آزاد می شود. با این حال، قبل از انجام این کار حتما از پایگاه داده یک نسخه پشتیبان تهیه کنید، زیرا حذف فایل LDB در صورت انجام نادرست می تواند باعث از بین رفتن یا خراب شدن داده ها شود.

## فرمت فایل LDB - اطلاعات بیشتر

یک فایل LDB در مایکروسافت اکسس حاوی اطلاعاتی درباره کاربرانی است که در حال حاضر به پایگاه داده دسترسی دارند مانند نام کاربری، نام رایانه و زمان ورود به سیستم. فایل LDB همچنین حاوی اطلاعاتی در مورد قفل هایی است که در پایگاه داده قرار داده شده است، مانند رکوردهایی که توسط کدام کاربر ویرایش می شوند.

در اینجا لیست دقیق تری از انواع اطلاعاتی که در فایل LDB یافت می شود آورده شده است:

- ** نام کاربری ** - نام کاربری که در حال حاضر به پایگاه داده دسترسی دارد
- **نام رایانه** - نام رایانه ای که کاربر از آنجا به پایگاه داده دسترسی دارد
- **زمان ورود** - زمانی که کاربر برای اولین بار پایگاه داده را باز کرد
- **قفل های ضبط ** - اطلاعاتی در مورد رکوردهایی که در حال حاضر توسط کدام کاربر در حال ویرایش هستند
- **قفل شی** - اطلاعاتی درباره اینکه کدام اشیاء پایگاه داده (مانند جداول، فرم ها یا گزارش ها) در حال حاضر توسط کدام کاربر ویرایش می شوند.
- **اطلاعات اتصال** - اطلاعاتی در مورد نحوه اتصال کاربر به پایگاه داده (به عنوان مثال، اینکه آیا آنها از اتصال محلی یا شبکه استفاده می کنند)

اطلاعات موجود در فایل LDB توسط مایکروسافت اکسس برای جلوگیری از ایجاد تغییرات متناقض در یک پایگاه داده به طور همزمان توسط چندین کاربر استفاده می شود. هنگامی که کاربر تلاش می کند رکورد یا شی ای را ویرایش کند که قبلاً توسط کاربر دیگری قفل شده است، مایکروسافت اکسس پیامی را نشان می دهد که نشان می دهد شی قبلاً در حال استفاده است. فایل LDB با باز و بسته شدن پایگاه داده و ایجاد تغییرات در اشیاء قفل شده توسط کاربران به روز می شود.

## منابع
* [What is an LDB File?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)
