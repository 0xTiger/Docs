{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PST - আউটলুক ব্যক্তিগত তথ্য স্টোর ফাইল ফর্ম্যাট",
  "description": "PST ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি PST ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "PST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-pst-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি PST ফাইল কি?

.pst এক্সটেনশন সহ ফাইলগুলি আউটলুক ব্যক্তিগত স্টোরেজ ফাইলগুলিকে প্রতিনিধিত্ব করে (যাকে ব্যক্তিগত স্টোরেজ টেবিলও বলা হয়) যা ব্যবহারকারীর বিভিন্ন তথ্য সঞ্চয় করে। ব্যবহারকারীর তথ্য বিভিন্ন ধরনের ফোল্ডারে সংরক্ষণ করা হয় যার মধ্যে ইমেল, ক্যালেন্ডার আইটেম, নোট, পরিচিতি এবং অন্যান্য ফাইল ফরম্যাট রয়েছে। PST ফাইলগুলি অফলাইনে ইমেল ডেটা সংরক্ষণাগারের জন্য ব্যবহৃত হয় যা পরে লোড করা যায় এবং বিভিন্ন অ্যাপ্লিকেশনে দেখা যায়।

## PST ফাইল ফরম্যাট স্পেসিফিকেশন

PST ফাইল ফরম্যাট [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) Microsoft থেকে বিনামূল্যে এবং অপরিবর্তনীয় বিনামূল্যে পেটেন্ট লাইসেন্স হিসাবে ওপেন স্পেসিফিকেশন প্রতিশ্রুতির মাধ্যমে উপলব্ধ।

### PST ফরম্যাটের প্রকার

PST ফাইল ফরম্যাটগুলি ফাইলের প্রকারের এনকোডিংয়ের উপর ভিত্তি করে দুটি প্রকারে শ্রেণীবদ্ধ করা হয়। ANSI এনকোড করা PST ফাইলগুলি পুরানো ফাইল ফর্ম্যাট এবং শুধুমাত্র Outlook 2002 এবং পূর্ববর্তী সংস্করণগুলি দ্বারা সমর্থিত৷ এই ধরনের ফাইলগুলির সর্বোচ্চ আকার সীমা 2 GB (2^^31^^ বাইট) এবং ইউনিকোড সমর্থন করে না। ইউনিকোড এনকোডিংয়ের উপর ভিত্তি করে একটি আরও আধুনিক ফাইল ফরম্যাট টাইপ, ফাইলের আকারের সীমাবদ্ধতা দূর করে এবং সর্বোচ্চ 50GB ডেটা আকারে পৌঁছাতে পারে।

### PST ফাইল ফরম্যাটের লজিক্যাল অর্গানাইজেশন

PST ফাইল ফরম্যাটের গোড়ায় রয়েছে B-Tree যা ডেটা বাছাই করে রাখে এবং লগারিদমিক সময়ে অনুসন্ধান, অনুক্রমিক অ্যাক্সেস, সন্নিবেশ, মুছে ফেলা ইত্যাদির অনুমতি দেয়। একটি PST ফাইলের সামগ্রিক গঠন তিনটি স্তরে সংগঠিত হয়।

![Logical layers of a PST file](/email/PST-1.png "Logical layers of a PST file")

`নোড ডাটাবেস (NDB) লেয়ার` - নোড ডাটাবেস স্তর একটি PST ফাইলের নিম্ন স্তরে থাকে এবং নোডের ডাটাবেস অন্তর্ভুক্ত করে। এই নোডগুলি আসলে PST ফাইল ফর্ম্যাটের নিম্ন-স্তরের স্টোরেজ সুবিধাগুলিকে উপস্থাপন করে। NDB স্তরে রয়েছে হেডার, ফাইল বরাদ্দ সংক্রান্ত তথ্য, ব্লক, এবং BTrees (Node BTree এবং BTree ব্লক) স্টোরেজের দৃষ্টিকোণ থেকে। এনডিবি লেয়ারের নোড এবং ব্লকগুলি ডেটা বিআইডির মাধ্যমে লিঙ্ক করা হয়েছে যা নোড রেফারেন্সের চারটি বৈশিষ্ট্যের মধ্যে একটি অর্থাৎ এনআইডি (নোড আইডি), প্যারেন্ট এনআইডি, ডেটা বিআইডি (ব্লক বিআইডি) এবং সাবনোড বিআইডি।

`তালিকা, টেবিল এবং প্রপার্টিজ লেয়ার -` LTP লেয়ার NDB-এর উপরে উচ্চ-স্তরের ধারণার যৌক্তিক বোঝার ব্যবস্থা করে। অন্যান্য উপাদানের পাশাপাশি, এলটিপি স্তরে প্রধানত প্রপার্টি কনটেক্সট (পিসি) এবং টেবিল কনটেক্সট (টিসি) রয়েছে। PC হল বৈশিষ্ট্যের একটি সংগ্রহ, যখন TC হল বৈশিষ্ট্যের সংগ্রহের একটি দ্বি-মাত্রিক ম্যাট্রিক্স বনাম এইগুলির উপস্থিতি। PC এবং TC-এর দক্ষ বাস্তবায়ন, LTP স্তর NDB নোডের উপরে নিম্নলিখিত দুটি ধরনের ডেটা স্ট্রাকচার ব্যবহার করে:

* হিপ অন নোড (HN) - একটি নোডের ডেটা স্ট্রীমকে ছোট, পরিবর্তনশীল-আকারের টুকরোগুলিতে উপ-বরাদ্দ করতে সক্ষম করে।

* BTree on Heap (BTH) - BTH ডেটা পিসিগুলির মাধ্যমে অনুসন্ধানের একটি সুবিধাজনক এবং ব্যবহারিক উপায় প্রদান করে, উপরে বর্ণিত, BTH হিসাবে প্রয়োগ করা হয় এবং সেই কারণে এটি একটি HN কাঠামোর ভিতরে তৈরি করে প্রয়োগ করা হয়।


`মেসেজিং লেয়ার -` PST ফাইলগুলির সাথে কাজ করার জন্য উচ্চ স্তরের নিয়ম এবং ব্যবসায়িক যুক্তি এই স্তরে প্রয়োগ করা হয়। এই স্তরটির যৌক্তিক আউটপুট ফোল্ডার অবজেক্ট, মেসেজ অবজেক্ট, অ্যাটাচমেন্ট অবজেক্ট এবং প্রোপার্টি হিসাবে পাওয়া যায় যা LTP এবং NDB স্তরগুলিকে একত্রিত করে সম্ভব হয়েছে। নিয়ম এবং প্রয়োজনীয়তা, যা PST বিষয়বস্তু পরিবর্তন করার সময় অনুসরণ করা প্রয়োজন, এই স্তরে সংজ্ঞায়িত করা হয়েছে।

### PST ফাইল ফরম্যাটের ভৌত সংগঠন

PST ফাইলের ফাইল সংগঠনের উচ্চ স্তর নীচের চিত্রে দেখানো হয়েছে। এটি শুধুমাত্র PST ফাইলের লজিক্যাল উপাদান থেকে বিভিন্ন ধারণার একটি ওভারভিউ।

![Physical organization of the PST file format](/email/PST-2.png "Physical organization of the PST file format")


#### PST হেডার তথ্য

PST ফাইলের HEADER গঠনটি 0 অফসেটে ফাইলের একেবারে শুরুতে অবস্থিত। এটিতে পিএসটি ফাইল সম্পর্কে মেটাডেটা তথ্য এবং উপরে বর্ণিত এনডিবি লেয়ার ডেটা স্ট্রাকচার অ্যাক্সেস করার জন্য রুট তথ্য রয়েছে। PST ফাইল ফরম্যাটের ইউনিকোড এবং ANSI সংস্করণের জন্য HEADER গঠন ভিন্ন।

শিরোনামটি একটি 4-বাইট জাদু শব্দ দিয়ে শুরু হয় **!BDN** বাইট (0x21, 0x42, 0x44, 0x4E) দ্বারা উপস্থাপিত। আরেকটি 2-বাইট ম্যাজিক নম্বর, **SM** (0x53, 0x4D), ফাইলের শুরু থেকে অফসেট 8 এ অবস্থিত। সংস্করণ তথ্য (ANSI বা ইউনিকোড) ফাইলের শুরু থেকে 10 এর অফসেটে রয়েছে। হেক্স মান (0x17) ইউনিকোড পিএসটি ফাইল নির্দিষ্ট করে যখন 0x0E বা 0x0F ANSI ফাইল বিন্যাস উপস্থাপন করে।

|ক্ষেত্র | বর্ণনা
---|---|
|dwMagic (4 বাইট)|{ 0x21, 0x42, 0x44, 0x4E } (!BDN) হতে হবে
|dwCRCPartial (4 বাইট)|wMagicClient (0ffset 0x0008) থেকে শুরু হওয়া 471 বাইট ডেটার 32-বিট CRC মান
|wMagicClient (2 বাইট)|{ 0x53, 0x4D } হতে হবে।
|wVer (2 বাইট)|ফাইল ফরম্যাট সংস্করণ। ফাইলটি একটি ANSI PST ফাইল হলে এই মানটি 14 বা 15 হতে হবে এবং ফাইলটি একটি ইউনিকোড PST ফাইল হলে 23 হতে হবে৷
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. এই নথির উপর ভিত্তি করে একটি নতুন PST ফাইলের নির্মাতাদের এই মানটি 19-এ শুরু করা উচিত।
|bPlatformCreate (1 বাইট)|এই মানটি 0x01 এ সেট করা আবশ্যক।
|bPlatformAccess (1 বাইট)|এই মানটি 0x01 এ সেট করা আবশ্যক।
|dwReserved (8 বাইট)|
|bidUused (শুধুমাত্র 8 বাইট ইউনিকোড)|ইউনিকোড PST ফাইল বিন্যাস তৈরি করার সময় অব্যবহৃত প্যাডিং যোগ করা হয়েছে।
|bidNextP (ইউনিকোড: 8 বাইট; ANSI: 4 বাইট)|পরবর্তী পৃষ্ঠা বিআইডি। বিড ইনডেক্স মান বরাদ্দ করার জন্য পৃষ্ঠাগুলির একটি বিশেষ কাউন্টার রয়েছে। পৃষ্ঠাগুলির জন্য বিআইডিগুলির জন্য বিডইনডেক্সের মান এই কাউন্টার থেকে বরাদ্দ করা হয়।
|bidNextB     (4 bytes ANSI only): |Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. আরো বিস্তারিত জানার জন্য, বিভাগ 2.2.2.2 দেখুন।
|dwUnique (4 বাইট)|এটি একটি একঘেয়ে-বর্ধমান মান যা প্রতিবার PST ফাইলের HEADER কাঠামো পরিবর্তন করা হয়। এই মানের কাজ হল একটি অনন্য মান প্রদান করা এবং প্রতিটি শিরোনাম পরিবর্তনের পরে HEADER CRC গুলি আলাদা তা নিশ্চিত করা।
|rgnid[] (128 বাইট)|32টি NID-এর একটি নির্দিষ্ট অ্যারে, প্রতিটি সম্ভাব্য 32টি NID_TYPEগুলির একটির সাথে সম্পর্কিত
|qwUnused (8 বাইট)|অব্যবহৃত স্থান; শূন্য সেট করা আবশ্যক. শুধুমাত্র ইউনিকোড PST ফাইল ফরম্যাট।
|রুট (ইউনিকোড: 72 বাইট; ANSI: 40 বাইট) | একটি রুট গঠন (বিভাগ 2.2.2.5)।
|dwAlign (4 বাইট)|অব্যবহৃত প্রান্তিককরণ বাইট; শূন্য সেট করা আবশ্যক. শুধুমাত্র ইউনিকোড PST ফাইল ফরম্যাট।
|rgbFM (128 বাইট)|অপ্রচলিত FMap. এটি আর ব্যবহার করা হয় না এবং 0xFF দিয়ে পূরণ করা আবশ্যক৷ পাঠকদের এই বাইটের মান উপেক্ষা করা উচিত।
|rgbFP (128 বাইট)|অপ্রচলিত FPMap। এটি আর ব্যবহার করা হয় না এবং 0xFF দিয়ে পূরণ করা আবশ্যক৷ পাঠকদের এই বাইটের মান উপেক্ষা করা উচিত।
|bSentinel (1 বাইট)| অবশ্যই 0x80 এ সেট করতে হবে।
|bCryptMethod (1 বাইট)|পিএসটি ফাইলের মধ্যে ডেটা কীভাবে এনকোড করা হয় তা নির্দেশ করে। পূর্ব-নির্ধারিত মানগুলির একটিতে সেট করা আবশ্যক (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC)৷
|rgb সংরক্ষিত (2 বাইট)| সংরক্ষিত; শূন্য সেট করা আবশ্যক.
|bidNextB (8 বাইট)| পরবর্তী উপলব্ধ BID মান নির্দেশ করে। শুধুমাত্র ইউনিকোড PST ফাইল ফরম্যাট।
|bidNextB     (Unicode ONLY: 8 bytes)|Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. আরো বিস্তারিত জানার জন্য, বিভাগ 2.2.2.2 দেখুন।
|dwCRCFull (4 বাইট)|wMagicClient থেকে শুরু করে bidNextB পর্যন্ত 516 বাইট ডেটার 32-বিট CRC মান, অন্তর্ভুক্ত। শুধুমাত্র ইউনিকোড PST ফাইল ফরম্যাট।
|ullReserved (8 বাইট)|সংরক্ষিত; শূন্য সেট করা আবশ্যক. শুধুমাত্র ANSI PST ফাইল ফরম্যাট।
|dwReserved (4 বাইট)|সংরক্ষিত; শূন্য সেট করা আবশ্যক. শুধুমাত্র ANSI PST ফাইল ফরম্যাট।
|rgbReserved2 (3 বাইট)|
|b সংরক্ষিত (1 বাইট) |
|rgbReserved3 (32 বাইট) |

### তথ্য সুরক্ষা ###

নিরাপত্তার জন্য, PST ফাইলগুলিও পাসওয়ার্ড সুরক্ষিত হতে পারে যার জন্য লোডিং অ্যাপ্লিকেশনের পাসওয়ার্ডটি দেখার আগে প্রয়োগ করতে হয়। PST ফাইলে প্রয়োগ করা পাসওয়ার্ড মেসেজ স্টোরে সংরক্ষণ করা হয়। যাইহোক, এটি শক্তিশালী ডেটা সুরক্ষা প্রদান করে না কারণ উপলব্ধ সরঞ্জামগুলি দ্বারা পাসওয়ার্ড সরানো যেতে পারে। এছাড়াও, সাইফার অ্যালগরিদম এনকোডিং এবং ডিকোডিংয়ের জন্য ব্যবহারকারীর নির্দিষ্ট পাসওয়ার্ড কী-এর অংশ হিসেবে ব্যবহার করা হয় না। সুতরাং, অ-অনুমোদিত পক্ষগুলি দ্বারা অ্যাক্সেস করা ডেটা সুরক্ষিত করার কোন সুবিধা নেই। মূল স্ট্রিং-এর CRC-32 হ্যাশ হিসাবে পাসওয়ার্ডের স্টোরেজ এটিকে ব্রুট-ফোর্স পদ্ধতির বিরুদ্ধে ডেটা সুরক্ষার জন্য একটি দুর্বল পদ্ধতিতে পরিণত করে।

## তথ্যসূত্র ##

* [আউটলুক পার্সোনাল ফোল্ডার (.pst) ফাইল ফরম্যাট](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [পার্সোনাল ফোল্ডার ফাইল ফরম্যাট স্পেসিফিকেশন](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

