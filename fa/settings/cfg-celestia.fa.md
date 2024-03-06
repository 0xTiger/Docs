{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"فایل cfg",
"فایل پیکربندی cfg celestia",
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
  "title": "فرمت فایل CFG - فایل پیکربندی Celestia",
  "description": "درباره فرمت فایل پیکربندی CFG Celestia و APIهایی که می‌توانند فایل‌های CFG را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia-fa",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## فایل CFG چیست؟

یک فایل پیکربندی Celestia یک فایل متنی ساده است که توسط Celestia، برنامه شبیه سازی جهان سه بعدی استفاده می شود. این فایل‌ها برای سفارشی کردن نحوه رفتار Celestia، نمایش چه اجرام آسمانی و نحوه نمایش برنامه‌ها حیاتی هستند. با این حال، ویرایش این فایل‌ها نیازمند توجه دقیق است، زیرا تغییرات نامناسب می‌تواند روند بارگیری Celestia را مختل کند و از اجرای صحیح آن جلوگیری کند.

## سلستیا

Celestia یک نرم افزار رایگان و منبع باز شبیه سازی نجوم سه بعدی است که به کاربران اجازه می دهد جهان را به شیوه ای بسیار واقعی و تعاملی کاوش و تجسم کنند. این توسط کریس لورل توسعه داده شد و اولین بار در اوایل دهه 2000 منتشر شد. Celestia برای سیستم عامل های Windows، macOS و Linux در دسترس است.

ویژگی ها و جنبه های کلیدی Celestia عبارتند از:

- ** تجسم سه بعدی واقع گرایانه: ** Celestia نمایش دقیق و دقیقی از منظومه شمسی ما و همچنین ستارگان، کهکشان ها و سایر اجرام آسمانی ارائه می دهد. از مدل‌ها و بافت‌های سه بعدی با کیفیت بالا برای ایجاد تجربه‌ای فراگیر بصری استفاده می‌کند.

- **پایگاه داده گسترده آسمانی:** این نرم افزار دارای پایگاه داده داخلی گسترده ای از اجرام آسمانی شناخته شده، از جمله ستارگان، سیارات، قمرها، سیارک ها، دنباله دارها و فضاپیماها است. کاربران به راحتی می توانند این اشیاء را پیدا کرده و کاوش کنند.

- **دقت علمی:** در حالی که Celestia ابزار تجسم است، هدف آن نمایش اجرام و پدیده های آسمانی تا حد امکان دقیق بر اساس داده های علمی موجود است.

## فرمت های فایل استفاده شده توسط Celestia

Celestia از فرمت های مختلف فایل برای جنبه های مختلف شبیه سازی نجوم سه بعدی خود استفاده می کند. در اینجا برخی از فرمت های فایل کلیدی استفاده شده توسط Celestia آمده است:

1. **فایل های پیکربندی (cel.)**
- *توضیح*: فایل های متنی ساده که به کاربران اجازه می دهد رفتار، ظاهر و محتوای Celestia را سفارشی کنند.
- *هدف*: سفارشی کردن تنظیمات، تعیین مکان ها، و مشخص کردن اجرام آسمانی.

2. **مدل های سه بعدی و مش**
- *قالب‌ها*: [.3ds](/3d/3ds/)، [.obj](/3d/obj/)، [.dae](/3d/dae/)، .ac
- *توضیح*: فرمت های فایل مدل سه بعدی پشتیبانی شده برای رندر اجرام آسمانی و فضاپیماها.
- *هدف*: نمایش اشیاء سه بعدی در Celestia.

3. **فایل های بافت**
- *قالب*ها: [.jpg](/image/jpeg/)، [.png](/image/png/)، [.dds](/image/dds/)
- *توضیح*: این فایل ها بافت های سطحی اجرام آسمانی را ارائه می دهند.
- *هدف*: نگاشت بافت ها بر روی مدل های سه بعدی برای ظاهر واقعی.

4. **کاتالوگ ستاره و فایل های داده**
- *قالب‌ها*: قالب‌های سفارشی، [.csv](/spreadsheet/csv/)، [.tsv](/spreadsheet/tsv/)
- *توضیح*: فایل های داده ای که برای نشان دادن ستارگان و سایر اجرام آسمانی استفاده می شوند و شبیه سازی دقیق را تضمین می کنند.
- *هدف*: نمایش دقیق اجرام سماوی.

5. **نقشه های مکعب بافت**
- *توضیح*: نقشه های مکعب برای شبیه سازی ظاهر اجرام آسمانی دور مانند کهکشان ها استفاده می شود.
- *هدف*: رندر کردن اشیاء دور با بافت های واقعی.

6. **فایل های اسکریپت**
- *توضیح*: این فایل ها حاوی اسکریپت های سفارشی هستند که به زبان برنامه نویسی Celestia نوشته شده اند.
- *هدف*: کاربران را قادر می سازد تا رویدادها و انیمیشن های پویا را در جهان Celestia ایجاد کنند.

## فایل پیکربندی Celestia

در اینجا یک نمای کلی از آنچه می توانید با فایل پیکربندی Celestia انجام دهید آورده شده است:

1. **تنظیم موقعیت مکانی**: می توانید موقعیت مکانی خود را روی زمین با استفاده از پارامترهای طول و عرض جغرافیایی و ارتفاع مشخص کنید. این به Celestia اجازه می دهد تا آسمان شب را به طور دقیق از موقعیت شما نمایش دهد.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **سفارشی کردن گزینه های مشاهده:** می توانید گزینه های مختلف مشاهده مانند میدان دید، تنظیمات زمان و تنظیمات برگزیده رندر را تنظیم کنید.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. ** بارگیری اجرام آسمانی:** می توانید اجرام آسمانی مانند ستاره ها، سیارات، سیارک ها، فضاپیماها و موارد دیگر را به شبیه سازی خود اضافه کنید. هر شی در فایل پیکربندی با ویژگی های آن تعریف می شود.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **تعریف سفینه‌های فضایی:** می‌توانید فضاپیمای خیالی خود را ایجاد کنید یا با تعیین پارامترهای آنها مانند موقعیت، جهت‌گیری و مدل‌های سه‌بعدی از فضاپیماهای واقعی استفاده کنید.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **ایجاد اسکریپت:** می توانید اسکریپت هایی را به زبان برنامه نویسی سفارشی Celestia بنویسید تا رویدادها و انیمیشن های پویا ایجاد کنید.

## چگونه فایل CFG را باز کنیم؟

برنامه هایی که فایل های CFG را باز می کنند یا به آنها ارجاع می دهند

- Celestia (رایگان) برای (ویندوز، مک، لینوکس)

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
* [سلستیا](https://en.wikipedia.org/wiki/Celestia)

