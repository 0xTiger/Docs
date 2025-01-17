{
  "date": "2023-06-08",
  "keywords": [
"فایل hpp",
"فایل hpp چیست",
"فایل hpp شامل چه چیزی است",
"نمونه فایل hpp",
"فرمت فایل hpp چیست",
"فایل",
"پسوند فایل hpp",
"افزونه"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل HPP - C++ Header File",
  "description": "درباره فرمت HPP و APIهایی که می‌توانند فایل‌های HPP را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp-fa",
      "parent": "programming"
}
},
  "lastmod": "2023-06-08"
}

## فایل HPP چیست؟

فرمت فایل .hpp معمولا برای فایل های هدر در زبان برنامه نویسی C++ استفاده می شود. فایل‌های هدر معمولاً حاوی اعلان‌ها و تعاریف توابع، کلاس‌ها، متغیرها و ثابت‌هایی هستند که توسط فایل‌های کد منبع دیگر در پروژه C++ استفاده می‌شوند.

هدف از استفاده از فایل‌های هدر، ارائه راهی برای به اشتراک گذاشتن کدهای مشترک بین چندین فایل کد منبع بدون تکرار کد است. هنگامی که فایل منبع C++ نیاز به دسترسی به اعلان‌ها یا تعاریف از فایل هدر دارد، شامل فایل هدر با استفاده از دستورالعمل پیش‌پردازنده «#include» می‌شود.

پسوند فایل .hpp اغلب برای نشان دادن اینکه یک فایل یک فایل هدر C++ است استفاده می شود. استفاده از این پسوند خاص برای فایل‌های هدر الزامی نیست، و همچنین ممکن است با فایل‌های هدر با .h یا پسوندهای دیگر مواجه شوید. انتخاب پسوند تا حد زیادی به قرارداد و ترجیح شخصی بستگی دارد.

هنگامی که یک فایل منبع C++ شامل فایل هدر با استفاده از «#include» می‌شود، کامپایلر قبل از کامپایل کردن آن به‌عنوان یک واحد، به‌طور مؤثر محتوای فایل هدر را با فایل منبع ترکیب می‌کند. این به فایل منبع اجازه می دهد تا به اعلان ها و تعاریف موجود در فایل هدر دسترسی داشته باشد و اطلاعات لازم را برای کامپایلر برای انجام بررسی نوع و تولید کد فراهم می کند.

## فایل HPP شامل چه چیزی است؟

در اینجا برخی از مطالب رایجی که ممکن است در فایل .hpp بیابید آمده است:

- **اعلان های تابع:** فایل های سرصفحه اغلب شامل اعلان های تابع بدون اجرای واقعی آنها هستند. این اعلان‌ها اطلاعاتی درباره نام تابع، نوع بازگشتی و پارامترها ارائه می‌کنند و به فایل‌های کد منبع دیگر اجازه می‌دهند تا بدون نیاز به دانستن جزئیات پیاده‌سازی از تابع استفاده کنند.
- **اعلان های کلاس:** فایل های هدر می توانند شامل اعلان های کلاس، از جمله نام کلاس، متغیرهای عضو، توابع عضو و مشخص کننده های دسترسی باشند. با گنجاندن اعلان کلاس در فایل هدر، فایل های کد منبع دیگر می توانند اشیایی از آن کلاس ایجاد کرده و به اعضای آن دسترسی داشته باشند.
- **اعلان های ثابت:** فایل های سرصفحه می توانند ثابت هایی را تعریف کنند، مانند متغیرهای سراسری یا مقادیر enum که قرار است در چندین فایل کد منبع به اشتراک گذاشته شوند. این ثابت‌ها را می‌توان با گنجاندن فایل هدر در فایل‌های منبع دیگر، دستیابی به آن‌ها امکان استفاده از ثابت‌های تعریف‌شده را فراهم کرد.
- **تعریف نوع:** فایل های سرصفحه ممکن است دارای تعاریف نوع با استفاده از کلمه کلیدی typedef یا تایپ نام مستعار با استفاده از کلمه کلیدی using باشند. این تعاریف نام های جدیدی را برای انواع موجود ایجاد می کند و کد را قابل خواندن و نگهداری تر می کند.
- **تعریف تابع درون خطی:** در برخی موارد، فایل های هدر ممکن است دارای تعاریف تابع درون خطی باشند. توابع درون خطی، توابع کوچکی هستند که به جای فراخوانی به عنوان تابع مجزا، در سایت فراخوانی گسترش می یابند. گنجاندن تعریف تابع درون خطی در فایل هدر به کامپایلر اجازه می دهد تا مستقیماً فراخوانی تابع را با بدنه تابع جایگزین کند و به طور بالقوه عملکرد را بهبود بخشد.

## نمونه فایل HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## فرمت فایل HPP چیست؟

HPP یک فایل متنی ساده است اما از قوانین کلی و نحو زبان برنامه نویسی C++ پیروی می کند. در اینجا فرمت و ساختار کلی فایل .hpp به صورت تفکیک شده است:

- **حفاظ‌های هدر:** معمولاً یک فایل .hpp با محافظ‌های هدر شروع می‌شود تا از درج چندگانه یک فایل جلوگیری کند. این امر با استفاده از دستورالعمل‌های پیش‌پردازنده مانند «#ifndef»، «#define» و «#endif» به دست می‌آید. محافظ سرصفحه تضمین می کند که محتویات فایل فقط یک بار در طول فرآیند کامپایل گنجانده شده است.
- **شامل عبارات:** بعد از محافظ های هدر، می توانید سایر فایل های هدر لازم را با استفاده از دستورالعمل '#include' اضافه کنید. اینها ممکن است شامل سرصفحه های استاندارد کتابخانه یا سایر سرصفحه های سفارشی مورد نیاز کد شما باشد.
- **اعلان ها و تعاریف:** محتوای اصلی فایل .hpp عبارت است از اعلان ها و در برخی موارد، تعاریف کلاس ها، توابع، ثابت ها، نام مستعار نوع و عناصر دیگر. برای مثال، می‌توانید کلاس‌ها را با استفاده از کلمه کلیدی «class»، توابع را با استفاده از نوع بازگشتی، نام و فهرست پارامترها و ثابت‌ها را با استفاده از کلمه کلیدی «const» و سپس نوع و نام آن‌ها اعلام کنید.
- **تعاریف تابع درون خطی:** در موارد خاص، ممکن است تعاریف تابع درون خطی را مستقیماً در فایل hpp. قرار دهید. توابع درون خطی معمولاً در بدنه کلاس تعریف می شوند، به این معنی که تعریف تابع در کنار اعلان آن گنجانده شده است. این را می توان با پیشوند تعریف تابع با کلمه کلیدی inline انجام داد.
- **اعلام فضای نام:** اگر از فضای نام در کد خود استفاده می کنید، می توانید آنها را در فایل .hpp اعلام کنید. این کار با استفاده از کلمه کلیدی «space» به دنبال نام فضای نام و محصور کردن کد مربوطه در بلوک فضای نام انجام می شود.

## منابع
* [فایل های سرصفحه (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


