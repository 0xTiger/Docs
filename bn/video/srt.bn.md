---
date: 2019-10-11
keywords: srt, .srt, srt file format, .srt file format, .srt extension, srt extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lএসআরটি ফাইল ফরম্যাট এবং এপিআই সম্পর্কে আয় করুন যা এসআরটি ফাইল তৈরি এবং খুলতে পারেs.
title: Sআরটি ফাইল ফর্মat
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## একটি SRT ফাইল কি? ##

এসআরটি (সাবরিপ ফাইল ফরম্যাট) হল একটি সাধারণ সাবটাইটেল ফাইল যা .srt এক্সটেনশন সহ সাবরিপ ফাইল ফরম্যাটে সংরক্ষিত। এতে সাবটাইটেল, শুরু এবং শেষের টাইমস্ট্যাম্প এবং সাবটাইটেল পাঠ্যের একটি ক্রমিক সংখ্যা রয়েছে। এসআরটি ফাইলগুলি উত্পাদিত হওয়ার পরে ভিডিও সামগ্রীতে সাবটাইটেল যুক্ত করা সম্ভব করে।

## SRT ফাইলের গঠন ##

SRT ফাইলে প্রতিটি সাবটাইটেলের চারটি অংশ থাকে।

1. সাবটাইটেলের সংখ্যা বা অবস্থান নির্দেশ করে একটি সংখ্যাসূচক কাউন্টার।
1. সাবটাইটেলের শুরু এবং শেষ সময় --> অক্ষর দ্বারা বিভক্ত
1. এক বা একাধিক লাইনে সাবটাইটেল পাঠ্য।
1. একটি ফাঁকা লাইন সাবটাইটেলের শেষ নির্দেশ করে।

### SRT এর উদাহরণ ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

সময় নির্দিষ্ট করতে *ঘন্টা:মিনিট:সেকেন্ড,মিলিসেকেন্ড (00:00:00,000)* বিন্যাস ব্যবহার করা হয়।

## SRT ফাইলের ফরম্যাটিং ##

SRT ফাইলের বিন্যাস HTML ট্যাগ থেকে উদ্ভূত হয়। SRT ফাইলের ফর্ম্যাটিং ট্যাগগুলি নীচে তালিকাভুক্ত করা হয়েছে৷

| প্রভাব | ট্যাগ |
| --- | --- |
|বোল্ড|**\ <b>...\</b> ** বা {b}...{/b}|
|ইটালিক|**\ <i>...\</i> ** বা **{i}...{/i}**|
|আন্ডারলাইন|**\ <u>...\</u> ** বা **{u}...{/u}**|
|ফন্টের রঙ |**\ <font color=white>...\</font> **|
|লাইন অবস্থান|**{\a3}** (ইঙ্গিত করে যে পাঠ্যটি লাইন 3 এ প্রদর্শিত হওয়া উচিত)

## সাবরিপ সফটওয়্যার ##

SubRip হল একটি বিনামূল্যের সফটওয়্যার প্রোগ্রাম যা উইন্ডোজে চলে। এটি বিভিন্ন ভিডিও ফরম্যাট থেকে সাবটাইটেল এবং তাদের সময় বের করে এবং SRT ফরম্যাটে সাবটাইটেল সংরক্ষণ করে। SubRip লাইভ ভিডিও, অন্যান্য ভিডিও ফাইল এবং DVD থেকে সাবটাইটেল বের করতে অপটিক্যাল ক্যারেক্টার রিকগনিশন ব্যবহার করে।

## তথ্যসূত্র ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)