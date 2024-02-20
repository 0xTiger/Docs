{
  "date": "2021-07-29",
  "keywords": [
    "pes file",
    "pes file format",
    "what is a pes file",
    "file",
    "pes example",
    "pes file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PES ফাইল ফরম্যাট - ভাই PE এমব্রয়ডারি ফরম্যাট",
  "description": "PES ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি PES ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "PES",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-pes-bn"
    }
  },
  "lastmod": "2021-07-29"
}

## একটি PES এমব্রয়ডারি ফাইল কি?

PES এমব্রয়ডারি ফাইল হল একটি ডিজাইন ফাইল যাতে এমব্রয়ডারি/সেলাই মেশিনের জন্য নির্দেশনা থাকে। এটি ব্রাদার ইন্ডাস্ট্রিজ তাদের এমব্রয়ডারি মেশিনের জন্য ডেভেলপ করেছিল কিন্তু পরে সাধারণ ফাইল ফরম্যাট হিসেবে আনুষ্ঠানিক রূপ দেওয়া হয়েছিল। PES ফাইলগুলি সেলাই মেশিন দ্বারা ফ্যাব্রিকের উপর একটি প্যাটার্ন সেলাই করার জন্য নির্দেশাবলী পড়তে ব্যবহৃত হয়। এই ফাইল দুটি উদ্দেশ্য পরিবেশন; প্রথমে ব্রাদার ইন্ডাস্ট্রিজ দ্বারা তৈরি পিই-ডিজাইন অ্যাপ্লিকেশনের জন্য ডিজাইনের তথ্য প্রদান করে এবং দ্বিতীয়টি, ডিজাইনের নাম, রঙ এবং এমব্রয়ডারি মেশিন কোড যেমন স্টপ, জাম্প, এবং ট্রিম প্রদান করে।

## PES ফাইল ফরম্যাট - আরও তথ্য

একটি PES ফাইল বাইনারি ফাইল বিন্যাসে ডিস্কে সংরক্ষণ করা হয়। এটিতে একাধিক বিভাগ রয়েছে যাতে পূর্বনির্ধারিত পদ্ধতি ব্যবহার করে সেলাইয়ের তথ্য সংরক্ষণ করা হয়। PES ফাইল বিন্যাস অনুসরণ করা হয়.

 * ভার্সন ডেটা - ভার্সন তথ্য দেয় এবং যেকোনো মান হতে পারে `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
 * পিইসি সিক ভ্যালু - একটি 4 বাইট লিটল-এন্ডিয়ান পূর্ণসংখ্যা অবিলম্বে সংস্করণ ডেটা অনুসরণ করে এবং পিইসি বিভাগের জন্য অনুসন্ধান মান উপস্থাপন করে যাতে নকশার বিবরণ তথ্য রয়েছে
 * PSE বিভাগ - ব্রাদার PE-ডিজাইনের সাথে প্রাসঙ্গিক ডিজাইনের তথ্য রয়েছে এবং অন্যান্য সেলাই অ্যাপ্লিকেশন হতে পারে
 * PCE বিভাগ - PSE ফাইলের যেকোনো জায়গায় হতে পারে কিন্তু PEC সিক ভ্যালু দ্বারা উল্লেখ করা হয়েছে।

## PES ফাইল ব্যবহার করে সেলাই মেশিনের ধরন

PES ফাইলগুলি মূলত ব্রাদার সেলাই মেশিনের সাথে ব্যবহৃত PE-ডিজাইন সফ্টওয়্যার দ্বারা তৈরি করা হয়। PES ফাইলগুলিকে সমর্থন করতে পারে এমন কিছু অন্যান্য মেশিনের মধ্যে রয়েছে Babylock এবং Bernina হোম এমব্রয়ডারি মেশিন।

## কিভাবে PSE ফাইল কনভার্ট করবেন?

PE-ডিজাইন সফ্টওয়্যার অ্যাপ্লিকেশনটি অন্যান্য বিন্যাসে [convert PSE file](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl=pes+file) করতে পারে যেমন .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd, বা .xxx . এটি ফাইলটি খোলার এবং রূপান্তর বিন্যাস নির্বাচন করে PE-ডিজাইন অ্যাপ্লিকেশন ব্যবহার করে করা যেতে পারে।

## তথ্যসূত্র

* [PE ডিজাইন - নির্দেশিকা ম্যানুয়াল](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

