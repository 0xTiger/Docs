{
  "date": "2022-10-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فایل HDM - فایل زبان نشانه گذاری دستگاه دستی",
  "description": "با فرمت فایل HDM و APIهایی که می توانند فایل های HDM ایجاد و باز کنند آشنا شوید.",
  "linktitle": "HDM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hd-fam"
}
},
  "lastmod": "2022-10-12"
}

## فایل HDM چیست؟

فایل HDM یک فایل صفحه وب زبان نشانه گذاری است که در زبان نشانه گذاری دستگاه دستی (HDML) ایجاد می شود. این شامل برچسب‌های نشانه‌گذاری شبیه به زبان [HTML](/web/html/) است، اما برای دستگاه‌های الکترونیکی دستی مانند تلفن‌های هوشمند و PDA طراحی شده است. [HDML file format specifications](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) برای استانداردسازی به W3C ارسال شد اما نتوانست به استاندارد تبدیل شود. HDM بر اساس مشخصات فرمت فایل [HDML](/web/hdml/) موجود در وب سایت W3 است.

## فرمت فایل HDM - اطلاعات بیشتر

فایل HDM از تگ های نشانه گذاری تشکیل شده است که به وب سایت های طراحی شده بصری در دستگاه های دستی ارائه می شوند. فایل های HDM با استفاده از پروتکل HDTP (پروتکل حمل و نقل دستگاه دستی) به جای پروتکل HTTP که برای صفحات HTML استفاده می شود، در دستگاه ها کپی می شوند.

## عناصر فایل HDML

در زیر تعدادی از عناصر ارائه شده است که محیط زمان اجرا را برای HDML فراهم می کند و به عنوان عامل کاربر شناخته می شود.

| عنصر|توضیحات|
---|---|
|کارت|این بلوک اصلی HDML است و نمایش می دهد و به کاربر اجازه می دهد با کارت های اطلاعات تعامل داشته باشد. |
|عرشه|کارت های HDML با هم در عرشه ها گروه بندی می شوند. یک عرشه HDML شبیه یک صفحه HTML است که با URL [RFC1738] شناسایی می شود و واحد محتوای درخواستی از یک سرور و ذخیره شده توسط کاربر است.
|Actions|عملکردها می توانند از نوع PREV، SOFT1-SOFT8 و HELP باشند. اینها انتزاعی هستند و در رابط کاربری به شیوه ای خاص از عامل کاربر پشتیبانی می شوند.|
|فعالیت ها|یک فعالیت مانند گروهی از کارت های مرتبط است که یک عملکرد منطقی را انجام می دهند. اینها ممکن است یک یا چند عرشه را شامل شوند. مدل ناوبری و وضعیت HDML حول فعالیت ها ساختار یافته است.|
|ناوبری مبتنی بر تاریخ|عامل کاربر تاریخچه ای از کارت های نمایش داده شده به کاربر را حفظ می کند. هر کارتی که به آن دسترسی داشته باشید به تاریخچه کارت اضافه می شود. عامل کاربر به کاربر اجازه می دهد تا به راحتی به کارت قبلی در تاریخچه برگردد.|

## منابع

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [مشخصات HDML - مدارس W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)


