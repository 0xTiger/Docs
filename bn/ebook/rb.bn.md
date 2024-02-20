{
  "date": "2021-03-08",
  "keywords": [
    "RB",
    "Nuvo Media’s Rocket eBook device",
    "file",
    "extension",
    "format",
    "eBook"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "নুভো মিডিয়ার রকেট ইবুক ডিভাইস এবং এপিআইগুলির জন্য RB ফাইল বিন্যাস সম্পর্কে জানুন যা RB ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "title": "আরবি - রকেট ইবুক ফাইল",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-rb-bn"
    }
  },
  "lastmod": "2021-03-08"
}

## একটি RB ফাইল কি?

The file with extension .rb holds the Rocket eBook content. The Rocket eBook is actually a device made by Nuvo Media; they released this device in 1998. যদিও রকেট ইবুক ইমেজ প্রদর্শন করতে সক্ষম, কিন্তু শুধুমাত্র কালো এবং সাদা ডিসপ্লেতে। এটির একটি 4.5 x 3-ইঞ্চি টাচ স্ক্রিনে 106 dpi বা 480 x 320 পিক্সেলের একটি স্ক্রিন রয়েছে। রকেট ইবুক আরবি ফাইল ফরম্যাটে ইবুক ডাউনলোড করতে সিরিয়াল পোর্ট সংযোগের মাধ্যমে একটি কম্পিউটারের সাথে সংযোগ করে। RB ফাইলগুলি DRM ব্যবহার করতে সক্ষম কিন্তু এই প্রযুক্তিটি আধুনিক ইবুকগুলিতে ব্যবহার করা হচ্ছে না। RB ফাইলে প্রচলিতভাবে ছবিসহ একটি HTML ফাইল এবং সমস্ত মেটাডেটা (.info) সহ একটি ছদ্ম-OPF ফাইল থাকে।

## আরবি ফাইল ফরম্যাটের প্রযুক্তিগত স্পেসিফিকেশন ##

ফাইলের প্রথম 4 বাইটে একটি ম্যাজিক সংখ্যা (হেক্সে) প্রদর্শিত হয়: B0 0C B0 0C।

দেখা যাচ্ছে যে পরবর্তী দুটি বাইট একটি সংস্করণ নম্বর, যেমন 02 00, যা প্রধান সংস্করণ 2 এবং ছোট সংস্করণ 0 এর জন্য দাঁড়ায়।

পরবর্তী চারটি বাইটে NUVO পাঠ্য রয়েছে, তারপরে 00h এর 4 বাইট রয়েছে।

The next 4-byte is the date when the book was created, encoded as an int16. এটি আমাদের অফসেট 0Eh এ রাখে। ORocketLibrary-এর পুরানো সংস্করণটি বছরের সম্পূর্ণ মান এনকোড করেছে (অর্থাৎ, 1999 ছিল CF 07, 2000 ছিল D0 07)। সাম্প্রতিক সংস্করণে, tm_year শব্দার্থে সংরক্ষিত হয়, অর্থাৎ 2000 সালের জন্য 100 (64 00)। বছরের পরে একটি int8 আসে যা 1-আপেক্ষিক মাসের সংখ্যাকে প্রতিনিধিত্ব করে এবং একটি int8 মাসের দিনকে প্রতিনিধিত্ব করে।

পরবর্তী 6 বাইট হল 00h. সময় নির্ধারণের জন্য, এগুলি সংরক্ষিত হতে পারে।

বিষয়বস্তুর সারণী এর পরম অফসেট অফসেট 18h-এ একটি int32-এ রয়েছে৷

এর পরে .rb ফাইলের দৈর্ঘ্য ধারণকারী একটি int32। এটি ফাইলগুলি সম্পূর্ণ কিনা তা নির্ধারণ করতে ব্যবহৃত হয়।

বাইটের এই পুরো অংশটি (20h থেকে 128h) শুধুমাত্র এনক্রিপ্ট করা শিরোনামের জন্য প্রয়োজন বলে মনে হয়। নন-এনক্রিপ্টেড শিরোনামে, তারা সবসময় শূন্য।

বেশিরভাগ ক্ষেত্রে, বিষয়বস্তুর সারণী অনুসরণ করে (অফসেট 128 এ)। এটি ToC-তে পৃষ্ঠা এন্ট্রির (.rb-ফাইল বিভাগ) সংখ্যার একটি int32 গণনা দিয়ে শুরু হয়। প্রতিটি এন্ট্রিতে একটি নাম থাকে (শূন্য-প্যাডেড থেকে 32 বাইট), তারপরে 3 int32s: ডেটা সেগমেন্টের দৈর্ঘ্য, .rb ফাইলের অবস্থান এবং এই এন্ট্রির জন্য একটি পতাকা। আজকের হিসাবে, পরিচিত মানগুলি হল: 1 (এনক্রিপ্ট করা), 2 (তথ্য পৃষ্ঠা), এবং 8 (ডিফ্লেটেড)। নামগুলো সবগুলোই ইউনিক তা নিশ্চিত করার জন্য প্রয়োজন অনুযায়ী তৈরি করা হয়েছে।

## তথ্যসূত্র

* [ই-রিডার - মোবাইলরিড দ্বারা](https://en.wikipedia.org/wiki/E-reader)

