{
  "date": "2021-07-15",
  "keywords": [
"TMP",
"افزونه",
"فایل",
"قالب",
"سیستم",
"فایل TMP",
"اسناد TMP",
"فایل های TMP",
"فایل موقت",
"کاربرد",
"برنامه ها"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "TMP - فرمت فایل موقت",
  "description": "با فرمت فایل TMP و APIهایی که می توانند فایل های TMP را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "TMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-tm-fap"
}
},
  "lastmod": "2021-07-15"
}

## فایل TMP چیست؟ ##

یک فایل TMP به یک پشتیبان گیری موقت، ذخیره سازی، یا سایر سیستم فایل های تولید شده توسط یک برنامه نرم افزاری اشاره دارد. گاهی اوقات به عنوان یک فایل نامرئی ایجاد می شود و اغلب با خروج از برنامه از بین می رود. فایل های TMP همچنین می توانند برای ذخیره موقت اطلاعات در حین ساخت فایل جدید استفاده شوند.

## فرمت فایل TMP ##

یک فایل TMP معمولا از داده های خام تشکیل شده است که به عنوان مرحله ای در فرآیند تبدیل مواد از یک سبک به سبک دیگر استفاده می شود. Microsoft Word و Apple Safari دو برنامه‌ای هستند که می‌توانند فرمت فایل TMP را تولید و استفاده کنند.

اسناد TMP تولید شده، در تئوری، باید به طور خودکار زمانی که برنامه بسته می شود یا دستگاه خاموش می شود، حذف شوند. در عمل، همیشه اینطور نیست. در نتیجه، هنگام پیمایش در اسناد برنامه خود، ممکن است با فایل های گذرا مواجه شوید که به طور فعال توسط سیستم یا هیچ نرم افزار دیگری استفاده نمی شود.

### حافظه کمکی ###

حافظه مجازی در سیستم عامل ها استفاده می شود، با این حال، برنامه هایی که از حجم عظیمی از اطلاعات استفاده می کنند ممکن است نیاز به ایجاد اسناد موقت داشته باشند.

### ارتباط بین فرآیندی ###

اکثر سیستم عامل ها برای انتقال داده ها بین برنامه ها، مانند لوله ها، سوکت ها یا حافظه اصلی، اصول اولیه را ارائه می دهند، اما ساده ترین روش انتقال فایل ها به یک فایل موقت و توصیه به برنامه دریافت کننده مکان فایل موقت است.


## مشخصات فنی ##

به دست آوردن نام اسناد موقت متمایز معمولاً توسط سیستم عامل ها و برنامه های نرم افزاری ارائه می شود.
فایل های موقت را می توان با استفاده از توابع کتابخانه mkstemp یا tmpfile با خیال راحت در سیستم های POSIX تولید کرد. برخی از سیستم ها شامل برنامه قبلی POSIX (از زمان گذشته) mktemp هستند. این فایل‌ها معمولاً در دایرکتوری موقت معمولی در پلتفرم‌های یونیکس در /TMP یا %TEMP% (ویژه برای ورود به سیستم) در ماشین‌های ویندوز یافت می‌شوند.

هنگامی که برنامه متوقف می شود یا سند بسته می شود، فایل گذرا تولید شده با tmpfile به طور خودکار حذف می شود. GetTempFileName (ویندوز) یا tmpnam (POSIX) را می توان برای ایجاد نام فایل موقتی که بیشتر از برنامه ای که آن را ایجاد کرده است، استفاده کرد.

## ارجاع ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)