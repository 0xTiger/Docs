{
  "date": "2021-04-08",
  "keywords": [
    "dar file",
    "dar file format",
    "what is a dar file",
    "file",
    "dar example",
    "dar file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DAR - ডিস্ক আর্কাইভার ফাইল ফরম্যাট",
  "description": "DAR ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি DAR ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "DAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-dar-bn"
    }
  },
  "lastmod": "2021-04-09"
}

## একটি DAR ফাইল কি?

.dar এক্সটেনশন সহ একটি ফাইল হল একটি সংকুচিত সংরক্ষণাগার যা DAR ডিস্ক সংরক্ষণাগার ব্যবহার করে তৈরি করা হয়। এটি সম্পূর্ণ ডিস্ক বা ফাইলগুলির একটি গ্রুপের জন্য ব্যাকআপ/আর্কাইভ তৈরি করতে পারে। এটি UNIX OS-এ [TAR](/compression/tar/) ফাইল বিন্যাস প্রতিস্থাপন করার জন্য তৈরি করা হয়েছে এবং প্রচুর সংখ্যক ফাইলের জন্য বিভক্ত সংরক্ষণাগার ফাইল হিসাবে তৈরি করা যেতে পারে। DAR আর্কাইভ সিস্টেম থেকে ফাইল মুছে ফেলার বিকল্প সমর্থন করে যা আর্কাইভের প্রধান ফাইলগুলির সাথে লিঙ্ক করা আছে। এর ডিফারেনশিয়াল, ইনক্রিমেন্টাল এবং ডিক্রিমেন্টাল ব্যাকআপ প্রদানের ক্ষমতা এটিকে TAR ফাইলের চেয়ে উন্নত করে তোলে।

## DAR ফাইল ফরম্যাট

DAR ফাইল হল সংকুচিত আর্কাইভ যা যেকোনো ফাইল প্রতি কম্প্রেশন যেমন [gzip](/compression/gz/), [bzip2](/compression/bz2/), lzo, xz বা lzma ব্যবহার করতে পারে। একটি DAR ফাইলের সঠিক ফাইল বিন্যাস নির্ভর করে সংরক্ষণাগারের বিষয়বস্তু সংকুচিত করতে কোন ধরনের বিন্যাস ব্যবহার করা হয় তার উপর। এটি ঐচ্ছিক ব্লোফিশ, টুফিশ, এইএস, সর্পেন্ট, ক্যামেলিয়া এনক্রিপশন এবং পাবলিক কী এনক্রিপশন এবং স্বাক্ষর (ওপেনপিজিপি) অনুমতি দেয়।

### DAR বৈশিষ্ট্য

DAR ফাইল ফরম্যাটের কিছু বৈশিষ্ট্য নিম্নরূপ।

 * যেকোনো ধরনের ইনোডের যত্ন নেয় (ডিরেক্টরি, প্লেইন ফাইল, সিমলিঙ্ক, বিশেষ ডিভাইস, নামযুক্ত পাইপ, সকেট, দরজা, ...)
 * হার্ড-লিঙ্কড ইনোডের যত্ন নেয় (হার্ড-লিঙ্কড প্লেইন ফাইল, চার ডিভাইস, ব্লক ডিভাইস, হার্ড-লিঙ্কড সিমলিঙ্ক)
 * স্পার্স ফাইলের যত্ন নেয়
 * লিনাক্স ফাইল এক্সটেন্ডেড অ্যাট্রিবিউটের যত্ন নেয়,
 * লিনাক্স ফাইল ACL এর যত্ন নেয়
 * Mac OS X ফাইল ফর্কের যত্ন নেয়
 * HFS+ ফাইলসিস্টেমের জন্মতারিখ এবং অপরিবর্তনীয়, ডেটা-জার্নালিং, সুরক্ষিত-মোছা, নো-টেল-মার্জিং, আনডিলিটেবল, ext2/3/4 ফাইল সিস্টেমের নোয়াটাইম বৈশিষ্ট্যের মতো কিছু ফাইল সিস্টেম নির্দিষ্ট বৈশিষ্ট্যের যত্ন নেয়।
 * Gzip, bzip2, lzo, xz বা lzma সহ প্রতি-ফাইল কম্প্রেশন (পুরো সংরক্ষণাগার সংকুচিত করার বিপরীতে)। একজন ব্যক্তি তাদের ফাইলের নাম প্রত্যয়ের উপর ভিত্তি করে ইতিমধ্যে সংকুচিত ফাইলগুলিকে সংকুচিত না করা বেছে নিতে পারেন।
 * আর্কাইভের যেকোনো জায়গা থেকে ফাইল দ্রুত-নিষ্কাশন
 * সংরক্ষণাগারে ফাইলের ক্যাটালগ সংরক্ষণের মাধ্যমে সংরক্ষণাগার বিষয়বস্তুর দ্রুত তালিকা
 * লাইভ ফাইল সিস্টেম ব্যাকআপ: ব্যাকআপের জন্য পড়ার সময় একটি ফাইল কখন পরিবর্তন করা হয়েছে তা সনাক্ত করে এবং একটি প্রদত্ত সর্বাধিক সংখ্যক পুনঃপ্রচারে এটি সংরক্ষণ করার পুনরায় চেষ্টা করতে পারে
 * হ্যাশ ফাইল (MD5, SHA1 বা SHA-512) প্রতিটি স্লাইসের জন্য অন-ফ্লাই তৈরি করা হয়েছে, ফলস্বরূপ ফাইলটি md5sum বা sha1sum-এর সাথে সামঞ্জস্যপূর্ণ, প্রতিটি স্লাইসের অখণ্ডতা দ্রুত পরীক্ষা করতে সক্ষম হবে
 * ফাইল সিস্টেম স্বাধীন: এটি একটি সিস্টেমকে একটি ভিন্ন আকারের পার্টিশনে এবং/অথবা একটি ভিন্ন ফাইল সিস্টেমের সাথে একটি পার্টিশনে পুনরুদ্ধার করতে ব্যবহার করা যেতে পারে[5]

## তথ্যসূত্র

* [DAR](http://dar.linux.free.fr/)

* [DAR ডিস্ক আর্কিভার](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

