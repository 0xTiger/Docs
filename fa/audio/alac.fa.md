---
date: 2021-03-21
keywords: alac, alac file format, .alac extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lدر مورد فرمت فایل ALAC و APIهایی که می توانند فایل ALAC را ایجاد و باز کنند، کسب درآمد کنیدs.
title: ALAC - فرم فایل کدک صوتی Apple Losslessat
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## فایل ALAC چیست؟

فرمت فایل ALAC، کدک صوتی بدون ضرر اپل (ALAC) است که از ظرف QuickTime سازگار با MPEG-4 استفاده می کند. در سال 2004 به عنوان فرمت فایل اختصاصی معرفی شد تا اینکه در سال 2011 اپل آن را منبع باز و بدون حق امتیاز در دسترس قرار داد. قالب مشابه [FLAC](/audio/flac/) (کدک صوتی بدون اتلاف رایگان) است اما فشرده سازی بیشتری را در مقایسه با آن ارائه می دهد. این جایگزین صدای بهتری برای [AAC](/audio/aac/) یا [MP3](/audio/mp3/) ارائه می دهد. فایل های صوتی کدگذاری شده با کدک ALAC را می توان با استفاده از Apple QuickTime، Apple iTunes و Micrsoft Windows Media Player با کدک K-Lite باز کرد.

## فرمت فایل ALAC

فایل‌های مبتنی بر کدک ALAC، فایل‌های باینری هستند که به عنوان [open source on GitHub](https://github.com/macosforge/alac) برای مرجع توسعه‌دهنده در دسترس هستند. این شامل منابع برای رمزگذار و رمزگشا ALAC است. اپل همچنین یک ابزار خط فرمان به نام alacconvert را برای خواندن و نوشتن داده‌های صوتی در/از فایل‌های Core Audio Format (CAF) و [WAVE](/audio/wav/) ارائه کرده است. در ادامه نکات کلیدی در مورد فرمت فایل ALAC آورده شده است.

 1. عمق بیت - 16، 20، 24 و 32 بیت.
 1. «نرخ نمونه» - هر نرخ نمونه صحیح دلخواه از 1 تا 384000 هرتز. نرخ های نظری تا 4294967295 (2^32 - 1) هرتز می تواند پشتیبانی شود.
 1. اندازه بسته - اندازه بسته پیش فرض 4096 فریم نمونه صدا در هر بسته است. اندازه های دیگر بسته مطمئناً امکان پذیر است. با این حال، اندازه بسته‌های غیر پیش‌فرض تضمین نمی‌شود که به درستی در همه دستگاه‌های سخت‌افزاری که Apple Lossless را پشتیبانی می‌کنند، کار کنند. بسته های بالای 16384 فریم نمونه پشتیبانی نمی شوند.
 1. کانال های پشتیبانی شده - از یک تا هشت کانال پشتیبانی می کند. هر کانال دارای ترتیب اطلاعات زیر است.

|نوم چان| سفارش|
|---|---|
|1 |مونو|
|2 |استریو (چپ، راست)|
|3 |MPEG 3.0 B (مرکز، چپ، راست)|
|4 |MPEG 4.0 B (مرکز، چپ، راست، مرکز فراگیر)|
|5 |MPEG 5.0 D (مرکز، چپ، راست، ساراوند چپ، فراگیر راست)|
|6 |MPEG 5.1 D (مرکز، چپ، راست، چپ فراگیر، راست فراگیر، افکت های فرکانس پایین)|
|7 |Apple AAC 6.1 (Center, Left, Right, Left Surround, Right Surround, Center Surround, Low Frequency Effects)|
|8 |MPEG 7.1 B (مرکز، مرکز چپ، مرکز راست، چپ، راست، چپ فراگیر، راست فراگیر، جلوه های فرکانس پایین)|

## منابع

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)

* [کدک صوتی بدون ضرر اپل](https://macosforge.github.io/alac/)

* [macosforge - alac در GitHub](https://github.com/macosforge/alac)


