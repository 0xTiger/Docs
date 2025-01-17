{
  "date": "2021-06-30",
  "keywords": [
"فایل exe",
"فرمت فایل exe",
"یک فایل exe چیست",
"فایل",
"مثال exe",
"پسوند فایل exe",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "فایل exe یک فایل اجرایی مایکروسافت است که بر روی سیستم عامل ویندوز اجرا می شود. درباره فرمت فایل EXE بیشتر بدانید.",
  "title": "فایل EXE اجرایی چیست؟",
  "linktitle": "EXE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ex-fae"
}
},
  "lastmod": "2021-06-30"
}

## فایل EXE چیست؟

کلمه EXE مخفف ** اجرایی ** است. فایل exe برنامه ای است که می تواند بر روی سیستم عامل مایکروسافت ویندوز اجرا شود. توسعه دهندگان برنامه ها بیشتر برنامه های خود را برای سیستم عامل ویندوز در قالب اجرایی به صورت فایل exe منتشر می کنند. این فرمت استاندارد فایل برای اجرای برنامه ها در ویندوز است. **Setup.exe**، **Install.exe** و **cmd.exe** برخی از نام های رایج و آشنای فایل های EXE هستند.

## فرمت فایل EXE

کامپایلرهای MS-DOS با مدل های حافظه با محدودیت حافظه 64K معرفی شدند. مفهوم کلی این است که رجیسترهای سگمنت مختلف را در CPU x86 (CS، DS، ES، SS) تنظیم کنیم تا به بخش‌های مختلف یا مشابه اشاره کنند، بنابراین درجات مختلفی از دسترسی به حافظه را ممکن می‌سازند. برخی از مدل های حافظه خاص عبارت بودند از:

- **Tiny**: تمام دسترسی های حافظه 16 بیتی هستند (ثبت نام های بخش بدون تغییر). به جای فایل EXE، یک فایل COM تولید می کند.
- **Small**: تمام دسترسی های حافظه 16 بیتی هستند (ثبت نام های بخش بدون تغییر).
- ** فشرده**: آدرس های داده شامل هر دو بخش و افست، بارگیری مجدد رجیسترهای DS یا ES در هنگام دسترسی و اجازه حداکثر 1M داده است. دسترسی‌های کد، رجیستر CS را تغییر نمی‌دهند، و اجازه 64K کد را می‌دهند.
- **متوسط**: آدرس های کد شامل آدرس بخش، بارگیری مجدد CS در هنگام دسترسی و اجازه حداکثر 1M کد است. دسترسی به داده‌ها، رجیسترهای DS و ES را تغییر نمی‌دهند، و اجازه می‌دهند 64K داده.
- **بزرگ**: هر دو آدرس کد و داده جفت (قطعه، افست) هستند و همیشه آدرس های بخش را بارگذاری مجدد می کنند. کل فضای حافظه 1M بایتی هم برای کد و هم برای داده در دسترس است.
- **Huge**: همانند مدل بزرگ، با محاسبات اضافی که توسط کامپایلر ایجاد می شود تا امکان دسترسی به آرایه های بزرگتر از 64K را فراهم کند.

توسعه دهندگان باید تصمیم بگیرند که در هنگام ایجاد یک فایل exe چه مدلی باید انتخاب شود.

### فرمت فایل EXE قابل حمل

فرمت فایل قابل حمل قابل حمل (PE) شامل تعدادی هدر اطلاعاتی است که در زیر لیستی از هدرها آمده است:

- **سربرگ DOS**: هدر MS-DOS یا سازگاری رو به عقب یا کاهش برازنده انواع فایل های جدید را تضمین می کند.
- ** PE Header **: در آفست 60 (0x3C) از ابتدای هدر DOS یک اشاره گر به هدر PE File است.
- **COFF Header**: سربرگ COFF دارای اطلاعاتی است که برای یک فایل اجرایی مفید است و برخی اطلاعات بیشتر برای یک فایل شیء مفید است.
- ** PE Optional Header **: PE Optional Header مستقیماً بعد از هدر COFF رخ می دهد و برخی منابع حتی دو هدر را به عنوان بخشی از یک ساختار نشان می دهند.
- **Section Table**: بلافاصله بعد از PE Optional Header یک جدول بخش پیدا می کنیم. جدول بخش شامل آرایه ای از ساختارهای IMAGE_SECTION_HEADER است.
- **بخش های قابل نقشه برداری**: می تواند با نگاشت کد یک کتابخانه در بیش از یک فرآیند، فضا را در حافظه ذخیره کند.

## آیا می توانید یک فایل EXE را در مک اجرا کنید؟

فایل های exe به عنوان فایل های اجرایی در سیستم عامل مک استفاده نمی شوند. با این حال، اگر می خواهید یک فایل exe را در سیستم عامل مک اجرا کنید، می توان از روش های زیر استفاده کرد.

 1. **Wine** - Wine راه حل عالی برای افرادی است که می خواهند از برنامه های رایانه شخصی خود در سیستم های مک استفاده کنند. این مخفف مخفف عبارت Wine Is Not A Emulator است، به این معنی. Wine همان محیط دایرکتوری هایی را ایجاد می کند که توسط مایکروسافت استفاده می شود تا بتوانید برنامه ویندوز خود را با استفاده از آن اجرا کنید.
 2. **ماشین های مجازی** - یک ماشین مجازی ویندوز با استفاده از دسکتاپ موازی یا جعبه مجازی VM ایجاد کنید و برنامه خود را در داخل ماشین مجازی اجرا کنید.
 3. **Boot Camp** - نصب و پیکربندی Windows Boot Camp در سیستم عامل مک به شما امکان می دهد سیستم عامل ویندوز را روی دستگاه مک اجرا کنید.

## منابع

* [.exe- توسط Wikipewdia](https://en.wikipedia.org/wiki/.exe)

* [x86 Disassembly/Windows Executable Files](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)


