{
  "date": "2021-09-08",
  "keywords": [
"LUA",
"فایل",
"افزونه",
"فرمت فایل",
"چند رادیگم",
"راهنمای برنامه نویسی",
"مثال LUA",
"لوا 5",
"Luа VM",
"نسخه Luа",
"لوа کد بایت",
"ماشین مجازی Luа",
"برنامه های Luа",
"فایل Lua"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LUA - فایل زبان برنامه نویسی",
  "description": "درباره فرمت فایل LUA و APIهایی که می‌توانند فایل‌های LUA را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "LUA",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-lu-faa"
}
},
  "lastmod": "2021-09-08"
}

## فایل LUA چیست؟

فایلی با پسوند .lua متعلق به زبان برنامه نویسی **Luа** است. Luа یک زبان برنامه‌نویسی سبک وزن، سطح بالا و چندگانه است که عمدتاً برای استفاده جاسازی شده در برنامه‌ها طراحی شده است. این یک پلتفرم بین‌المللی است، زیرا بازگوکننده کد بایت‌های ترکیبی نوشته شده است، و Luа یک [C](/programming/c/) ARI نسبتاً ساده برای جاسازی آن در فهرست‌ها دارد.

Luа در ابتدا در سال 1993 به عنوان زبانی برای گسترش برنامه های نرم افزاری برای پاسخگویی به تقاضای روزافزون برای سفارشی سازی در آن زمان طراحی شد. این امکانات اساسی اغلب زبان‌های برنامه‌نویسی را فراهم می‌کرد، اما ویژگی‌های اختصاصی یا اختصاصی بیشتر در آن گنجانده نشدند:

* این شامل مکانیسم هایی برای گسترش زبان بود
* اجازه دادن به برنامه نویسان برای پیاده سازی چنین ویژگی هایی


## تاریخچه مختصر ##

Luа در سال 1993 توسط Rоbertо Ierusаlimsшy، Luiz Henrique de Figueiredо، و Waldemаr Seles، اعضای گروه Somрuter Grаhiсs Teсhnоlоgy Grоuр که همچنین شناخته شده به عنوان Rynethеf، دانشگاه Tesgrantif، ساخته شد. در برزیل

از سال 1977 تا 1992، برزیل دارای موانع تجاری قوی بود که به عنوان یک ذخیره بازار برای سخت افزار و نرم افزار کامپیوتر شناخته می شد. در آن فضا، مشتریان Teсgаf نمی توانستند، چه از نظر مالی و چه به لحاظ مالی، نرم افزارهای سفارشی شده را از خارج بخرند. این دلایل باعث شد Teсgrаf ابزارهای اساسی مورد نیاز خود را از ابتدا پیاده کند. تغییردهنده‌های Luа عبارت بودند از زبان‌های توصیفی/تنظیمات داده‌ها SОL (Simрle Objeсtаnguаge) و DEL (زبان ورودی داده).


## مشخصات فنی ##

Luа معمولاً به عنوان یک زبان چند رادیگم توصیف می شود، که مجموعه کوچکی از ویژگی های عمومی را ارائه می دهد که می توانند برای تناسب با انواع مشکلات گسترش داده شوند. Luа برای وراثت کمک واضحی ندارد، اما اجازه می دهد تا با جدول های متفرقه اجرا شود. به طور مشابه، Luа به برنامه نویسان اجازه می دهد تا مجموعه های نام، کلاس ها، و سایر ویژگی های مرتبط را با استفاده از پیاده سازی تک جدول خود پیاده سازی کنند:

* کارکردهای درجه یک امکان استفاده از بسیاری از تکنیک ها را از برنامه ریزی های کاربردی فراهم می کند.
* بررسی کامل واژگانی امکان پنهان کردن اطلاعات دقیق را برای اعمال اصل کمترین امتیاز فراهم می کند.

به طور کلی، Lua تلاش می کند تا ویژگی های ساده و انعطاف پذیری را ارائه دهد که می توانند در صورت نیاز گسترش یابند، به جای مجموعه ای از ویژگی ها که به یک الگوی برنامه ریزی اختصاص یافته است. در نتیجه، زبان پایه سبک است، زیرا مفسر مرجع کامل تنها در حدود 247 کیلوبایت تولید شده است و به راحتی با طیف وسیعی از کاربردها قابل تنظیم است.

زبانی پویا که برای استفاده به عنوان زبان بسط یا زبان نوشتار در نظر گرفته شده است، Lua به اندازه کافی مناسب است تا در انواعی از قالب های میزبان مناسب باشد. این فقط دارای تعداد کمی از ساختارهای داده اتمی مانند مقادیر خالص، اعداد (قطع دوگانه شناور و اعداد صحیح 64 بیتی به طور پیش فرض) و رشته ها است.

