{
  "date": "2021-07-18",
  "keywords": [
"LOC",
"فایل",
"افزونه",
"فرمت فایل",
"موقعیت مکانی GPS",
"نقطه راه"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOC - فرمت فایل مکان GPS",
  "description": "درباره قالب فایل LOC و APIهایی که می‌توانند فایل‌های LOC را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "LOC",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-lo-fac"
}
},
  "lastmod": "2021-07-18"
}

## فایل LOC چیست؟

یک فایل با پسوند loc. یک فایل موقعیت مکانی GPS است که شامل مکان های مکانی به عنوان ایستگاه های بین راه است. نقطه بین یک جفت مقدار طول و عرض جغرافیایی است که به مکانی اشاره دارد که توسط برنامه های سیستم اطلاعات جغرافیایی (GIS) استفاده می شود. برنامه های نقشه برداری GPS، مانند DeLorme Topo، از فایل های LOC برای خواندن و نمایش اطلاعات موجود در این فایل های LOC به عنوان لایه های قابل انتخاب توسط کاربران نهایی استفاده می کنند. علاوه بر این، از اینها برای تبادل داده های GPS بین برنامه ها استفاده می شود. فایل‌های LOC را می‌توان با استفاده از برنامه‌هایی مانند [TopoGrafix EasyGPS](https://www.easygps.com/) باز کرد که محتویات این فایل‌ها را مانند لایه‌ها و داده‌های ترسیم شده روی نقشه در موقعیت جغرافیایی مربوطه نشان می‌دهد.

## فرمت فایل LOC - اطلاعات بیشتر

فایل‌های LOC شباهت‌هایی با فایل‌های [GPX](/gis/gpx/) دارند اما در قالب‌های مختلف ذخیره می‌شوند. این فایل‌ها به‌عنوان فایل‌های [XML](/web/xml/) ذخیره می‌شوند، جایی که محتوای نقاط راه و اطلاعات مرتبط در برچسب‌های ساختاریافته موجود است. از آنجایی که XML یک زبان تعمیم یافته برای تبادل داده بین برنامه های مختلف است، این امر تبادل داده های LOC با سایر برنامه ها را تسهیل می کند.

## فرمت فایل LOC - مثال

در زیر سرصفحه و متن یک نقطه راه از یک فایل LOC آمده است. همانطور که مشاهده می شود، اطلاعات هدر حاوی منبع مکان برای داده ها است. ایستگاه بین راه حاوی اطلاعاتی مانند «ID» و داده‌های محتوای مرتبط با ایستگاه بین راه است. در نهایت، ایستگاه بین راه مجموعه ای از مقادیر طول و عرض جغرافیایی و متن مرتبط با این نقطه راه خاص است.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## منابع

* [TopGraphic EasyGPS](https://www.easygps.com/)

