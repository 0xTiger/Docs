---
date: 2019-10-11
keywords: f4v, .f4v, f4v file format, .f4v file format, .f4v extension, f4v extension, f4v video format, how to open f4v files, what are f4v files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LF4V ফাইল ফরম্যাট এবং APIগুলি উপার্জন করুন যা F4V ফাইল তৈরি এবং খুলতে পারেes
title: F4V ফাইল ফর্মat
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## একটি F4V ফাইল কি? ##

F4V (ফ্ল্যাশ MP4 ভিডিও ফাইল) হল .f4v এক্সটেনশনের সাথে সংরক্ষিত একটি ভিডিও ফাইল। এটি ISO বেস মিডিয়া ফাইল ফরম্যাটের উপর ভিত্তি করে (MPEG-4 পার্ট 12)। এটি [MP4](/video/mp4/)-এর সাথে খুব সাদৃশ্যপূর্ণ তাই এটিকে অনানুষ্ঠানিকভাবে Flash MP4 নামেও উল্লেখ করা হয়। H.264/ACC বিষয়বস্তু স্ট্রিম করার সময় [FLV](/video/flv/)-এর সীমাবদ্ধতা ছিল যার ফলে Adobe Systems নতুন F4V ফর্ম্যাট তৈরি করেছে৷ Flash Player 9 Update 3 প্রকাশের পর থেকে ফ্ল্যাশ প্লেয়ার F4V ফাইল চালাতে পারে।

## F4V ফাইলের গঠন ##

F4V ফাইল ফরম্যাটটি ISO বেস মিডিয়া ফাইল ফরম্যাটের (MPEG-4 পার্ট 12) উপর ভিত্তি করে তৈরি এবং MP4 ফরম্যাটের মতোই। গঠন সংক্রান্ত বিশদ বিবরণের জন্য, অনুগ্রহ করে [MP4](/video/mp4/) পৃষ্ঠাটি দেখুন৷ F4V এবং MP4 এর মধ্যে প্রধান পার্থক্য হল মেটাডেটা ফর্ম্যাট যা F4V সংরক্ষণ করতে পারে। F4V ফর্ম্যাট দ্বারা সমর্থিত মেটাডেটা ফর্ম্যাটের তালিকা নীচে দেওয়া হল৷

- **Tag box**: Additional four optional tag boxes (auth, title, dscp, cprt) within the Movie (moov) box.
- **XMP মেটাডেটা বক্স**: এই বক্সটি মুভি (moov) বক্সের ঠিক পরে আসে৷ এটির মাধ্যমে, ফাইলটি অ্যাকশনস্ক্রিপ্টের মাধ্যমে একটি SWF মুভিতে XMP মেটাডেটা যোগাযোগ করতে পারে।
- **ilst বক্স**: এই বক্সটি মেটা (মেটা) বক্সের ভিতরে থাকে এবং এতে অনেকগুলি মেটাডেটা ট্যাগ থাকতে পারে। সমর্থিত ডেটা প্রকারগুলি নীচে দেওয়া হল।
  - "**0**: কাস্টম ডেটা।"
  - "**1**: টেক্সট ডেটা।"
  - "**12, 14**: বাইনারি ডেটা"
  - "**21**: জেনেরিক ডেটা।"
- **টেক্সট ট্র্যাক মেটাডেটা বক্স**: মিডিয়া ডেটাবক্সের (mdat) ভিতরে টেক্সট নমুনা (টেক্সট বা tx3g)। এতে নিম্নলিখিত মেটাডেটা বক্স থাকতে পারে।
  - "**স্টাইল বক্স**: টেক্সট স্টাইল স্পেসিফিকেশন।"
  - "**হাইলাইট বক্স**: হাইলাইট করার জন্য পাঠ্যের পরিসর নির্দিষ্ট করে।"
  - "**হাইলাইট কালার বক্স**: টেক্সটের জন্য হাইলাইট কালার নির্দিষ্ট করে।"
  - "**ক্যারাওকে বক্স**: কারাওকে মেটাডেটা নির্দিষ্ট করে।"
  - "**স্ক্রোল বিলম্ব বক্স**: স্ক্রোল বিলম্ব নির্দিষ্ট করে।"
  - "**ড্রপ শ্যাডো অফসেট বক্স**: পাঠ্যের জন্য ড্রপ শ্যাডো অফসেট স্থানাঙ্ক নির্দিষ্ট করে।"
  - "**ড্রপ শ্যাডো আলফা বক্স**: পাঠ্যের জন্য ড্রপ শ্যাডো আলফা মান নির্দিষ্ট করে।"
  - "**হাইপারটেক্সট বক্স**: একটি টেক্সট পরিসরে অল্ট টেক্সট সহ হাইপারটেক্সট টেক্সট নির্দিষ্ট করে।"
  - "**টেক্সট বক্স বক্স**: টেক্সট বক্সের জন্য স্থানাঙ্ক সংজ্ঞায়িত করে।"
  - "**ব্লিঙ্কিং বক্স**: টেক্সটের একটি পরিসরের জন্য ব্লিঙ্কিং নির্দিষ্ট করে।"
  - "**টেক্সট র‍্যাপ বক্স**: টেক্সটের জন্য টেক্সট র‍্যাপ ফ্ল্যাগ সেট করে।"
  - "**টেক্সট র‍্যাপ বক্স**: টেক্সটের জন্য টেক্সট র‍্যাপ ফ্ল্যাগ সেট করে।"

## তথ্যসূত্র ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

