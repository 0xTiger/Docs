{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AVL - ArcView Legend File",
  "description":"درباره فرمت فایل AVL و API هایی که می توانند فایل های AVL ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl-fa",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## فایل AVL چیست؟

یک فایل AVL یک فایل افسانه ای است که حاوی کلیدی برای نقشه تولید شده با نرم افزار ESRI ArcView GIS (سیستم اطلاعات جغرافیایی) است. این شامل اطلاعات نمادشناسی مرجع مورد استفاده در نقشه مربوطه برای دسترسی است. یک فایل AVL می‌تواند حاوی اطلاعات بیشتری مانند نمادشناسی، تنظیمات نمایش، مانند شفافیت، ویژگی‌های نمایش وابسته به مقیاس، اطلاعات جدول مرتبط/جدول مرتبط، جستجوی تعریف، ویژگی‌های برچسب‌گذاری برای لایه‌های ویژگی، و ویژگی‌های نمایش حاشیه‌نویسی برای لایه‌های حاشیه‌نویسی بسته به نوع باشد. نوعی لایه

ممکن است یک فایل AVL از فایل پروژه ArcView [.APR](/gis/apr/) ارجاع داده شود.

## فرمت فایل AVL - اطلاعات بیشتر

فایل های AVL در قالب فایل متنی ساده ذخیره می شوند. این بدان معناست که می توانید فایل های AVL را در هر ویرایشگر متنی مانند Notepad، Notepad++ و Apple TextEdit باز کنید. پس از باز شدن، نه تنها می توانید محتوای فایل را مشاهده کنید، بلکه می توانید آنها را نیز تغییر دهید.

### تفاوت بین فایل های .LYR و .AVL

 * **تفاوت فرمت فایل** - .lyr یک فایل باینری است در حالی که .avl یک فایل متنی است
 * **تفاوت محتوا** - یک فایل .lyr حاوی اطلاعات بیشتری نسبت به فایل avl است. یک فایل AVL فقط اطلاعات نمادشناسی را ذخیره می کند، در حالی که یک فایل LYR تمام اطلاعات موجود در کادر محاوره ای ویژگی های لایه در ArcMap را ذخیره می کند.

## منابع

* [تفاوت بین فایل‌های .lyr و .avl](https://support.esri.com/en/technical-article/000005936)

