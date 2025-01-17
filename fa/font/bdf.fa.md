{
  "date": "2021-02-25",
  "keywords": [
"فایل bdf",
"فرمت فایل bdf",
"فایل bdf چیست",
"فایل",
"نمونه bdf",
"پسوند فایل bdf",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "BDF - فرمت توزیع بیت مپ Glyph",
  "description": "درباره فرمت فایل BDF و APIهایی که می‌توانند فایل‌های BDF را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "BDF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-bd-faf"
}
},
  "lastmod": "2021-02-25"
}

## فایل BDF چیست؟
فایل‌های BDF به صورت قابل خواندن توسط انسان هستند و معمولاً در یک رمزگذاری ASCII توزیع می‌شوند. فایل با اطلاعات کلی مربوط به فونت کامل شروع می‌شود و سپس اطلاعات و بیت مپ‌های حروف‌نویسی افراد قرار می‌گیرد. داده های موجود در آن برای فونت برای یک جهت یک اندازه نشان می دهد. معیارهایی که در بیش از یک جهت استفاده می شود ممکن است در یک فایل واحد باشد. در فایل BDF، هر مورد در یک خط متن جداگانه در فایل قرار دارد. از فاصله ها برای جداسازی آیتم ها در یک خط استفاده می شود.

## فرمت فایل BDF
شورت های BDF برای فرمت توزیع بیت مپ Glyph. متعلق به Adobe یک فرمت فایل برای ذخیره فونت های نوع بیت مپ است. محتوا به شکل یک فایل متنی است که برای رایانه و همچنین قابل خواندن توسط انسان طراحی شده است. BDF به ویژه در محیط های پنجره یونیکس X استفاده می شود. به طور گسترده ای با فرمت فونت PCF که قرار است کارآمدتر باشد و فونت های OpenType و TrueType جایگزین شده است.
### ساختار فایل BDF
یک فایل فونت BDF از سه بخش تشکیل شده است:

- یک بخش سراسری که برای تمام حروف های یک فونت اعمال می شود.
- یک بخش با یک ورودی جداگانه برای هر علامت.
- بیانیه ENDFONT.

## مثال
در اینجا یک فونت مثال حاوی یک علامت، برای ASCII بزرگ است. اعلامیه های جهانی آن با خط STARTFONT شروع می شود و با خط CHARS پایان می یابد
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## منابع
 * [قالب توزیع بیت مپ Glyph](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
 * [مشخصات فرمت توزیع بیت مپ Glyph (BDF)](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

