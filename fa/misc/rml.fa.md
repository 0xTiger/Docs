{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "RML - فایل قالب گزارش اکسیر",
  "description":"درباره فایل‌های RML و APIهایی که می‌توانند فایل‌های RML را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml-fa",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## فایل RML چیست؟

یک فایل RML یک فایل الگوی گزارش با موتور گزارش دهی [Elixir Repertoire](https://elixirtech.com/repertoire-2/) است. فایل قالب برای تولید گزارش با منبع داده متصل به Elixir FileSystem استفاده می شود. داده‌ها در فایل الگوی RML خوانده می‌شوند و پر می‌شوند و می‌توانند به تعدادی از قالب‌های فایل مختلف مانند [PDF](/pdf/)، [RTF](/word-processing/rtf/) و صفحه گسترده [XLS](/spreadsheet/xls/) صادر شوند. موتور گزارش‌دهی Elixir Repertoire را می‌توان به طیف گسترده‌ای از منابع داده JDBC متصل کرد.

## فرمت فایل RML

جزئیات ساختار فایل داخلی فرمت فایل RML به صورت عمومی در دسترس نیست. فایل‌ها توسط اپلیکیشن Elixir Repertoire به صورت داخلی تولید و ذخیره می‌شوند تا گزارش‌هایی با داده‌های پر شده از منابع داده متصل تولید کنند. فایل الگوی RML حاوی اطلاعات چیدمان کلی و مکان‌نماهای گزارش نهایی است که از داده‌ها تولید می‌شود.

## چگونه فایل قالب RML ایجاد کنیم؟

برای تولید قالب RML در اکسیر رپرتوار می توان مراحل زیر را دنبال کرد.

1. یک منبع داده JDBC را به سیستم فایل متصل کنید.
1. برنامه Report Template Wizard را اجرا کنید
1. از نرم افزار برای مکان یابی فایل .ds منبع داده استفاده کنید
1. گزارش جدولی را به عنوان انتخاب صادرات انتخاب کنید
1. فیلدهایی را که باید در قالب گزارش گنجانده شوند انتخاب کنید
1. در نهایت با کلیک بر روی دکمه Finish، First report.rml به مخزن اضافه شده و برای نمایش تب Layout باز می شود.

## منابع

* [Elixir Repertoire](https://elixirtech.com/repertoire-2/)

