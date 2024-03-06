---
date: 2019-10-11
keywords: WEBM, What is a WEBM file, WEBM File Format
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lدر مورد فرمت فایل WEBM و APIهایی که می توانند فایل WEBM را ایجاد و باز کنند، کسب درآمد کنیدs.
title: WEBM - فرم فایل ویدئویی WebMat
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## فایل WEBM چیست؟

فایلی با پسوند .webm یک فایل ویدیویی است که بر اساس فرمت فایل WebM باز و بدون حق امتیاز است. برای به اشتراک گذاری ویدئو در وب طراحی شده است و ساختار محفظه فایل را شامل فرمت های ویدئویی و صوتی تعریف می کند. WebM 100% رایگان است و با کیفیت بالا بر اساس فناوری‌های باز مانند HTML، HTTP و TCP/IP که برای پیاده‌سازی برای هر کسی باز است، پیاده‌سازی می‌کند. WebM به طور خاص برای ارائه ویدیو در وب طراحی شده است که آن را برای پخش جریانی با ردپای محاسباتی کم بهینه می کند. این باعث می شود که برای پخش فیلم ها در هر دستگاهی به خصوص نت بوک ها، گوشی های دستی و تبلت های کم مصرف مناسب باشد.

## فرمت فایل WEBM

ساختار فایل WebM بر اساس زیرمجموعه ای از قالب فایل کانتینری Matroska [MKV](/video/mkv/) است. جریان های ویدیویی موجود در یک فایل WebM با استفاده از فناوری های فشرده سازی VP8 یا VP9 فشرده می شوند که در فشرده سازی بسیار کارآمد هستند. به طور مشابه، جریان های صوتی در یک فایل WebM با استفاده از کدک های Vorbis یا Opus که توسط [Xiph Foundation](https://www.xiph.org/) توسعه داده شده اند، فشرده می شوند. همه این ویدیوها و کدک های صوتی بدون حق امتیاز هستند و می توان بدون هیچ هزینه ای از آنها استفاده کرد.

در زیر مشخصات خلاصه شده برای فرمت فایل WebM آمده است.

| فیلد|توضیحات|
---|---|
|نوع MIME |ویدئو/وبم|
|نوع MIME فقط صوتی |audio/webm|
|شناسه نوع یکنواخت| org.webmproject.webm|
|نام کدک ویدیو| VP8 یا VP9|
|نام کدک صوتی| Vorbis یا Opus|

### عناصر WebM

WebM, being a subset of the Matroska specifications, provides support for some of the Matroska functionality. Following is a description of the supported elements.

#### EBML

| نام | توضیحات|
---|---|
|EBML|ویژگی های EBML داده ها را برای دنبال کردن تنظیم کنید. هر سند EBML باید با این شروع شود.|
|EBMLVersion |نسخه تجزیه کننده EBML مورد استفاده برای ایجاد فایل.|
|EBMLReadVersion|حداقل نسخه EBML که تجزیه کننده باید برای خواندن این فایل پشتیبانی کند.|
|EBMLMaxIDLength |حداکثر طول شناسه هایی که در این فایل خواهید یافت (4 یا کمتر در Matroska).|
|EBMLMaxSizeLength|حداکثر طول اندازه هایی که در این فایل خواهید یافت (8 یا کمتر در Matroska). این اندازه عنصر نشان داده شده در ابتدای یک عنصر را لغو نمی کند. عناصری که دارای اندازه مشخص شده بزرگتر از حد مجاز EBMLMaxSizeLength هستند نامعتبر در نظر گرفته می شوند.
|DocType|رشته ای که نوع سندی را که از این هدر EBML پیروی می کند (در مورد ما webm) توضیح می دهد.|
|DocTypeVersion|نسخه مفسر DocType مورد استفاده برای ایجاد فایل.|
|DocTypeReadVersion|حداقل نسخه DocType که مترجم برای خواندن این فایل باید پشتیبانی کند.|

#### عناصر جهانی

در حال حاضر، فقط عنصر «Void» پشتیبانی می‌شود که برای باطل کردن داده‌های آسیب‌دیده استفاده می‌شود تا از رفتارهای غیرمنتظره هنگام استفاده از داده‌های آسیب‌دیده جلوگیری شود. محتوا کنار گذاشته شده است. همچنین برای رزرو فضا در یک عنصر فرعی برای استفاده بعدی استفاده می شود.

#### بخش
این عنصر شامل سایر عناصر سطح بالا (سطح 1) است. به طور معمول یک فایل Matroska از 1 بخش تشکیل شده است.

#### اطلاعات متا جستجو

جستجوی اطلاعات زیر پشتیبانی می شود.

|نام عنصر |توضیحات|
---|---|
|SeekHead |حاوی موقعیت عنصر سطح 1 دیگر.|
|Seek |شامل یک ورودی جستجو به یک عنصر EBML است.|
|SeekID |شناسه باینری مربوط به نام عنصر.|
|SeekPosition |موقعیت عنصر در بخش به اکتت (0 = عنصر سطح اول 1).|

## منابع

* [WebM](https://www.webmproject.org/)

* [مخازن کد WebM](https://www.webmproject.org/code/#webp-repositories)

