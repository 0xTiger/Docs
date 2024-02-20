{
  "date": "2020-03-16",
  "keywords": [
    "DXF File",
    "File Format",
    "CAD"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "DXF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি DXF ফাইল তৈরি এবং খুলতে পারে।",
  "title": "DXF ফাইল ফরম্যাট",
  "linktitle": "DXF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dxf-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি DXF ফাইল কি?

DXF, ড্রয়িং ইন্টারচেঞ্জ ফরম্যাট, বা ড্রয়িং এক্সচেঞ্জ ফরম্যাট, অটোক্যাড অঙ্কন ফাইলের একটি ট্যাগ করা ডেটা উপস্থাপনা। ফাইলের প্রতিটি উপাদানের একটি উপসর্গ পূর্ণসংখ্যা রয়েছে যাকে গ্রুপ কোড বলা হয়। এই গ্রুপ কোডটি আসলে সেই উপাদানটির প্রতিনিধিত্ব করে যা অনুসরণ করে এবং একটি প্রদত্ত বস্তুর প্রকারের জন্য একটি ডেটা উপাদানের অর্থ নির্দেশ করে। DXF একটি অঙ্কন ফাইলে প্রায় সমস্ত ব্যবহারকারী-নির্দিষ্ট তথ্য উপস্থাপন করা সম্ভব করে তোলে।

ডিএক্সএফ ফাইল ফরম্যাট অটোডেস্ক দ্বারা অটোক্যাড এবং অন্যান্য অ্যাপ্লিকেশনের মধ্যে ডেটা আন্তঃঅপারেবিলিটির জন্য সিএডি ডেটা ফাইল ফর্ম্যাট হিসাবে বিকাশ করা হয়েছিল। এইভাবে, DXF ফাইল ফরম্যাটের ইন্টারঅপারেবিলিটি স্পেসিফিকেশন অনুযায়ী অন্যান্য ফরম্যাট থেকে DXF থেকে AutoCAD-এ ডেটা আমদানি করা যেতে পারে।

## সংক্ষিপ্ত ইতিহাস ##


The history of DXF file format dates back to 1982 when it was introduced as part of AutoCAD 1.0. AutoCAD-এর প্রাথমিক সংস্করণগুলি শুধুমাত্র DXF-এর ASCII ফাইল ফর্ম্যাটকে সমর্থন করে। 1988 সালে অটোক্যাড (এবং তার উপরে) 10 প্রকাশের সাথে, অটোক্যাড-এ ASCII এবং বাইনারি DXF ফাইল ফর্ম্যাট উভয়ের জন্য সমর্থন চালু করা হয়েছিল। পূর্ববর্তী পর্যায়ে, অটোডেস্ক কোনো ফাইল ফরম্যাট স্পেসিফিকেশন শেয়ার করেনি এবং এর কারণে, DXF ফাইলের সঠিক আমদানি সহজ ছিল না। যাইহোক, Autodesk এখন DXF স্পেসিফিকেশন প্রকাশ করে এবং সাধারণ জনগণের জন্য উপলব্ধ।

## ফাইল ফরম্যাট স্পেসিফিকেশন ##

ডিএক্সএফ ফাইল ফরম্যাট গ্রুপ কোড এবং মান জোড়া ব্যবহার করে বিষয়বস্তুকে বিভাগগুলিতে সাজায়। প্রতিটি বিভাগ রেকর্ডের সমন্বয়ে গঠিত যেখানে প্রতিটি রেকর্ড একটি গ্রুপ কোড এবং ডেটা আইটেম নিয়ে গঠিত। প্রতিটি গ্রুপ কোড এবং মান DXF ফাইলে তাদের নিজস্ব লাইনে রয়েছে। প্রতিটি বিভাগ একটি গ্রুপ কোড 0 দিয়ে শুরু হয় এবং তারপরে স্ট্রিং, SECTION। এটি একটি গ্রুপ কোড 2 এবং একটি স্ট্রিং দ্বারা অনুসরণ করা হয় যা বিভাগের নাম নির্দেশ করে (উদাহরণস্বরূপ, SECTION1)। প্রতিটি বিভাগ গ্রুপ কোড এবং মানগুলির সমন্বয়ে গঠিত যা এর উপাদানগুলিকে সংজ্ঞায়িত করে। একটি বিভাগ 0 দিয়ে শেষ হয় এবং তারপরে ENDSEC স্ট্রিং হয়।

DXF ফাইল বিন্যাস বস্তুগুলিকে সত্তা থেকে আলাদা বিবেচনা করে। অবজেক্টের এখানে কোন গ্রাফিকাল উপস্থাপনা নেই কিন্তু সত্তার আছে। সুতরাং, ডিএক্সএফ-এ এন্ট্রিগুলিকে গ্রাফিকাল অবজেক্ট হিসাবে উল্লেখ করা হয় যখন অবজেক্ট অবজেক্টগুলিকে নন-গ্রাফিক্যাল অবজেক্ট হিসাবে উল্লেখ করা হয়। DXF ফাইলের BLOCK এবং ENTITIES বিভাগে Entities রয়েছে এবং এই দুটি বিভাগে গ্রুপ কোডের ব্যবহার অভিন্ন। একটি সত্তার সমাপ্তি পরবর্তী 0 গ্রুপ দ্বারা নির্দেশিত হয়, যা পরবর্তী সত্তা শুরু হয় বা বিভাগের শেষ নির্দেশ করে।

### ফাইল স্ট্রাকচার ###

একটি DXF ফাইলের বিভাগগুলি নিম্নলিখিত ক্রমে সাজানো হয়েছে:

|Section|Basic description
---|---|
|হেডার|এই বিভাগে অঙ্কন সম্পর্কে সাধারণ তথ্য রয়েছে। এটি আপনার ফোনের সেটিংস কার্যকারিতার মতো, যেটিতে অঙ্কন এবং এর সাথে সম্পর্কিত মানগুলির সাথে যুক্ত বিভিন্ন ভেরিয়েবল রয়েছে৷ উদাহরণস্বরূপ, হেডার বিভাগটি নির্ধারণ করবে যে DXF ফাইলটি কোন অটোক্যাড সংস্করণ ব্যবহার করে ($ACADVER ভেরিয়েবল) বা ফাইলের কোণ পরিমাপ করতে ব্যবহৃত ইউনিট ($AUNITS পরিবর্তনশীল)
|শ্রেণীসমূহ
|টেবিলগুলি উদাহরণ স্বরূপ [line type](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) টেবিল (LTYPE) DXF ফাইলে ড্যাশ, ডট, টেক্সট এবং চিহ্নের প্যাটার্ন এবং সেগুলি কীভাবে স্কেল করা হয় তা সংজ্ঞায়িত করে। এই বিভাগে পাওয়া টেবিলগুলির একটি সম্পূর্ণ তালিকা এখানে রয়েছে:<ul><li> অ্যাপ্লিকেশন আইডি (APPID) টেবিল</li><li> ব্লক রেকর্ড (BLOCK_RECORD) টেবিল</li><li> মাত্রা শৈলী (DIMSTYPE) টেবিল</li><li> স্তর (LEYER) টেবিল</li><li> লাইনটাইপ (LTYPE) টেবিল</li><li> পাঠ্য শৈলী (স্টাইল) টেবিল</li><li> ইউজার কোঅর্ডিনেট সিস্টেম (UCS) টেবিল</li><li> দেখুন (ভিউ) টেবিল</li><li> ভিউপোর্ট কনফিগারেশন (VPORT) টেবিল</li></ul>
|ব্লকগুলি
|সত্তা এটি কাঁচা ডেটা অন্তর্ভুক্ত করতে পারে - উদাহরণস্বরূপ, একটি বৃত্ত সত্তা তার বেধ, কেন্দ্র বিন্দু, এর ব্যাসার্ধ এবং এক্সট্রুশন দিক দ্বারা সংজ্ঞায়িত করা হয়।
|অবজেক্টস|এখানে, আপনি অঙ্কনের অ-গ্রাফিকাল অংশগুলি খুঁজে পাবেন। উদাহরণস্বরূপ, অটোক্যাড অভিধান এখানে সংরক্ষিত আছে।

## তথ্যসূত্র ##

* [DXF File Specifications](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [উইকিপিডিয়া দ্বারা অটোক্যাড ডিএক্সএফ](https://en.wikipedia.org/wiki/AutoCAD_DXF)

