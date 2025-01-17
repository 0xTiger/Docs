---
date: 2021-03-21
keywords: alac, alac file format, .alac extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: LALAC ফাইল ফরম্যাট এবং API সম্পর্কে আয় করুন যা ALAC ফাইল তৈরি এবং খুলতে পারেs.
title: ALAC - অ্যাপল লসলেস অডিও কোডেক ফাইল ফর্মat
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## একটি ALAC ফাইল কি?

ALAC ফাইল ফরম্যাট হল Apple Lossless Audio Codec (ALAC) যা MPEG-4 কমপ্লায়েন্ট QuickTime কন্টেইনার ব্যবহার করে। এটি 2004 সালে মালিকানাধীন ফাইল ফরম্যাট হিসাবে চালু করা হয়েছিল, 2011 পর্যন্ত যখন অ্যাপল এটিকে ওপেন সোর্স এবং রয়্যালটি-মুক্ত উপলব্ধ করেছিল। বিন্যাসটি [FLAC](/audio/flac/) (ফ্রি লসলেস অডিও কোডেক) এর অনুরূপ কিন্তু তুলনামূলকভাবে আরও কম্প্রেশন অফার করে। এটি [AAC](/audio/aac/) বা [MP3](/audio/mp3/)-এর আরও ভাল শব্দের বিকল্প অফার করে৷ ALAC কোডেক দিয়ে এনকোড করা অডিও ফাইল অ্যাপল কুইকটাইম, অ্যাপল আইটিউনস এবং কে-লাইট কোডেক সহ মাইক্রোসফ্ট উইন্ডোজ মিডিয়া প্লেয়ার ব্যবহার করে খোলা যেতে পারে।

## ALAC ফাইল ফরম্যাট

ALAC কোডেক ভিত্তিক ফাইলগুলি হল বাইনারি ফাইল যা বিকাশকারীর রেফারেন্সের জন্য [open source on GitHub](https://github.com/macosforge/alac) হিসাবে উপলব্ধ৷ এতে ALAC এনকোডার এবং ডিকোডারের উৎস রয়েছে। অ্যাপল কোর অডিও ফরম্যাট (CAF) এবং [WAVE](/audio/wav/) ফাইলে/থেকে অডিও ডেটা পড়তে এবং লিখতে `alacconvert` নামে একটি কমান্ড লাইন ইউটিলিটি প্রদান করেছে। ALAC ফাইল ফরম্যাট সম্পর্কে কিছু মূল বিষয় নিচে দেওয়া হল।

 1. `বিট গভীরতা` - 16, 20, 24 এবং 32 বিট।
 1. `স্যাম্পল রেট` - 1 থেকে 384,000 Hz পর্যন্ত যেকোনো ইচ্ছামত পূর্ণসংখ্যার নমুনা হার। 4,294,967,295 (2^32 - 1) Hz পর্যন্ত তাত্ত্বিক হার সমর্থিত হতে পারে।
 1. `প্যাকেটের আকার` - ডিফল্ট প্যাকেটের আকার প্রতি প্যাকেটে অডিওর 4096 নমুনা ফ্রেমে ডিফল্ট। অন্যান্য প্যাকেট আকার অবশ্যই সম্ভব। যাইহোক, অ্যাপল লসলেস সমর্থন করে এমন সমস্ত হার্ডওয়্যার ডিভাইসে নন-ডিফল্ট প্যাকেট আকারগুলি সঠিকভাবে কাজ করার গ্যারান্টি দেওয়া হয় না। 16,384 নমুনা ফ্রেমের উপরে প্যাকেট সমর্থিত নয়।
 1. সমর্থিত চ্যানেল' - এটি এক থেকে আটটি চ্যানেল সমর্থন করে। প্রতিটি চ্যানেলের তথ্যের নিম্নোক্ত ক্রম রয়েছে।

|নাম চান| অর্ডার|
|---|---|
|1 |মনো |
|2 |স্টেরিও (বাম, ডান)|
|3 |MPEG 3.0 B (কেন্দ্র, বাম, ডান)|
|4 |MPEG 4.0 B (কেন্দ্র, বাম, ডান, কেন্দ্র চারপাশ)|
|5 |MPEG 5.0 D (কেন্দ্র, বাম, ডান, বাম চারপাশ, ডান চারপাশ)|
|6 |MPEG 5.1 D (কেন্দ্র, বাম, ডান, বাম চারপাশ, ডান চারপাশ, কম ফ্রিকোয়েন্সি প্রভাব)|
|7 |Apple AAC 6.1 (কেন্দ্র, বাম, ডান, বাম চারপাশ, ডান চারপাশ, কেন্দ্র চারপাশ, নিম্ন ফ্রিকোয়েন্সি প্রভাব)|
|8 |MPEG 7.1 B (কেন্দ্র, বাম কেন্দ্র, ডান কেন্দ্র, বাম, ডান, বাম চারপাশ, ডান চারপাশ, নিম্ন ফ্রিকোয়েন্সি প্রভাব)|

## তথ্যসূত্র

* [ALAC - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Apple_Lossless)

* [অ্যাপল লসলেস অডিও কোডেক](https://macosforge.github.io/alac/)

* [macosforge - GitHub-এ alac](https://github.com/macosforge/alac)


