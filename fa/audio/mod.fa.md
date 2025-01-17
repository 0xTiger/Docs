{
  "date": "2021-08-04",
  "keywords": [
"مد",
"mp3",
"فایل",
"افزونه",
"قالب",
"فرمت فایل مود چیست",
"موسیقی",
"فرمت فایل mod",
"مود در مقابل MP3",
"مشخصات فرمت فایل mod"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل MOD و API هایی که می توانند فایل های MOD را ایجاد، تبدیل و باز کنند، بیاموزید.",
  "title": "MOD - فایل ماژول موسیقی",
  "linktitle": "MOD",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mo-fad"
}
},
  "lastmod": "2021-08-04"
}

## فایل MOD چیست؟
یک فایل با پسوند .mod یک فایل ماژول موسیقی است که با استفاده از قالب استاندارد ماژول موسیقی ایجاد شده است که بر اساس فرمت ماژول **Amiga** توسعه یافته توسط Karsten Obarski و با نرم افزار **Ultimate Soundtracker** برای Commodore منتشر شده است. سیستم آمیگا مشابه فایل [MIDI](/audio/mid/)، شامل الگوهای نت و نمونه های صوتی است که نشان دهنده سازهای مختلفی است که مطابق نت ها پخش می شوند. فایل‌های MOD به‌ویژه در بازی‌های ویدیویی به‌عنوان موسیقی پس‌زمینه و در خرده‌فرهنگ هنر کامپیوتری **demoscene** استفاده می‌شوند.

## فرمت فایل MOD

MOD یک فرمت فایل کامپیوتری است که عملکرد اصلی آن نمایش موسیقی است و اولین فرمت فایل ماژول بود. فایل‌های MOD از پسوند فایل .mod استفاده می‌کنند، به جز در **Amiga** که هدر فایل را برای تعیین نوع فایل می‌خواند، بنابراین به پسوندهای نام فایل متکی نیست. یک فایل MOD از مجموعه ای از سازهای مختلف به شکل نمونه، تعدادی الگو که نحوه و زمان نواختن نمونه ها را مشخص می کند، و لیستی از الگوهای نواختن به چه ترتیبی است.

### مشخصات فرمت فایل MOD

یک الگوی فایل MOD در واقع در یک رابط کاربری ترتیب‌دهنده به‌عنوان یک جدول با یک ستون در هر کانال طراحی شده است، بنابراین این جدول دارای چهار ستون است (یکی برای هر کانال سخت‌افزاری آمیگا. هر ستون دارای 64 ردیف است).

یک سلول در جدول می‌تواند باعث شود یکی از اقدامات زیر در کانال ستون آن هنگام رسیدن به زمان سطر آن اتفاق بیفتد:

- شروع یک ساز با نواختن یک نت جدید در این کانال با حجم مشخص، احتمالاً با یک افکت ویژه روی آن
- تغییر صدا یا جلوه ویژه در حال اعمال به یادداشت فعلی
- تغییر جریان الگو؛ به موقعیت آهنگ یا الگوی خاص یا حلقه درون یک الگو بپرید
- هیچ کاری نکن هر نت موجود در این کانال پخش می شود

ابزار یک نمونه منفرد همراه با مشخصات اختیاری است که بخشی از نمونه را می توان برای حفظ یک نت جامد تکرار کرد.

### زمان سنجی
حداقل بازه زمانی 0.02 ثانیه در فایل اصلی MOD یا یک بازه خالی عمودی (VSync) بود، زیرا نرم افزار اصلی از زمان بندی VSync مانیتور استفاده می کرد که با فرکانس 50 هرتز (برای PAL) یا 60 هرتز (برای NTSC) کار می کرد. برای زمان بندی

## منابع

* [MOD (فرمت فایل) - توسط ویکی پدیا](https://en.wikipedia.org/wiki/MOD_(file_format))


