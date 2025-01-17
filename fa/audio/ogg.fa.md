---
date: 2019-12-13
keywords: ogg, ogg file format, .ogg extension, ogg audio format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lدر مورد فرمت فایل OGG و APIهایی که می توانند فایل OGG را ایجاد و باز کنند، کسب درآمد کنیدs.
title: Oفایل GG - Ogg Vorbis Audio File
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## فایل OGG چیست؟

OGG یک فایل صوتی فشرده Ogg Vorbis است که با پسوند .ogg ذخیره می شود. فایل‌های OGG برای ذخیره‌سازی داده‌های صوتی استفاده می‌شوند و می‌توانند شامل اطلاعات هنرمند و آهنگ و متادیتا نیز باشند. OGG یک فرمت کانتینر آزاد و باز است که توسط بنیاد Xiph.Org نگهداری می شود.

## تاریخچه مختصر فرمت فایل OGG

پروژه Ogg به عنوان بخشی از یک پروژه بزرگتر در سال 1993 شروع شد و Squish نام گرفت، اما به دلیل یک علامت تجاری موجود، به OggSquish تغییر نام داد. این به عنوان تلاشی برای ایجاد یک فرمت صوتی فشرده انعطاف پذیر برای برنامه های صوتی مدرن توصیف شد. مرجع OGG در 2 سپتامبر 2000 از Vorbis جدا شد.

OGM was created in 2002 due to the lack of formal video support in OGG. This allowed embedding video from the Microsoft DirectShow framework into an OGG-based wrapper. By 2006, OGG was supported by many video game engines and was commonly used to encode free content. The Free Software Foundation started a campaign on May 15, 2007, to increase the use of Vorbis as a superior alternative to MP3. در 30 ژوئن 2009، OGG تنها فرمت کانتینری بود که توسط اجرای HTML5 فایرفاکس 3.5 پشتیبانی می شد.

## فرمت فایل OGG

فرمت OGG از تکه های داده تشکیل شده است. هر تکه صفحه Ogg نامیده می شود. هر صفحه برای شناسایی فرمت Ogg با OggS شروع می شود. هدر شامل شماره سریال و شماره صفحه است که هر صفحه را به عنوان بخشی از یک سری مشخص می کند. صفحه از اجزای زیر تشکیل شده است.

- **سرصفحه صفحه**
  - "** الگوی ضبط (32 بیت) **: برای همگام سازی هنگام تجزیه فایل های OGG استفاده می شود."
  - "**نسخه(8 بیت)**: نشان دهنده نسخه جریان بیت Ogg است."
  - "**نوع سربرگ(8 بیت)**: نوع صفحه را نشان می دهد."

| بیت | ارزش | توضیحات |
| --- | --- | --- |
| 0 | 0x01 | نشان می دهد که اولین بسته صفحه ادامه بسته قبلی در جریان بیت منطقی است. |
| 1 | 0x02 | نشان می دهد که این صفحه اولین صفحه در بیت استریم منطقی است. |
| 2 | 0x04 | نشان می دهد که این صفحه آخرین صفحه در بیت استریم منطقی است. |

  - "**موقعیت گرانول(64 بیت)**: نشانگر زمانی است که معنای آن توسط کدک تعیین می شود."
  - "** شماره سریال بیت استریم (32 بیت)**: شماره سریالی است که صفحه متعلق به یک جریان بیت منطقی خاص را مشخص می کند."
  - "**شماره ترتیب صفحه (32 بیت)**: نشان دهنده ترتیب صفحه با شروع صفحه اول از 0 است."
  - "**Checkssum(32 بیت)**: جمع کنترلی CRC32 کل داده های صفحه را ارائه می دهد."
  - "**Page segments(8 bit)**: تعداد قسمت های صفحه را نشان می دهد."
  - "**جدول بخش**: آرایه ای از مقادیر 8 بیتی است که طول هر بخش را در بدنه صفحه نشان می دهد."
- **فراداده**: VorbisComment گسترده ترین مکانیسم پشتیبانی شده برای ذخیره ابرداده است. مکانیسم های دیگر شامل موارد زیر است:
  - "بلوک های فراداده FLAC"
  - "اسکلت اوگ"
  - "زبان نشانه گذاری رسانه پیوسته"

## منابع ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

