{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ISO - ডিস্ক ইমেজ ফাইল ফরম্যাট",
  "description":"একটি ISO ফাইল এবং APIগুলি কী যা ISO ফাইলগুলি তৈরি এবং খুলতে পারে।",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso-bn",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## একটি ISO ফাইল কি?

.iso এক্সটেনশন সহ একটি ফাইল হল একটি সংকুচিত আর্কাইভ ডিস্ক ইমেজ ফাইল যা একটি অপটিক্যাল ডিস্ক যেমন সিডি বা ডিভিডিতে সমগ্র ডেটার বিষয়বস্তু উপস্থাপন করে। [ISO-9660](https://www.iso.org/standard/17505.html) স্ট্যান্ডার্ডের উপর ভিত্তি করে, ISO ইমেজ ফাইল ফরম্যাটে ডিস্ক ডেটা সহ ফাইল সিস্টেমের তথ্য থাকে যা এতে সংরক্ষিত থাকে। আইএসও ফাইলের বিষয়বস্তুর সঠিক প্রতিরূপ ধারণ করার ক্ষমতা এটিকে সিডি/ডিভিডি-র কপি তৈরির জন্য নিখুঁত ফাইল টাইপ করে তোলে এবং বেশিরভাগই ইনস্টলেশনের জন্য বুটেবল ডেটা সংরক্ষণ করতে ব্যবহৃত হয়। বেশিরভাগ সময়, ইনস্টলেশনের জন্য মেশিন বুট করার জন্য বুটযোগ্য বিষয়বস্তু হিসাবে ISO ফাইলগুলি USB/CD/DVD তে বার্ন করা হয়। ISO ফাইলে MIME ধরনের অ্যাপ্লিকেশন/x-iso9660-image আছে।

## ISO ফাইল ফরম্যাট

ISO ফাইল ফরম্যাট অন্যান্য কনটেইনার ফাইল ফাইল ফরম্যাটের মতো নয় যদিও এটি ডেটার নির্দিষ্ট বিষয়বস্তু সংরক্ষণ করে। আর্কাইভটি একটি বাইনারি ফাইল হিসাবে তৈরি করা হয়েছে বিষয়বস্তু এবং ফাইল সিস্টেমের তথ্যের সঠিক কাঠামোর সাথে। ISO ফাইলের বিন্যাসটিকে [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) দ্বারা অনুসরণ করা হয়েছে৷

### ISO ফাইলের টপ লেভেল স্ট্রাকচার

ফাইলের সামগ্রিক কাঠামোর মধ্যে রয়েছে:

 * সিস্টেম এলাকা' - 32,768 বাইট এবং ISO_9660 দ্বারা অব্যবহৃত
 * `ডেটা এরিয়া` - ভলিউম বর্ণনাকারী সেট এবং পাথ টেবিল, ডিরেক্টরি এবং ফাইল নিয়ে গঠিত

### ভলিউম বর্ণনাকারী সেট

ডেটা এলাকাটি ভলিউম বর্ণনাকারী সেট দিয়ে শুরু হয়, এক বা একাধিক ভলিউম বর্ণনাকারীর একটি সেট একটি ভলিউম বর্ণনাকারী সেট টার্মিনেটরের সাথে সমাপ্ত হয়। এগুলি সম্মিলিতভাবে ডেটা এলাকার জন্য একটি শিরোনাম হিসাবে কাজ করে, এর বিষয়বস্তু বর্ণনা করে (FAT, HPFS এবং NTFS ফরম্যাটেড ডিস্ক দ্বারা ব্যবহৃত BIOS প্যারামিটার ব্লকের অনুরূপ)।

একটি ভলিউম বর্ণনাকারী সেট নীচে দেখানো হয়েছে.

|ভলিউম বর্ণনাকারী সেট|
---|
|ভলিউম বর্ণনাকারী #1|
|...|
|ভলিউম বর্ণনাকারী #N|
|ভলিউম বর্ণনাকারী সেট টার্মিনেটর|

#### ভলিউম বর্ণনাকারী

প্রতিটি ভলিউম বর্ণনাকারীর আকার 2048 বাইট এবং নিম্নলিখিত কাঠামো রয়েছে:

|পার্ট |টাইপ |আইডেন্টিফায়ার |সংস্করণ |ডেটা |
---|---|---|---|---|
|আকার |1 বাইট |5 বাইট (সর্বদা 'CD001') |1 বাইট (সর্বদা 0x01) |2,041 বাইট |

## তথ্যসূত্র

* [অপটিক্যাল ডিস্ক ইমেজ - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Optical_disc_image)

* [ফাইল স্বাক্ষর](https://www.garykessler.net/library/file_sigs.html)

* [ISO 9660 - উইকিপিডিয়া](https://en.wikipedia.org/wiki/ISO_9660)


