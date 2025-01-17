{
  "date": "2022.01.31",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فایل P7S - پیام ایمیل با امضای دیجیتال",
  "description": "درباره فرمت فایل P7S و APIهایی که می‌توانند فایل‌های P7S را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "P7S",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-p7-fas"
}
},
  "lastmod": "2022.01.31"
}

## فایل P7S چیست؟

فایل P7S یک امضای دیجیتال است که با یک ایمیل امضا شده دیجیتال دریافت می شود. وجود این فایل به عنوان پیوست همراه با ایمیل تایید می کند که ایمیل از منبع معتبر ارسال شده است. این تضمین می کند که فرستنده یک گواهی نامه امضای ایمیل روی رایانه خود نصب کرده است. هنگامی که چنین ایمیل امضا شده ای از رایانه کاربر ارسال می شود، فایل P7S به آن پیوست می شود که حاوی نام فرستنده است. سرویس گیرندگان ایمیلی که از ایمیل های امضا شده پشتیبانی می کنند می توانند اطلاعات فرستنده را ببینند.

## فرمت فایل P7S - اطلاعات بیشتر

S/MIME (برنامه های افزودنی اینترنتی ایمن/چند منظوره) فایل های P7S حاوی اطلاعات در قالب متن ساده است که قابل خواندن توسط انسان است. کلاینت‌های ایمیل مانند Microsoft Outlook، Apple Mail و Mozilla Thunderbird از خواندن اطلاعات امضا شده دیجیتالی از یک ایمیل S/MIME پشتیبانی می‌کنند. امضای یک ایمیل هویت فرستنده را تأیید می کند و به گیرنده می گوید که پیام معتبر است. وقتی ایمیل‌ها از کلاینت‌های ایمیل دانلود می‌شوند (به‌عنوان [EML](/email/eml/) یا [MSG](/email/msg/))، این فایل‌های P7S به همراه این ایمیل‌ها پیوست می‌شوند.

یک فایل P7S حاوی اطلاعات زیر است:

 * منبع منبع ایمیل
 * تاریخ و ساعت ارسال،
 * این که آیا در حین انتقال اصلاح شده است

این اطلاعات با استفاده از فناوری رمزنگاری کلید عمومی شماره 7 (PKCS7) برای پیوست کردن دیجیتالی امضاهای رمزگذاری شده به ایمیل جاسازی شده است.

## منابع ##

* [ابزار ثبت نام مایکروسافت](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)


