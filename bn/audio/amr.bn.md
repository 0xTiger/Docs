{
  "date": "2021-04-29",
  "keywords": [
    "amr",
    ".amr",
    "file",
    "extension",
    "format",
    "what is an amr file",
    "music",
    "amr file format",
    "amr file",
    "convert amr file to mp3",
    "play amr file"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "AMR ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি AMR ফাইল তৈরি, রূপান্তর এবং খুলতে পারে।",
  "title": "AMR - অভিযোজিত মাল্টি-রেট কোডেক ফাইল",
  "linktitle": "AMR",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-amr-bn"
    }
  },
  "lastmod": "2021-04-29"
}

## একটি AMR ফাইল কি?
.amr এক্সটেনশন সহ ফাইলটি একটি অডিও ডেটা ফরম্যাট যা **অ্যাডাপ্টিভ মাল্টি-রেট** অডিও কোডেকের সাথে প্রাসঙ্গিক; একটি মাল্টি-রেট ন্যারোব্যান্ড স্পিচ কোডেক রয়েছে যা 4.75-12.2 kbit/s বিট রেটে ন্যারোব্যান্ড সিগন্যাল এনকোড করে এবং টোল কোয়ালিটি স্পিচ 7.4 kbit/s থেকে শুরু হয়; আটটি ভিন্ন বিট রেট ভিত্তিক একটি থেকে নির্বাচন করতে লিঙ্ক অভিযোজন ব্যবহার করে।

## AMR ফাইল ফরম্যাট
AMR file format uses many coding techniques, the ACELP (Algebraic Code Excited Linear Prediction) algorithm one of the best technique; designed for compressing human spoken audio in a more efficient way. The AMR was set as the standard voice or speech codec by 3GPP in 1999. AMR ফাইল ফরম্যাটটি **অ্যাডাপ্টিভ মাল্টি-রেট** অডিও কোডেক ব্যবহার করে কথ্য অডিও সংরক্ষণ করতে ব্যবহৃত হয় যা অনেক স্মার্ট ফোনে রেকর্ড করা বক্তৃতা সংরক্ষণ করতে ব্যবহৃত হয়।

### ফাইল ফরম্যাটের গঠন
এএমআর (অ্যাডাপ্টিভ মাল্টি-রেট) একটি অডিও ফরম্যাট; বিভিন্ন মোবাইল অ্যাপ্লিকেশন এবং ডিভাইসে ব্যাপকভাবে ব্যবহৃত হয়, সাধারণত অডিও প্লেয়ার/রেকর্ডারে বা ভিওআইপি ধরনের অ্যাপ্লিকেশনে। AMR আরও শ্রেণীবদ্ধ করা যেতে পারে:

1. AMR-NB ( ন্যারোব্যান্ড )
2. AMR-WB (ওয়াইডব্যান্ড)

সাধারণত, AMR বলতে AMR-NB বোঝায়। এএমআর ফাইল ফরম্যাটের নিম্নলিখিত কাঠামো রয়েছে:

প্রতিটি AMR ফাইলে একটি 6-বাইট শিরোনাম রয়েছে যা ফাইলটিকে একটি AMR অডিও হিসেবে স্বীকৃতি দেয়। এই শিরোনাম সবসময় সেট করা হয়:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

এটি সাধারণত সমস্ত AMR-NB ফাইল জুড়ে থাকে। যদি শিরোনামটি একটি মান অনুসরণ করে, তাহলে সম্ভবত ফাইলটি নষ্ট হয়ে গেছে এবং এটি ব্যবহার করা উচিত নয়। AMR ফাইলে অডিওর পুরো সংখ্যক প্যাক করা ফ্রেম থাকে। এই ফ্রেম প্রতিটি 20ms অডিও রচনা. প্রতিটি ফ্রেম বৈধ AMR-NB মোড (0-7, DTX মোডে 8 SID) ব্যবহার করে এনকোড করা যেতে পারে। যেহেতু, ফ্রেমগুলিকে বিভিন্ন বিট হারে এনকোড করা যেতে পারে, এই সাধারণ পদ্ধতিটিকে অভিযোজিত মাল্টি-রেট (AMR) বলা হয়।
#### AMR মোড
নিম্নলিখিত বিভিন্ন AMR মোড এবং তাদের সংশ্লিষ্ট বিটরেটগুলি রয়েছে:

|মোড| বিট রেট|
---|---|
|0| AMR 4.75 - 4.75kbit/s| এ এনকোড করে
|1 | AMR 5.15 - 5.15kbit/s| এ এনকোড করে
|2 | AMR 5.9 - 5.9kbit/s| এ এনকোড করে
|3 | AMR 6.7 - 6.7kbit/s| এ এনকোড করে
|4 | AMR 7.4 - 7.4kbit/s| এ এনকোড করে
|5 | AMR 7.95 - 7.95kbit/s| এ এনকোড করে
|6 | AMR 10.2 - 10.2kbit/s| এ এনকোড করে
|7 | AMR 12.2 - 12.2kbit/s| এ এনকোড করে

বাইটে AMR মোডের ফ্রেমের আকার (হেডার বাইট সহ) নিচে দেওয়া হল:

|CMR |মোড |FRAME SIZE(বাইটে)|
---|---|---|
|0 |AMR 4.75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7.95 |21|

## তথ্যসূত্র ##

* [অ্যাডাপ্টিভ মাল্টি-রেট অডিও কোডেক - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)

* [আরটিপি পেলোড ফর্ম্যাট এবং এএমআর এবং এএমআর-ডব্লিউবি অডিও কোডেকগুলির জন্য ফাইল স্টোরেজ ফর্ম্যাট](https://tools.ietf.org/html/rfc4867#page-35)


