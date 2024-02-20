---
date: 2019-10-11
keywords: json, .json, json file format, how to open json files, javascript object notation, json data format, .json file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON ফাইল ফরম্যাট - একটি JSON ফাইল কিe?
linktitle: JSON
description: LJSON ফাইল ফরম্যাট এবং API সম্পর্কে আয় করুন যা JSON ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## একটি JSON ফাইল কি?

JSON (জাভাস্ক্রিপ্ট অবজেক্ট নোটেশন) হল ডেটা শেয়ার করার জন্য একটি ওপেন স্ট্যান্ডার্ড ফাইল ফরম্যাট যা ডেটা সঞ্চয় ও প্রেরণের জন্য মানব-পাঠযোগ্য পাঠ্য ব্যবহার করে। JSON ফাইল .json এক্সটেনশনের সাথে সংরক্ষণ করা হয়। JSON এর কম বিন্যাস প্রয়োজন এবং এটি [XML](/web/xml/) এর জন্য একটি ভাল বিকল্প৷ JSON জাভাস্ক্রিপ্ট থেকে প্রাপ্ত তবে এটি একটি ভাষা-স্বাধীন ডেটা বিন্যাস। JSON-এর জেনারেশন এবং পার্সিং অনেক আধুনিক প্রোগ্রামিং ভাষা দ্বারা সমর্থিত। *application/json* হল JSON-এর জন্য ব্যবহৃত মিডিয়া প্রকার।

## JSON ফাইল বিন্যাস - সংক্ষিপ্ত ইতিহাস

There was a need for real-time server to client communication that lead to the creation of JSON. The JSON format was first specified by Douglas Crockford in March 2001. JSON স্ট্যান্ডার্ড ECMA-262 3য় সংস্করণের উপর ভিত্তি করে তৈরি হয়েছিল—ডিসেম্বর 1999 যা জাভাস্ক্রিপ্টের একটি উপসেট।

The first edition of JSON standard ECMA-404 was published in October 2013 by Ecma International. RFC 7159 became the main reference for JSON's Internet uses in 2014. নভেম্বর 2017 সালে, ISO/IEC 21778:2017 একটি আন্তর্জাতিক মান হিসাবে প্রকাশিত হয়েছিল। RFC 8259 13 ডিসেম্বর 2017 এ ইন্টারনেট ইঞ্জিনিয়ারিং টাস্ক ফোর্স দ্বারা প্রকাশিত হয়েছিল যা ইন্টারনেট স্ট্যান্ডার্ড STD 90 এর বর্তমান সংস্করণ।

## JSON ফাইল স্ট্রাকচার

JSON ডেটা **কী/মান** জোড়ায় লেখা হয়। কী এবং মান মাঝখানে একটি কোলন(:) দ্বারা বাম দিকের কী এবং ডানদিকের মান দিয়ে আলাদা করা হয়েছে। বিভিন্ন কী/মান জোড়া একটি কমা(,) দ্বারা পৃথক করা হয়। কী হল একটি স্ট্রিং যার চারপাশে ডবল উদ্ধৃতি চিহ্ন রয়েছে যেমন নাম। মান নিম্নলিখিত ধরনের হতে পারে.

- 'সংখ্যা
- `স্ট্রিং`: ডবল উদ্ধৃতি চিহ্ন দ্বারা বেষ্টিত ইউনিকোড অক্ষরের ক্রম।
- `বুলিয়ান`: সত্য বা মিথ্যা।
- `অ্যারে`: বর্গাকার বন্ধনী দ্বারা বেষ্টিত মানগুলির একটি তালিকা, উদাহরণস্বরূপ

``জসন
[আপেল, কলা, কমলা]
```

- `অবজেক্ট`: কোঁকড়া ধনুর্বন্ধনী দ্বারা বেষ্টিত কী/মান জোড়ার একটি সংগ্রহ, উদাহরণস্বরূপ

``জসন
{নাম: জ্যাক, বয়স: ৩০, প্রিয় খেলা : ফুটবল}
```

JSON অবজেক্টগুলিও ডেটার গঠন উপস্থাপন করতে নেস্ট করা যেতে পারে। নীচে একটি JSON অবজেক্টের উদাহরণ দেওয়া হল।

### JSON ফর্ম্যাটের উদাহরণ

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## JSON ফাইলের সর্বোচ্চ আকার কত?

JSON ফাইলের সর্বোচ্চ আকারের কার্যত কোন সীমা নেই। বিষয়বস্তু সংরক্ষণ করার জন্য প্রয়োজনীয় স্থান হিসাবে এটি দীর্ঘ হতে পারে।

