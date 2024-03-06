{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "فایل CPIO - فرمت فایل آرشیو یونیکس CPIO",
  "description":"یاد بگیرید که یک فایل CPIO و API هایی که می توانند فایل های CPIO را ایجاد و باز کنند چیست.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio-fa",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## فایل CPIO چیست؟

یک فایل CPIO یک فایل بایگانی است که در قالب یونیکس Copy In Copy Out (CPIO) ایجاد شده است. این فرمت مشابه فرمت فایل TAR است غیر از اینکه فشرده نشده است. فایل‌های CPIO می‌توانند فایل‌های دستگاه، پیوندهای نمادین و ویژگی‌های فایل گسترده را ذخیره کنند.

## فرمت فایل CPIO

یک بایگانی CPIO به عنوان یک فایل باینری ایجاد می شود که توسط انسان قابل خواندن نیست. مجموعه ای از فایل ها و دایرکتوری ها را ذخیره می کند. محتویات بایگانی CPIO با اطلاعات فراداده مانند نام فایل ها، مجوزها، مالکیت و مُهرهای زمانی شناسایی می شود. این اطلاعات فراداده نیز برای دسترسی جانبی سیستم در فایل آرشیو ذخیره می شود.

## فرمت آرشیو CPIO

یک فایل CPIO از یک یا چند فایل عضو به هم پیوسته تشکیل شده است. هر فایل در بایگانی شامل یک هدر است که به صورت اختیاری با محتویات فایل همانطور که در هدر ذکر شده است دنبال می شود. بایگانی حاوی هدر دیگری در پایان است که با یک فایل خالی به نام TRAILER توضیح داده شده است.

### انواع آرشیو CPIO

دو نوع آرشیو CPIO وجود دارد. اینها فقط در سبک هدر متفاوت هستند.

* بایگانی های ASCII - این بایگانی های CPIO دارای یک هدر قابل چاپ هستند که اگر آرشیو خود از فایل های ASCII تشکیل شده باشد بخشی از بایگانی CPIO می شود.

* بایگانی های باینری - این بایگانی های CPIO دارای هدرهای باینری هستند.


## کار با CPIO Archive

### چگونه آرشیو CPIO ایجاد کنیم؟

با استفاده از دستور **cpio** می توانید یک CPIO در سیستم های مشابه یونیکس ایجاد کنید. دستور زیر تمام فایل ها و دایرکتوری های یک دایرکتوری فعلی و زیر شاخه های آن را پیدا می کند. سپس این خروجی به دستور cpio منتقل می شود که یک بایگانی جدید CPIO به نام archive.cpio ایجاد می کند.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### چگونه فایل ها را از آرشیو CPIO استخراج کنیم؟

دستور زیر فایل ها را از یک آرشیو موجود استخراج می کند.

```
cpio -id < archive_cpio.cpio
```
فایل archive.cpio را از ورودی استاندارد می خواند و فایل ها را به دایرکتوری فعلی استخراج می کند.


## منابع

* [CPIO - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/Cpio)

* [CPIO File Format](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)
