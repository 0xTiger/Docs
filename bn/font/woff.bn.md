{
  "date": "2020-08-20",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "WOFF - ওয়েব ওপেন ফাইল ফরম্যাট",
  "description": "একটি WOFF ফাইল হল একটি ওপেন ফন্ট ফরম্যাট যা ওয়েব ওপেন ফন্ট ফরম্যাটে তৈরি করা হয়।",
  "linktitle": "WOFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-bn"
    }
  },
  "lastmod": "2020-09-30"
}

## একটি WOFF ফাইল কি?

.woff এক্সটেনশন সহ একটি ফাইল হল ওয়েব ওপেন ফন্ট ফরম্যাট (WOFF) এর উপর ভিত্তি করে একটি ওয়েব ফন্ট ফাইল। এটিতে TrueType (.TTF) বা OpenType (.OTT) ফন্ট প্রকারের উপর ভিত্তি করে ফর্ম্যাট-নির্দিষ্ট সংকুচিত কন্টেইনার রয়েছে৷ ডেস্কটপ অ্যাপ্লিকেশনগুলিতে ব্যবহৃত ফন্ট ফাইলগুলি থেকে ওয়েব ফন্টগুলিকে আলাদা করার লক্ষ্যে WOFF চালু করা হয়েছিল। উপরন্তু, নেটওয়ার্কের মাধ্যমে সার্ভার থেকে ক্লায়েন্টের কম্পিউটারে ফন্ট স্থানান্তরের লেটেন্সি কমাতে লক্ষ্য করা বিন্যাস। বেশ কিছু টুল উপলব্ধ রয়েছে যা WOFF ফাইলগুলিকে TTF এবং অন্যান্য ফন্ট ফাইল ফর্ম্যাটে রূপান্তর করতে পারে।

## WOFF ফাইল ফরম্যাট

WOFF ফন্ট ফরম্যাট বিভিন্ন ফন্টের ধরন যেমন TrueType, OpenType এবং Open Font Format-এ ব্যবহৃত টেবিল-ভিত্তিক sfnt কাঠামোর ফন্ট ডেটা টেবিলকে সংকুচিত করে। এটি এই ধরনের ফন্টের জন্য একটি পাত্রের মতো এবং এতে ফন্টের মেটাডেটা এবং ব্যক্তিগত-ব্যবহারের ডেটা অন্তর্ভুক্ত করার জন্য কন্টেনারে অন্তর্ভুক্ত করার জায়গা রয়েছে। রূপান্তরকারীরা sfnt ফাইলগুলিকে একটি WOFF ফর্ম্যাট করা ফাইলে ব্যবহার করে এবং ব্যবহারকারী এজেন্টরা ওয়েব ডকুমেন্টের সাথে ব্যবহারের জন্য এনকোড করা ফাইলটি পুনরুদ্ধার করে। উল্লেখ্য যে পুনরুদ্ধার করা ফন্ট ডেটা সব দিক থেকে ইনপুট ফন্ট বিন্যাসের সাথে হুবহু মিলে যায়।

WOFF ফাইল ইউটিলিটিগুলিতে প্রায়শই অতিরিক্ত বৈশিষ্ট্য থাকে যেমন গ্লাইফ সাবসেটিং, বৈধতা বা ফন্ট বৈশিষ্ট্য সংযোজন কিন্তু এটি প্রয়োজনীয় নয়। নির্মাতা এবং ব্যবহারকারী উভয়কেই নিশ্চিত করতে হবে যে অন্তর্নিহিত ফন্ট ডেটার বৈধতা সংরক্ষিত আছে।

### WOFF ফাইল স্ট্রাকচার

