---
date: 2019-10-11
keywords: java, .java, java file format, how to open java files, how to run java files, java file, java sample code
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Jفرم فایل avaat
linktitle: Java
description: Lدر مورد فرمت فایل جاوا و APIهایی که می توانند فایل جاوا را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## فایل جاوا چیست؟ ##
یک فایل حاوی کد منبع جاوا و ذخیره شده با پسوند فایل جاوا به عنوان فایل جاوا شناخته می شود. جاوا یکی از پرکاربردترین فناوری ها برای توسعه بازی ها، موبایل، وب و اپلیکیشن های دسکتاپ است. از آنجایی که جاوا مستقل از پلتفرم است، بدون نقص در ویندوز، مک، لینوکس، رزبری پای و غیره کار می کند. جاوا بسیار شبیه به C# و C++ است، بنابراین جابجایی بین این زبان ها آسان تر است.

## تاریخچه مختصر ##

پروژه جاوا در ژوئن 1991 توسط جیمز گاسلینگ، مایک شریدان و پاتریک ناتون آغاز شد. جاوا در ابتدا Oak نام داشت. بعداً به Green و در نهایت به جاوا تغییر نام داد. جیمز گاسلینگ جاوا را با نحوی شبیه به C/C++ طراحی کرد. اولین نسخه عمومی جاوا در سال 1996 توسط Sun Microsystems منتشر شد. این می تواند بر روی تمام سیستم های محبوب اجرا شود که باعث می شود جاوا به سرعت محبوب شود. با انتشار جاوا 2 در دسامبر 1998، پیکربندی های متعددی برای انواع مختلف پلتفرم ها ساخته شد. نسخه ها به شرح زیر بود

- J2EE (Java EE): برای راه حل های سازمانی
- J2ME (Java ME): برای برنامه های موبایل
- J2SE (Java SE): برای برنامه های دسکتاپ

در 19 نوامبر 2006، ماشین مجازی جاوا (JVM) توسط Sun به عنوان نرم افزار رایگان و منبع باز منتشر شد. پس از اینکه شرکت اوراکل شرکت Sun Microsystems را در سال‌های 2009 تا 2010 خریداری کرد، جیمز گاسلینگ در 2 آوریل 2010 از اوراکل استعفا داد.

## نحوه اجرا / اجرای کد جاوا ##

برای اجرای کد جاوا ابتدا باید کامپایل شود. برای آن، Java SDK مورد نیاز است. Java SDK کد جاوا را در یک فایل کلاس بایت کد کامپایل می کند. IDE هایی مانند Eclipse و IntelliJ Idea وجود دارند که کار با فایل های جاوا را با ارائه تکمیل کد و رابط کاربری آسان برای کامپایل و اجرای کد جاوا آسان تر می کنند.

## فرمت فایل جاوا ##

سینتکس جاوا به شدت تحت تأثیر C و C++ بود، اما برخلاف C++، جاوا تقریباً منحصراً به عنوان یک زبان شی گرا ساخته شد. در جاوا، تمام کدها در داخل کلاس ها نوشته می شوند و هر آیتم داده یک شی است. برخلاف C++، جاوا از بارگذاری بیش از حد اپراتور یا وراثت چندگانه پشتیبانی نمی کند.

### کد نمونه جاوا ###

در زیر نمونه ای از نحو جاوا آورده شده است.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
در کد بالا کلمه کلیدی **public** نشان دهنده اصلاح کننده دسترسی است. بیان می کند که این کلاس ممکن است توسط کلاس های خارج از سلسله مراتب کلاس قابل دسترسی باشد. اصلاح کننده دسترسی همچنین می تواند **محافظت شود** (در همان بسته قابل دسترسی است) یا **خصوصی** (روش ها فقط توسط همان کلاس قابل دسترسی هستند). *استاتیک** جلوی متد نشان می دهد که متد را می توان بدون نمونه خاصی از کلاس فراخوانی کرد. **void** نشان می دهد که متد چیزی بر نمی گرداند. برای چاپ رشته در کنسول. از دستور System.out.println استفاده شده است. در این دستور، کلاس *System* دارای یک فیلد ثابت *out* است که نمونه ای از کلاس *PrintStream* حاوی متد *println* است.

نام فایل فایل های جاوا باید با نام کلاس یکی باشد. بنابراین فایل جاوا برای کد مثال، *ExampleApp.java* نامیده می شود.

## منابع ##

- [Java (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))
