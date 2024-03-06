{
  "date": "2021-06-30",
  "keywords": [
"فایل mst",
"فرمت فایل mst",
"فایل mst چیست",
"فایل",
"مثال mst",
"پسوند فایل mst",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل MST و APIهایی که می‌توانند فایل‌های MST را ایجاد و باز کنند، بیاموزید.",
  "title": "MST - فایل بسته Windows Installer",
  "linktitle": "MST",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-fat"
}
},
  "lastmod": "2021-06-30"
}

## فایل MST چیست؟
فایل‌های با پسوند mst. برای تبدیل محتوای یک بسته MSI استفاده می‌شوند. آنها معمولاً توسط مدیران سیستم برای اعمال تنظیمات سفارشی بر روی یک فایل MSI موجود استفاده می شوند. فایل‌های MST همراه با بسته اصلی MSI در سیستم‌های توزیع نرم‌افزاری خود مانند سیاست‌های گروهی استفاده می‌شوند. فایل‌های MST معمولاً در توسعه و آزمایش نرم‌افزار برای پیکربندی نسخه‌های در حال توسعه نرم‌افزار استفاده می‌شوند.

## فرمت فایل MST
یک فایل MST یا Transform برای جمع آوری گزینه های نصب برنامه هایی که از Microsoft Windows Installer در یک فایل استفاده می کنند استفاده می شود. این فایل‌ها معمولاً در خط فرمان Installer (MSIEXEC.EXE) یا در خط‌مشی گروهی نصب نرم‌افزار استفاده می‌شوند. در دامنه اکتیو دایرکتوری مایکروسافت. فایل های MST را می توان با نصب کننده های اجرایی پیچیده نیز استفاده کرد. یک مورد کلی این است که شخصی می خواهد پارامترهای خط فرمان را به نصب کننده پیچیده شده ارسال کند. برای انجام این کار به یک فایل MST نیاز دارید که ویژگی WRAPPED_ARGUMENTS را به جدول ویژگی اضافه کند. این فایل ها را نمی توان با استفاده از ویرایشگرهای عمومی ایجاد یا ویرایش کرد. ابزارهای خاصی برای این منظور موجود است.

### چگونه از فایل های MST استفاده کنیم؟
فایل های MST را می توان با استفاده از ابزارهای مختلف تولید کرد و Ocra به طور کلی برای تولید فایل های MST استفاده می شود. سپس تنظیمات را می توان با توجه به نیاز سفارشی کرد و آنها را در یک مکان خاص ذخیره کرد. پس از آن فایل‌های MST را می‌توان همراه با فایل‌های MSI استفاده کرد. اگر می خواهید این فایل ها را تست کنید؛ از دستور زیر در خط فرمان استفاده کنید

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### ویژگی TRANSFORMS

همچنین می توانید از ویژگی **TRANSFORMS** نصب کننده ویندوز استفاده کنید که در واقع لیستی از تبدیل هایی است که نصب کننده هنگام نصب بسته اعمال می کند. نصب کننده تبدیل ها را به همان ترتیبی که در ویژگی TRANSFORM فهرست شده اند اجرا می کند. تبدیل ها را می توان با نام فایل با پسوند mst. یا مسیر کامل مشخص کرد. برای تعیین بیش از یک تبدیل، نام هر فایل یا یک نقطه ویرگول مانند مثال زیر را جدا کنید.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## منابع 

* [فایل‌های تبدیل MST](https://www.exemsi.com/documentation/mst-transformation-files/)

* [ویژگی TRANSFORMS](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)