WOFF ফাইলের গঠন sfnt ফন্টের মতই। এটি একটি টেবিল ডিরেক্টরির উপর ভিত্তি করে যা প্রতিটি ফন্ট ডেটা টেবিলের দৈর্ঘ্য এবং অফসেট ধারণ করে। এই প্রাথমিক তথ্যের পরে সমস্ত টেবিল অনুসরণ করা হয়। ফাইলটিতে ফন্ট ডাটাবেস রয়েছে যা মূল ফন্টগুলির মতোই। টেবিলের ক্রমও একই তবে প্রতিটি সংকুচিত হতে পারে। যদিও WOFF টেবিল ডিরেক্টরি মূল টেবিল ডিরেক্টরি প্রতিস্থাপন করে।

একটি WOFF ফাইল নিম্নলিখিতগুলি নিয়ে গঠিত:

 * WOFFHeader - মৌলিক ফন্ট টাইপ এবং সংস্করণ সহ ফাইল হেডার, মেটাডেটা এবং ব্যক্তিগত ডেটা ব্লকের অফসেট সহ।
 * TableDirectory - ফন্ট টেবিলের ডিরেক্টরি, WOFF ফাইলের মধ্যে প্রতিটি টেবিলের আসল আকার, সংকুচিত আকার এবং অবস্থান নির্দেশ করে।
 * FontTables - ইনপুট sfnt ফন্ট থেকে ফন্ট ডেটা টেবিল, ব্যান্ডউইথের প্রয়োজনীয়তা কমাতে সংকুচিত।
 * এক্সটেন্ডেড মেটাডেটা - এক্সটেন্ডেড মেটাডেটার একটি ঐচ্ছিক ব্লক, XML ফর্ম্যাটে উপস্থাপিত এবং WOFF ফাইলে স্টোরেজের জন্য সংকুচিত।
 * প্রাইভেটডেটা- ফন্ট ডিজাইনার, ফাউন্ড্রি বা বিক্রেতার ব্যবহারের জন্য ব্যক্তিগত ডেটার একটি ঐচ্ছিক ব্লক।

### WOFF হেডার
WOFF শিরোনামটি একটি সনাক্তকারী স্বাক্ষর নিয়ে গঠিত যা ফাইলটিতে অন্তর্ভুক্ত ডেটার প্রকার নির্দেশ করে। WOFF শিরোনাম এবং এর ক্ষেত্রগুলি অনুসরণ করা হয়েছে।

|প্রকার|ক্ষেত্রের নাম|বিবরণ|
---|---|---|
|UInt32|স্বাক্ষর |0x774F4646 'wOFF' |
|UInt32| স্বাদ |ইনপুট ফন্টের sfnt সংস্করণ৷|
|UInt32| দৈর্ঘ্য |WOFF ফাইলের মোট আকার।|
|UInt16| numTables |ফন্ট টেবিলের ডিরেক্টরিতে এন্ট্রির সংখ্যা।|
|UInt16| সংরক্ষিত |সংরক্ষিত; শূন্য সেট.|
|UInt32| totalSfntSize |sfnt শিরোনাম, ডিরেক্টরি এবং ফন্ট টেবিল (প্যাডিং সহ) সহ অসঙ্কোচিত ফন্ট ডেটার জন্য প্রয়োজনীয় মোট আকার।|
|UInt16| majorVersion |WOFF ফাইলের প্রধান সংস্করণ।|
|UInt16| minorVersion |WOFF ফাইলের ছোট সংস্করণ।|
|UInt32| metaOffset |WOFF ফাইলের শুরু থেকে মেটাডেটা ব্লকে অফসেট।|
|UInt32| metaLength |সংকুচিত মেটাডেটা ব্লকের দৈর্ঘ্য।|
|UInt32| metaOrigLength |মেটাডেটা ব্লকের অসংকুচিত আকার।|
|UInt32| privOffset |WOFF ফাইলের শুরু থেকে ব্যক্তিগত ডেটা ব্লকে অফসেট।|
|UInt32| privLength |ব্যক্তিগত ডেটা ব্লকের দৈর্ঘ্য।|

## তথ্যসূত্র

 * [w3 WOFF ফাইল ফরম্যাট](https://www.w3.org/TR/WOFF/)
