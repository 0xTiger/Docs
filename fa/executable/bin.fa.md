{
   "date":"2023-07-20",
   "keywords":[
"صندوقچه",
"فایل BIN",
"فایل",
"پسوند فایل BIN",
"افزونه",
"فایل"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"فرمت فایل BIN - فایل اجرایی Unix",
   "description":"درباره قالب BIN و APIهایی که می‌توانند فایل‌های BIN را ایجاد و باز کنند، بیاموزید.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin-fa",
         "parent":"executable"
}
},
   "lastmod":"2023-07-20"
}

## فایل BIN چیست؟

فایل BIN یک فایل اجرایی بر روی سیستم عامل های مبتنی بر یونیکس مانند لینوکس یا FreeBSD است. این برنامه دارای یک برنامه کامپایل شده متشکل از کد باینری مشتق شده از کد منبع است که آن را با معماری سیستم زیرین سازگار می کند. فایل‌های BIN اجرایی یونیکس را می‌توان با فایل‌های Windows.EXE و فایل‌های macOS.APP از نظر نقش آنها به عنوان فرمت‌های اجرایی مقایسه کرد.

در حوزه توسعه نرم افزار برای سیستم های یونیکس، فایل های BIN معمولاً توسط توسعه دهندگان برای بسته بندی و توزیع برنامه ها استفاده می شود. آنها ابزاری مناسب برای ارائه نرم افزار به کاربران ارائه می دهند که امکان نصب و اجرای آسان را فراهم می کند. در کنار فایل‌های BIN، انواع دیگری از فایل‌های اجرایی یونیکس، از جمله [.ELF](/executable/elf/)، .X86، [.RUN](/executable/run/) و .X86_64 وجود دارد که هر کدام برای سخت‌افزار یا نیازهای سیستمی خاص طراحی شده‌اند.

وقتی صحبت از ساختار داخلی یک فایل BIN می شود، شامل داده های کدگذاری شده ای است که سیستم عامل یونیکس از آنها برای شناسایی، خواندن و اجرای برنامه محصور شده استفاده می کند. این سیستم برای شناسایی فایل BIN به عنوان یک فایل اجرایی و به دنبال آن تفسیر و اجرای دستورالعمل های باینری موجود در داخل، به امضاها یا هدرهای فایل خاص متکی است.

فایل‌های BIN اغلب همراه با فایل **INSTALL.TXT** همراه هستند که دستورالعمل‌های دقیقی را در مورد نحوه نصب و راه‌اندازی صحیح برنامه ارائه می‌دهد. این مستندات تضمین می‌کند که کاربران می‌توانند فرآیند نصب را با موفقیت طی کنند و بدون پیچیدگی شروع به استفاده از نرم‌افزار کنند.

## چگونه فایل BIN را باز کنیم؟

فایل های BIN برای باز کردن و مشاهده مستقیم طراحی نشده اند. با این حال، می توانید برنامه ها را اجرا کنید یا داده های موجود در آنها را استخراج کنید. برای دسترسی به محتویات یک فایل BIN، با فرض اینکه نام فایل BIN sample.bin باشد، این مراحل را در خط فرمان دنبال کنید:

1. **اطمینان از مجوزهای اجرایی:**

قبل از اجرای فایل BIN، مطمئن شوید که مجوزهای لازم برای اجرا به عنوان یک فایل اجرایی را دارد. از دستور استفاده کنید:

```
$ chmod +x sample.bin
```

این دستور به فایل امتیازات اجرایی می دهد.

2. **فایل BIN را اجرا کنید:**

پس از تنظیم مجوزهای اجرایی، می توانید فایل BIN را با وارد کردن دستور زیر اجرا کنید:

```
$ ./sample.bin
```

**هشدار**

_هنگام برخورد با فایل های BIN بارگیری شده یا ایمیل شده احتیاط کنید، زیرا می توانند توسط مجرمان سایبری برای توزیع بدافزار استفاده شوند. برای کاهش خطر حملات اجرایی مخرب، فقط فایل های BIN را از منابع قابل اعتماد اجرا کنید._

## سایر فایل های BIN

در اینجا انواع فایل دیگری وجود دارد که از پسوند فایل **.bin** استفاده می کنند.

- [BIN - MacBinary Encoded File](/compression/bin/)
- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## منابع
* [How to Execute Binary Files in Linux](https://linuxhint.com/execute-binary-files-in-linux/)