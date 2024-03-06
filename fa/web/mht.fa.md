{
  "date": "2019-10-11",
  "keywords": [
"mht",
"فایل mht",
"فرمت فایل mht",
"نوع فایل mht",
"فایل",
"نوع",
"فایل mht چیست"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل MHT - MIME HTML",
  "description": "درباره فرمت فایل MHT و APIها برای ایجاد و باز کردن فایل های MHT بیاموزید.",
  "linktitle": "MHT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mh-fat"
}
},
  "lastmod": "2021-02-29"
}

## فایل MHT چیست؟

یک فایل با پسوند mht. یک فرمت فایل بایگانی با قابلیت MIME است که شامل انواع مختلف داده در یک فایل واحد است. این می تواند داده هایی مانند متن، تصاویر، استایل صفحه را در قالب فایل های [CSS](/web/css/)، جاوا اسکریپت و سایر منابع به عنوان منابع جاسازی شده در خود ذخیره کند. فایل‌های MHT، با نوع MIME message/rfc822، تمام محتویات یک فایل HTML را به عنوان یک فایل بایگانی واحد برای ذخیره در بایگانی در دستگاه‌های ذخیره‌سازی کپسوله می‌کنند. برنامه های نرم افزاری مانند Microsoft Word به شما امکان می دهد اسناد WORD خود را با صادرات به عنوان فایل MHT به MHT تبدیل کنید. فایل های MHT را می توان با استفاده از مرورگرهای محبوب مانند Microsoft Internet Explore و Google Chrome باز کرد.

## فرمت فایل MHT

مانند [MHTML](/web/mhtml/)، MHT نیز یک کپسوله سازی MIME از اسناد HTML انبوه است. محتویات سند داخل یک سند MHT مانند تصاویر درون خطی، شیوه نامه ها، اپلت ها و غیره با MIME کدگذاری شده اند، جایی که از طریق URI به یک منبع ریشه پیوند داده می شوند. سرویس گیرنده های ایمیل مانند Microsoft Outlook ایمیل ها (معمولاً [EML](/email/eml/)) را در قالب فایل MHT ذخیره می کند. مشخصات کامل فرمت فایل MHT در [RFC 822](https://tools.ietf.org/html/rfc822) موجود است و برای توسعه نرم افزار نرم افزاری که می تواند فایل های MHT را پردازش کند می توان به آن مراجعه کرد.

## تفاوت بین MHT و MHTML

در حین ذخیره یک صفحه آنلاین، از کاربر خواسته می شود تا نوع فرمت فایلی را که در آن صفحه آنلاین باید در سیستم بومی ذخیره شود، تعیین کند. معمولاً کاربر بین زبان نشانه گذاری و فرمت فایل MHTML گیج می شود. آنها متوجه می شوند که دیدن اینکه فرمت فایل بین اینها سالم تر است، مشکل ساز است.

هنگامی که کاربر تصمیم می گیرد از هدر رفتن صفحه آنلاین به عنوان زبان نشانه گذاری جلوگیری کند، آنگاه یک پوشه تشکیل می شود که حاوی چندین فایل برای محتویات مختلف صفحه است، یعنی واحد منطقه فایل های کاملاً متفاوتی که برای متن، گرافیک، اپلت ها و غیره ایجاد شده است. از طرف مقابل، صرفه جویی می شود. صفحه آنلاین به عنوان MHTML یک فایل برای صفحه آنلاین کامل ایجاد می کند. تمام عناصر صفحه به همراه گرافیک، لینک ها و واحد منطقه فایل های جایگزین درون یک فایل تعبیه شده است.

به طور طبیعی، رسیدگی به فایل‌های MHT یا MHTML کار ساده‌ای است، زیرا فایل ممکن است به سادگی از طریق ایمیل محافظت شده و به اشتراک گذاشته شود. با این حال، واحد منطقه فایل های زبان نشانه گذاری زیر احتمال از دست دادن اطلاعات به دلیل از دست دادن یا حذف حتی یک فایل می تواند پوشه زبان نشانه گذاری کامل را برای کاربر بی فایده ایجاد کند.

## منابع

* [MHTML - Wikipedia](https://en.wikipedia.org/wiki/MHTML)

* [MHT RFC](https://tools.ietf.org/html/rfc822)

