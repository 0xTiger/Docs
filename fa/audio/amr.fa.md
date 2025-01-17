{
  "date": "2021-04-29",
  "keywords": [
"amr",
".amr",
"فایل",
"افزونه",
"قالب",
"فایل amr چیست",
"موسیقی",
"فرمت فایل amr",
"فایل amr",
"تبدیل فایل amr به mp3",
"پخش فایل amr"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل AMR و APIهایی که می‌توانند فایل‌های AMR را ایجاد، تبدیل و باز کنند، بیاموزید.",
  "title": "AMR - فایل کدک چند نرخی تطبیقی",
  "linktitle": "AMR",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-am-far"
}
},
  "lastmod": "2021-04-29"
}

## فایل AMR چیست؟
فایل با پسوند amr. یک فرمت داده صوتی مربوط به کدک صوتی **Adaptive Multi-Rate** است. متشکل از یک کدک گفتار باند باریک چند نرخی است که سیگنال‌های باند باریک را با نرخ بیت 4.75-12.2 کیلوبیت بر ثانیه با کیفیت صدایی که از 7.4 کیلوبیت بر ثانیه شروع می‌شود، رمزگذاری می‌کند. از تطبیق پیوند برای انتخاب یکی از هشت نرخ بیت مختلف بر اساس استفاده می کند.

## فرمت فایل AMR
AMR file format uses many coding techniques, the ACELP (Algebraic Code Excited Linear Prediction) algorithm one of the best technique; designed for compressing human spoken audio in a more efficient way. The AMR was set as the standard voice or speech codec by 3GPP in 1999. فرمت فایل AMR همچنین برای ذخیره صدای گفتاری با استفاده از کدک صوتی **Adaptive Multi-Rate** که توسط بسیاری از تلفن های هوشمند برای ذخیره سخنرانی های ضبط شده استفاده می شود، استفاده می شود.

### ساختار فرمت فایل
AMR (Adaptive Multi-Rate) یک فرمت صوتی است. به طور گسترده در برنامه ها و دستگاه های مختلف تلفن همراه، به طور معمول در پخش کننده / ضبط کننده صوتی یا در نوع برنامه های VoIP استفاده می شود. AMR را می توان بیشتر به صورت زیر طبقه بندی کرد:

1. AMR-NB (باند باریک)
2. AMR-WB (باند پهن)

معمولاً AMR به AMR-NB اشاره دارد. فرمت فایل AMR دارای ساختار زیر است:

هر فایل AMR شامل یک هدر 6 بایتی است که فایل را به عنوان صدای AMR می شناسد. این هدر همیشه به صورت زیر تنظیم می شود:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

این معمولاً در تمام فایل‌های AMR-NB شبیه‌تر است. اگر هدر از استاندارد پیروی کند، احتمالاً فایل خراب است و نباید استفاده شود. فایل AMR از تعداد کامل فریم های صوتی تشکیل شده است. این فریم ها هر کدام 20 میلی ثانیه صدا می سازند. هر فریم را می توان با استفاده از هر یک از حالت های معتبر AMR-NB (0-7، 8 SID در حالت DTX) کدگذاری کرد. از آنجایی که فریم ها را می توان با نرخ بیت های مختلف کدگذاری کرد، این روش معمولی به نام Adaptive Multi-Rate (AMR) نامیده می شود.
#### حالت های AMR
در زیر حالت های مختلف AMR و بیت ریت مربوط به آنها آورده شده است:

|حالت| نرخ بیت|
---|---|
|0| AMR 4.75 - رمزگذاری با سرعت 4.75 کیلوبیت بر ثانیه|
|1 | AMR 5.15 - رمزگذاری با سرعت 5.15 کیلوبیت بر ثانیه|
|2 | AMR 5.9 - رمزگذاری با سرعت 5.9 کیلوبیت بر ثانیه|
|3 | AMR 6.7 - کدگذاری با سرعت 6.7 کیلوبیت بر ثانیه|
|4 | AMR 7.4 - رمزگذاری با سرعت 7.4 کیلوبیت بر ثانیه|
|5 | AMR 7.95 - رمزگذاری با سرعت 7.95 کیلوبیت بر ثانیه|
|6 | AMR 10.2 - کدگذاری با سرعت 10.2 کیلوبیت بر ثانیه|
|7 | AMR 12.2 - رمزگذاری با سرعت 12.2 کیلوبیت بر ثانیه|

اندازه فریم حالت های AMR بر حسب بایت (شامل بایت هدر) در زیر آورده شده است:

|CMR |MODE |اندازه فریم(به بایت)|
---|---|---|
|0 |AMR 4.75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7.95 |21|

## منابع ##

* [کدک صوتی تطبیقی چند نرخی - توسط ویکی پدیا](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)

* [فرمت RTP Payload و فرمت ذخیره‌سازی فایل برای کدک‌های صوتی AMR و AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)