যখন ইন্টারনেটে ডেটা স্থানান্তর করার জন্য JSON ফাইল ফর্ম্যাট ব্যবহার করার কথা আসে, তখন কম্পিউটারের উপলব্ধ সংস্থানগুলি সম্পর্কে সতর্ক হওয়া দরকার। বড় JSON ডেটা স্থানান্তর করা হলে, ক্লায়েন্ট ব্রাউজারে সীমিত মেমরি থাকলে স্থানান্তর প্রভাবিত হবে।


স্পেসিফিকেশন দ্বারা সংজ্ঞায়িত কোন কঠিন সীমা নেই, তবে আপনার ব্যবহারকারীদের কম্পিউটারে সংস্থান শেষ না করার বিষয়ে আপনাকে সতর্ক থাকতে হবে, কারণ এটি তাদের ব্যবহারকারীর অভিজ্ঞতাকে দ্রুত অবনমিত করবে এবং তারা সম্ভবত আপনার অ্যাপটি ত্যাগ করবে।

## JSON বনাম XML

**XML** হল ইন্টারনেটে ডেটা আদান-প্রদানের জন্য আরেকটি সাধারণ এবং বহুল ব্যবহৃত ফাইল ফরম্যাট। যখন অ্যাপ্লিকেশনগুলির মধ্যে ডেটা বিনিময়ের কথা আসে, তখন বিকাশকারীদের কাছে XML এবং JSON ফাইল ফর্ম্যাট উভয়ই ব্যবহার করার বিকল্প থাকে। যাইহোক, JSON নিম্নলিখিত কারণে ইন্টারনেটে অ্যাপ্লিকেশনগুলির মধ্যে ডেটা বিনিময়ের জন্য সবচেয়ে সুবিধাজনক উপায় হিসাবে গৃহীত হয়৷

 1. JSON XML ফাইল ফরম্যাটের তুলনায় ডেটার একটি পরিষ্কার এবং সহজে পড়ার দৃশ্য দেয়
 1. JSON ইন্টারনেটে ডেটা স্থানান্তরের ওভারহেড হ্রাস করে কারণ এতে XML-এর তুলনায় ডেটার একই সেট সংজ্ঞায়িত করার জন্য অক্ষরের সংখ্যা কম থাকে
 1. আধুনিক প্রোগ্রামিং ভাষাগুলি ওয়েবে JSON প্রতিক্রিয়া পার্স করার জন্য বিল্টইন পার্সার প্রদান করে।

## FAQs

 * **JSON ফাইলটি কিসের জন্য ব্যবহার করা হয়?** JSON ফাইল ফরম্যাটটি একটি ওয়েবসাইটে জমা দেওয়া ফর্ম থেকে ডেটা তৈরি করা ডেটা সংরক্ষণের জন্য একটি মধ্যবর্তী ফাইল ফর্ম্যাট হিসাবে ব্যবহার করা যেতে পারে। এটি যেকোন প্রোগ্রামিং ভাষার জন্য ডেটা ফরম্যাট ফাইল হিসাবেও ব্যবহৃত হয় এবং বিভিন্ন ধরণের ডেটার মধ্যে আন্তঃঅপারেবিলিটি প্রদান করে।
 * **JSON এবং XML ফাইল কি একই?** আসলেই না। JSON XML থেকে আলাদা যে JSON ছোট, পড়া যায় এবং ঠিক দ্রুত, অ্যারে ব্যবহার করতে পারে এবং এটি শেষ ট্যাগ ব্যবহার করে না।
 * **Can I convert JSON to CSV?** Yes, there are certain online converter apps such as **GroupDocs Conversion apps** that can [convert JSON to CSV](https://products.groupdocs.app/conversion/json-to-csv).
 * **কিভাবে JSON কে PDF তে রূপান্তর করবেন?** আপনি সেলের জন্য Asopse.app এর মতো অনলাইন অ্যাপ ব্যবহার করতে পারেন [JSON ফাইলকে PDF এ কনভার্ট করুন](https://products.aspose.app/cells/conversion/json-to- পিডিএফ)।
 * **কীভাবে Word-এ JSON ফাইল খুলবেন?** আপনি Aspose.app-এর মতো অনলাইন অ্যাপ ব্যবহার করতে পারেন [JSON ফাইলকে Word-এ রূপান্তর করুন](JSON ফরম্যাটকে Android-এ জাভা-এর মাধ্যমে WORD-এ রূপান্তর করুন)।

## তুমি কি জানতে?

You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about JSON or Web file formats, you can post your findings in [Web File Format News](https://news.fileformat.com/t/Web) section for people to learn more form these.

## তথ্যসূত্র

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [An Introduction to JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)
