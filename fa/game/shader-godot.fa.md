{
   "date":"2023-10-11",
   "keywords":[
"سایه زن",
"فایل سایه زن",
"فایل shader engine shader godot",
"نحوه باز کردن فایل شیدر",
"فایل",
"پسوند فایل shader",
"افزونه",
"فایل"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"فرمت فایل SHADER - فایل Shader Engine Godot",
   "description":"با فرمت فایل SHADER Godot Engine Shader و API هایی که می توانند فایل های SHADER را ایجاد و باز کنند آشنا شوید.",
   "linktitle":"SHADER Godot",
   "menu":{
      "docs":{
         "identifier":"game-shader-godot-fa",
         "parent":"game"
}
},
   "lastmod":"2023-10-11"
}

## فایل SHADER چیست؟

**Godot Engine Shader File** فایلی است که در **موتور بازی Godot** برای تعریف شیدرهای سفارشی استفاده می شود. سایه بان ها راهی برای دستکاری ظاهر اشیا در بازی سه بعدی یا دو بعدی با مشخص کردن نحوه رندر شدن آنها هستند. این فایل‌های سایه‌زن معمولاً به زبانی به نام Godot Shader Language (GDScript) نوشته می‌شوند که یک زبان سایه‌زنی سفارشی است که برای استفاده در موتور بازی گودو طراحی شده است.

## چگونه SHADER ایجاد کنیم؟

در گودو، می توانید سایه بان ها را برای دستیابی به جلوه های بصری مختلف ایجاد کنید، از جمله:

1.  تغییر رنگ یا بافت یک شی
2.  استفاده از افکت های مختلف نور و سایه.
3.  ایجاد مواد سفارشی برای مدل های سه بعدی.
4.  تحریف یا متحرک کردن ظاهر اشیا.

## نمونه فایل SHADER

فایل Godot Shader معمولاً دارای پسوند .shader است و حاوی کد سایه زن است که نحوه نمایش یک شی را مشخص می کند. در اینجا یک مثال ساده از یک فایل بسیار ابتدایی Godot Shader آورده شده است:

```gdscript
shader_type canvas_item;

void fragment() {
    // Modify fragment color
    COLOR = vec4(1.0, 0.0, 0.0, 1.0); // Red color
}
```

در این مثال، کد سایه زن برای یک آیتم بوم دو بعدی نوشته شده است و به سادگی رنگ شی را قرمز می کند. این یک سایه زن بسیار ابتدایی است و در عمل، شیدرها می توانند برای دستیابی به جلوه های بصری پیشرفته بسیار پیچیده شوند.

Godot یک ویرایشگر سایه‌زن بصری ارائه می‌کند که به شما امکان می‌دهد بدون نوشتن کد مستقیم، سایه‌بان ایجاد کنید و آن را برای توسعه‌دهندگان بازی که ممکن است تجربه عمیقی با برنامه‌نویسی شیدر نداشته باشند، در دسترس قرار دهد. این ویرایشگر بصری به شما اجازه می دهد تا گره های مختلف را برای ایجاد سایه بان های سفارشی متصل کنید.

برای استفاده از شیدر در پروژه گودو خود، آن را به متریال متصل می‌کنید، که سپس می‌توانید آن را روی یک مدل سه بعدی یا هر شی دیگری که می‌خواهید با افکت سایه‌زن مشخص رندر کنید اعمال کنید.

## موتور بازی گودو

Godot یک موتور بازی متن باز و چند پلتفرمی است که به توسعه دهندگان اجازه می دهد بازی های دو بعدی و سه بعدی و برنامه های کاربردی تعاملی ایجاد کنند. این به دلیل کاربر پسند بودن، تطبیق پذیری و مجموعه ای از ویژگی های قوی شناخته شده است. در اینجا برخی از جنبه ها و ویژگی های کلیدی موتور بازی گودو آورده شده است:

1.  **منبع باز:** گودو تحت مجوز MIT منتشر شده است، به این معنی که استفاده از آن رایگان و منبع باز است. توسعه دهندگان می توانند به کد منبع دسترسی داشته باشند و آن را تغییر دهند و آن را بسیار قابل تنظیم می کند.
    
2.  **Cross-Platform:** Godot از طیف گسترده ای از پلتفرم ها از جمله Windows، macOS، Linux، Android، iOS، HTML5 و موارد دیگر پشتیبانی می کند. شما می توانید بازی خود را بر روی یک پلتفرم توسعه دهید و آن را به چندین پلتفرم دیگر صادر کنید.
    
3.  **اسکریپت نویسی:** گودو از چندین زبان برنامه نویسی، از جمله GDScript (زبان پایتون مانند طراحی شده برای گودو)، C# و VisualScript (یک زبان برنامه نویسی بصری) پشتیبانی می کند. این انعطاف‌پذیری به توسعه‌دهندگان اجازه می‌دهد تا زبانی را که با آن راحت‌تر هستند انتخاب کنند.
    
4.  **سیستم صحنه:** گودو از یک سیستم صحنه مبتنی بر گره استفاده می کند که سازماندهی و ترکیب عناصر بازی را آسان می کند. صحنه ها می توانند از گره های مختلفی تشکیل شوند که می توانند اشیا، کاراکترها، عناصر رابط کاربری و موارد دیگر را نشان دهند.
    
5.  **فیزیک:** گودو دارای یک موتور فیزیک دو بعدی و سه بعدی داخلی است که ساخت بازی با تعاملات فیزیک واقع گرایانه را آسان می کند.
    
6.  ** انیمیشن:** گودو یک سیستم انیمیشن قوی برای ایجاد انیمیشن های پیچیده ارائه می دهد که می تواند روی اشیا، کاراکترها و عناصر رابط کاربری اعمال شود.
    
7.  **مدیریت دارایی:** گودو سیستم منبعی را برای مدیریت دارایی ها از جمله تصاویر، صدا، مدل های سه بعدی و موارد دیگر ارائه می دهد. منابع به راحتی وارد شده و در موتور سازماندهی می شوند.
    
8.  ** سایه بان های بصری: ** گودو دارای یک ویرایشگر سایه زن بصری است که به توسعه دهندگان این امکان را می دهد تا بدون نوشتن کد، افکت های سایه زن پیچیده ایجاد کنند.
    
9.  **ویرایشگر:** ویرایشگر گودو کاربرپسند و دارای امکانات فراوان است. این شامل ابزارهایی برای طراحی سطح، انیمیشن، ویرایش اسکریپت و موارد دیگر است. از ویرایش بلادرنگ و اشکال زدایی زنده پشتیبانی می کند.
    
10.  **GDNative:** GDNative به شما امکان می دهد ماژول ها و افزونه ها را به زبان هایی مانند C و C++ بنویسید و آنها را به طور یکپارچه با گودو ادغام کنید.
    

Godot یک انتخاب عالی برای توسعه دهندگان بازی های مستقل، علاقمندان و تیم های بازی سازی کوچک تا متوسط است. این یک پلت فرم قدرتمند و انعطاف پذیر برای ایجاد بازی ها و برنامه های کاربردی تعاملی ارائه می دهد و در عین حال برای توسعه دهندگان با سطوح مختلف تجربه در دسترس باقی می ماند.

## چگونه فایل SHADER را باز کنیم؟

برنامه هایی که فایل های SHADER را باز می کنند یا به آنها ارجاع می دهند شامل می شوند

- **Godot Engine** (رایگان) برای (ویندوز، مک، لینوکس)

## سایر فایل های SHADER

در اینجا انواع فایل دیگری وجود دارد که از پسوند فایل **.shader** استفاده می کنند.

**فایل های بازی**
- [SHADER - Godot Engine Shader File](/game/shader-godot/)
- [SHADER - Quake 3 Engine Shader File](/game/shader-quake/)
- [SHADER - Unity Shader Asset](/game/shader-unity/)

## منابع
* [Godot (موتور بازی)](https://en.wikipedia.org/wiki/Godot_(game_engine))


