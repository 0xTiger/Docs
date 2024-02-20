{
  "date": "2019-10-11",
  "keywords": [
    "gif file",
    "gif file format",
    "what is a gif file",
    "file",
    "gif example",
    "gif file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "GIF - ইমেজ ফাইল ফরম্যাট",
  "description": "GIF ফাইল ফর্ম্যাট এবং APIগুলি সম্পর্কে জানুন যা GIF ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "GIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gif-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি GIF ফাইল কি? ##

একটি জিআইএফ বা গ্রাফিকাল ইন্টারচেঞ্জ ফরম্যাট হল এক ধরণের উচ্চ সংকুচিত চিত্র। Unisys মালিকানাধীন, GIF LZW কম্প্রেশন অ্যালগরিদম ব্যবহার করে যা ছবির গুণমানকে অবনমিত করে না। প্রতিটি ছবির জন্য GIF সাধারণত পিক্সেল প্রতি 8 বিট পর্যন্ত অনুমতি দেয় এবং ছবি জুড়ে 256টি রঙের অনুমতি দেওয়া হয়। একটি [JPEG](/image/jpeg/) চিত্রের বিপরীতে, যা 16 মিলিয়ন রঙ পর্যন্ত প্রদর্শন করতে পারে এবং মোটামুটি মানুষের চোখের সীমা স্পর্শ করে। ইন্টারনেটের আবির্ভাব হওয়ার পরে, জিআইএফগুলি সর্বোত্তম পছন্দ ছিল কারণ তাদের কম ব্যান্ডউইথের প্রয়োজন এবং গ্রাফিক্সের জন্য সামঞ্জস্যপূর্ণ যা রঙের কঠিন অঞ্চলগুলি ব্যবহার করে। একটি অ্যানিমেটেড GIF একটি একক ফাইলে অসংখ্য ছবি বা ফ্রেমকে একত্রিত করে এবং একটি অ্যানিমেটেড ক্লিপ বা একটি ছোট ভিডিও তৈরি করতে একটি ক্রমানুসারে প্রদর্শন করে। প্রতিটি ফ্রেমের জন্য রঙের সীমাবদ্ধতা 256 পর্যন্ত এবং কালার গ্রেডিয়েন্ট সহ অন্যান্য ছবি এবং ফটোগ্রাফগুলি পুনরুত্পাদনের জন্য সবচেয়ে কম উপযুক্ত হতে পারে।

## GIF ফাইল ফরম্যাট ##

ধারণাগতভাবে, GIF ফাইলগুলির একটি নির্দিষ্ট-আকারের গ্রাফিকাল এলাকা থাকে যা শূন্য বা তার বেশি চিত্র দ্বারা ভরা হয়। কিছু GIF ফাইল স্থির আকারের গ্রাফিকাল এলাকা বা ব্লককে সাব-ইমেজে বিভক্ত করে যা অ্যানিমেটেড GIF-এর ক্ষেত্রে অ্যানিমেটেড ফ্রেম হিসেবে কাজ করতে সক্ষম। GIF বিন্যাস বিটম্যাপ ডেটা সংরক্ষণ করতে 1 থেকে 8 বিটের পিক্সেল গভীরতা ব্যবহার করে। আরজিবি কালার মডেল এবং প্যালেট ডেটা সবসময় ইমেজ সংরক্ষণ করতে ব্যবহার করা হয়। সংস্করণের উপর নির্ভর করে, একটি নির্দিষ্ট দৈর্ঘ্যের শিরোনাম (GIF87a বা GIF89a) একটি সাধারণ GIF ফাইলের শুরুকে সংজ্ঞায়িত করে।

বর্তমানে, GIF এর দুটি সংস্করণ: 87a এবং 89a উপলব্ধ। আগেরটি আসল জিআইএফ ফরম্যাট এবং পরেরটি নতুন জিআইএফ ফর্ম্যাট। এই ফাইল বিন্যাসে, ব্লক এবং পিক্সেল মাত্রার বৈশিষ্ট্য একটি নির্দিষ্ট দৈর্ঘ্যের লজিক্যাল স্ক্রিন বর্ণনাকারীতে উল্লেখ করা হয়েছে। একটি গ্লোবাল কালার টেবিলের অস্তিত্ব এবং আকার স্ক্রিন বর্ণনাকারী দ্বারা নির্দিষ্ট করা যেতে পারে, যা উপস্থিত থাকলে আরও বিশদ ট্র্যাক করে। ট্রেলারটি ফাইলের শেষ বাইট যা একটি ASCII সেমিকোলনের একক বাইট ধারণ করে। একটি সাধারণ GIF87a ফাইল বিন্যাস নিম্নরূপ:

### হেডার ###

হেডার ছয় বাইট ধারণ করে এবং ফাইলের ধরন GIF হিসাবে নির্দিষ্ট করতে ব্যবহৃত হয়। যদিও লজিক্যাল স্ক্রিন বর্ণনাকারী প্রকৃত হেডার থেকে আলাদা করা হয় তবুও মাঝে মাঝে এটি দ্বিতীয় শিরোনাম হিসাবে বিবেচিত হয়। একই কাঠামো যা হেডার সংরক্ষণ করতে ব্যবহৃত হয় তা লজিক্যাল স্ক্রীন বর্ণনাকারী সংরক্ষণ করতে পারে। সমস্ত GIF ফাইল 3-বাইটের স্বাক্ষর দিয়ে শুরু হয় এবং একটি শনাক্তকারী হিসাবে GIF অক্ষর ব্যবহার করে। সংস্করণটি আকারে তিন বাইট এবং GIF ফাইলের সংস্করণ ঘোষণা করে।

### লজিক্যাল স্ক্রীন বর্ণনাকারী ###

একটি নির্দিষ্ট দৈর্ঘ্যের চিত্র বর্ণনাকারী জিআইএফ চিত্র তৈরি করার জন্য প্রয়োজনীয় স্ক্রীন এবং রঙের তথ্য নির্দিষ্ট করে। উচ্চতা এবং প্রস্থ ক্ষেত্রগুলি স্ক্রীন রেজোলিউশনের ক্ষুদ্রতম মানকে আবদ্ধ করে, যা চিত্রের ডেটা দেখাতে বাধ্য। যদি ডিসপ্লে ডিভাইসটি নির্দিষ্ট রেজোলিউশন প্রদর্শন করতে অক্ষম হয়, তাহলে চিত্রটি যথাযথভাবে প্রদর্শন করার জন্য স্কেলিং প্রয়োজন হবে। স্ক্রীন এবং কালার ম্যাপ তথ্য নীচের টেবিলের চারটি সাবফিল্ড দ্বারা প্রদর্শিত হয় (যেখানে বিট 0 হল সর্বনিম্ন উল্লেখযোগ্য বিট):


|বিটস|সাবফিল্ড
---|---|
|0-2|গ্লোবাল কালার টেবিলের আকার
|3|রঙের টেবিল সাজানোর পতাকা
|4-6|কালার রেজোলিউশন
|7|গ্লোবাল কালার টেবিল পতাকা

#### গ্লোবাল কালার টেবিল ####

লজিক্যাল স্ক্রীন বর্ণনাকারীর ঠিক পরে একটি ঐচ্ছিক গ্লোবাল কালার টেবিল স্থাপন করা হয়। এই টেবিলটি চিত্র ডেটার ভিতরে পিক্সেল রঙের ডেটা সূচীতে ম্যাপ করা হয়েছে। গ্লোবাল কালার টেবিলের অনুপস্থিতিতে, GIF ফাইলের প্রতিটি ছবি তার স্থানীয় রঙ ব্যবহার করে। গ্লোবাল এবং স্থানীয় রঙের টেবিল অনুপস্থিত থাকলে একটি ডিফল্ট রঙের টেবিল সরবরাহ করা ভাল। তিন-বাইট ট্রিপলের একটি সিরিজ রঙ টেবিলের উপাদানগুলি রচনা করে। প্রতিটি বাইট একটি RGB রঙের মান চিহ্নিত করে। লাল, সবুজ এবং নীল রঙ প্রতিটি রঙের টেবিল উপাদানের মান হিসাবে ব্যবহৃত হয়। গ্লোবাল কালার টেবিলের এন্ট্রিগুলি সর্বাধিক 256টি এন্ট্রিতে আঘাত করে এবং সর্বদা দুইটির শক্তিতে উপস্থাপন করে।

#### চিত্র ডেটা ####

ইমেজ ডেটা LZW-এনকোডেড ডেটা সহ সাব-এর লিঙ্কযুক্ত-তালিকা দ্বারা অনুসরণ করে আনকোড করা প্রতীকগুলির একটি বাইট সংরক্ষণ করে।

#### লতা ####

ট্রেলার ডেটার একক বাইট প্রতিনিধিত্ব করে যা ফাইলের শেষ অক্ষর। এই বাইটের মান স্থায়ীভাবে 3Bh এবং ডেটা স্ট্রিমের শেষ নির্দিষ্ট করে। প্রতিটি GIF ফাইলের প্রতিটি ফাইলের শেষাংশে ট্রেলার থাকতে হবে।

## তথ্যসূত্র ##

* [GIF ফাইল ফরম্যাট](https://en.wikipedia.org/wiki/GIF)

