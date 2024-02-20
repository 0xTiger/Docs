{
  "date": "2021-09-08",
  "keywords": [
    "rel file",
    "rel file format",
    "what is a rel file",
    "file",
    "rel example",
    "rel file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "REL ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি REL ফাইল তৈরি এবং খুলতে পারে।",
  "title": "REL - রিলোকেটেবল মডিউল ফাইল",
  "linktitle": "REL",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-rel-bn"
    }
  },
  "lastmod": "2021-09-08"
}

## একটি REL ফাইল কি?
.rel এক্সটেনশন সহ একটি ফাইল বিভিন্ন ধরণের উদ্দেশ্যে ব্যবহার করা যেতে পারে। তাই, গেমের শ্রেণীবিভাগের পরিপ্রেক্ষিতে এটি একটি রিলোকেটেবল মডিউল ফাইল হিসাবে পরিচিত যা কিছু নিন্টেন্ডো উই গেম দ্বারা ব্যবহৃত হয়, যেমন ব্রাউল, সুপার স্ম্যাশ ব্রোস এবং মারিও কার্ট উই। এটি চরিত্রের মডেল এবং পর্যায় সহ গেমপ্লে ডেটা অন্তর্ভুক্ত করে। REL ফাইলগুলি মাইক্রোসফ্ট উইন্ডোজ দ্বারা ব্যবহৃত .DLL ফাইলগুলির অনুরূপ কাজ করে৷

## REL ফাইল বিন্যাস
একটি REL ফাইল ফরম্যাটে, ফাইলটিকে কয়েকটি বিভাগে ভাগ করা হয়, যেমন অ্যাক্সেস দ্বারা গোষ্ঠীবদ্ধ, যেমন একটি বিভাগে শুধুমাত্র ডেটা পড়ুন, সমস্ত এক্সিকিউটেবল কোড অন্যটিতে স্থাপন করা হয় ইত্যাদি। ফাইলটি একটি হেডার বিভাগ দিয়ে শুরু হয়, তারপরে:
- বিভাগ তথ্য ধারণকারী টেবিল.
- বিভাগের তথ্য।
- স্থানান্তরের তথ্য।

### ফাইল হেডার
ফাইলটি 0x4C বাইট পর্যন্ত হেডার দিয়ে শুরু হয়:
| অফসেট | আকার | ক্ষেত্রের নাম | বর্ণনা |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Arbitrary identification number. Must be unique amongst all RELs used by a game. Must not be 0. |
| 0x04 | 4 | পরবর্তী | পরবর্তী মডিউলে নির্দেশক, রানটাইমে পূর্ণ। |
| 0x08 | 4 | পূর্ববর্তী | পূর্ববর্তী মডিউলে নির্দেশক, রানটাইমে ভরা। |
| 0x0c | 4 | সংখ্যা বিভাগ | ফাইলে বিভাগের সংখ্যা। |
| 0x10 | 4 | sectionInfoOffset | বিভাগ টেবিলের শুরুতে অফসেট। |
| 0x14 | 4 | nameOffset | মডিউলের নাম ধারণকারী ASCII স্ট্রিং-এ অফসেট। NULL হতে পারে। REL ফাইলের শুরুর সাথে সম্পর্কিত। |
| 0x18 | 4 | নামের আকার | বাইটে মডিউল নামের আকার। |
| 0x1c | 4 | সংস্করণ | REL ফাইল ফরম্যাটের সংস্করণ নম্বর। |
| 0x20 | 4 | bssSize | '.bss' বিভাগের আকার। |
| 0x24 | 4 | relOffset | স্থানান্তর টেবিলে অফসেট। |
| 0x28 | 4 | impOffset | imp টেবিল অফসেট. |
| 0x2c | 4 | impSize | বাইটে imp টেবিলের আকার। |
| 0x30 | 1 | prologSection | Index into section table which prolog is relative to. Skip if this field is 0. |
| 0x31 | 1 | epilogSection | Index into section table which epilog is relative to. Skip if this field is 0. |
| 0x32 | 1 | unresolvedSection | Index into section table which unresolved is relative to. Skip if this field is 0. |
| 0x33 | 1 | bssSection | বিভাগ টেবিলে সূচী যা bss আপেক্ষিক। রানটাইমে ভরা! |
| 0x34 | 4 | prolog | _prolog ফাংশনের নির্দিষ্ট বিভাগে অফসেট। |
| 0x38 | 4 | এপিলগ | _epilog ফাংশনের নির্দিষ্ট বিভাগে অফসেট। |
| 0x3c | 4 | অমীমাংসিত | _অমীমাংসিত ফাংশনের নির্দিষ্ট বিভাগে অফসেট। |
| 0x40 | 4 | align | Version ≥ 2 only. Alignment constraint on all sections, expressed as power of 2. |
| 0x44 | 4 | bssAlign | Version ≥ 2 only. Alignment constraint on all '.bss' section, expressed as power of 2. |
| 0x48 | 4 | fixSize | শুধুমাত্র সংস্করণ ≥ 3। REL যদি OSLinkFixed (OSLink-এর পরিবর্তে) সাথে লিঙ্ক করা হয়, তাহলে এই ঠিকানার পরে থাকা স্থানটি অন্য উদ্দেশ্যে (যেমন BSS) ব্যবহার করা যেতে পারে। |

