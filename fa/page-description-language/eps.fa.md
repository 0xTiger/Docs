{
  "date": "2019-12-12",
  "keywords": [
"EPS",
"فایل",
"افزونه",
"فرمت فایل",
"صفحه آرایی",
"پست اسکریپت کپسوله شده"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل EPS و APIهایی که می‌توانند فایل‌های EPS را ایجاد و باز کنند، بیاموزید.",
  "title": "فرمت فایل EPS - فایل پست اسکریپت کپسوله شده",
  "linktitle": "EPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-ep-fas"
}
},
  "lastmod": "2019-09-10"
}

## فایل EPS چیست؟

فایل .eps یک فایل تصویری است که با فرمت فایل Postscript Encapsulated روی دیسک ذخیره می شود. ممکن است حاوی هر ترکیبی از متن، گرافیک و تصویر باشد. فایل‌های EPS ممکن است شامل یک تصویر پیش‌نمایش بیت مپ باشد که در داخل آن برای نمایش توسط برنامه‌هایی که می‌توانند چنین فایل‌هایی را باز کنند، نمایش داده شود.

## تاریخچه مختصر فرمت فایل EPS

نگاهی سریع به فرمت فایل EPS از منظر تاریخچه اطلاعات زیر را نشان می دهد:

* اولین نسخه EPS توسط Adobe بین سال های 1985 و 1988 منتشر شد

* نسخه 2.0 مشخصات EPS در ژانویه 1989 منتشر شد

* مشخصات نسخه 3.0 EPS به عنوان یک سند جداگانه در سال 1992 منتشر شد. این آخرین نسخه منتشر شده است.


EPS، در ترکیب با مکانیسم فرمت کنوانسیون ساختار باز توضیح داده شده در بند 9 از مشخصات قراردادهای ساختار اسناد زبان پست اسکریپت Adobe، اساس نسخه های اولیه فرمت فایل Adobe Illustrator Artwork را تشکیل داد.

## فرمت فایل EPS

EPS یک فرمت اختصاصی است اما به صورت عمومی مستند شده است و مشخصات فرمت فایل EPS به صورت عمومی برای مرجع توسعه دهنده در دسترس است. EPS یک [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (کنوانسیون ساختار اسناد) است که با فرمت فایل مطابقت دارد و به تمام قوانین تعیین شده توسط DSC پایبند است. DSC یک فرمت فایل ویژه برای اسناد PostScript توسط Adobe است. هر برنامه ای که ادعا می کند می تواند فایل های EPS را بخواند باید با DSC سازگار باشد.

یک فایل EPS از دو بخش اصلی تشکیل شده است که در زیر توضیح داده شده است.

### پیش نمایش تصویر ###

یک فایل EPS معمولی حاوی یک تصویر پیش‌نمایش در قالبی است که برای استفاده راحت در جریان کاری که شامل چندین سیستم یا برنامه است، در نظر گرفته شده است. هدف از پیش‌نمایش، داشتن یک تصویر در قالبی است که اکثر برنامه‌های گرافیکی بتوانند آن را ارائه کنند. یک پیش‌نمایش معمولاً با وضوح کمتر، در ابعاد پیکسل و/یا در عمق بیت است. فایل پیش نمایش می تواند در یکی از چندین فرمت باشد. مشخصات EPS_3 سه فرمت پیش‌نمایش «ویژه دستگاه» را فهرست می‌کند:

* برای مکینتاش اپل، یک تصویر PICT که توسط برنامه QuickDraw استفاده می شود

* برای کامپیوترهای DOS، یک بیت مپ TIFF

* Windows Metafile.


PICT و Windows Metafile می توانند هم داده های بیت مپ و هم گرافیک برداری را در خود جای دهند. علاوه بر این، مشخصات، یک نمایش بسیار ساده مستقل از دستگاه را برای یک تصویر پیش نمایش بیت مپ تعبیه شده تعریف می کند. این نمایش به عنوان فرمت تبادل پست اسکریپت محصور شده (EPSI) شناخته می شود.

پیش‌نمایش EPSI یک بیت مپ است که به صورت هگزادسیمال ASCII نشان داده می‌شود، بین چند کامنت PostScript برای شناسایی پیچیده می‌شود و در نظر گرفته شده است که ساده و به راحتی قابل حمل باشد. به منظور تشخیص فایل‌های EPS با فرمت‌های پیش‌نمایش مختلف، پسوندهای مختلف فایل DOS و انواع فایل‌های مکینتاش در مشخصات EPS توصیه شده‌اند.

### کد پست اسکریپت

حداقل، فرمت فایل EPS باید شامل موارد زیر باشد:

* یک نظر سرصفحه، %!PS-Adobe-3.0 EPSF-3.0

* و یک نظر کادر محدود، %%BoundingBox: llx lly urx ury، که مرزهای تصویر را توصیف می کند. این چهار آرگومان با گوشه‌های پایین-چپ (llx، lly) و بالا-راست (urx، ury) گوشه‌های مرزبندی مطابقت دارند.


یک فایل EPS نمی تواند از هیچ یک از عملگرهای زیر استفاده کند:

*دستگاه باند،

* پشته cleardict

* صفحه کپی

* پاک کردن

* سرور خروجی

* فریم دستگاه

* grestoreall

* initclip

* Initgraphics

* initmatrix

*ترک کردن

* رندر باندها

* مجموعه جهانی

* دستگاه تنظیم صفحه

* مجموعه به اشتراک گذاشته شده

* کار شروع


## تبدیل EPS به فرمت های دیگر فایل

فایل های EPS را می توان با استفاده از برنامه های مختلف مانند Adobe Illustrator، Photoshop و PaintShop Pro به فرمت های تصویر استاندارد مانند [JPG](/image/jpeg/)، [PNG](/image/png/)، [TIFF](/image/tiff/) و [PDF](/pdf/) تبدیل کرد.

به دلیل وجود [security vulnerability](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) در فایل‌های EPS، Office 2016، Office 2013، Office 2010 و Office 365 قابلیت درج فایل‌های EPS را در اسناد آفیس غیرفعال کرده‌اند.

## منابع

* [پست اسکریپت محصور شده - توسط ویکی پدیا](https://en.wikipedia.org/wiki/Encapsulated_PostScript)


