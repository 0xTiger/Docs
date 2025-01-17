{
  "date": "2021-09-14",
  "keywords": [
"mrc",
"فایل",
"افزونه",
"فرمت فایل",
"پیاده سازی mrc",
"راهنمای برنامه نویسی",
"مثال mrc",
"mIRC",
"زبان برنامه نویسی mIRC",
"فایل های INI",
"زبان برنامه نویسی mSL",
"زبان mIRC",
"اسکریپت های mIRC",
"زبان برنامه نویسی"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "MRC - فایل زبان اسکریپت mIRC",
  "description": "درباره فرمت فایل MRC و APIهایی که می‌توانند فایل‌های MRC را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MRC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mr-fac"
}
},
  "lastmod": "2021-09-14"
}

## فایل MRC چیست؟

mIRC یک زبان برنامه نویسی است که به عنوان یک کلاینت IRC (Internet Relay Chat) در سیستم عامل ویندوز تعبیه شده است. این یک تسهیلات محافظتی در برابر هرزنامه برای استفاده شخصی و کانال فراهم می کند. برای ارائه تجربه بهتری از سازگاری کاربر، این زبان برنامه نویسی mIRC اجازه ایجاد پنجره های گفتگو را می دهد. فایل‌هایی که حاوی اسکریپت‌ها هستند، عمدتاً در قالب متن ساده با پسوند MRC یا به عنوان فایل‌های [INI](/system/ini/) ذخیره می‌شوند. توابع این زبان به عنوان دستورات و شناسه (زمانی که مقدار را برمی گرداند) شناخته می شوند.

زبان mIRC بارگذاری چندین فایل اسکریپت را در یک زمان فراهم می کند. از طرف دیگر، یک فایل می تواند باعث شود که دیگری در هنگام بارگذاری همزمان دیگر استفاده نشود. دستورات ذخیره می شوند و می توانند به طور خودکار در IRC وجود داشته باشند. دستورات و نام مستعار استفاده شده در این زبان اولویت هیچ یک از کاراکترها را ندارند.

mIRC به طور گسترده برای مدیریت خودکار یک کانال توسط ربات ها استفاده می شود، اما می توان آن را با زبان برنامه نویسی mSL نیز تغییر داد. می‌تواند بسیاری از ویژگی‌های جدید مانند ماکروها، توانایی پخش موسیقی، ماکروها و عملکردهای کوچک، بازی‌های اساسی یا اجرای برنامه‌های کوچک را معرفی کند.


## تاریخچه مختصر ##

این زبان اسکریپت برای اولین بار در سال 1995 توسط خالد آدام بی توسعه یافت. طراحی زبان اسکریپت نیز توسط خالد ساخته شده است. هدف این زبان برنامه نویسی رویداد محور بود. در ابتدا پسوند فایل مورد استفاده برای فایل های این زبان برنامه نویسی mrc. و .ini بود. علاوه بر این، تحت مجوز نرم افزار اختصاصی توسعه یافته است.

## مشخصات فنی ##

برخی از توابع از طریق این زبان mIRC سفارشی شده و به نام مستعار شناخته می شوند. هنگامی که این نام مستعار مقادیری را برمی گرداند، به عنوان شناسه های سفارشی شناخته می شوند. تمام متغیرهای موجود در این زبان mIRC به صورت پویا تایپ می شوند. Sigil ها توسط اسکریپت های mIRC استفاده می شوند. یکی دیگر از ویژگی های این زبان برنامه نویسی پاپ آپ است. کاربران می توانند پاپ آپ ها را به سادگی با انتخاب آنها فراخوانی کنند. ریموت ها برای رویدادهای خاصی مشخص می شوند. ریموت ها زمانی فراخوانی می شوند که رویداد نسبی رخ دهد.

برای شکستن هر خط کد این زبان از نشانه‌های فاصله‌دار استفاده می‌شود. برخی از پسوندهای محبوب دیگر مانند MDX (mIRC Dialog Extension) و DCX (Dialog Control Extension) برای فایل‌های mIRC استفاده می‌شوند. هر دوی اینها پسوند دیالوگ هستند و نسبتاً محبوب تر هستند. ساختارهای زبان با نامگذاری این زبان اسکریپت نویسی به آن اشاره می شود. زبان mIRC شامل جنبه های مختلف یک زبان برنامه نویسی مانند متغیرهای محلی و سراسری، متغیرهای باینری، جداول هش و مدیریت فایل است.


## فرمت فایل MRC مثال ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## ارجاع ##

* [MIRC - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/MIRC_scripting_language)