### বিভাগ তথ্য টেবিল
বিভাগ তথ্য সারণীতে প্রতিটি 0x8 বাইট দীর্ঘ **সংখ্যা বিভাগ** এন্ট্রি রয়েছে:
| অফসেট | আকার | বর্ণনা |
-------|------------|-------------|
| 0x0 | 30 বিট | REL এর শুরু থেকে বিভাগ পর্যন্ত অফসেট। যদি এটি শূন্য হয়, বিভাগটি একটি অপ্রবর্তিত বিভাগ (যেমন .bss)। |
| 0x3.6 | 1 বিট | অজানা। |
| 0x3.7 | 1 বিট | এক্সিকিউটেবল পতাকা; যদি এটি 1 হয় তবে বিভাগটি সম্পাদনযোগ্য। |
| 0x4 | 4 | বিভাগের বাইটে দৈর্ঘ্য। যদি এটি শূন্য হয়, তাহলে এই এন্ট্রিটি এড়িয়ে যাবে। |
| 0x8 | পরবর্তী এন্ট্রি | পরবর্তী এন্ট্রি |

### রিলোকেশন ডেটা
স্থানান্তর ডেটা হল 0x8 বাইট স্ট্রাকচারের এক বা একাধিক তালিকা। প্রতিটি তালিকার শেষ বিশেষ টাইপ কোড 203 দ্বারা চিহ্নিত করা হয়েছে:
| অফসেট | নাম | আকার | বর্ণনা |
-------|------------|------------|-----|
| 0x0 | অফসেট | 2 | এটিতে পূর্ববর্তী স্থানান্তর থেকে বাইটে অফসেট। যদি এটি বিভাগে প্রথম স্থানান্তর হয় তবে এটি বিভাগ শুরুর সাথে সম্পর্কিত। |
| 0x2 | প্রকার | 1 | স্থানান্তরের ধরন। নীচে বর্ণিত. |
| 0x3 | বিভাগ | 1 | প্রতীকের যে বিভাগটির বিপরীতে স্থান পরিবর্তন করতে হবে। স্পেশাল রিলোকেশন টাইপ 202-এর জন্য, এটি হল এই ফাইলের সেকশনের নম্বর যার জন্য নিম্নলিখিত রিলোকেশন এন্ট্রিগুলি প্রযোজ্য। |
| 0x4 | যোগ করুন | 4 | চিহ্নের বাইটে অফসেট এর বিপরীতে স্থানান্তর করার জন্য, এটির বিভাগের শুরুর সাথে সম্পর্কিত। এটি main.dol এর বিপরীতে স্থানান্তরের পরিবর্তে একটি পরম ঠিকানা। |
| 0x8 | পরবর্তী এন্ট্রি | পরবর্তী এন্ট্রি | পরবর্তী এন্ট্রি |


 



## তথ্যসূত্র 

* [রিলোকেটেবল অবজেক্ট মডিউল ফরম্যাট](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


