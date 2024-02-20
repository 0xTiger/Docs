---
date: 2019-10-11
keywords: WEBM, What is a WEBM file, WEBM File Format
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: LWEBM ফাইল ফরম্যাট এবং API সম্পর্কে আয় করুন যা WEBM ফাইল তৈরি এবং খুলতে পারেs.
title: WEBM - WebM ভিডিও ফাইল ফর্মat
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## একটি WEBM ফাইল কি?

একটি .webm এক্সটেনশন সহ একটি ফাইল হল খোলা, রয়্যালটি-মুক্ত WebM ফাইল ফর্ম্যাটের উপর ভিত্তি করে একটি ভিডিও ফাইল৷ এটি ওয়েবে ভিডিও শেয়ার করার জন্য ডিজাইন করা হয়েছে এবং ভিডিও এবং অডিও ফরম্যাট সহ ফাইল কন্টেইনার গঠনকে সংজ্ঞায়িত করে। WebM 100% বিনামূল্যে, HTML, HTTP, এবং TCP/IP-এর মতো উন্মুক্ত প্রযুক্তির উপর ভিত্তি করে উচ্চ-মানের বাস্তবায়ন করে যা বাস্তবায়নের জন্য সকলের জন্য উন্মুক্ত। WebM বিশেষভাবে ওয়েবে ভিডিও পরিবেশনের জন্য ডিজাইন করা হয়েছে যা এটিকে কম কম্পিউটেশনাল ফুটপ্রিন্ট সহ স্ট্রিমিংয়ের জন্য অপ্টিমাইজ করে। এটি যেকোনো ডিভাইসে বিশেষ করে কম-পাওয়ার নেটবুক, হ্যান্ডহেল্ড এবং ট্যাবলেটে ভিডিও প্লেব্যাকের জন্য উপযুক্ত করে তোলে।

## WEBM ফাইল ফরম্যাট

WebM ফাইলের কাঠামো ম্যাট্রোস্কা [MKV](/video/mkv/) কন্টেইনার ফাইল ফর্ম্যাটের একটি উপসেটের উপর ভিত্তি করে। একটি WebM ফাইলে উপলব্ধ ভিডিও স্ট্রিমগুলি VP8 বা VP9 কম্প্রেশন প্রযুক্তি ব্যবহার করে সংকুচিত করা হয় যা কম্প্রেশনে অত্যন্ত দক্ষ। একইভাবে, একটি WebM ফাইলের অডিও স্ট্রিমগুলি [Xiph Foundation](https://www.xiph.org/) দ্বারা বিকশিত Vorbis বা Opus কোডেক ব্যবহার করে সংকুচিত হয়৷ এই সমস্ত ভিডিও এবং অডিও কোডেকগুলি রয়্যালটি-মুক্ত এবং কোনও চার্জ ছাড়াই ব্যবহার করা যেতে পারে৷

WebM ফাইল ফরম্যাটের সংক্ষিপ্ত বিবরণ নিচে দেওয়া হল।

|ক্ষেত্র | বর্ণনা |
---|---|
|MIME-টাইপ |ভিডিও/ওয়েবএম|
|অডিও-শুধু MIME-টাইপ |audio/webm|
|ইউনিফর্ম টাইপ আইডেন্টিফায়ার| org.webmproject.webm|
|ভিডিও কোডেক নাম| VP8 বা VP9|
|অডিও কোডেক নাম| ভরবিস বা ওপাস|

### WebM উপাদান

WebM, being a subset of the Matroska specifications, provides support for some of the Matroska functionality. Following is a description of the supported elements.

#### ইবিএমএল

|নাম |বিবরণ |
---|---|
|EBML| অনুসরণ করার জন্য ডেটার EBML বৈশিষ্ট্য সেট করুন। প্রতিটি EBML নথি এটি দিয়ে শুরু করতে হবে।|
|EBMLVersion |ফাইলটি তৈরি করতে ব্যবহৃত EBML পার্সারের সংস্করণ।|
|EBMLReadVersion|এই ফাইলটি পড়ার জন্য একজন পার্সারকে সর্বনিম্ন EBML সংস্করণ সমর্থন করতে হবে।|
|EBMLMaxIDLength |এই ফাইলটিতে আপনি যে আইডিগুলি পাবেন তার সর্বোচ্চ দৈর্ঘ্য (মাট্রোস্কায় 4 বা তার কম)|
|EBMLMaxSizeLength|এই ফাইলটিতে আপনি যে মাপের সর্বোচ্চ দৈর্ঘ্য পাবেন (মাট্রোস্কায় 8 বা তার কম)। এটি একটি উপাদানের শুরুতে নির্দেশিত উপাদানের আকারকে ওভাররাইড করে না। EBMLMaxSizeLength দ্বারা অনুমোদিত আকারের চেয়ে বড় একটি নির্দেশিত আকার আছে এমন উপাদানগুলিকে অবৈধ বলে গণ্য করা হবে৷|
|DocType|একটি স্ট্রিং যা এই EBML হেডার (আমাদের ক্ষেত্রে webm) অনুসরণ করে এমন নথির প্রকার বর্ণনা করে।|
|DocTypeVersion|DocType দোভাষীর সংস্করণটি ফাইল তৈরি করতে ব্যবহৃত হয়।|
|DocTypeReadVersion|এই ফাইলটি পড়ার জন্য একজন দোভাষীকে সর্বনিম্ন ডকটাইপ সংস্করণ সমর্থন করতে হবে।|

#### বৈশ্বিক উপাদান

এই মুহুর্তে, শুধুমাত্র 'Void' উপাদানটি সমর্থিত যা ক্ষতিগ্রস্ত ডেটা বাতিল করতে, ক্ষতিগ্রস্ত ডেটা ব্যবহার করার সময় অপ্রত্যাশিত আচরণ এড়াতে ব্যবহৃত হয়। বিষয়বস্তু বাতিল করা হয়. এছাড়াও পরবর্তী ব্যবহারের জন্য একটি উপ-উপাদানে স্থান সংরক্ষিত করতে ব্যবহৃত হয়।

#### সেগমেন্ট
এই উপাদানটিতে অন্যান্য সমস্ত শীর্ষ-স্তরের (লেভেল 1) উপাদান রয়েছে। সাধারণত একটি Matroska ফাইল 1 সেগমেন্ট নিয়ে গঠিত।

#### মেটা সেক ইনফরমেশন

নিম্নলিখিত অনুসন্ধান তথ্য সমর্থিত.

|উপাদানের নাম |বিবরণ |
---|---|
|SeekHead |অন্য স্তর 1 উপাদানের অবস্থান ধারণ করে৷|
|অনুসন্ধান|একটি EBML উপাদানে একটি একক অনুসন্ধান এন্ট্রি রয়েছে৷|
|SeekID | উপাদানের নামের সাথে সংশ্লিষ্ট বাইনারি আইডি৷|
|SeekPosition |অক্টেটে সেগমেন্টে উপাদানটির অবস্থান (0 = প্রথম স্তর 1 উপাদান)।|

## তথ্যসূত্র

* [ওয়েবএম](https://www.webmproject.org/)

* [ওয়েবএম কোড ভান্ডার](https://www.webmproject.org/code/#webp-repositories)

