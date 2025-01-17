{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAS - فرمت فایل Lidar LASer",
  "description": "با فرمت فایل LAS و APIهایی که می توانند فایل های LAS را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "LAS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-fas"
}
},
  "lastmod": "2023-07-18"
}

## فایل LAS چیست؟

فرمت فایل LAS (Lidar LASer) یک فرمت فایل باینری است که به طور خاص برای ذخیره داده های ابر نقطه لیدار طراحی شده است. این فرمت توسط انجمن فتوگرامتری و سنجش از دور آمریکا (ASPRS) به عنوان یک قالب استاندارد برای تبادل داده‌های لیدار و قابلیت همکاری ایجاد شده و نگهداری می‌شود.

فایل‌های LAS اطلاعات دقیق درباره نقاط لیدار، از جمله مختصات سه بعدی (x، y، و z)، مقادیر شدت، کدهای طبقه‌بندی و ویژگی‌های اضافی را ذخیره می‌کنند. این فرمت از داده‌های لیدار بازگشت گسسته و شکل موج کامل پشتیبانی می‌کند و امکان ذخیره بازگشت‌های متعدد در هر پالس لیزر را فراهم می‌کند.

## فرمت فایل LAS

ساختار یک فایل LAS از سه بخش اصلی تشکیل شده است: هدر فایل، رکوردهای طول متغیر (VLR) و رکوردهای داده نقطه ای.

1. سربرگ فایل: هدر فایل حاوی اطلاعات ضروری در مورد فایل LAS است، مانند نسخه فرمت داده، فرمت داده نقطه، تعداد نقاط، مختصات جعبه مرزی، سیستم مرجع مختصات (CRS) و سایر ابرداده ها. خلاصه ای از داده های لیدار موجود در فایل را ارائه می دهد.

2. Variable Length Records (VLRs): VLRs are optional and can store additional metadata and custom information about the lidar data. VLRs allow for flexibility in extending the format to accommodate specific user requirements. Examples of VLRs include information about the sensor system, data processing parameters, or classification schemes.

3. سوابق داده های نقطه ای: سوابق داده های نقطه ای اندازه گیری های واقعی لیدار را ذخیره می کنند. هر رکورد داده نقطه ای یک نقطه لیدار را نشان می دهد و دارای ویژگی هایی مانند مختصات x، y و z، مقادیر شدت، کدهای طبقه بندی (به عنوان مثال، زمین، پوشش گیاهی، ساختمان ها) و سایر ویژگی های تعریف شده توسط کاربر است. رکوردهای نقطه همچنین می توانند مهرهای زمانی، تعداد بازگشت و زوایای اسکن را ذخیره کنند.

فایل های LAS از فرمت های مختلف داده (0 تا 10) پشتیبانی می کنند تا انواع مختلف داده های لیدار و سطح اطلاعات مورد نیاز را در خود جای دهند. به عنوان مثال، فرمت 0 یک فرمت نقطه ای ساده با اطلاعات پایه را نشان می دهد، در حالی که فرمت های 1 تا 3 داده های جامع تری از جمله اطلاعات شکل موج را برای هر بازگشت ارائه می دهند.

فایل‌های LAS به‌طور گسترده توسط نرم‌افزار لیدار و ابزارهای پردازش پشتیبانی می‌شوند و آنها را به فرمت استانداردی برای تبادل و تجزیه و تحلیل داده‌های لیدار تبدیل می‌کند. علاوه بر این، فایل‌های LAS را می‌توان با استفاده از تکنیک‌های فشرده‌سازی بدون اتلاف فشرده کرد تا اندازه فایل را کاهش دهد و در عین حال صحت داده‌های اصلی را حفظ کند. نسخه فشرده فایل های LAS اغلب به عنوان LAZ شناخته می شود که قابلیت ذخیره سازی و انتقال داده کارآمد را ارائه می دهد.

## منابع

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
