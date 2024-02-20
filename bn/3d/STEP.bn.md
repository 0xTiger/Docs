---
date: 2019-10-11
keywords: step, .step, step file format, how to open step files, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP ফাইল ফর্মat
linktitle: STEP
description: Lস্টেপ ফাইল ফরম্যাট এবং এপিআই সম্পর্কে আয় করুন যা STEP ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## একটি STEP ফাইল কি?

STEP ফাইল কম্পিউটার-এডেড ডিজাইন (CAD) এর জন্য একটি বহুল ব্যবহৃত ডেটা এক্সচেঞ্জ ফরম্যাট। এটি 1994 সালে ISO 10303-21 নামে ISO কমিটি দ্বারা প্রমিত করা হয়েছিল। ISO 10303-21 এক্সপ্রেস ডেটা মডেলিং ভাষাতে ডেটা উপস্থাপনের জন্য এনকোডিং প্রক্রিয়া সংজ্ঞায়িত করে। একটি স্টেপ-ফাইল p21-ফাইল এবং স্টেপ ফিজিক্যাল ফাইল নামেও পরিচিত। STEP-ফাইলের জন্য ব্যবহৃত ফাইল এক্সটেনশনগুলি হল .stp এবং .step৷

## মৌলিক ইতিহাস

In 1994, the original Part 21 specification was issued. It has some bugs which were corrected by the technical corrigendum issued in 1996. দ্বিতীয় সংস্করণটি 2002 সালে প্রকাশিত হয়েছিল যাতে বেশ কয়েকটি ডেটা বিভাগের জন্য সংশোধনী এবং এক্সটেনশন অন্তর্ভুক্ত ছিল। তৃতীয় সংস্করণটি 2016 সালে প্রকাশিত হয়েছিল যা অ্যাঙ্কর এবং রেফারেন্স বিভাগগুলি যুক্ত করেছিল যা সত্তা এবং মানগুলিকে বহিরাগত ফাইলগুলিতে সংরক্ষণ করার অনুমতি দেয়। UTF-8 সমর্থন স্ট্রিং যোগ করা হয়েছে. ফাইলের বিষয়বস্তু যাচাই করতে এবং শংসাপত্রগুলি যাচাই করতে ডিজিটাল স্বাক্ষর যুক্ত করা হয়েছিল। জিপ ব্যবহার করে এক্সচেঞ্জ স্ট্রাকচার সংকুচিত এবং সংরক্ষণের জন্য সমর্থনও যোগ করা হয়েছিল।

## স্টেপ ফাইল ফরম্যাট

The plain text format for a STEP-file consists of a sequence of records. The character set is defined as code points of ISO 10646. ISO-10303-21; প্রথম রেকর্ডের প্রথম অক্ষর। মন্তব্যগুলি /* এবং */ অক্ষর দ্বারা বেষ্টিত। শেষ রেকর্ডে রয়েছে END-ISO-10303-21; যদি STEP-ফাইলটি 2002 সংস্করণের সাথে সামঞ্জস্যপূর্ণ হয়। এটি 2016 সংস্করণের সাথে সামঞ্জস্যপূর্ণ হলে, END-ISO-10303-21; এর পরে এক বা একাধিক ডিজিটাল স্বাক্ষর থাকতে পারে। টার্মিনেটর লাইন ব্রেকগুলি \N দ্বারা চিহ্নিত করা হয় এবং পৃষ্ঠা বিরতিগুলি \F দ্বারা চিহ্নিত করা হয়।

STEP ফাইলটি বিভাগে বিভক্ত এবং তাদের নাম সংরক্ষিত পদ। সমস্ত বিভাগ ENDSEC রেকর্ড দিয়ে শেষ হয় এবং নীচে দেখানো ক্রমে হতে হবে৷

- **হেডার**: এটি একটি বাধ্যতামূলক এবং অ-পুনরাবৃত্ত বিভাগ। এটি নিম্নলিখিত সত্তা নিয়ে গঠিত:
  - file_description (mandatory)
  - "ফাইল_নাম (বাধ্যতামূলক)"
  - "ফাইল_স্কিমা (বাধ্যতামূলক)"
  - "স্কিমা_জনসংখ্যা (ঐচ্ছিক)"
  - "ফাইল_জনসংখ্যা (ঐচ্ছিক)"
  - "বিভাগ_ভাষা (ঐচ্ছিক)"
  - "বিভাগ_প্রসঙ্গ (ঐচ্ছিক)"
- **ANCHOR**: এটি একটি ঐচ্ছিক নন-রিপিটিং বিভাগ যা 2016 সংস্করণে চালু করা হয়েছিল। এটি উদাহরণের জন্য বাহ্যিক নামগুলিকে সংজ্ঞায়িত করে যাতে সেগুলি উল্লেখ করা যায়।
- **রেফারেন্স**: এটি একটি ঐচ্ছিক নন-রিপিটিং বিভাগ যা 2016 সংস্করণেও চালু করা হয়েছিল। এই বিভাগের প্রতিটি এন্ট্রি একটি বহিরাগত ফাইলের একটি দৃষ্টান্ত/মূল্যের সাথে একটি এন্ট্রি/মান ইনস্ট্যান্স নামকে সংযুক্ত করে।
- **ডেটা**: এটি একটি ঐচ্ছিক পুনরাবৃত্তিযোগ্য বিভাগ যাতে মডেল উদাহরণের মূল বিষয়বস্তু থাকে।
- **SIGNATURE**: It is an optional repeatable section that was introduced in the 2016 version. It holds the digital signature to verify the file's content or to validate credentials.

## তথ্যসূত্র

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
