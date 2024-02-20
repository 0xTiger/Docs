{
  "date": "2021-04-08",
  "keywords": [
    "lzma file",
    "lzma file format",
    "what is an lzma file",
    "file",
    "lzma example",
    "lzma file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "LZMA - LZMA সংকুচিত ফাইল বিন্যাস",
  "description": "একটি LZMA ফাইল এবং APIগুলি কী যা LZMA ফাইলগুলি তৈরি এবং খুলতে পারে।",
  "linktitle": "LZMA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lzma-bn"
    }
  },
  "lastmod": "2021-04-18"
}

## একটি LZMA ফাইল কি?

.lzma এক্সটেনশন সহ একটি ফাইল হল একটি সংকুচিত সংরক্ষণাগার ফাইল যা LZMA (Lempel-Ziv-Markov চেইন অ্যালগরিদম) কম্প্রেশন পদ্ধতি ব্যবহার করে তৈরি করা হয়। এগুলি প্রধানত ইউনিক্স অপারেটিং সিস্টেমে পাওয়া/ব্যবহৃত হয় এবং ফাইলের আকার ছোট করার জন্য অন্যান্য কম্প্রেশন অ্যালগরিদম যেমন [ZIP](/compression/zip/) এর মতো। LZMA হল একটি লিগ্যাসি ফাইল ফরম্যাট, যা .xz ফর্ম্যাট দ্বারা প্রতিস্থাপিত হচ্ছে বা করা হয়েছে৷ .lzma ফরম্যাটের MIME প্রকার হল \`application/x-lzma'। এই ফাইল বিন্যাসটি ইগর পাভলভ LZMA SDK-তে ব্যবহারের জন্য ডিজাইন করেছেন।

## LZMA ফাইল ফরম্যাট

LZMA ফাইল দুটি প্রধান অংশ নিয়ে গঠিত:

 1. হেডার
 1. সংকুচিত ডেটা


### LZMA হেডার

LZMA ফাইলগুলির একটি 13-বাইট হেডার রয়েছে যা LZMA সংকুচিত ডেটা দ্বারা অনুসরণ করা হয়। LZMA হেডারে রয়েছে:

 * বৈশিষ্ট্য
 * অভিধান আকার
 * সংকুচিত আকার

#### LZMA হেডারের বৈশিষ্ট্য

বৈশিষ্ট্য ক্ষেত্রে তিনটি বৈশিষ্ট্য রয়েছে। একটি সংক্ষিপ্ত নাম বন্ধনীতে দেওয়া হয়, তারপরে সম্পত্তির মান পরিসীমা। ক্ষেত্র গঠিত

1) আক্ষরিক প্রসঙ্গ বিটের সংখ্যা (lc, [0, 8]);
2) আক্ষরিক অবস্থান বিট সংখ্যা (lp, [0, 4]); এবং
3) অবস্থান বিটের সংখ্যা (pb, [0, 4])।

#### LZMA অভিধানের আকার

এটি 2^n এবং 2^n + 2^(n-1) এর মান সহ একটি স্বাক্ষরবিহীন 32-বিট লিটল এন্ডিয়ান পূর্ণসংখ্যা হিসাবে সংরক্ষণ করা হয়। LZMA Utils যেকোনো অভিধানের আকারের সাথে ফাইলগুলিকে ডিকম্প্রেস করতে পারে।

#### আনকম্প্রেসড সাইজ
আনকপ্রেসড সাইজ স্বাক্ষরবিহীন 64-বিট লিটল এন্ডিয়ান পূর্ণসংখ্যা হিসাবে সংরক্ষণ করা হয়। 0xFFFF_FFFF_FFFF_FFFF এর একটি বিশেষ মান নির্দেশ করে যে অসঙ্কোচিত আকার অজানা। মানটি পেলোড মার্কারের শেষ (\*) দ্বারা উপস্থাপিত হয় যদি এবং শুধুমাত্র যদি অসঙ্কোচিত আকার অজানা থাকে।

## তথ্যসূত্র

* [LZMA ফাইল ফরম্যাট](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)

* [লেম্পেল–জিভ–মার্কভ চেইন অ্যালগরিদম](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

