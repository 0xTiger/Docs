{
  "date": "2019-10-11",
  "keywords": [
    "psd file",
    "psd file format",
    "what is a psd file",
    "file",
    "psd example",
    "psd file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PSD - ফটোশপ ইমেজ ফাইল ফরম্যাট",
  "description": "PSD ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা PSD ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "PSD",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-psd-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি PSD ফাইল কি?

PSD, ফটোশপ ডকুমেন্ট, গ্রাফিক্স ডিজাইনিং এবং ডেভেলপমেন্টের জন্য ব্যবহৃত অ্যাডোব ফটোশপের নেটিভ ফাইল ফরম্যাটের প্রতিনিধিত্ব করে। PSD ফাইলে ইমেজ লেয়ার, অ্যাডজাস্টমেন্ট লেয়ার, লেয়ার মাস্ক, অ্যানোটেশন, ফাইল ইনফরমেশন, কীওয়ার্ড এবং অন্যান্য ফটোশপ-নির্দিষ্ট উপাদান থাকতে পারে। ফটোশপ ফাইলগুলিতে .PSD হিসাবে ডিফল্ট এক্সটেনশন থাকে এবং সর্বোচ্চ উচ্চতা এবং প্রস্থ 30,000 পিক্সেল এবং দৈর্ঘ্যের সীমা দুই গিগাবাইট।

## PSD ফাইল ফরম্যাট স্পেসিফিকেশন ##

একটি PSD ফাইলের ডেটা বড় এন্ডিয়ান বাইট ক্রমে সংরক্ষণ করা হয়। এটি উইন্ডোজ প্ল্যাটফর্মে পড়ার বা লেখার সময় ছোট এবং দীর্ঘ পূর্ণসংখ্যার অদলবদল বোঝায়। ফটোশপ ফাইল ফরম্যাট পাঁচটি প্রধান অংশে বিভক্ত। এটিতে অনেক দৈর্ঘ্য চিহ্নিতকারী রয়েছে যা এক বিভাগ থেকে অন্য বিভাগে যেতে ব্যবহার করা যেতে পারে। দৈর্ঘ্য চিহ্নিতকারী সাধারণত 2 বা 4 বাইট ব্যবধানে বৃত্তাকারে বাইট দিয়ে প্যাড করা হয়। পাঁচটি প্রধান অংশ হল:

* ফাইল হেডার

* কালার মোড ডেটা

* চিত্র সম্পদ

* স্তর এবং মাস্ক তথ্য

* ইমেজ ডেটা


সামঞ্জস্যের জন্য, বিভাগে এই সমস্ত ক্ষেত্রে ডেটা লেখা উচিত, কারণ ফটোশপ পুরো বিভাগটি পড়ার চেষ্টা করতে পারে। এটিও বোঝায় যে একটি ফাইলে লেখার সময় এড়িয়ে যাওয়া ক্ষেত্রগুলিতে শূন্য লেখা হবে। দৈর্ঘ্য-সীমাবদ্ধ বিভাগে দৈর্ঘ্য ক্ষেত্রটি কখন পড়া বন্ধ করতে হবে তা সিদ্ধান্ত নিতে ব্যবহার করা উচিত। বেশিরভাগ ক্ষেত্রে, দৈর্ঘ্য ক্ষেত্রটি বাইটের সংখ্যা নির্দেশ করে, রেকর্ড নয়, অনুসরণ করে। ফাইল পড়ার সময় নিচের বিষয়গুলো মনে রাখতে হবে।

* সমস্ত টেবিলের "দৈর্ঘ্য" কলামের মানগুলি বাইটে রয়েছে৷

* ইউনিকোড স্ট্রিং হিসাবে সংজ্ঞায়িত সমস্ত মান রয়েছে:

* একটি 4-বাইট দৈর্ঘ্যের ক্ষেত্র, স্ট্রিং-এ অক্ষরের সংখ্যা প্রতিনিধিত্ব করে (বাইট নয়)।

* ইউনিকোড মানের স্ট্রিং, প্রতি অক্ষর দুই বাইট।


### ফাইল হেডার ###

ফাইল হেডারে ছবির মৌলিক বৈশিষ্ট্য রয়েছে।

|দৈর্ঘ্য | বর্ণনা
---|---|
|4|স্বাক্ষর: সর্বদা '8BPS' এর সমান। স্বাক্ষর এই মান মেলে না যদি ফাইল পড়ার চেষ্টা করবেন না.
|2|Version: always equal to 1. ফাইলটি পড়ার চেষ্টা করবেন না যদি সংস্করণটি এই মানটির সাথে মেলে না। (~*~*PSB~*~* সংস্করণ হল ২।)
|6|সংরক্ষিত: শূন্য হতে হবে।
|2|যেকোন আলফা চ্যানেল সহ ছবিতে চ্যানেলের সংখ্যা। সমর্থিত পরিসর হল 1 থেকে 56।
|4|পিক্সেলে ছবির উচ্চতা। সমর্থিত পরিসর হল 1 থেকে 30,000।
|4|ছবির প্রস্থ পিক্সেলে। সমর্থিত পরিসর হল 1 থেকে 30,000।
|2|গভীরতা: প্রতি চ্যানেলে বিটের সংখ্যা। সমর্থিত মান হল 1, 8, 16 এবং 32।
|2|ফাইলের রঙের মোড। সমর্থিত মানগুলি হল: বিটম্যাপ # 0; গ্রেস্কেল # 1; সূচীকৃত # 2; আরজিবি #3; CMYK # 4; মাল্টিচ্যানেল # 7; ডুওটোন # 8; ল্যাব # 9।

### কালার মোড ডেটা সেকশন ###

রঙ মোড ডেটা বিভাগটি নিম্নরূপ গঠন করা হয়েছে:


|দৈর্ঘ্য | বর্ণনা
---|---|
|4|নিম্নলিখিত কালার ডেটার দৈর্ঘ্য
|পরিবর্তনশীল|কালার ডেটা

ফাইল হেডার বিভাগে মোড ক্ষেত্র দ্বারা সংজ্ঞায়িত হিসাবে কালার মোড ডেটা শুধুমাত্র সূচীকৃত রঙ এবং ডুওটোনের জন্য উপলব্ধ। অন্যান্য সমস্ত মোডের জন্য, এই বিভাগটি 4-বাইট জিরোড মান দ্বারা উপস্থাপিত হয়। সূচীকৃত রঙিন চিত্রগুলির জন্য, দৈর্ঘ্য 768 এবং রঙের ডেটাতে ছবির রঙের সারণী রয়েছে, অ-বিচ্ছিন্ন ক্রমে। Duotone চিত্রগুলির জন্য, রঙের ডেটাতে ডুটোন স্পেসিফিকেশন রয়েছে (যার বিন্যাসটি নথিভুক্ত নয়)। ফটোশপ ফাইলগুলি পড়ার অন্যান্য অ্যাপ্লিকেশনগুলি একটি ডুটোন ইমেজকে একটি ধূসর চিত্র হিসাবে বিবেচনা করতে পারে এবং ফাইলটি পড়ার এবং লেখার সময় ডুওটোন তথ্যের বিষয়বস্তু সংরক্ষণ করতে পারে।

### চিত্র সম্পদ বিভাগ ###

ফাইলের তৃতীয় বিভাগে চিত্র সম্পদ রয়েছে। এটি একটি দৈর্ঘ্যের ক্ষেত্র দিয়ে শুরু হয়, তারপরে রিসোর্স ব্লকের একটি সিরিজ।


|দৈর্ঘ্য | বর্ণনা
---|---|
|4|ইমেজ রিসোর্স সেকশনের দৈর্ঘ্য। দৈর্ঘ্য শূন্য হতে পারে।
|ভেরিয়েবল|ইমেজ রিসোর্স (ইমেজ রিসোর্স ব্লক)

ইমেজ রিসোর্সগুলি পেন টুল পাথের মতো ছবির সাথে যুক্ত নন-পিক্সেল ডেটা সঞ্চয় করতে ব্যবহৃত হয়। এগুলিকে রিসোর্স ব্লক হিসাবে উল্লেখ করা হয় কারণ তারা ফটোশপের প্রাথমিক সংস্করণগুলিতে ম্যাকিনটোশের রিসোর্সে সংরক্ষিত ডেটা ধারণ করে৷ ইমেজ রিসোর্স ব্লকের মৌলিক কাঠামো নীচে দেখানো হয়েছে:


|দৈর্ঘ্য | বর্ণনা
---|---|
|4|স্বাক্ষর: '8BIM
|2|রিসোর্সের জন্য স্বতন্ত্র শনাক্তকারী। ইমেজ রিসোর্স আইডিগুলিতে ফটোশপ দ্বারা ব্যবহৃত রিসোর্স আইডিগুলির একটি তালিকা রয়েছে৷
|ভেরিয়েবল
|4|সম্পদ তথ্যের প্রকৃত আকার যা অনুসরণ করে
|পরিবর্তনশীল এটি আকার সমান করতে প্যাড করা হয়.

ইমেজ রিসোর্স বিভিন্ন স্ট্যান্ডার্ড আইডি নম্বর ব্যবহার করে।

### স্তর এবং মাস্ক তথ্য ###

একটি ফটোশপ ফাইলের চতুর্থ বিভাগে স্তর এবং মুখোশ সম্পর্কে তথ্য রয়েছে যেমন স্তরগুলির সংখ্যা, স্তরগুলিতে চ্যানেল, ব্লেন্ডিং রেঞ্জ, সমন্বয় স্তর কী, প্রভাব স্তর এবং মাস্ক প্যারামিটার। কোন স্তর বা মুখোশ না থাকলে, এই বিভাগটি শূন্যযুক্ত 4-বাইট ক্ষেত্র দ্বারা উপস্থাপিত হয়। শূন্য মানগুলির কারণে এই বিভাগটি পড়ার সময় বিভাগগুলির দৈর্ঘ্যের দিকে বিশেষ মনোযোগ দেওয়া দরকার। লেয়ার এবং মাস্ক বিভাগের বিন্যাস নিম্নরূপ:


|দৈর্ঘ্য | বর্ণনা
---|---|
|4|স্তর এবং মুখোশ তথ্য বিভাগের দৈর্ঘ্য। (PSB দৈর্ঘ্য 8 বাইট।)
|পরিবর্তনশীল|স্তরের তথ্য
|ভেরিয়েবল|গ্লোবাল লেয়ার মাস্ক তথ্য
|পরিবর্তনশীল

#### স্তরের তথ্য ####

নিচের সারণীটি স্তরের তথ্যের উচ্চ-স্তরের সংগঠন দেখায়।


|দৈর্ঘ্য | বর্ণনা
---|---|
|4|Length of the layers info section, rounded up to a multiple of 2. (PSB দৈর্ঘ্য 8 বাইট।)
|2|স্তর গণনা। যদি এটি একটি ঋণাত্মক সংখ্যা হয়, তবে এর পরম মান হল স্তরগুলির সংখ্যা এবং প্রথম আলফা চ্যানেলে মার্জ করা ফলাফলের জন্য স্বচ্ছতা ডেটা রয়েছে৷
|পরিবর্তনশীল|প্রতিটি স্তর সম্পর্কে তথ্য। দেখুন লেয়ার রেকর্ড প্রতিটি স্তরের জন্য এই তথ্যের গঠন বর্ণনা করে।
|ভেরিয়েবল|চ্যানেল ইমেজ ডেটা। প্রতিটি স্তরের জন্য এক বা একাধিক চিত্র ডেটা রেকর্ড রয়েছে৷ স্তর তথ্য হিসাবে একই ক্রমে হয়

### চিত্র ডেটা ###

ইমেজ পিক্সেল ডেটা ফাইলের ইমেজ ডেটা বিভাগে থাকে। ইমেজ ডাটা সেকশনে ডাটার বিন্যাস করা হয় প্ল্যানার অর্ডারে অর্থাৎ প্রথমে সমস্ত লাল ডাটা, তারপর সব সবুজ ডাটা ইত্যাদি। প্রতিটি প্লেন স্ক্যান-লাইন ক্রমে সংরক্ষণ করা হয়, কোনো প্যাড বাইট ছাড়াই, ইমেজ ডাটা সেকশনটি একটি ফরম্যাটে সাজানো হয়। নিম্নলিখিত সারণীতে দেখানো হয়েছে।

|দৈর্ঘ্য | বর্ণনা
---|---|
|2|Compression method: *0 = Raw image data * 1 = RLE সংকুচিত চিত্র ডেটা সমস্ত স্ক্যান লাইনের জন্য বাইট গণনা দিয়ে শুরু হয় (সারি * চ্যানেল), প্রতিটি গণনা একটি দুই-বাইট মান হিসাবে সংরক্ষণ করা হয়। RLE সংকুচিত ডেটা অনুসরণ করে, প্রতিটি স্ক্যান লাইন আলাদাভাবে সংকুচিত হয়। RLE কম্প্রেশন হল একই কম্প্রেশন অ্যালগরিদম যা Macintosh ROM রুটিন PackBits এবং TIFF স্ট্যান্ডার্ড ব্যবহার করে। *2 = জিপ পূর্বাভাস ছাড়া *3 = ভবিষ্যদ্বাণী সহ জিপ।
|পরিবর্তনশীল|চিত্রের তথ্য। প্ল্যানার অর্ডার = RRR GGG BBB, ইত্যাদি।

## তথ্যসূত্র ##

* [PSD ফাইল ফরম্যাট স্পেসিফিকেশন - Adobe দ্বারা](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)

* [Adobe Photoshop ফাইল ফরম্যাট](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

