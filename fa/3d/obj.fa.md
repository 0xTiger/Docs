{
  "date": "2019-10-11",
  "keywords": [
"فایل obj",
"فرمت فایل obj",
"فایل obj چیست",
"فایل",
"مثال obj",
"پسوند فایل obj",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل OBJ",
  "description": "درباره فرمت فایل OBJ و APIهایی که می‌توانند فایل‌های OBJ را باز کرده و ایجاد کنند، بیاموزید.",
  "linktitle": "OBJ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-ob-faj"
}
},
  "lastmod": "2019-09-10"
}

## فایل OBJ چیست؟

فایل های **OBJ** توسط برنامه ویژوالایزر پیشرفته Wavefront برای تعریف و ذخیره اشیاء هندسی استفاده می شود. انتقال به عقب و جلو داده های هندسی از طریق فایل های OBJ امکان پذیر است. هر دو هندسه چند ضلعی مانند نقاط، خطوط، رئوس بافت، چهره ها و هندسه آزاد (منحنی ها و سطوح) با فرمت OBJ پشتیبانی می شوند. این قالب از انیمیشن یا اطلاعات مربوط به نور و موقعیت صحنه پشتیبانی نمی کند.

یک فایل OBJ معمولاً محصول نهایی فرآیند مدل سازی سه بعدی است که توسط یک CAD (طراحی به کمک رایانه) تولید می شود. ترتیب پیش‌فرض برای ذخیره رئوس در خلاف جهت عقربه‌های ساعت است و از اعلام صریح حالت عادی اجتناب می‌شود. اگرچه فایل های OBJ اطلاعات مقیاس را در یک خط نظر اعلام می کنند، اما هیچ واحدی برای مختصات OBJ اعلام نشده است.

## تاریخچه فرمت OBJ سه بعدی

Wavefront Technologies created OBJ file format for its Advanced Visualizer application to store geometric objects and 3D data. Its version 2.11 is superseded by a newly documented version 3. فرمت فایل باز است و توسط سایر فروشندگان برای برنامه گرافیکی سه بعدی خود پیاده سازی شده است. Wavefront Technologies این فرمت فایل را منبع باز و خنثی نگه داشت.

## فرمت فایل OBJ

در اشیاء سه بعدی، رمزگذاری هندسه سطح یک کار چالش برانگیز است که فرمت فایل OBJ آن را به خوبی انجام داد. این قالب کاملاً همه کاره است زیرا تعدادی انتخاب برای رمزگذاری هندسه سطح ارائه می دهد. در زیر سه قالب مجاز وجود دارد که مزایا و معایب خاص خود را دارند:

### Tessellation با چهره های چند ضلعی

فرمت فایل OBJ به کاربر این امکان را می دهد که سطح مدل سه بعدی را با استفاده از اشکال هندسی ساده یا پیچیده تسلیت دهد. برای رمزگذاری هندسه سطح یک مدل، یک فایل رئوس و نرمال هر چند ضلعی را ذخیره می کند. اگرچه Tessellation باعث افزایش درشتی مدل می شود، اما لازم است تعادل صحیح بین اندازه یک فایل و کیفیت چاپ آن کشف شود.

### منحنی فرم آزاد

فرمت فایل OBJ به منحنی های سطح آزاد تعریف شده توسط کاربر اجازه می دهد تا هندسه سطح یک مدل را مشخص کنند. از آنجایی که منحنی‌های فرم آزاد پیچیده‌تر از چهره‌های چند ضلعی هستند، زیرا با تعداد کمی پارامترهای ریاضی، خطوط منحنی را می‌توان به بهترین شکل با منحنی‌های آزاد تعریف کرد. بنابراین، با داده‌های کمتر در مقایسه با قالب‌های چند ضلعی، منحنی‌های فرم آزاد برای ایجاد کدگذاری با کیفیت بالا از هر مدل سه بعدی بدون افزایش اندازه فایل استفاده می‌شوند.

### سطوح آزاد شکل

فرمت فایل OBJ همچنین کاشی کاری هندسه سطح را با تکه های سطح آزاد مشخص می کند. این نوع تکه‌های سطحی آزاد (NURBS) برای سطوح بدون ابعاد شعاعی صلب مانند بدنه یک کامیون، بال‌های هلیکوپتر یا بدنه قایق بسیار مناسب است. استفاده از سطوح آزاد بسیار سودمند است زیرا برای کوچکتر نگه داشتن اندازه فایل با دقت بالاتر دقیق تر هستند. این سطوح بخش مهمی از صنعت هوافضا و خودرو هستند که دقت پایین آن نابخشودنی است.

کلمات کلیدی زیر بر اساس نوع داده مرتب شده اند تا هندسه سطح را تعریف کنند.


|عناصر|منحنی شکل آزاد/ بیانیه های بدنه سطح|منحنی شکل آزاد/ویژگی های سطح
---|---|---|
|p|نقطه|پارم|مقادیر پارامتر|درجه|درجه
|l|خط|تریم|حلقه پیرایش بیرونی|bmat|ماتریس پایه
|f|صورت|سوراخ|حلقه پیرایش داخلی|گام|اندازه گام
|منحنی|منحنی|scrv|منحنی خاص|ctype|منحنی یا نوع سطح
|curv2|منحنی 2 بعدی|sp|نقطه ویژه|**اتصال و گروه بندی سطوح**
|surf|سطح|پایان|اظهار پایان|کان|اتصال
|**نمایش/پرداخت ویژگی**|g|نام گروه
|مورب|درون یابی مخروطی|shadow_obj|ریخته گری سایه|ها|گروه هموارسازی
|lod|سطح جزئیات|trace_obj|ردیابی پرتو|mg|گروه ادغام
|d_interp|انحلال درونیابی|ctech|تکنیک تقریب منحنی|o|نام شی
|c_interp| درون یابی رنگ|stech|تکنیک تقریب سطح|
|usemtl|نام ماده|mtllib|کتابخانه مواد|
|**رئوس هندسی**|
|v|رئوس هندسی|vn|نرمال های رئوس|
|vt|رئوس بافت|vp|رئوس فضای پارامتر|

### رنگ و بافت

فایل OBJ به اطلاعات رنگ و بافت اجازه می دهد تا در یک فرمت فایل مرتبط به نام Material Template Library (MTL) ذخیره شوند. مدل های هندسی چند رنگ با استفاده از این دو فایل با هم رندر می شوند. فایل‌های MTL مبتنی بر ASCII هستند و با توصیف ویژگی‌های بازتاب نور یک سطح با استفاده از مدل بازتاب Phong، رندر رایانه را تسهیل می‌کنند. این استاندارد توسط تعداد زیادی از فروشندگان نرم افزار پذیرفته شده است که از مزایای آن برای تبادل مواد استفاده می کنند. فرمت MTL به دلیل عدم پشتیبانی از آخرین فناوری ها مانند نقشه های specular و parallax کمی قدیمی است.

## منابع

* [فایل Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

