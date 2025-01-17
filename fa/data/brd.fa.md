{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "فایل BRD - EAGLE Circuit Board File - فایل brd چیست و چگونه آن را باز کنیم؟",
  "description" : "با فایل برد مدار BRD EAGLE و نحوه باز کردن آن آشنا شوید.",
  "linktitle" : "BRD",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-brd-fa",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## فایل BRD چیست؟

فرمت فایل BRD در نرم افزار اتوماسیون طراحی الکترونیکی (EDA) برای طراحی برد مدار چاپی (PCB) استفاده می شود. نرم افزارهای طراحی PCB مانند Eagle، KiCad، Altium Designer و سایرین از این فرمت فایل برای ذخیره طرح، اتصالات و سایر اطلاعات مربوط به طراحی یک برد مدار چاپی استفاده می کنند.

فایل BRD نوعی فایل CAD است که فایل های دیجیتالی هستند که توسط مهندسان و طراحان برای ایجاد، اصلاح و تجزیه و تحلیل طرح ها استفاده می شود. فایل BRD مربوط به Autodesk EAGLE است که نرم افزاری است که معمولاً در صنعت الکترونیک برای طراحی بردهای مدار چاپی (PCB) استفاده می شود. Autodesk EAGLE ابزارهایی را هم برای تصویربرداری شماتیک (ایجاد نمایش بصری مدار) و هم برای چیدمان PCB (ترتیب اجزا و اتصالات مسیریابی) فراهم می کند.

فایل BRD با استفاده از EAGLE Layout Editor که جزء مجموعه نرم افزار Autodesk EAGLE است ایجاد می شود. این ویرایشگر به کاربران اجازه می دهد تا طرح بندی PCB را طراحی کنند که شامل قرار دادن قطعات، مسیریابی ردیابی، تعریف قوانین طراحی و ایجاد فایل های لازم برای ساخت می باشد.

فایل‌های BRD به‌عنوان الگو یا نقشه‌ای برای طراحی مدارهای الکترونیکی روی PCB عمل می‌کنند. طراحان از فایل های EAGLE و .brd استفاده می کنند تا نمودارهای شماتیک خود را به طرح های فیزیکی قابل ساخت ترجمه کنند.

فایل های .BRD را می توان در قالب داده های مته Gerber ذخیره کرد. فایل‌های Gerber فرمت استانداردی هستند که در تولید PCB برای توصیف الگوها، لایه‌ها و ویژگی‌های طراحی PCB استفاده می‌شوند. ذخیره فایل های .brd در این فرمت به آنها اجازه می دهد تا توسط برنامه های تولید به کمک کامپیوتر (CAM) استفاده شوند، که دستورالعمل های لازم برای ساخت PCB را تولید می کند.

## نمایشگر فایل BRD

چندین ابزار نرم‌افزاری برای مشاهده فایل‌های «.brd» وجود دارد که به کاربران امکان می‌دهد طرح‌بندی‌های PCB ایجاد شده با نرم‌افزارهایی مانند Autodesk EAGLE را تجسم و بررسی کنند.

1.  **Autodesk EAGLE**: اگر به Autodesk EAGLE دسترسی دارید، می توانید به سادگی فایل های .brd را مستقیماً در نرم افزار برای مشاهده و ویرایش باز کنید.
    
2.  **KiCad**: KiCad یک مجموعه نرم افزار منبع باز EDA است که شامل ویرایشگر طرح بندی PCB است. این قابلیت وارد کردن و مشاهده فایل های .brd ایجاد شده با Autodesk EAGLE را دارد.
    
3.  **ViewPlot**: ViewPlot یک نمایشگر مستقل Gerber است که از فرمت های مختلف فایل PCB از جمله .brd پشتیبانی می کند. این به کاربران اجازه می دهد تا طرح های PCB را بدون نیاز به نرم افزار طراحی اصلی مشاهده کنند.
    
4.  **GC-Prevue**: GC-Prevue یکی دیگر از نمایشگرهای محبوب Gerber است که می تواند فایل های .brd را نیز مدیریت کند. این ویژگی برای تجسم طرح‌بندی PCB، اندازه‌گیری فواصل و بازرسی جزئیات طراحی فراهم می‌کند.
    
5.  **Gerbv**: Gerbv یک نمایشگر Gerber منبع باز است که از مشاهده فایل های Gerber پشتیبانی می کند، که می تواند شامل فایل های .brd ذخیره شده در قالب Gerber باشد.
    
6.  **ابزارهای مشاهده آنلاین**: ابزارهای آنلاینی نیز وجود دارد که به شما امکان می دهد فایل های .brd را مستقیماً در مرورگر وب خود آپلود و مشاهده کنید. یکی از این نمونه‌ها «Online Gerber Viewer» توسط EasyEDA است که از مشاهده فرمت‌های مختلف فایل PCB از جمله Gerber و «.brd» پشتیبانی می‌کند.

## چگونه یک فایل BRD را باز کنیم؟

فایل های BRD که در طراحی PCB استفاده می شوند، می توانند در برنامه های مختلف طراحی PCB باز شوند.

- **Autodesk EAGLE**: این نرم افزار طراحی PCB چند پلتفرمی است که توسط Autodesk توسعه یافته است. از ایجاد نمودارهای شماتیک، طرح بندی PCB و مسیریابی اتصالات الکتریکی پشتیبانی می کند. کاربران می توانند فایل های .brd را مستقیماً در Autodesk EAGLE برای مشاهده و ویرایش بیشتر باز کنند.
    
- **Altium Designer**: Altium Designer نرم افزار جامع طراحی PCB است که عمدتاً برای سیستم عامل های ویندوز است. طیف گسترده ای از ویژگی ها را برای تصویربرداری شماتیک، طرح PCB و تجزیه و تحلیل طراحی ارائه می دهد. Altium Designer همچنین از باز کردن فایل های .brd پشتیبانی می کند و به کاربران امکان می دهد طرح های ایجاد شده در نرم افزارهای دیگر را وارد کرده و با آنها کار کنند.
    
- **Open Board Viewer**: Open Board Viewer یک نرم افزار مشاهده PCB است که به طور خاص برای سیستم عامل های لینوکس طراحی شده است. این یک ابزار منبع باز است که به کاربران اجازه می دهد تا طرح بندی PCB را تجسم کنند، اجزا را بررسی کنند و جزئیات مسیریابی را بررسی کنند. Open Board Viewer از باز کردن فایل‌های .brd پشتیبانی می‌کند و به کاربران در پلتفرم‌های لینوکس امکان مشاهده و تجزیه و تحلیل طرح‌های ایجاد شده در نرم‌افزارهای دیگر را می‌دهد.

در اینجا لیستی از برنامه هایی وجود دارد که می توانید برای باز کردن فایل های BRD از آنها استفاده کنید.

- **Autodesk EAGLE** (آزمایشی رایگان) برای (ویندوز، مک، لینوکس)
- **Altium Designer** (آزمایشی رایگان) برای (ویندوز، مک، لینوکس)
- **نمایشگر برد باز ** (رایگان) برای لینوکس

## منابع
* [برنامه EAGLE](https://en.wikipedia.org/wiki/EAGLE_(program))


