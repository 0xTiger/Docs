{
  "date": "2019-10-11",
  "keywords": [
    "wmf file",
    "wmf file format",
    "what is a wmf file",
    "file",
    "wmf example",
    "wmf file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "WMF - মাইক্রোসফট উইন্ডোজ মেটাফাইল ফরম্যাট",
  "description": "WMF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি WMF ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "WMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-wmf-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি WMF ফাইল কি?

WMF এক্সটেনশন সহ ফাইলগুলি ভেক্টরের পাশাপাশি বিটম্যাপ-ফরম্যাট ইমেজ ডেটা সংরক্ষণের জন্য Microsoft Windows মেটাফাইল (WMF) প্রতিনিধিত্ব করে। আরও সঠিক হতে, WMF গ্রাফিক্স ফাইল ফরম্যাটের ভেক্টর ফাইল ফরম্যাট বিভাগের অন্তর্গত যা ডিভাইস স্বাধীন। উইন্ডোজ গ্রাফিক্যাল ডিভাইস ইন্টারফেস (জিডিআই) পর্দায় একটি চিত্র প্রদর্শন করতে একটি WMF ফাইলে সংরক্ষিত ফাংশন ব্যবহার করে। WMF-এর আরও উন্নত সংস্করণ, যা এনহ্যান্সড মেটা ফাইল (EMF) নামে পরিচিত, পরে প্রকাশিত হয়েছিল যা ফরম্যাটটিকে আরও সমৃদ্ধ করে তোলে। কার্যত, WMF SVG এর অনুরূপ।

## WMF ফাইল ফরম্যাট স্পেসিফিকেশন ##

A WMF file referred to 16-bit file format at the time of its launching with Windows 3.0. ফাইল ফরম্যাটে ভেরিয়েবল-দৈর্ঘ্যের রেকর্ডের একটি সিরিজ রয়েছে যা গ্রাফিক্স অঙ্কন কমান্ড, বস্তুর সংজ্ঞা এবং বৈশিষ্ট্য ধারণ করে। যেহেতু WMF ফাইলগুলি GDI-কে ইমেজ আঁকার জন্য রেন্ডার করা কমান্ডের উপর ভিত্তি করে তৈরি করা হয়, তাই এটি ইমেজের একটি ডিজিটাল রেকর্ডিং হিসাবেও পরিচিত যা সেই চিত্রটি পুনরুত্পাদন করতে আবার প্লে করা যেতে পারে। WMF এর সম্পূর্ণ ফাইল ফরম্যাট স্পেসিফিকেশন অনলাইনে পাওয়া যায় এবং WMF ফাইলগুলির সাথে কাজ করার জন্য অ্যাপ্লিকেশনগুলির বিকাশের জন্য উল্লেখ করা উচিত। একটি WMF ফাইল একটিতে সংগঠিত হয়:

* WMF হেডার রেকর্ড

* WMF রেকর্ড (গুলি)

* WMF এন্ড-অফ-ফাইল রেকর্ড


### WMF হেডার রেকর্ড ###

**META_HEADER রেকর্ড**-এ এমন তথ্য রয়েছে যা মেটাফাইলের বৈশিষ্ট্যগুলিকে সংজ্ঞায়িত করে, যার মধ্যে রয়েছে:

* মেটাফাইলের ধরন

* মেটাফাইলের সংস্করণ

* মেটাফাইলের আকার

* মেটাফাইলে সংজ্ঞায়িত বস্তুর সংখ্যা

* মেটাফাইলের বৃহত্তম একক রেকর্ডের আকার


### WMF স্থাপনযোগ্য হেডার রেকর্ড ###

**META_PLACEABLE রেকর্ড**-এ ছবি সম্পর্কিত বর্ধিত তথ্য রয়েছে, যার মধ্যে রয়েছে:

* একটি আবদ্ধ আয়তক্ষেত্র

* লজিক্যাল ইউনিট আকার, স্কেলিং জন্য

* একটি চেকসাম, বৈধতার জন্য


### WMF রেকর্ড ###

WMF রেকর্ডগুলির একটি জেনেরিক বিন্যাস রয়েছে, যা স্পেসিফিকেশন নথিতে উল্লেখ করা হয়েছে। প্রতিটি WMF রেকর্ডে নিম্নলিখিত তথ্য রয়েছে:

* রেকর্ড আকার

* রেকর্ড ফাংশন

* রেকর্ড ফাংশনের জন্য পরামিতি, যদি থাকে


## তথ্যসূত্র ##

* [[MS-WMF]: উইন্ডোজ মেটাফাইল ফরম্যাট](https://msdn.microsoft.com/en-us/library/cc250370.aspx)

* [উইন্ডোজ মেটাফাইল - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Windows_Metafile)


