{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSR ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি OSR ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "OSR ফাইল - osu! রিপ্লে ফাইল ফরম্যাট",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-bn",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## একটি OSR ফাইল কি?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**ওএসআর ফাইল ফরম্যাটের MIME প্রকার:** x-osu-রিপ্লে

## OSR ফাইল ফরম্যাট

OSR ফাইলগুলি স্থির এবং পরিবর্তনশীল দৈর্ঘ্যের ডেটা ক্ষেত্রগুলির সাথে বাইনারি ফাইল হিসাবে সংরক্ষণ করা হয়।

|ডেটা টাইপ| বিন্যাস|
---|---|
|বাইট |রিপ্লের গেম মোড (0 = ওসু! স্ট্যান্ডার্ড, 1 = তাইকো, 2 = ক্যাচ দ্য বিট, 3 = ওসু! ম্যানিয়া)|
|পূর্ণসংখ্যা
|স্ট্রিং |ওসু! বিটম্যাপ MD5 হ্যাশ|
|স্ট্রিং| প্লেয়ারের নাম|
|স্ট্রিং| ওসু রিপ্লে MD5 হ্যাশ (রিপ্লে এর কিছু বৈশিষ্ট্য অন্তর্ভুক্ত)|
|সংক্ষিপ্ত | 300 এর সংখ্যা|
|সংক্ষিপ্ত | স্ট্যান্ডার্ডে 100 এর সংখ্যা, তাইকোতে 150, সিটিবিতে 100, ম্যানিয়াতে 100
|সংক্ষিপ্ত | স্ট্যান্ডার্ডে ৫০ সেকেন্ড, সিটিবিতে ছোট ফল, ম্যানিয়ায় ৫০ সেকেন্ড|
|সংক্ষিপ্ত | স্ট্যান্ডার্ডে গেকিসের সংখ্যা, ম্যানিয়াতে সর্বাধিক 300s|
|সংক্ষিপ্ত | স্ট্যান্ডার্ডে কাটুসের সংখ্যা, ম্যানিয়ায় 200
|সংক্ষিপ্ত | মিস সংখ্যা|
|পূর্ণসংখ্যা | স্কোর রিপোর্টে প্রদর্শিত মোট স্কোর|
|সংক্ষিপ্ত | স্কোর রিপোর্টে প্রদর্শিত সর্বশ্রেষ্ঠ কম্বো|
|বাইট| নিখুঁত/পূর্ণ কম্বো (1 = কোন মিস এবং কোন স্লাইডার বিরতি এবং কোন প্রাথমিক সমাপ্ত স্লাইডার নেই)|
|পূর্ণসংখ্যা | মোড ব্যবহার করা হয়েছে। মোড মানগুলির তালিকার জন্য নীচে দেখুন
|স্ট্রিং| লাইফ বার গ্রাফ: কমা বিভক্ত জোড়া u/v, যেখানে u হল গানের মিলিসেকেন্ডে সময় এবং v হল 0 - 1 থেকে একটি ফ্লোটিং পয়েন্ট মান যা প্রদত্ত সময়ে আপনার জীবনের পরিমাণকে প্রতিনিধিত্ব করে (0 = লাইফ বার হল খালি, 1 = জীবন বার পূর্ণ)|
|দীর্ঘ| টাইম স্ট্যাম্প (উইন্ডোজ টিক)|
|পূর্ণসংখ্যা | সংকুচিত রিপ্লে ডেটার বাইটে দৈর্ঘ্য|
|বাইট |অ্যারে সংকুচিত রিপ্লে ডেটা|
|দীর্ঘ| অনলাইন স্কোর আইডি|
|ডাবল | অতিরিক্ত মোড তথ্য। টার্গেট প্র্যাকটিস সক্ষম হলেই উপস্থিত।|

## তথ্যসূত্র

* [ওএসইউ! রিদম গেম](https://osu.ppy.sh/home)

* [OSR ফাইল ফরম্যাট](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)