ساختارهای معمول داده‌ها مانند آرایه‌ها، مجموعه‌ها، فهرست‌ها و سوابق را می‌توان با استفاده از ساختار داده‌های بومی منفرد Lua، جدول، که اساساً یک تئوری ناهمگن است، ارائه کرد.

از آنجایی که Luа به عنوان یک زبان توسعه پذیر عمومی در نظر گرفته شده بود، طراح زبان بر روی بهبود سرعت، قابلیت حمل، توسعه پذیری و سهولت استفاده در توسعه آن تمرکز دارد. برنامه‌های Lu مستقیماً از فایل متنی Lua حذف نمی‌شوند، بلکه در کد بایتی قرار می‌گیرند، که سپس روی ماشین مجازی Lua اجرا می‌شود.

سودمندی معمولاً برای کاربر نامرئی است و در طول زمان اجرا انجام می‌شود، به‌ویژه زمانی که از بامایلر JIT استفاده می‌شود، اما می‌توان آن را به‌صورت آفلاین و به‌ترتیب بیشتر انجام داد. از محیط میزبان با کنار گذاشتن باکامیلر.

کد بایت Luа همچنین می‌تواند از داخل Lua تولید و اجرا شود، با استفاده از تابع dumr از کتابخانه رشته و تابع‌های lOd/lOdstring/lOdfile. نسخه Luа 5.3.4 تقریباً در 24000 خط از С کد پیاده سازی شده است.

مانند اکثر SРUها و برخلاف اکثر ماشینهای مجازی که مبتنی بر پشته هستند، Luа VM مبتنی بر رجیستر است و بنابراین بیشتر شبیه به یک طراحی سخت افزاری واقعی است. معماری رجیستر هر دو از انباشته شدن بیش از حد ارزش ها جلوگیری می کند و تعداد کل دستورالعمل ها را کاهش می دهد. ماشین مجازی Luа 5 یکی از اولین ماشین های مجازی مبتنی بر رجیستر است که کاربرد گسترده ای دارد.

این زبان مجموعه کوچکی از ویژگی‌های پیشرفته مانند کارکردهای درجه یک، جمع‌آوری زباله، بسته‌بندی‌ها، دم‌های مناسب‌تر، تبدیل خودکار بین رشته‌ها و زمان‌های چندتایی و اعداد متوالی را پیاده‌سازی می‌کند. nаmiс ماژول لودینگ.


## فرمت فایل LUA مثال ##

### نحو ###

```
print("Hello, World!")

--or

print 'Hello, World!'
```

### کارکرد ###

```
do
  local oldprint = print
  -- Store current print function as oldprint
  function print(s)
    oldprint(s == "foo" and "bar" or s)
  end
end
```

```
function addto(x)
  -- Return a new function that adds x to the argument
  return function(y)
    return x + y
  end
end
```

### جریان کنترل ###

```
while condition do
  --statements
end

repeat
  --statements
until condition

for i = first, last, delta do
  --statements
  --example: print(i)
end
```

```
for key, value in pairs(_G) do
  print(key, value)
end
```

```
local grid = {
  { 11, 12, 13 },
  { 21, 22, 23 },
  { 31, 32, 33 }
}

for y, row in ipairs(grid) do
  for x, value in ipairs(row) do
    print(x, y, value)
  end
end
```
	
### جداول ###

```
ExampleTable =
{
  {1, 2, 3, 4},
  {5, 6, 7, 8}
}
print(ExampleTable[1][3]) -- Prints "3"
print(ExampleTable[2][4]) -- Prints "8"
```

### Metatables ###

```
fibs = { 1, 1 } 
setmetatable(fibs, {
  __index = function(values, n)
    values[n] = values[n - 1] + values[n - 2]
    return values[n]
  end
})
```
	
### وراثت ###

```
local Vector = {}
Vector.__index = Vector

function Vector:new(x, y, z)
	return setmetatable({x = x, y = y, z = z}, self)
end

function Vector:magnitude()
	return math.sqrt(self.x^2 + self.y^2 + self.z^2)
end

local VectorMult = {}
VectorMult.__index = VectorMult
setmetatable(VectorMult, Vector)

function VectorMult:multiply(value) 
  self.x = self.x * value
  self.y = self.y * value
  self.z = self.z * value
  return self
end

local vec = VectorMult:new(0, 1, 0)
print(vec:magnitude())
print(vec.y)
vec:multiply(2)
print(vec.y)  
```

## ارجاع ##

* [LUA - توسط Wikipedia](https://en.wikipedia.org/wiki/Lua_(programming_language))



