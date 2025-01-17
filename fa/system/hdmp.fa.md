{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فایل HDMP - فرمت فایل Windows Heap Dump",
  "description": "درباره فرمت فایل HDMP و APIهایی که می‌توانند فایل‌های HDMP را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "HDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-hdm-fap"
}
},
  "lastmod": "2022-08-19"
}

## فایل HDMP چیست؟

فایل HDMP هنگامی که یک برنامه یا برنامه به دلیل خطا از کار می افتد، یک حافظه فشرده نشده تخلیه می شود. این برنامه فقط توسط ویندوز XP/Vista ایجاد شده است و حاوی تصویری از وضعیت برنامه در هنگام خراب شدن است. از آنجایی که فایل‌های HDMP فشرده نیستند، در مقایسه با فایل‌های Minidump [MDMP](/system/mdmp/) که برای گزارش‌دهی فشرده شده‌اند، فضای بیشتری روی دیسک اشغال می‌کنند.

برنامه هایی که می توانند برای **باز کردن** یا تجزیه و تحلیل فایل های HDMP استفاده شوند عبارتند از Microsoft Visual Studio با ابزارهای Debugging برای ویندوز.

## فرمت فایل HDMP

فایل‌های HDMP به‌عنوان فایل‌های باینری روی دیسک ذخیره می‌شوند و اگر بدون برنامه‌های کاربردی مناسب باز شوند، هیچ مزیتی ندارند. اینها حاوی داده های مربوط به سیستم هستند که هنگام وقوع خطا ثبت شده اند.

### تفاوت بین فرمت های فایل HDMP و MDMP

HDMP فایل‌های ذخیره‌سازی حافظه غیرفشرده هستند. در مقابل، MDMP فایل های کوچک دامپی هستند که برای کاهش حجم فایل فشرده شده و برای گزارش مشکل به مایکروسافت ارسال می شوند.

## ارجاع ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


