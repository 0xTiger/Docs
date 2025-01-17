{
  "date": "2021-07-08",
  "keywords": [
    "SYS",
    "extension",
    "file",
    "format",
    "system",
    "Driver",
    "System File",
    "programs",
    "computer",
    "application"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "SYS - সিস্টেম ফাইল ফরম্যাট",
  "description": "SYS ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি SYS ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "SYS",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sys-bn"
    }
  },
  "lastmod": "2021-07-08"
}

## একটি SYS ফাইল কি? ##

SYS ফাইলগুলি হল Windows OS এবং MS-DOS অ্যাপ্লিকেশনে ব্যবহৃত সিস্টেম ফাইল। এই ফাইলগুলি সরাসরি খোলা যাবে না এবং ডিভাইসের ড্রাইভার এবং কনফিগারেশন নিয়ে গঠিত। SYS ফাইলগুলি অপারেটিং সিস্টেমের মূল ফাংশনগুলির ফাইলগুলি ধারণ করার জন্য দায়ী৷ এগুলি ডিভাইস ড্রাইভারের সমালোচনামূলক ফাইল হিসাবে বিবেচিত হয় এবং রেস ড্রাইভারের যেকোন সমস্যা সমাধানের সময়ও ব্যবহার করা যেতে পারে। এগুলি একটি কম্পিউটার সিস্টেমের সঠিক কার্যকারিতার জন্য দায়ী, এবং .sys ফাইলগুলি অবশ্যই সঠিক এবং সম্পূর্ণ হতে হবে৷


## প্রযুক্তিগত স্পেসিফিকেশন ##

.sys ফাইলগুলি আসলে [BMP](/image/bmp/) ফর্ম্যাটের উপসেট কারণ এটি শুধুমাত্র নির্দিষ্ট সংমিশ্রণের অনুমতি দেয়৷ এই ফাইলগুলির স্বাভাবিক বিন্যাস হল LOGOS.SYS, LOGOW.SYS, এবং LOGO.SYS৷ অন্য কোনো ফাইলে এই বিন্যাস নেই।

এই ফাইলগুলি বেশিরভাগ ইনস্টলেশনের সময় উইন্ডোজের *C* ডিরেক্টরির মধ্যে ব্যবহৃত হয়। বেশিরভাগ সমস্যা যা ডিভাইস ড্রাইভারের চারপাশে ঘোরাফেরা করে Windows OS আপডেট করার মাধ্যমে সমাধান করা হয়। এই ফাইলগুলির বিবরণ এবং তথ্য উইন্ডোজ ওএসের অন্তর্নির্মিত প্রোগ্রামগুলি ব্যবহার করে দেখা যেতে পারে। এগুলি একটি অপারেটিং সিস্টেমের বিভিন্ন মডিউলের উল্লেখও অন্তর্ভুক্ত করে।
সিস্টেম ফাইলের কিছু উদাহরণ হল:

* IO.SYS (ডিস্ক অপারেটিং সিস্টেমের এই স্টোর ডিভাইস ড্রাইভার)

* MSDOS.SYS ( এতে কার্নেল বা অপারেটিং সিস্টেমের মূল কোড থাকে)

* CONFIG.SYS (এতে বিভিন্ন কনফিগারেশন বিকল্প রয়েছে)

* KEYBOARD.SYS (এতে কীবোর্ড লেআউট সম্পর্কিত তথ্য রয়েছে) 

* COUNTRY.SYS ( এই কন্টান দেশ এবং কোডপৃষ্ঠা সম্পর্কিত তথ্য)


## SYS ফাইল ফরম্যাট ##

মাইক্রোসফ্ট .sys এক্সটেনশন সহ ফাইলগুলি তৈরি করেছে। ভেরিয়েবল এবং ফাংশন SYS ফাইলে অন্তর্ভুক্ত করা হয়। এগুলি বেশিরভাগ মাইক্রোসফ্ট অপারেটিং সিস্টেম দ্বারা ব্যবহৃত হয়। এই ফাইলগুলি মূলত ডিস্কের রুট ডিরেক্টরিতে অবস্থিত:

* C:\Windows\system32\drivers

* C:\Windows\WinSxS


SYS ফাইল সম্পর্কে কিছু সাধারণ সতর্কতা নিম্নরূপ:

* এই ফাইলগুলির নাম পরিবর্তন করা উচিত নয় কারণ এই ফাইলগুলি অপারেটিং সিস্টেমের মূল ফাংশন এবং ভেরিয়েবলের জন্য দায়ী
* এই ফাইলগুলি মুছে ফেলা উচিত নয় কারণ এই ফাইলগুলির অনুপস্থিতি ত্রুটির কারণ হতে পারে
* .sys ফাইলগুলি ইন্টারনেট থেকে ডাউনলোড করা উচিত নয় যতক্ষণ না আপনি উৎসের বৈধতা সম্পর্কে নিশ্চিত হন
* কেউ এই ফাইলগুলির সাথে তালগোল পাকানো উচিত নয় কারণ সেগুলি পরিবর্তন করা বা এইগুলির সাথে জগাখিচুড়ি করার ফলে সিস্টেমের গুরুতর ত্রুটি হয়৷
* যদি এই ফাইলগুলি কোনও ভাইরাস বা ম্যালওয়্যার দ্বারা দূষিত হয়ে যায়, তবে এগুলি পুনরায় ইনস্টল করা উচিত

## SYS উদাহরণ ##

নিম্নলিখিত একটি সাধারণ SYS সিস্টেম কনফিগারেশন ফাইলের একটি উদাহরণ:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
