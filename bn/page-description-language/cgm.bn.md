{
  "date": "2019-10-11",
  "keywords": [
    "CGM",
    "Computer Graphics Metafile",
    "File",
    "Extension",
    "File Format",
    "Vector Graphics",
    "Metafile Descriptor"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "CGM ফাইল ফরম্যাট",
  "description": "CGM ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি CGM ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "CGM",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-cgm-bn"
    }
  },
  "lastmod": "2021-04-23"
}

## একটি CGM ফাইল কি? ##

কম্পিউটার গ্রাফিক্স মেটাফাইল (CGM) হল বিনামূল্যে, প্ল্যাটফর্ম-স্বাধীন, ভেক্টর গ্রাফিক্স (2D), রাস্টার গ্রাফিক্স এবং টেক্সট সংরক্ষণ ও বিনিময়ের জন্য আন্তর্জাতিক মানের মেটাফাইল বিন্যাস। CGM ইমেজ উৎপাদনের জন্য একটি অবজেক্ট-ওরিয়েন্টেড পদ্ধতি এবং অনেক ফাংশন বিধান ব্যবহার করে। CGM এই অবজেক্ট-ওরিয়েন্টেড বৈশিষ্ট্যগুলি ব্যবহার করে একটি চিত্র রেন্ডার করার জন্য গ্রাফিকাল উপাদানগুলিকে রিমল্ড করার জন্য। একটি মেটাফাইলে প্রয়োজনীয় তথ্য থাকে যা অন্যান্য ফাইলকে সংজ্ঞায়িত করে। CGM-এ, একটি টেক্সট-ভিত্তিক সোর্স ফাইলে সমস্ত গ্রাফিকাল উপাদান থাকে যা পরে একটি বাইনারি ফাইলে কম্পাইল করা যেতে পারে। মূলত, CGM হল 2D গ্রাফিকাল ডেটা আদান-প্রদান সহজতর করার একটি উপায়, কোনো নির্দিষ্ট প্ল্যাটফর্ম বা ডিভাইস থেকে স্বাধীন।

CGM ফরম্যাট ফাংশন সঞ্চালনের জন্য বিভিন্ন উপাদান প্রদান করে, এবং জ্যামিতিক আদিম এবং গ্রাফিকাল তথ্য সামঞ্জস্য করার জন্য বস্তুকে নির্দেশ করে। যদিও CGM ওয়েব পৃষ্ঠাগুলিতে গ্রাফিক আর্টগুলি প্রদর্শনের জন্য অন্যান্য ফর্ম্যাটগুলির দ্বারা বাতিল করা হয়েছে কারণ এটি ওয়েব পৃষ্ঠাগুলি দ্বারা সমর্থিত নয়, তবুও এটি শিল্প, বৈমানিক এবং অন্যান্য প্রযুক্তিগত অ্যাপ্লিকেশনগুলির মধ্যে খুব জনপ্রিয়। যদিও ওয়ার্ল্ড ওয়াইড ওয়েব কনসোর্টিয়াম ওয়েবসিজিএম তৈরি করেছে, ওয়েবে সিজিএম ব্যবহারের জন্য একটি বিকল্প পদ্ধতি। প্রাথমিক CGM বাস্তবায়ন ছিল গ্রাফিক্যাল কার্নেল সিস্টেমের (GKS) মৌলিক ক্রিয়াকলাপের অনুক্রমের একটি চিত্র। এটি পেশাদার ডিজাইনে খুব বেশি গৃহীত হয়নি তবে এটি মূলত DXF এবং SVG এর মতো অন্যান্য ফর্ম্যাট দ্বারা প্রতিস্থাপিত হয়েছে।

## ইতিহাস ##

CGM 1987 সালে একটি আন্তর্জাতিক মান হিসাবে পরিণত হয়েছিল (ISO 8632-1987) এবং BSI এবং USA দ্বারা ANSI দ্বারা যুক্তরাজ্যে একটি জাতীয় মান হিসাবেও গৃহীত হয়েছিল। 1991 সালে বেশ কয়েকটি সংশোধনীর পর 1992 সালে CGM-এর একটি সংশোধিত মান প্রকাশিত হয়েছিল (ISO 8632:1992)। 2001 সালে, ওয়ার্ল্ড ওয়াইড ওয়েব কনসোর্টিয়াম ওয়েবপেজগুলির সাথে ব্যবহার করার জন্য উন্নত ক্ষমতা সহ WebCGM তৈরি করেছে। 2007 সালে WebCGM-এর দ্বিতীয় সংস্করণ প্রকাশিত হয়েছিল এবং 2010 সালে উন্নত ক্ষমতা সহ তৃতীয় সংস্করণ প্রকাশিত হয়েছিল।

