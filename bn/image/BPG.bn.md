---
date: 2020-08-12
keywords: bpg, .bpg, bpg file format, how to open bpg files, .bpg extension, bpg extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Bপিজি ফাইল ফর্মat
linktitle: BPG
description: LBPG ফাইল ফরম্যাট এবং APIs সম্পর্কে আয় করুন যা BPG ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## একটি BPG ফাইল কি? ##

BPG (বেটার পোর্টেবল গ্রাফিক্স) হল একটি ফাইল ফরম্যাট যা 2014 সালে ফেব্রিস বেলার্ড ডিজিটাল ছবির জন্য তৈরি করেছিলেন। তিনি JPEG-এর পরিবর্তে BPG-এর প্রস্তাব করেছিলেন কারণ BPG বেশি কম্প্রেশন বা আকার দক্ষ ছিল। BPG HEVC (High-Efficiency Video Coding) ভিডিও কম্প্রেশন স্ট্যান্ডার্ডের ইন্ট্রা-ফ্রেম এনকোডিং ব্যবহার করে।

BPG হ্যান্ডহেল্ড এবং IoT ডিভাইসে কাজ করার জন্য একটি বহনযোগ্য মেমরি-দক্ষ বিন্যাস হিসাবে ডিজাইন করা হয়েছে। বর্তমানে, ওয়েব ব্রাউজারগুলি BPG ফর্ম্যাট সমর্থন করে না, তবে ওয়েবসাইটগুলি এখনও বেলার্ডের লেখা একটি জাভাস্ক্রিপ্ট লাইব্রেরি ব্যবহার করে বিপিজি ছবি সরবরাহ করতে পারে। BPG HEVC এর প্রধান 4:4:4 16 স্টিল পিকচার প্রোফাইল ব্যবহার করে প্রতি নমুনা 14 বিট পর্যন্ত।

## স্পেসিফিকেশন ##

BPG কন্টেইনার ফরম্যাট হল একটি জেনেরিক ইমেজ ফরম্যাট, HEVC-তে ব্যবহৃত কাঁচা বিটস্ট্রিমের পরিবর্তে। BPG 4:4:4, 4:2:2, এবং 4:2:0 রঙের বিন্যাস সমর্থন করে। আলফা চ্যানেলটি আলাদাভাবে কোড করা অতিরিক্ত চ্যানেল বা CMYK ছবির চতুর্থ চ্যানেলের সাথেও সমর্থিত। BPG Exif, ICC প্রোফাইল, এবং XMP এর জন্য মেটাডেটা সমর্থন প্রদান করে। BPG YCbCr (ITU-R BT.601, BT.709, এবং BT.2020 (নন-কনস্ট্যান্ট লুমিনেন্স)), YCgCo, RGB, CMYK, এবং গ্রেস্কেল রঙের স্থান সমর্থন করে। BGP অ্যানিমেশন এবং ক্ষতিকর এবং ক্ষতিহীন HEVC ডেটা কম্প্রেশনকেও সমর্থন করে।

## তথ্যসূত্র ##

- [Better Portable Graphics - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

