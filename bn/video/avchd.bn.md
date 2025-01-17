{
  "date": "2021-14-04",
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "title": "AVCHD ফাইল ফরম্যাট",
  "keywords": [
    "avchd",
    "file",
    "extension",
    "format",
    "video format",
    "what is an avchd file",
    "How to open AVCHD files"
  ],
  "description": "AVCHD ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা তৈরি করতে পারে এবং দেখায় যে কিভাবে AVCHD ফাইল খুলতে হয়।",
  "linktitle": "AVCHD",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-avchd-bn"
    }
  },
  "lastmod": "2021-14-04"
}

## একটি AVCHD ফাইল কি? ##

একটি AVCHD ফাইল হল একটি রেকর্ডিং ফাইল ফরম্যাট যা ডিভিডি, হার্ড ডিস্ক ড্রাইভ এবং মেমরি কার্ডে হাই-ডেফিনিশন (HD) ভিডিও সংরক্ষণ করার জন্য চালু করা হয়েছে। ডিভিডি এবং ব্লু-রেতে রেকর্ড করা AVCHD ভিডিওগুলি বেশিরভাগ ব্লু-রে ডিস্ক প্লেয়ারে সহজেই চালানো যায়। এছাড়াও, AVCHD স্টাফগুলি SD কার্ডে রেকর্ড করা যেতে পারে এবং অনেক ব্লু-রে ডিস্ক প্লেয়ার, টেলিভিশন সেট এবং মিডিয়া কনসোল দ্বারা প্লে করা যেতে পারে। **ffdshow tryouts** এবং **Libavcodec** হল ওপেন-সোর্স কোডেক যা AVCHD ফাইলগুলিকে ডিকোড করতে পারে।


## AVCHD ফাইল ফরম্যাট

AVCHD ফাইল ফরম্যাট হাই-ডেফিনেশন ডিজিটাল ভিডিও ক্যামেরাকে HD সিগন্যাল রেকর্ড করতে দেয়; উচ্চ-দক্ষ কম্প্রেশন কোডিং প্রযুক্তি ব্যবহার করে। ভিডিও সংকুচিত করতে; [MPEG-4](/video/mp4/) AVC/[H.264](/video/h264/) ফর্ম্যাট গৃহীত হয়েছে, এবং ডলবি ডিজিটাল® অডিও ডেটা সংকুচিত করতে ব্যবহৃত হয়। যেখানে, MPEG-4 AVC/H.264 ফরম্যাট প্রচলিত ইমেজ কম্প্রেসিং ফরম্যাটের চেয়ে বেশি দক্ষ। অধিকন্তু, 3D (MVC ফরম্যাট) এবং 1080/60p(1080/50p) ভিডিও ফরম্যাটগুলি AVCHD ফাইল ফরম্যাটে এর সংস্করণ 2.0 (AVCHD 3D, AVCHD প্রগ্রেসিভ) ফরম্যাটের জন্য একটি এক্সটেনশন হিসাবে যুক্ত করা হয়েছে।
অনুগ্রহ করে মনে রাখবেন যে AVCHD V. 2.0 সম্পর্কিত ভিডিওগুলি পরিচালনা করতে একটি ডিভাইস অবশ্যই AVCHD V. 2.0 এর সাথে সামঞ্জস্যপূর্ণ হতে হবে৷

## AVCHD এবং MP4 ফাইল ফরম্যাটের মধ্যে তুলনা ##

অ্যাডভান্সড ভিডিও কোডেক হাই ডেফিনিশন (AVCHD) ফাইল ফরম্যাটটি ব্লু-রে ডিস্ক® রেকর্ডিং তৈরি এবং একটি HDTV দেখার জন্য উপযুক্ত। তুলনায়, MP4 পোর্টেবল ডিভাইসে চালানো অনেক সহজ এবং ওয়েবে সরানো, অনুলিপি করা এবং সংরক্ষণ করাও সহজ।

উভয় ফরম্যাটের পার্থক্য নীচের টেবিলে দেওয়া হয়েছে:

|স্পেসিফিকেশন |AVCHD|MP4|
|------------|------|----|
| ছবির আকার (আকৃতির অনুপাত) |1920 x 1080/60i, 50i (16:9) 1440 x 1080/60i, 50i (16:9)|1440 x 1080/30p (16:9) 1280 x 720/30p (16:9) 9) 640 x 480/30p (4:3)|
| অডিও চ্যানেল / নমুনা ফ্রিকোয়েন্সি |2 চ্যানেল/48 kHz 5.1 চ্যানেল/48 kHz|2 চ্যানেল/48 kHz.|
| ফাইল এক্সটেনশন |.M2TS|.MP4|
| সামঞ্জস্য|ব্লু-রে ডিস্ক বিন্যাসের সাথে সামঞ্জস্যপূর্ণ|Apple® QuickTime® বিন্যাসের সাথে সামঞ্জস্যপূর্ণ|
| |বিভিন্ন রেকর্ডিং মিডিয়া ডিভাইসের সাথে সামঞ্জস্যপূর্ণ যেমন একটি হার্ড|প্লেস্টেশন নেটওয়ার্ক দ্বারা প্লেস্টেশন® ভিডিও সহ বিভিন্ন রেকর্ডিং মিডিয়া এবং নেটওয়ার্কের সাথে সামঞ্জস্যপূর্ণ|
| |xv.Color প্রযুক্তির সাথে সামঞ্জস্যপূর্ণ|Windows 7 অপারেটিং সিস্টেমের সাথে সামঞ্জস্যপূর্ণ এবং উপরে স্থানীয়ভাবে MP4 সমর্থন করে|
| |Windows® 7 অপারেটিং সিস্টেমের সাথে সামঞ্জস্যপূর্ণ এবং তার উপরে স্থানীয়ভাবে AVCHD সমর্থন করে||


## তথ্যসূত্র ##

- [AVCHD - Wikipedia](https://en.wikipedia.org/wiki/AVCHD)
- [What is the AVCHD format?](https://www.sony.com/electronics/support/articles/00016537)



