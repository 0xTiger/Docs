---
date: 2019-10-11
keywords: vob, .vob, vob file format, .vob file format, .vob extension, vob extension, vob video format, vob dvd files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lدر مورد فرمت فایل VOB و APIهایی که می توانند فایل VOB را ایجاد و باز کنند، کسب درآمد کنیدs.
title: Vفرم فایل OBat
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## فایل VOB چیست؟ ##

فایل‌های VOB معمولاً در فهرست VIDEO_TS روی یک DVD با پسوند vob. ذخیره می‌شوند. فایل‌های VOB حاوی داده‌های ویدیویی و صوتی و همچنین داده‌های دیگری مانند منوها و زیرنویس‌ها هستند. VOB بر اساس فرمت جریان برنامه MPEG-2 است، اما محدودیت ها و مشخصات اضافی در استریم های خصوصی دارد. فایل‌های VOB زیرمجموعه‌ای دقیق از جریان‌های برنامه MPEG هستند، بنابراین همه فایل‌های VOB جریان‌های برنامه MPEG هستند، اما همه جریان‌های برنامه MPEG با VOB سازگار نیستند.

## ساختار دی وی دی ویدئو ##

هنگامی که یک DVD در رایانه باز می شود، VIDEO_TS فهرست راهنمای سطح بالا با AUDIO_TS است. AUDIO_TS خالی است و استفاده نمی شود. در داخل فهرست VIDEO_TS، فایل های VOB، BUP و IFO وجود دارد. فایل های VOB حاوی محتوای MPEG هستند. اینها به قطعات 1 گیگابایتی یا کمتر تقسیم می شوند تا با همه سیستم عامل ها سازگار باشند. فایل های IFO حاوی اطلاعاتی در مورد منوها و ساختار عنوان هستند. فایل های BUK فایل های پشتیبان فایل های IFO با همین نام هستند. قرار است این فایل ها به صورت فیزیکی در یک قسمت جداگانه نگهداری شوند تا در صورت آسیب دیدن فایل IFO به دلیل آسیب فیزیکی به DVD، فایل BUK بتواند همان اطلاعات را ارائه دهد.

### چیدمان فیزیکی ###

- تمامی فایل های روی دیسک باید به هم پیوسته باشند.
- فایل های مرتبط باید در کنار یکدیگر (VOB، IFO، BUP) باشند.
- فایل های شماره گذاری شده به ترتیب صعودی باشند.

## محافظت از کپی ##

بسیاری از دی وی دی های ویدئویی رمزگذاری شده اند و از کپی کردن داده ها از دی وی دی جلوگیری می کنند. کلیدهای احراز هویت و رمزگشایی برای پخش فایل هایی که در ناحیه ورودی غیرقابل دسترس DVD قرار دارند، مورد نیاز است. این کلیدها توسط نرم افزار رمزگشایی CSS که در پخش کننده DVD یا پخش کننده نرم افزار وجود دارد استفاده می شود. بدون کلید، فایل‌های ویدیویی قابل پخش نیستند، زیرا هنگام باز کردن فایل‌ها، کلیدها درخواست می‌شوند.

## منابع ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)
