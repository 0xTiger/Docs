{
  "date": "2019-10-11",
  "keywords": [
"AVI",
"فیلم صوتی فشرده",
"فایل",
"افزونه",
"فرمت فایل",
"ظرف چند رسانه ای",
"XVid",
"DivX",
"کدک ها",
"فرمت فایل تبادل منابع",
"RIFF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل AVI - یک فایل صوتی تصویری Interleave",
  "description": "با فرمت فایل AVI و API هایی که می توانند فایل های AVI را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "AVI",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-av-fai"
}
},
  "lastmod": "2021-04-23"
}

## فایل AVI چیست؟ ##

فرمت فایل **AVI** یک فرمت فایل ظرف چندرسانه ای صوتی تصویری است که توسط مایکروسافت معرفی شده است. داده های صوتی و تصویری ایجاد شده و فشرده شده با استفاده از چندین کدک (Coders/Decoder) مانند **XVid** و **DivX** را نگه می دارد. از آنجایی که کدک‌های مختلف را می‌توان برای رمزگذاری محتویات AVI استفاده کرد، برنامه‌های بازیابی، یعنی پخش‌کننده‌های AVI، تنها در صورتی باید بتوانند این کدک‌ها را باز کنند که کدک‌های مورد نیاز را نصب کرده باشند که محتوای AVI با آن ایجاد شده است. این فرمت به طور پیش‌فرض در تمامی پلتفرم‌های **میکروسافت ویندوز** و همچنین تقریباً در تمام پلتفرم‌های اصلی دیگر پشتیبانی می‌شود. چندین برنامه کاربردی و API قابلیت ایجاد/ذخیره، خواندن و تبدیل AVI به فرمت های محبوب دیگر مانند MP4، MOV، WMV و غیره را فراهم می کنند.

## فرمت فایل AVI ##

فایلی با پسوند avi. یک فایل AVI است. این یک فرمت فرعی از فرمت فایل تبادل منابع (RIFF) است. RIFF داده ها را در بلوک ها یا تکه ها سازماندهی می کند که با یک تگ FourCC شناسایی می شوند. یک فایل AVI به سادگی یک تکه در یک فایل فرمت شده RIFF است.

در بخش فرعی اول، هدر فایل با تگ hdrl مشخص می شود. محتوای آن شامل عرض، ارتفاع و نرخ فریم ویدیو است. در بخش فرعی دوم، تگ حرکت نشان دهنده نرخ فریم ویدیو است. ویدئوی AVI از داده های صوتی/بصری واقعی در این بخش تشکیل شده است. همچنین یک زیرچونک اختیاری سوم با تگ idx1 وجود دارد که موقعیت تک تک تکه‌های داده متعلق به فایل را در فایل نشان می‌دهد.

### محدودیت ها ###

* اطلاعات نسبت ابعاد را نمی توان در مشخصات AVI اصلی کدگذاری کرد، اگرچه مشخصات OpenDML بعدی (AVI 2.0) یک روش استاندارد ارائه می دهد.

* اگرچه فایل‌های AVI به‌طور گسترده در تولیدات فیلم و تلویزیون مورد استفاده قرار می‌گیرند، روش‌های مختلف برای افزودن کد زمانی به آن‌ها با هم رقابت می‌کنند و بر قابلیت استفاده قالب تأثیر می‌گذارند.

* یک فایل ویدئویی کدگذاری شده در AVI نمی تواند از تکنیک فشرده سازی استفاده کند که به داده های فریم های آینده فراتر از فریم در حال کدگذاری (B-frame) نیاز دارد.

* استفاده از فایل های AVI با نرخ بیت متغیر (VBR) (مانند صدای MP3 با نرخ نمونه کمتر از 32 کیلوهرتز) مشکل ساز است.

* بسته به نحوه استفاده از فایل، یک فایل AVI که فیلم‌های ویژه با کیفیت استاندارد را به‌صورت معمولی مورد استفاده قرار می‌دهد، احتمالاً حدود 5 مگابایت در ساعت هزینه دارد.

* در صورتی که فایل‌های AVI نتوانند ضمیمه‌هایی مانند فونت‌ها و زیرنویس‌ها را در خود جای دهند، زیرنویس‌ها باید در جریان ویدئو کدگذاری شوند یا در یک فایل جداگانه توزیع شوند.


## تاریخچه مختصر ##

AVI توسط مایکروسافت در سال 1992 با هدف ارائه یک فرمت فایل صوتی و تصویری قوی تر و پیشرفته تر معرفی شد. این فرمت به سرعت با استفاده از اینترنت محبوب شد و به افراد اجازه می‌دهد فایل‌های ویدیویی را به‌طور مستقیم و غیرمستقیم از طریق ذخیره‌سازی رسانه مبتنی بر ابر به اشتراک بگذارند.

## منابع ##

* [AVI - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/Audio_Video_Interleave)


