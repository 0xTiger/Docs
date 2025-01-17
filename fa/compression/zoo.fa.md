{
   "date":"2023-11-09",
   "keywords":[
"باغ وحش",
"فایل باغ وحش",
"فایل فشرده باغ وحش",
"نحوه باز کردن فایل باغ وحش",
"فایل",
"پسوند فایل zoo",
"افزونه",
"فایل"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"فایل ZOO - فایل zoo چیست و چگونه آن را باز کنیم؟",
   "description":"درباره فرمت فایل فشرده ZOO و API هایی که می توانند فایل های ZOO را ایجاد و باز کنند، بیاموزید.",
   "linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo-fa",
         "parent":"compression"
}
},
   "lastmod":"2023-11-09"
}

## فایل ZOO چیست؟

فایل .zoo یک فرمت آرشیو است که برای فشرده سازی و ذخیره فایل ها و دایرکتوری ها استفاده می شود. شبیه سایر قالب‌های آرشیو مانند «.zip»، «.tar» و «.rar» است. قالب .zoo در روزهای اولیه محاسبات رایج بود اما در سال های اخیر کمتر رایج شده است. در ابتدا توسط **Rahul Dhesi** توسعه داده شد و عمدتاً در سیستم‌های Unix و DOS استفاده می‌شد.

یک فایل `.zoo` معمولاً شامل یک یا چند فایل و فهرست است که فشرده شده و در یک فایل بایگانی شده اند. با استفاده از ابزارهای نرم افزاری مختلف که از این فرمت پشتیبانی می کنند، می توانید فایل های `.zoo` را ایجاد و استخراج کنید.

بایگانی های باغ وحش دارای یک ویژگی منحصر به فرد هستند که به آن ها اجازه می دهد چندین نسخه از یک فایل را ذخیره کنند، مشروط بر اینکه هر نسخه در تاریخ های مختلف اصلاح شده باشد. این به این معنی است که کاربران باغ وحش می توانند فایل های قبلی را مستقیماً از بایگانی باغ وحش ذخیره کرده و به آن دسترسی داشته باشند. این ویژگی به کاربران امکان می‌دهد به نسخه قبلی فایل برگردند یا نسخه قدیمی‌تر را با نسخه جدیدتر مقایسه کنند که روشی مناسب برای مدیریت ویرایش‌ها و تغییرات فایل در طول زمان ارائه می‌دهد.

## عملیات متداول فایل های باغ وحش

در اینجا چند عملیات متداول مرتبط با فایل های «.zoo» آمده است:

1.  **ایجاد فایل `.zoo`:** می توانید از ابزار خط فرمان مانند zoo برای ایجاد فایل .zoo استفاده کنید. به عنوان مثال، دستور زیر بایگانی .zoo را از دایرکتوری ایجاد می کند:
    
zoo a -c archive.zoo directory/.
    
در این دستور، a مخفف add، -c فشرده سازی را مشخص می کند و archive.zoo نام آرشیو خروجی است.
    
2.  ** استخراج فایل ها از فایل .zoo:** برای استخراج محتویات بایگانی .zoo، می توانید از دستور زیر استفاده کنید:
    
zoo e archive.zoo.
    
این دستور فایل‌ها را از فایل «archive.zoo» استخراج می‌کند.
    
3.  **لیست کردن محتویات یک فایل .zoo:** می توانید محتویات بایگانی .zoo را بدون استخراج با استفاده از گزینه l فهرست کنید:
    
    
`zoo l archive.zoo`

## چگونه یک فایل باغ وحش را باز کنیم؟

برنامه هایی که فایل های ZOO را باز می کنند شامل

- **zoo** (رایگان) برای (ویندوز، لینوکس)

## منابع
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
