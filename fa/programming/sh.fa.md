{
  "date": "2019-10-11",
  "keywords": [
"فایل sh",
"فایل .sh",
"افزونه",
"قالب",
"نمونه فایل sh",
"فرمت فایل sh",
"نحوه اجرای فایل sh"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SH - فایل اسکریپت Bash Shell",
  "description": "با فرمت فایل SH و APIهایی که می توانند فایل های SH را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "SH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-s-fah"
}
},
  "lastmod": "2021-05-21"
}

## فایل SH چیست؟

یک فایل با پسوند .sh یک فایل دستورات زبان برنامه نویسی است که حاوی برنامه کامپیوتری است که باید توسط پوسته یونیکس اجرا شود. این می تواند شامل یک سری دستورات باشد که به صورت متوالی برای انجام عملیاتی مانند پردازش فایل ها، اجرای برنامه ها و سایر کارهایی از این قبیل اجرا می شوند. اینها از رابط خط فرمان توسط کاربر یا به صورت دسته ای اجرا می شوند تا چندین عملیات را همزمان انجام دهند. فایل‌های اسکریپت را می‌توان در ویرایشگرهای متنی مانند Notepad، Notepad++، Vim، Apple Terminal و سایر برنامه‌های مشابه در Windows، MacOS و Linux OS باز کرد.

## فرمت فایل SH

فایل های SH به صورت متنی ساده و به دنبال نحو تعریف شده نوشته می شوند. این فایل های اسکریپت پشتیبانی می کنند:

 * Comments - نظرات با # شروع می شوند و توسط پوسته نادیده گرفته می شوند.
 * میانبرها - می توان از آنها برای تغییر نام یک فرمان برای اجرای کوتاه و آسان استفاده کرد.
 * کارهای دسته ای - چندین دستور را می توان به طور خودکار اجرا کرد که در غیر این صورت باید به صورت دستی وارد شوند. این نیاز به منتظر ماندن کاربر برای راه اندازی هر مرحله از دنباله را از بین می برد.
 * تعمیم - با استفاده از حلقه های ساده، تعمیم بسیار بیشتری برای عملیاتی مانند تبدیل تصاویر از یک Fromat به دیگری بدست می آید.

## نمونه فایل SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## چگونه فایل SH را اجرا کنیم؟
فایل‌های SH معمولاً روی لینوکس اجرا می‌شوند، حتی در ویندوز باید با استفاده از نرم‌افزارهایی مانند Putty به ترمینال لینوکس متصل شوید تا فایل‌های sh را اجرا کنید. مراحل زیر برای اجرای یک فایل SH در ترمینال لینوکس آمده است.

1. ترمینال لینوکس را باز کنید و به دایرکتوری که فایل SH در آن قرار دارد بروید.
2. با استفاده از دستور 'chmod'، مجوز اجرا را روی اسکریپت خود تنظیم کنید (اگر قبلا تنظیم نشده باشد).
3. اسکریپت را با استفاده از یکی از موارد زیر اجرا کنید
	1. «./filename.sh».
	2.  sh filename.sh.
	3.  bash script-name-here.sh.

## منابع

* [Bashscripting برای مبتدیان](https://help.ubuntu.com/community/Beginners/BashScripting)

* [Shellscript](https://www.shellscript.sh/)


