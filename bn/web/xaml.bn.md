{
  "date": "2019-10-11",
  "keywords": [
    "xaml",
    "xaml file",
    "xaml file format",
    "xaml file type",
    "file",
    "type",
    "what is an xaml file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "XAML - XML ভিত্তিক মার্কআপ ভাষা",
  "description": "XAML ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি XAML ফাইলগুলি তৈরি এবং খুলতে পারে।",
  "linktitle": "XAML ",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xaml-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি XAML ফাইল কি?

XAML, এক্সটেনসিবল অ্যাপ্লিকেশন মার্কআপ ল্যাঙ্গুয়েজ, এক্সটেনশন ফাইলগুলি উইন্ডোজ প্রেজেন্টেশন ফাউন্ডেশন (WPF) এর উপর ভিত্তি করে সফ্টওয়্যার অ্যাপ্লিকেশনগুলির জন্য ব্যবহারকারী ইন্টারফেস উপাদানগুলি বর্ণনা করে। যদিও একটি ভাষা, এটি প্রোগ্রাম করার প্রয়োজন নেই কারণ এটি **[XML](/web/xml/)** এর স্ট্যান্ডার্ড ফর্ম্যাটের উপর ভিত্তি করে যা ব্যবহার করা এবং বোঝা সহজ। এক্সএএমএল (জ্যামেল হিসাবে উচ্চারিত) মাইক্রোসফ্ট দ্বারা ব্যবহারকারী ইন্টারফেস তৈরির জন্য নির্দিষ্ট লক্ষ্যে তৈরি করা হয়েছিল। এর সংক্ষিপ্ত রূপটি ছিল এক্সটেনসিবল অ্যাভালন মার্কআপ ল্যাঙ্গুয়েজ, যেখানে অ্যাভালন ছিল WPF-এর কোড-নাম। XAML ফাইলগুলি কখনও কখনও XOML এক্সটেনশনের সাথেও সংরক্ষণ করা হয়।

## XAML অ্যাপ্লিকেশন

XAML হল .NET Framework 3.0 এবং .NET Framework 4.0 প্রযুক্তি যেমন WPF, Silverlight, Windows Workflow Foundation (WF) এবং আরও কয়েকটিতে ব্যবহারের পছন্দ। UI উপাদান, ডেটা বাইন্ডিং, ইভেন্ট এবং অন্যান্য বৈশিষ্ট্যগুলি WPF-এ XAML ফর্ম দ্বারা সংজ্ঞায়িত করা হয়। একইভাবে, WF-এ কর্মপ্রবাহ XAML ব্যবহার করে সংজ্ঞায়িত করা যেতে পারে। এটি XML-এর উপর ভিত্তি করে এই কারণে সহজে সরঞ্জাম দ্বারা প্রক্রিয়া করা হয়। যেহেতু এটি একটি ঘোষণামূলক ভাষা এবং এটির সংকলনের প্রয়োজন নেই, তাই XAML-ভিত্তিক অ্যাপ্লিকেশনগুলির উপর ভিত্তি করে প্রচুর পণ্য উদ্ভূত হচ্ছে। XAML-এ যেকোন কিছু তৈরি বা প্রয়োগ করা হয় তা আরও প্রথাগত .NET ভাষা ব্যবহার করে প্রকাশ করা যেতে পারে, যেমন C# বা Visual Basic .NET।

## XAML ফাইল ফরম্যাট

XAML is totally based on the XML format. The initial specifications of [XAML Object Mapping](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML%5D.pdf) were published in 2006, followed by another [version](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf) published in 2009. এই স্পেসিফিকেশন দুটি বিমূর্ত তথ্য মডেল সংজ্ঞায়িত করে:

* XAML স্কিমা তথ্য সেট মডেল

* XAML তথ্য সেট মডেল


Xaml তথ্য সেট (সংক্ষেপে 'Xaml ইনফোসেট') তথ্যের কাঠামোকে সংজ্ঞায়িত করে যা একটি Xaml উদাহরণ উপস্থাপন করতে পারে। Xaml স্কিমা তথ্য সেট নির্দিষ্ট Xaml শব্দভান্ডারকে সংজ্ঞায়িত করার অনুমতি দেয়। এই স্পেসিফিকেশনটি XML নথিকে Xaml তথ্য সেটে রূপান্তর করার জন্য নিয়মগুলির একটি সেটও সংজ্ঞায়িত করে। XML হল Xaml-এর জন্য একটি সাধারণ বিন্যাস। (Xaml ডকুমেন্ট শব্দটি একটি XML নথিকে বোঝায় যা একটি Xaml তথ্য সেটের প্রতিনিধিত্ব করে।) কিন্তু যদিও এই স্পেসিফিকেশনটি অন্য কোনও উপস্থাপনাকে সংজ্ঞায়িত করে না, যে কোনও শারীরিক উপস্থাপনা ততক্ষণ ব্যবহার করা যেতে পারে যতক্ষণ না এটি Xaml তথ্য সেটের তথ্য উপস্থাপন করতে পারে। .

## তথ্যসূত্র

* [XAML - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Extensible_Application_Markup_Language)

* [XAML ফাইল ফর্ম্যাট স্পেসিফিকেশন](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf)

