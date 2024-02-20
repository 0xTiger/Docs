{
  "date": "2021-03-01",
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "title": "RDL - রিপোর্ট সংজ্ঞা ভাষা ফাইল",
  "keywords": [
    "rdl",
    "report definition language",
    "XmlTextWriter",
    "XSD",
    "RDL element"
  ],
  "description": "RDL ফাইল ফর্ম্যাট সম্পর্কে জানুন যা একটি SQL সার্ভার রিপোর্টিং পরিষেবা রিপোর্ট সংজ্ঞার একটি XML উপস্থাপনা।",
  "linktitle": "RDL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rdl-bn"
    }
  },
  "lastmod": "2021-03-01"
}

## একটি RDL ফাইল কি? ##

RDL (রিপোর্ট ডেফিনিশন ল্যাঙ্গুয়েজ) হল রিপোর্ট সংজ্ঞায়িত করার জন্য মাইক্রোসফট দ্বারা সেট করা একটি বেঞ্চমার্ক। একটি RDL ফাইল এক বা একাধিক RDL উপাদান নিয়ে গঠিত। যেখানে একটি RDL উপাদান এর ডেটা টাইপ এবং কার্ডিনালিটি নিয়ে গঠিত। একটি উপাদান সহজ বা জটিল হতে পারে। সাধারণ উপাদানটির কোনো শিশু উপাদান বা বৈশিষ্ট্য নেই, যেখানে একটি জটিল উপাদানের শিশু এবং ঐচ্ছিক বৈশিষ্ট্য রয়েছে।

## RDL XML স্কিমা সংজ্ঞা
একটি XML স্কিমা ডেফিনিশন (XSD) ফাইল RDL ফাইলটিকে বৈধ করে। স্কিমা একটি .rdl ফাইলে RDL উপাদানগুলি কোথায় ঘটতে পারে তার নিয়মগুলি সংজ্ঞায়িত করে। একটি RDL উপাদান সহজ বা জটিল হতে পারে। একটি সাধারণ উপাদানের শিশু উপাদান বা বৈশিষ্ট্য থাকে না এবং একটি জটিল উপাদানের শিশু এবং ঐচ্ছিকভাবে, বৈশিষ্ট্য থাকে।

## RDL তৈরি করা হচ্ছে
যেহেতু RDL প্রকৃতিতে উন্মুক্ত এবং সম্প্রসারণযোগ্য, তাই অনেক অ্যাপ্লিকেশন এবং টুল তৈরি করা যেতে পারে যা এর XML স্কিমার উপর ভিত্তি করে RDL ফাইল তৈরি করে। একটি অ্যাপ্লিকেশন থেকে RDL তৈরি করার সবচেয়ে সহজ উপায় হল **System.Xml** নামস্থান এবং System.Linq নামস্থানের Microsoft .NET ফ্রেমওয়ার্ক ক্লাসগুলি ব্যবহার করা। বিশেষ করে, **XmlTextWriter** ক্লাস, RDL লিখতে ব্যবহার করা যেতে পারে। আপনি **XmlTextWriter** ব্যবহার করে যেকোনো .NET ফ্রেমওয়ার্ক অ্যাপ্লিকেশনে শুরু থেকে শেষ পর্যন্ত একটি সম্পূর্ণ রিপোর্ট সংজ্ঞা তৈরি করতে পারেন। বিকাশকারীরা RDL প্রসারিত করতে কাস্টম বৈশিষ্ট্য সহ কাস্টম রিপোর্ট আইটেম যোগ করতে পারেন।

## আরডিএল প্রকার
নিম্নলিখিত সারণী RDL উপাদানগুলিতে ব্যবহৃত প্রকার এবং বৈশিষ্ট্যগুলি তালিকাভুক্ত করে৷

