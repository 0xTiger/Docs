---
date: 2019-10-11
keywords: vob, .vob, vob file format, .vob file format, .vob extension, vob extension, vob video format, vob dvd files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LVOB ফাইল ফরম্যাট এবং API সম্পর্কে আয় করুন যা VOB ফাইল তৈরি এবং খুলতে পারেs.
title: Vওবি ফাইল ফর্মat
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## একটি VOB ফাইল কি? ##

VOB ফাইলগুলি সাধারণত .vob এক্সটেনশন সহ একটি DVD-তে VIDEO_TS ডিরেক্টরিতে সংরক্ষণ করা হয়। VOB ফাইলগুলিতে ভিডিও এবং অডিও ডেটার পাশাপাশি অন্যান্য ডেটা যেমন মেনু এবং সাবটাইটেল থাকে। VOB MPEG-2 প্রোগ্রাম স্ট্রিম ফরম্যাটের উপর ভিত্তি করে তৈরি কিন্তু ব্যক্তিগত স্ট্রীমে এর অতিরিক্ত সীমাবদ্ধতা এবং স্পেসিফিকেশন রয়েছে। VOB ফাইল হল MPEG প্রোগ্রাম স্ট্রীমের একটি কঠোর উপসেট তাই সমস্ত VOB ফাইল MPEG প্রোগ্রাম স্ট্রীম কিন্তু সমস্ত MPEG প্রোগ্রাম স্ট্রীম VOB অনুগত নয়।

## ডিভিডি ভিডিওর গঠন ##

যখন একটি কম্পিউটারে একটি DVD খোলা হয়, VIDEO_TS হল AUDIO_TS-এর সাথে শীর্ষ স্তরের ডিরেক্টরি৷ AUDIO_TS খালি এবং ব্যবহার করা হয় না। VIDEO_TS ডিরেক্টরির ভিতরে, VOB, BUP, এবং IFO ফাইল আছে। VOB ফাইলে MPEG বিষয়বস্তু থাকে। এগুলিকে 1 জিবি বা কম আকারের খণ্ডে বিভক্ত করা হয়েছে যাতে এগুলি সমস্ত অপারেটিং সিস্টেমের সাথে সামঞ্জস্যপূর্ণ। IFO ফাইলগুলিতে মেনু এবং শিরোনাম গঠন সম্পর্কিত তথ্য রয়েছে। BUK ফাইলগুলি একই নামের IFO ফাইলগুলির ব্যাকআপ ফাইল। এই ফাইলগুলিকে শারীরিকভাবে একটি পৃথক এলাকায় রাখা হয় যাতে যদি DVD-এর শারীরিক ক্ষতির কারণে IFO ফাইলটি ক্ষতিগ্রস্ত হয়, BUK ফাইলটি একই তথ্য সরবরাহ করতে পারে।

### শারিরিক গঠন ###

- ডিস্কের সমস্ত ফাইল সংলগ্ন হতে হবে।
- সম্পর্কিত ফাইলগুলি একে অপরের পাশে থাকা উচিত (VOB, IFO, BUP)।
- নম্বরযুক্ত ফাইলগুলি আরোহী ক্রমে হওয়া উচিত।

## কপি সুরক্ষা ##

অনেক ভিডিও ডিভিডি এনক্রিপ্ট করা হয় এবং ডিভিডি থেকে ডেটা কপি করা প্রতিরোধ করে। ডিভিডির দুর্গম লিড-ইন এলাকায় অবস্থিত ফাইলগুলি চালানোর জন্য প্রমাণীকরণ এবং ডিক্রিপশন কীগুলির প্রয়োজন৷ এই কীগুলি ডিভিডি প্লেয়ার বা সফ্টওয়্যার প্লেয়ারে উপস্থিত CSS ডিক্রিপশন সফ্টওয়্যার দ্বারা ব্যবহৃত হয়। কী ছাড়া, ভিডিও ফাইলগুলি চালানো যাবে না কারণ ফাইলগুলি খোলার সময় কীগুলি অনুরোধ করা হবে৷

## তথ্যসূত্র ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)