## CGM ফাইল ফরম্যাট ##

কম্পিউটার গ্রাফিক্স মেটাফাইলগুলি মূলত গ্রাফিকাল তথ্যের জন্য ডাটাবেস এবং গ্রাফিকাল ডেটা ক্যাপচার, স্টোরেজ এবং সংক্রমণের উপায় সরবরাহ করে। ফলস্বরূপ, একটি মেটাফাইল বিন্যাসে একটি অ্যাপ্লিকেশন কার্যকর করার পাশাপাশি ডাটাবেস তৈরি করার জন্য একটি গ্রাফিক্যাল সিস্টেম উপাদান থাকতে হবে। বেশিরভাগ ক্ষেত্রে, এই উপাদানটি মেটাফাইল জেনারেটর। পাশাপাশি, আরেকটি উপাদানের প্রয়োজন রয়েছে যা একটি মেটাফাইলে গ্রাফিকাল ডেটা আনতে, ব্যাখ্যা করতে এবং রেন্ডার করতে পারে। এই প্রয়োজন মেটাফাইল দোভাষীর উপস্থিতি দ্বারা পূরণ করা হয়. নিচের চিত্রটি গ্রাফিকাল মেটাফাইল কাজের পরিবেশ উপস্থাপন করে।

একটি সাধারণ গ্রাফিক্স সিস্টেমের অন্যান্য উপাদানের সাথে CGM-এর সম্পর্ক উপরের চিত্রে দেখানো হয়েছে। এটি চিত্র থেকেও স্পষ্ট যে মেটাফাইলের কার্যকারিতা চূড়ান্ত ডিভাইস আউটপুটের উপর নির্ভর করে না।

Generally, there are two categories of metafile: **section capture** and **picture capture**. The primary functionality of picture capture metafile is the capturing of device-independent, multiple picture definitions. While session capture metafiles use the system interface to capture the output dialogue in a graphical system. CGM belongs to the category of static picture capture metafiles. CGM provides a well-organized arrangement of components with a two-level structure.

1. মেটাফাইল বর্ণনাকারী
1. যৌক্তিকভাবে স্বাধীন ছবির একটি পুল

প্রতিটি ছবি হল ছবি বর্ণনাকারীর একটি সংগ্রহ এবং একটি ছবির সংজ্ঞা সহ একটি ছবির বডি। মেটাফাইল বর্ণনাকারী বর্ণনামূলক তথ্য সংজ্ঞায়িত করে যা সেই মেটাফাইলের সমস্ত ছবির ক্ষেত্রে সমানভাবে প্রযোজ্য। এই তথ্য দোভাষীকে একটি মেটাফাইলকে সঠিকভাবে পার্স করতে এবং ছবির সঠিক রেন্ডারিংয়ের জন্য প্রয়োজনীয় সংস্থানগুলি চিনতে সাহায্য করে। যদিও ছবির বর্ণনাকারী বর্ণনামূলক তথ্যও ঘেরাও করে তবুও এটি শুধুমাত্র সেই চিত্রটিকে চিনতে পারে যেখানে বর্ণনাকারী থাকেন। এই ফাইল বিন্যাসে, প্রতিটি ছবির সংজ্ঞা স্বয়ংসম্পূর্ণ এবং যৌক্তিকভাবে সার্বভৌম। তারা একটি ফাইলের অন্যান্য সমস্ত ছবির সংজ্ঞা থেকে স্বাধীন। মেটা-ডেসক্রিপ্টারের ব্যাখ্যার পরে, ছবিগুলি এলোমেলোভাবে অ্যাক্সেস এবং ব্যাখ্যা করা যেতে পারে। আগের ছবিগুলোর অবস্থার পরিবর্তন তাদের উত্তরসূরিদের ওপর কোনো প্রভাব ফেলেনি। এই ছবির স্বাধীনতা হল CGM-এর আরেকটি বিশিষ্ট বৈশিষ্ট্য। CGM স্থানাঙ্ক স্থান নিয়ে গঠিত যা 2D কার্টেসিয়ান স্থানাঙ্ক যাকে ভার্চুয়াল ডিভাইস স্থানাঙ্ক বলা হয় এবং পরিসীমা এবং গ্রানুলারিটির প্রতিনিধিত্বকারী সংখ্যা বা নির্ভুলতার মাধ্যমে উপস্থাপন করা যেতে পারে। CGM রঙের সরাসরি নির্বাচন এবং সূচক-ভিত্তিক নির্বাচন উভয়ই নির্দিষ্ট করে। পূর্বে, কালার স্পেসিফায়ারে একটি RGB ট্রিপল থাকে যখন পরে, কালার স্পেসিফায়ার একটি কালার টেবিলে একটি সূচক নির্দেশ করে।

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.