|প্রকার|বর্ণনা|
---|---|
|বাইনারি |বেস-64 এনকোডেড বাইনারি মান সহ একটি সম্পত্তি।|
|বুলিয়ান | বস্তুর মান হিসাবে সত্য বা মিথ্যা সহ একটি সম্পত্তি। অন্যথায় নির্দিষ্ট না হলে, বাদ দেওয়া ঐচ্ছিক বুলিয়ান বস্তুর মান হল False.|
|Date	|A property with a fully specified date or datetime value specified in ISO8601 date format: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum | একটি স্ট্রিং টেক্সট মান সহ একটি সম্পত্তি যা অবশ্যই মনোনীত মানের তালিকার একটি হতে হবে।|
|ফ্লোট | ফ্লোট মান সহ একটি সম্পত্তি। একটি সময়কাল (.) ঐচ্ছিক দশমিক বিভাজক হিসাবে ব্যবহৃত হয়।|
|পূর্ণসংখ্যা | একটি পূর্ণসংখ্যা (int32) মান সহ একটি সম্পত্তি।|
ভাষা মানটি অবশ্যই একটি নির্দিষ্ট ভাষা বা একটি নিরপেক্ষ ভাষা হতে হবে যার জন্য Microsoft .NET ফ্রেমওয়ার্কে একটি ডিফল্ট ভাষা সংজ্ঞায়িত করা হয়েছে৷|
|নাম |স্ট্রিং টেক্সট মান সহ একটি সম্পত্তি। নাম অবশ্যই আইটেমের নামস্থানের মধ্যে অনন্য হতে হবে। যদি নির্দিষ্ট করা না থাকে, তাহলে একটি আইটেমের নামস্থান হল সবচেয়ে ভিতরের বস্তু যার একটি নাম আছে।|
|NormalizedString|স্ট্রিং টেক্সট মান সহ একটি সম্পত্তি যা স্বাভাবিক করা হয়েছে।|
|আকার একটি সিএসএস দৈর্ঘ্য ইউনিট যেমন cm, mm, in, pt, বা pc-এর জন্য নম্বরটি অবশ্যই একজন মনোনীতকারী দ্বারা অনুসরণ করা উচিত। সংখ্যা এবং মনোনীতকারীর মধ্যে একটি স্থান ঐচ্ছিক। সাইজ ডিজাইনার সম্পর্কে আরও তথ্যের জন্য, CSS মান এবং ইউনিট রেফারেন্স দেখুন। RDL-এ, সাইজের সর্বোচ্চ মান হল 160 ইঞ্চি। সর্বনিম্ন মাপ হল 0 ইঞ্চি।|
|স্ট্রিং |স্ট্রিং টেক্সট মান সহ একটি সম্পত্তি।|
|আনসাইনডইন্ট |একটি স্বাক্ষরবিহীন পূর্ণসংখ্যা (uint32) মান সহ একটি সম্পত্তি৷|
|ভেরিয়েন্ট |যেকোন সাধারণ XML প্রকার সহ একটি সম্পত্তি।|

## RDL ডেটা প্রকার
RDL-এ, DataType গণনা একটি বৈশিষ্ট্য, অভিব্যক্তি, বা প্যারামিটারের ডেটা প্রকারকে সংজ্ঞায়িত করে। নিম্নলিখিত সারণী দেখায় কিভাবে CLR ডেটা প্রকারগুলি RDL ডেটা প্রকারের সাথে মিলে যায়৷

|CLR প্রকার(গুলি) |সংশ্লিষ্ট ডেটা টাইপ|
---|---|
|বুলিয়ান | বুলিয়ান|
|তারিখ সময়, তারিখ সময়অফসেট |তারিখ সময় |
|Int16, Int32, UInt16, বাইট, SByte |পূর্ণসংখ্যা|
|একক, ডাবল |ফ্লোট |
|স্ট্রিং, চর, GUID, টাইমস্প্যান |স্ট্রিং|


## তথ্যসূত্র ##

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)
