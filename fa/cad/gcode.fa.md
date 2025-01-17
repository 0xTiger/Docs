{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"فایل GCODE - فایل .gcode چیست و چگونه آن را باز کنیم؟",
   "description":"درباره فرمت فایل GCODE و APIهایی که می‌توانند فایل‌های GCODE را ایجاد و باز کنند، بیاموزید.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-fa",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## فایل GCODE چیست؟

یک **فایل GCODE** یک فایل متنی ساده است که حاوی دستورالعمل هایی برای کنترل ماشین ابزارهای کامپیوتری و چاپگرهای سه بعدی است. G-code یا کد هندسی زبانی است که برای کنترل حرکات و اعمال ماشین‌های **CNC (کنترل عددی کامپیوتری)** استفاده می‌شود. ماشین های CNC شامل ماشین های فرز، ماشین تراش، روتر و چاپگرهای سه بعدی است.

دستورات G-code در نحو خاصی نوشته می شوند که معمولاً از حروف و اعداد تشکیل شده است. هر فرمان به ماشین دستور می دهد تا عمل خاصی مانند حرکت ابزار به موقعیت خاص، تغییر ابزار یا تنظیم سرعت را انجام دهد.

G-code اغلب توسط نرم افزار **CAM (Computer-Aided Manufacturing)** تولید می شود. نرم افزار CAM مدل سه بعدی یا طراحی دو بعدی را می گیرد و مسیرهای ابزار و دستورالعمل های G-code مربوطه را تولید می کند. سپس فایل G-code برای اجرا در دستگاه CNC یا چاپگر سه بعدی بارگذاری می شود.

فایل‌های G-code معمولاً دارای پسوند فایل «.nc» یا «.gcode» هستند، مثلاً «program.nc» یا «print.gcode».

## ساختار فایل GCODE:

فایل های GCODE فایل های متنی ساده ای هستند که هر خط حاوی دستور خاصی است. این دستورات از کنترل حرکت ماشین گرفته تا تنظیم دما، سرعت و سایر پارامترهای حیاتی برای ساخت یک شی را شامل می شود.

نحو GCODE شامل ترکیبی از حروف و اعداد است. هر یک عملکرد یا پارامتر متمایز را نشان می دهد. دستورات متداول عبارتند از G0 و G1 برای حرکت، M3 و M5 برای کنترل اسپیندل و S و F برای تنظیم سرعت و نرخ تغذیه به ترتیب.

## نسل GCODE:

نرم افزارهای برش مانند **Simplify3D** و **Slic3r**، نقشه های طراحی به کمک کامپیوتر (CAD) را به GCODE ترجمه می کند. نرم افزار CAD برای ایجاد مدل های سه بعدی استفاده می شود که سپس در قالب هایی مانند STL صادر می شوند. نرم افزار برش این مدل ها را می گیرد و فایل GCODE را تولید می کند که جزئیاتی مانند ارتفاع لایه، سرعت چاپ و تنظیمات دما را مشخص می کند.

## مثال GCODE

در اینجا مثال ساده ای از G-code برای جابجایی دستگاه CNC آورده شده است:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## چگونه یک فایل GCODE را باز کنیم؟

برای باز کردن فایل G-code بسته به نیاز خود می توانید از انواع نرم افزارها استفاده کنید.

اگر کد G را برای چاپگر سه بعدی تولید کرده اید. می‌توانید آن را با استفاده از نرم‌افزاری که همراه با چاپگر سه بعدی یا نرم‌افزار برش اختصاصی ارائه شده است، باز کنید. نمونه هایی شامل **PrusaSlicer**، **Cura**، **Simplify3D**، **MatterControl** یا **Repetier-Host**؛ این برنامه ها اغلب دارای رابط کاربر پسند هستند که به شما امکان بارگذاری و تجسم کد G را می دهد.

فایل های GCODE متن ساده هستند، بنابراین می توانید آنها را با هر ویرایشگر متنی باز کنید. ویرایشگرهای متن رایج شامل **Notepad (در ویندوز)**، **TextEdit (در macOS)**، یا **Gedit (در لینوکس)**؛ به سادگی روی فایل G-code **راست کلیک کنید**، **Open with** را انتخاب کنید و یک ویرایشگر متن را انتخاب کنید.

