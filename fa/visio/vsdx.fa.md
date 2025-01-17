{
  "date" : "2019-10-11",
  "keywords" : [ "vsdx file", "vsdx file format", "what is a vsdx file", "file", "vsdx example", "vsdx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSDX",
  "description":"درباره فرمت فایل VSDX و APIهایی که می توانند فایل های VSDX را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx-fa",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## فایل VSDX چیست؟

فایل‌های با پسوند vsdx. فرمت فایل Microsoft Visio را نشان می‌دهند که از Microsoft Office 2013 به بعد معرفی شده است. این برنامه برای جایگزینی فرمت فایل باینری، [.VSD](/visio/vsd/)، که توسط نسخه‌های قبلی مایکروسافت ویزیو پشتیبانی می‌شود، ایجاد شده است. همچنین در Visio Services در Microsoft SharePoint Server 2013 پشتیبانی می شود و برای انتشار در سرور شیرپوینت نیازی به فرمت فایل واسطه ای ندارد. فایل‌های Visio برای ایجاد نقشه‌هایی که شامل اشیاء بصری، نمودارهای جریان، نمودار UML، جریان اطلاعات، نمودارهای سازمانی، نمودارهای نرم‌افزار، طرح‌بندی شبکه، مدل‌های پایگاه داده، نقشه‌برداری اشیا و سایر اطلاعات مشابه هستند، استفاده می‌شوند. فایل‌های تولید شده با استفاده از Visio را می‌توان به فرمت‌های مختلف فایل مانند [PNG](/image/png/)، [BMP](/image/bmp/)، [PDF](/pdf/) و موارد دیگر صادر کرد.

## فرمت فایل ##

فایل های VSDX بر اساس قراردادهای بسته بندی باز و XML هستند و توسعه دهندگان می توانند با یادگیری نحوه کار با این فایل ها به صورت برنامه نویسی از این فرمت بهره مند شوند. این فرمت بسیاری از ساختارهای XML مشابه قطعات خود را از فرمت فایل Visio XML Drawing (vdx.) به ارث می برد. قابلیت همکاری با فایل های Visio بسیار افزایش یافته است زیرا نرم افزار شخص ثالث می تواند فایل های Visio را در سطح فرمت فایل دستکاری کند.

برخی از انواع فایل های دیگر که فرمت فایل Visio 2013 را تشکیل می دهند عبارتند از:

* vsdm. (نقاشی با قابلیت ماکرو Visio)

* .vssx (شابلون Visio)

* .vssm (استنسیل ماکرو فعال Visio)

* vstx. (الگوی Visio)

* .vstm (قالب ماکرو فعال Visio)


فرمت فایل Visio 2013 از ابزاری ساختاریافته برای ذخیره داده های برنامه همراه با منابع مرتبط در یک آرشیو مانند [ZIP](/compression/zip/) استفاده می کند. فایل ZIP را می توان با استفاده از هر ابزار استخراج استاندارد که در آن انواع فایل های دیگر نیز وجود دارد استخراج کرد. شما فقط می توانید پسوند فایل .vsdx را با .zip در ویندوز اکسپلورر جایگزین کنید تا محتویات داخل فایل VSDX را ببینید.

هر فایل Visio به عنوان بسته ای گفته می شود که فایل ها یا قطعات دیگری را در خود نگه می دارد. یک قسمت بسته می تواند یک فایل XML، یک تصویر یا حتی یک راه حل VBA باشد. قسمت های درون بسته را می توان به بخش های سند و رابطه تقسیم کرد.

### سند ###

بخش‌های سند حاوی محتوای واقعی و فراداده فایل Visio هستند، مانند نام فایل، صفحه اول و تمام اشکالی که در آن وجود دارد، و حتی اتصالات داده‌ای برای اشکال. تصاویر و فایل های متنی داخل بسته جزء سند محسوب می شوند.

### روابط ###

بخش های ارتباطی یک فایل Visio در پوشه \_rels ذخیره می شوند و نحوه ارتباط قطعات داخل بسته با هر یک را توضیح می دهند. همچنین ساختار فایل را ارائه می دهد. یک سند XML مستقل از رابطه والد/فرزند عناصر برای تعیین رابطه موجودیت ها با یکدیگر استفاده می کند. یک فرمت فایل معتبر Visio 2013 شامل مجموعه صحیح قطعات و بسته شامل روابط بین قطعات است.

بخش های رابطه اسناد XML هستند که روابط بین بخش های مختلف سند را در بسته توصیف می کنند. آنها ارتباط بین دو مورد را تعریف می کنند: یک منبع مشخص (تعریف شده با نام و مکان فایل رابطه) و یک بخش سند هدف مشخص. به عنوان مثال، از قطعات رابطه برای توصیف اینکه کدام استادهای شکل با فایل مرتبط هستند، چگونه صفحات با فایل و به یکدیگر مرتبط هستند، یا اینکه چگونه تصاویر و اشیاء با یک صفحه خاص ارتباط دارند، استفاده می شود.

## منابع ##

* [مقدمه ای بر فرمت فایل Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


