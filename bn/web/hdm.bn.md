{
  "date": "2022-10-12",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "HDM ফাইল - হ্যান্ডহেল্ড ডিভাইস মার্কআপ ল্যাঙ্গুয়েজ ফাইল",
  "description": "HDM ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা HDM ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "HDM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hdm-bn"
    }
  },
  "lastmod": "2022-10-12"
}

## একটি HDM ফাইল কি?

একটি HDM ফাইল হল একটি মার্কআপ ভাষার ওয়েবপেজ ফাইল যা হ্যান্ডহেল্ড ডিভাইস মার্কআপ ল্যাঙ্গুয়েজ (HDML) এ তৈরি করা হয়। এটিতে [HTML](/web/html/) ভাষার অনুরূপ মার্কআপ ট্যাগ রয়েছে, কিন্তু স্মার্টফোন এবং PDA-এর মতো হ্যান্ডহেল্ড ইলেকট্রনিক ডিভাইসগুলির জন্য ডিজাইন করা হয়েছে৷ [HDML file format specifications](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) স্ট্যান্ডার্ডাইজেশনের জন্য W3C-তে জমা দেওয়া হয়েছিল কিন্তু স্ট্যান্ডার্ড হয়ে উঠতে পারেনি। HDM W3 ওয়েবসাইটে উপলব্ধ [HDML](/web/hdml/) ফাইল ফর্ম্যাট স্পেসিফিকেশনের উপর ভিত্তি করে।

## HDM ফাইল ফরম্যাট - আরও তথ্য

HDM ফাইলে মার্কআপ ট্যাগ থাকে যা হ্যান্ডহেল্ড ডিভাইসে দৃশ্যত ডিজাইন করা ওয়েবসাইটে রেন্ডার করা হয়। HDM ফাইলগুলি এইচটিটিপি প্রোটোকলের পরিবর্তে HDTP (হ্যান্ডহেল্ড ডিভাইস ট্রান্সপোর্ট প্রোটোকল) প্রোটোকল ব্যবহার করে ডিভাইসে কপি করা হয় যা HTML পৃষ্ঠাগুলির জন্য ব্যবহৃত হয়।

## HDML ফাইল উপাদান

নিম্নলিখিত উপাদানগুলির একটি আলো রয়েছে যা HDML-এর জন্য রান-টাইম পরিবেশ প্রদান করে এবং এটি ব্যবহারকারী এজেন্ট হিসাবে উল্লেখ করা হয়।

|উপাদান|বর্ণনা|
---|---|
|কার্ডস|এটি HDML এর মৌলিক বিল্ডিং ব্লক, এবং ব্যবহারকারীকে তথ্যের কার্ডের সাথে ইন্টারঅ্যাক্ট করার অনুমতি দেয়। |
|ডেক্স একটি এইচডিএমএল ডেক একটি এইচটিএমএল পৃষ্ঠার অনুরূপ যে এটি URL [RFC1738] দ্বারা চিহ্নিত করা হয় এবং এটি একটি সার্ভার থেকে অনুরোধ করা সামগ্রীর একক এবং ব্যবহারকারী এজেন্ট দ্বারা ক্যাশ করা হয়৷|
|কর্ম এগুলি বিমূর্ত এবং একটি ব্যবহারকারী এজেন্ট নির্দিষ্ট পদ্ধতিতে ব্যবহারকারী ইন্টারফেসে সমর্থিত।|
|ক্রিয়াকলাপ|একটি ক্রিয়াকলাপ হল সম্পর্কিত কার্ডগুলির একটি গ্রুপের মতো যা একটি লজিক্যাল ফাংশন সম্পাদন করে। এই এক বা একাধিক ডেক স্প্যান হতে পারে. এইচডিএমএল নেভিগেশন এবং স্টেট মডেল ক্রিয়াকলাপকে ঘিরে গঠিত
|ইতিহাস-ভিত্তিক নেভিগেশন|ব্যবহারকারী এজেন্ট ব্যবহারকারীর কাছে প্রদর্শিত কার্ডের ইতিহাস বজায় রাখে। অ্যাক্সেস করা প্রতিটি কার্ড কার্ডের ইতিহাসে যোগ করা হয়। ব্যবহারকারী এজেন্ট ব্যবহারকারীকে ইতিহাসের আগের কার্ডে সহজেই নেভিগেট করতে দেয়।|

## তথ্যসূত্র

* [HDML - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [HDML স্পেসিফিকেশন - W3 স্কুল](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)


