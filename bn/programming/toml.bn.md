---
date: 2019-10-11
keywords: toml, .toml, toml file format, how to open toml files, .toml extension, toml extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Tওএমএল ফাইল ফর্মat
linktitle: TOML
description: LTOML ফাইল ফরম্যাট এবং API সম্পর্কে আয় করুন যা TOML ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## একটি TOML ফাইল কি? ##

TOML (Tom's Obvious Minimal Language) হল একটি ন্যূনতম কনফিগারেশন ফাইল ফরম্যাট যা .toml এক্সটেনশন ব্যবহার করে। TOML এর লক্ষ্য হল পড়া সহজ, অভিধানে দ্ব্যর্থহীনভাবে ম্যাপ করা এবং বিভিন্ন ডেটা স্ট্রাকচারে পার্স করা সহজ। TOML এর একটি ওপেন-সোর্স স্পেসিফিকেশন রয়েছে যা সম্প্রদায়ের অবদান পেয়েছে। TOML অনেক প্রোগ্রামিং ল্যাঙ্গুয়েজ যেমন C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, ইত্যাদি দ্বারা সমর্থিত। TOML ফাইলের MIME প্রকার হল *application/toml*।


## TOML ফাইল ফরম্যাট ##

TOML ফাইলগুলি প্রধানত কী/মান পেয়ার, বিভাগ/সারণী, মন্তব্য নিয়ে গঠিত এবং অবশ্যই একটি বৈধ UTF-8 এনকোডেড ইউনিকোড নথি হতে হবে। TOML স্ট্রিং, ইন্টিজার, ফ্লোট, বুলিয়ান, ডেটটাইম, অ্যারে এবং টেবিল (হ্যাশ টেবিল/ডিকশনারী) ডেটা প্রকার সমর্থন করে। TOML হল একটি কেস-সংবেদনশীল ভাষা।

### বাক্য গঠন ###

- **কী-মান জোড়া**: মূল-মান জোড়া সমান চিহ্ন (=) দ্বারা পৃথক করা হয়। প্রতিটি জোড়া একটি নতুন লাইন হতে হবে.

``টমল
প্রথম = টম
শেষ = প্রেস্টন-ওয়ার্নার
```

- **মন্তব্য**: মন্তব্য হ্যাশ (#) চিহ্ন দিয়ে শুরু হয়।

``টমল
# এটি একটি TOML নথি।
```

- **স্ট্রিংস**: স্ট্রিংগুলি উদ্ধৃতি () চিহ্ন দ্বারা বেষ্টিত।

``টমল
স্ট্রিং = উদাহরণ স্ট্রিং
```

- **মাল্টি-লাইন স্ট্রিংস**: মাল্টি-লাইন স্ট্রিংগুলি তিনটি উদ্ধৃতি () চিহ্ন দ্বারা বেষ্টিত।

``টমল
[বাসার ঠিকানা]
রাস্তা = 123 টর্নেডো অ্যালি
স্যুট 16
শহর = ইস্ট সেন্টারভিল
রাষ্ট্র = কেএস
```

- **পূর্ণসংখ্যা/ফ্লোট**

``টমল
পূর্ণসংখ্যা = 20
float = 20.5
```

- **বুলিয়ানস**: বুলিয়ান সবসময় ছোট হাতের হয়।

``টমল
bool1 = সত্য
bool2 = মিথ্যা
```

- **Date-Time**: For DateTime, you may use an RFC 3339 formatted date-time as shown in the example below.

``টমল
  offset_date_time = 1979-05-27 07:32:00Z
  local_date_time = 1979-05-27T07:32:00
স্থানীয়_তারিখ = 1979-05-27
local_time = 07:32:00
```

- **অ্যারে**: অ্যারেগুলি কমা (,) দ্বারা পৃথক করা উপাদান সহ বর্গাকার বন্ধনী দ্বারা বেষ্টিত।

``টমল
রং = [ লাল, হলুদ, সবুজ]
```

- **সারণী**: সারণী হল কী/মান জোড়ার সংগ্রহ যা বর্গাকার বন্ধনী ([]) দ্বারা বেষ্টিত একটি নতুন লাইনে হেডার দ্বারা সংজ্ঞায়িত করা হয়। একটি নতুন শিরোনাম প্রদান করা হলে বা ফাইল শেষ হলে টেবিলটি শেষ হয়।

``টমল
[বাসার ঠিকানা]
রাস্তা = 123 টর্নেডো অ্যালি
স্যুট 16
শহর = ইস্ট সেন্টারভিল
রাষ্ট্র = কেএস

[অফিসের ঠিকানা]
রাস্তা = 123 টর্নেডো অ্যালি
স্যুট 16
শহর = ইস্ট সেন্টারভিল
রাষ্ট্র = কেএস
```

ইনলাইন টেবিলগুলি কোঁকড়া ধনুর্বন্ধনী ({}) দ্বারা বেষ্টিত প্রতিটি কী/মান জোড়া কমা (,) দ্বারা পৃথক করা হয়।

``টমল
নাম = {প্রথম = টম, শেষ = পিট }
```

## তথ্যসূত্র ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)
