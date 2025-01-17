{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"فایل cfg",
"فایل اتصال سرور cfg citrix",
"فایل cfg چیست",
"نحوه باز کردن فایل cfg",
"فایل",
"پسوند فایل cfg",
"افزونه"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل CFG - فایل اتصال سرور Citrix",
  "description": "درباره فرمت فایل اتصال سرور CFG Citrix و APIهایی که می‌توانند فایل‌های CFG را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CFG Citrix",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-citrix-fa",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## فایل CFG چیست؟

فایل CFG با نام ** فایل اتصال سرور Citrix ** نیز شناخته می شود. این جزء حیاتی است که برای ایجاد اتصال به سرور Citrix استفاده می شود. این فایل حاوی اطلاعات ضروری برای اتصال موفق بین دستگاه مشتری و سرور Citrix است. معمولاً شامل جزئیاتی مانند نام میزبان یا آدرس IP سرور، پورت سرور خاص برای استفاده، و اعتبار مورد نیاز برای احراز هویت است که اغلب شامل نام کاربری و رمز عبور است.

این فایل‌های CFG نقش مهمی در پیکربندی نرم‌افزار مشتری Citrix دارند و کاربران را قادر می‌سازد تا به سرورهای مختلف Citrix متصل شوند. آنها به‌عنوان فایل‌های پیکربندی عمل می‌کنند که فرآیند اتصال را با از پیش تعریف پارامترهای ضروری ساده می‌کنند و نیاز کاربران را برای وارد کردن دستی این اطلاعات هر بار که می‌خواهند به سرور Citrix دسترسی داشته باشند، کاهش می‌دهند.

## سرور سیتریکس

سرور Citrix که با نام های Citrix XenApp یا Citrix XenDesktop نیز شناخته می شود، سرور تخصصی است که در راه حل های مجازی سازی Citrix استفاده می شود. Citrix شرکتی است که فناوری دسترسی از راه دور، مجازی سازی برنامه ها و مجازی سازی دسکتاپ را ارائه می دهد. سرورهای Citrix با تسهیل تحویل برنامه‌ها و محیط‌های دسکتاپ به کاربران راه دور یا دستگاه‌های مشتری، نقش اصلی را در این راه‌حل‌ها ایفا می‌کنند.

در اینجا نحوه عملکرد سرور Citrix به طور معمول آمده است:

1.  **تحویل برنامه و دسکتاپ**: سرورهای Citrix میزبان برنامه ها و محیط های دسکتاپ هستند. به جای اجرای مستقیم نرم افزار بر روی دستگاه کاربر، برنامه یا دسکتاپ روی سرور Citrix اجرا می شود و تنها رابط کاربری به دستگاه مشتری منتقل می شود. این به کاربران اجازه می دهد تا از طیف گسترده ای از دستگاه ها از جمله رایانه های شخصی، مک ها، تبلت ها و گوشی های هوشمند به برنامه های کاربردی ویندوز و دسکتاپ دسترسی داشته باشند.
    
2.  **دسترسی از راه دور**: سرورهای Citrix دسترسی از راه دور به برنامه‌ها و دسکتاپ‌ها را فعال می‌کنند و این امکان را برای کاربران فراهم می‌کنند که از هر کجا با اتصال به اینترنت کار کنند. این امر به ویژه برای تیم های از راه دور و توزیع شده ارزشمند است، زیرا تجربه محاسباتی ثابت و ایمن را فراهم می کند.
    
3.  **تعادل بار**: سرورهای Citrix اغلب در کلاسترها کار می کنند تا بار اتصالات ورودی را متعادل کنند. تعادل بار تضمین می کند که درخواست های کاربر به طور مساوی بین سرورها توزیع می شود و عملکرد و در دسترس بودن را بهینه می کند.

## فایل اتصال سرور Citrix

یک فایل اتصال سرور Citrix، که اغلب به عنوان فایل CFG نامیده می شود، یک فایل پیکربندی است که در محیط های Citrix برای ایجاد ارتباط بین دستگاه های مشتری و سرورهای Citrix استفاده می شود. جزئیات کلیدی که معمولاً در فایل اتصال سرور Citrix گنجانده شده است ممکن است شامل موارد زیر باشد:

1.  **نام میزبان یا آدرس IP**: این مکان شبکه سرور Citrix را مشخص می کند که دستگاه مشتری باید به آن متصل شود. محل میزبانی منابع Citrix را مشخص می کند.
    
2.  **درگاه سرور**: شماره پورتی که برای ارتباط با سرور Citrix استفاده می شود. این تضمین می کند که داده ها به سرویس صحیح روی سرور منتقل می شوند.
    
3.  ** نام کاربری و رمز عبور **: اعتبار کاربری، از جمله نام کاربری و رمز عبور، ممکن است برای اهداف احراز هویت گنجانده شود. این اعتبار به کاربران امکان می دهد هویت خود را ثابت کنند و به منابع Citrix دسترسی پیدا کنند.
    
4.  **تنظیمات اتصال**: فایل های CFG می توانند شامل تنظیمات اتصال مختلفی مانند تنظیمات رمزگذاری، مقادیر زمان پایان جلسه و گزینه های نمایش باشند. این تنظیمات به پیکربندی تجربه کاربر و پارامترهای امنیتی کمک می کند.
    
5.  **پیکربندی منبع**: بسته به پیکربندی، فایل CFG ممکن است مشخص کند که کدام منابع Citrix (برنامه های کاربردی یا دسکتاپ) باید هنگام برقراری اتصال راه اندازی شوند.

## فرمت های فایل استفاده شده توسط Citrix

سرورهای Citrix و فناوری‌های مرتبط Citrix از چندین فرمت فایل پشتیبانی می‌کنند تا بتوانند برنامه‌ها، دسکتاپ‌ها و محتوا را به کاربران راه دور تحویل دهند. در اینجا چند فرمت فایل رایج مرتبط با استقرار سرور Citrix آورده شده است:

1.  **ICA (معماری محاسباتی مستقل)**:
    
- **.ica**: فایل ICA جزء اصلی برنامه Citrix و تحویل دسکتاپ است. این شامل اطلاعاتی در مورد اتصال به سرور Citrix، مانند آدرس سرور، پورت، تنظیمات رمزگذاری، و تنظیمات برگزیده نمایش است. هنگامی که کاربر روی منبع Citrix کلیک می‌کند، فایل [.ica](/misc/ica/) تولید می‌شود و توسط مشتری Citrix Receiver (یا Citrix Workspace) برای برقراری ارتباط استفاده می‌شود.
2.  **بسته های گیرنده سیتریکس (یا فضای کاری سیتریکس)**:
    
- **.exe**: بسته های نصب Citrix Receiver یا Citrix Workspace اغلب در قالب قابل اجرا برای سیستم عامل های مختلف ارائه می شوند (به عنوان مثال، [.exe](/executable/exe/) برای Windows، [.dmg](/compression/dmg/) برای macOS). این بسته ها به کاربران اجازه می دهد تا نرم افزار مشتری را روی دستگاه های خود نصب کنند.
3.  **برنامه Citrix Workspace (گیرنده سابق Citrix)**:
    
- **.app**: در macOS، Citrix Workspace App به عنوان فایل برنامه macOS [.app](/executable/app/) بسته بندی شده است.
4.  **سازگاری با مرورگر وب**:
    
- راه حل های Citrix را می توان از طریق مرورگرهای وب، به طور معمول از HTML5 برای دسترسی مبتنی بر وب استفاده کرد. کاربران از طریق URL ها بدون نیاز به فرمت های فایل خاصی به منابع Citrix متصل می شوند.
5.  **تصاویر دیسک دسکتاپ مجازی**:
    
- **.vhd، .vhdx**: Citrix XenDesktop و XenApp می توانند دسکتاپ و برنامه های کاربردی مجازی را با استفاده از فایل های هارد دیسک مجازی [VHD](/disc-and-media/vhd/) یا [VHDX](/disc-and-media/vhdx/) ارائه دهند.
6.  **فراداده انتشار منابع**:
    
-***
7.  **فایل های درایور چاپگر**:
    
- محیط‌های Citrix ممکن است به فایل‌های درایور چاپگر خاصی نیاز داشته باشند (به عنوان مثال، inf.) برای اطمینان از عملکرد مناسب چاپ هنگام استفاده از برنامه‌های از راه دور.
8.  **اطلاعات مشخصات کاربر**:
    
- **.upm**: Citrix Profile Management می‌تواند داده‌های نمایه کاربر را در فایل‌های upm. ذخیره کند تا تجربیات کاربر ثابتی را در جلسات و دستگاه‌ها ارائه دهد.
9.  **فایل های پیکربندی**:
    
- **.conf**: فایل‌های پیکربندی مختلف، به عنوان مثال، ممکن است برای تعریف تنظیمات اجزای Citrix، مانند فایل‌های پیکربندی برای سرور مجوز Citrix (مانند CtxLicChk.conf) استفاده شود.
10.  **پیکربندی Citrix ADC (NetScaler)**:

- **.nsconfig:** فایل های پیکربندی برای Citrix Application Delivery Controllers (ADC)، که قبلاً NetScaler نامیده می شد، تنظیمات مربوط به تعادل بار، امنیت و مدیریت ترافیک را ذخیره می کند.

## چگونه فایل CFG را باز کنیم؟

برنامه هایی که فایل های CFG را باز می کنند یا به آنها ارجاع می دهند

- سرویس گیرنده دسترسی Citrix (ویندوز، مک، لینوکس)

## سایر فایل های CFG

در اینجا انواع فایل دیگری وجود دارد که از پسوند فایل **.cfg** استفاده می کنند.

**تنظیمات**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**بازی**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**سیستم و متفرقه**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## منابع
* [برنامه های مجازی سیتریکس](https://en.wikipedia.org/wiki/Citrix_Virtual_Apps)


