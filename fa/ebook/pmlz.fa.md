{
  "date": "2021-03-30",
  "keywords": [
"PMLZ",
"فایل زیپ شده Palm Markup Language",
"افزونه",
"فایل",
"قالب",
"کتاب الکترونیکی",
"زبان نشانه گذاری پالم"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل PMLZ، Palm Markup Language و APIهایی که می‌توانند فایل‌های PMLZ را ایجاد و باز کنند، بیاموزید.",
  "title": "PMLZ - فایل زبان نشانه گذاری پالم فشرده",
  "linktitle": "PMLZ",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-pml-faz"
}
},
  "lastmod": "2021-03-30"
}

## فایل PMLZ چیست؟

Palm Inc یک نوع فایل کتاب الکترونیکی را معرفی کرد. به عنوان فرمت فایل PMLZ که نسخه فشرده‌شده فرمت فایل [PML](/ebook/pml/) شناخته می‌شود، به همین دلیل فایل‌های با پسوند pmlz. به نام **فایل زبان علامت‌گذاری پالم فشرده** شناخته می‌شوند. فایل PMLZ فقط یک محفظه فشرده از یک فایل است که فایل‌های [PDB](/programming/pdb/) را برای ایجاد اسناد برای **eReader** (معروف به دستگاه خواندن کتاب الکترونیکی مانند رایانه لوحی) کامپایل می‌کند. فایل PML طرح بندی را به یک فایل PDB (شامل فایل های داده های مختلف) می دهد تا در دستگاه Palm نمایش داده شود. در حالی که یک فایل PDB یک فایل پایگاه داده است که توسط برنامه های مختلف از جمله Quicken، Pegasus، Microsoft Visual Studio و Palm Pilot استفاده می شود. به طور خلاصه، PMLZ یک محفظه فشرده از فایل های PML و PDB است.


## دانش در مورد زبان نشانه گذاری Palm
جدول زیر دستورات PML را مشخص می کند:

|فرمان|توضیحات|
---|---|
| \p | صفحه جدید |
| \x | فصل جدید؛ همچنین باعث شکستن صفحه جدید می شود. عنوان فصل (و هر کد سبک) را با \x و \x | ببندید
| \Xn | فصل جدید، n سطح تورفتگی (n بین 0 و 4 شامل) در گفتگوی فصل. باعث شکست صفحه نمی شود عنوان فصل (و هر کد سبک) را با \Xn و \Xn | محصور کنید
| \Cn=عنوان فصل | عنوان فصل را با سطح n در فهرست فصل وارد کنید (مانند \Xn). متن در صفحه نشان داده نمی شود و صفحه را مجبور به شکستن نمی کند. برای مثال، گاهی اوقات می‌تواند برای درج علامت فصل در ابتدای مقدمه فصل مفید باشد. |
| \c | این بلوک متن را در مرکز قرار دهید. بستن با \c در ابتدای خط |
| \r | بلوک متنی را توجیه کنید. بستن با \r در ابتدای خط |
| \i | بلوک مورب بستن با \i |
| \u | بلوک زیر خط بکش. بستن با \u |
| \o | بلوک Overstrike; بستن با \o |
| \v | متن نامرئی؛ بستن با \v (قابل استفاده برای نظرات) |
| \t | بلوک تورفتگی شروع از ابتدای یک خط، بستن با \t در انتهای یک خط |
| \T=50% | درصد مشخص شده از عرض صفحه را در این مورد 50 درصد فرورفتگی می کند. اگر موقعیت ترسیم فعلی از محل مشخص شده صفحه گذشته باشد، این برچسب نادیده گرفته می شود. |
| \w=50% | یک قاعده افقی با درصد معینی از عرض صفحه را جاسازی کنید، در این مورد 50%. این تگ باعث شکست خط قبل و بعد از آن می شود. قانون محور است. علامت درصد اجباری است. |
| \n | به فونت عادی که توسط کاربر مشخص شده است بروید
| \s | تغییر به stdFont؛ بستن با \s برای بازگشت به فونت عادی |
| \b | تغییر به boldFont؛ با \b ببندید تا به فونت عادی برگردید (منسوخ شده؛ به جای آن از \B استفاده کنید) |
| \l | تغییر به largeFont؛ بستن با \l برای بازگشت به فونت عادی |
| \B | متن را به صورت پررنگ علامت بزنید. برخلاف تگ \b، \B فونت را تغییر نمی دهد، بنابراین می توانید متن پررنگ بزرگی داشته باشید. شما نمی توانید \b و \B را در یک فایل PML مخلوط کنید. |
| \Sp | علامت گذاری متن به عنوان بالانویس نباید با سبک های دیگر مانند پررنگ، ایتالیک و غیره مخلوط شود. |
| \Sb | علامت گذاری متن به عنوان زیرمجموعه نباید با سبک های دیگر مانند پررنگ، ایتالیک و غیره مخلوط شود. متن زیر را با \Sb ضمیمه کنید. |
| \k | متن محصور شده را به حروف کوچک تبدیل کنید. بستن با \k. هر کاراکتر محصور در تگ \k (از جمله آنهایی که تاکید دارند) با حروف بزرگ ساخته می شوند و در اندازه نقطه کوچکتر از یک کاراکتر بزرگ معمولی ارائه می شوند. |
| \\ | نشان دهنده یک بک اسلش |
| \aXXX | نویسه غیر ASCII را وارد کنید که کد Windows-1252 آن XXX اعشاری است. برای جزئیات بیشتر به جدول کاراکترهای PML مراجعه کنید. |
| \UXX | نویسه غیر ASCII را وارد کنید که کد یونیکد آن هگزا دسیمال XXXX است. برای جزئیات بیشتر به جدول کاراکتر PML Extended مراجعه کنید. |
| \m=imagename.png | تصویر نامگذاری شده را درج کنید. بخش تصاویر زیر را ببینید. |
| \q=#linkanchorبرخی متن\q | به یک لنگر پیوند که در نقطه دیگری از سند است ارجاع دهید. رشته بعد از مشخصات لنگر و قبل از انتهای \q زیر خط کشیده می شود یا در صورت مشاهده سند به عنوان یک پیوند نشان داده می شود. |
| \Q=linkanchor | یک لنگر پیوند در سند مشخص کنید. |
| \- | یک خط فاصله نرم قرار دهید. خط فاصله ی نرم تنها در صورتی نشان داده می شود که لازم باشد کلمه ای در یک خط شکسته شود. |
| \Fn=footnote11\Fn | 1 را به پاورقی پیوند دهید که نام آن پاورقی 1 است که در انتهای سند PML برچسب گذاری شده است. بخش پاورقی ها و نوارهای جانبی را در زیر ببینید. |
| \Sd=sidebar1نوار کناری\Sd | متن نوار کناری را به نوار کناری که نام آن sidebar1 است، که در انتهای سند PML برچسب گذاری شده است، پیوند دهید. بخش پاورقی ها و نوارهای جانبی را در زیر ببینید. |
| \ من | علامت گذاری به عنوان یک آیتم شاخص مرجع. مورد فهرست (و هر کد سبک) را با \I و \I.| ببندید


## منابع

* [Palm Markup Language - By MobileRead](https://wiki.mobileread.com/wiki/EReader)

* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)

