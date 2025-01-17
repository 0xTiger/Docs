{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PDF/A ফাইল ফরম্যাট",
  "description": "PDF/A ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি PDF/A ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "PDF/A",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-a-bn"
    }
  },
  "lastmod": "2019-09-10"
}

# PDF/A কি? #

PDF/A পিডিএফ ফরম্যাটে ইলেকট্রনিক নথি সংরক্ষণের জন্য একটি ISO স্ট্যান্ডার্ড বিন্যাস। এর অস্তিত্বে আসার প্রাথমিক কারণ ছিল দীর্ঘমেয়াদী সংরক্ষণাগারের প্রয়োজনীয়তা পূরণ করা। স্ট্যান্ডার্ড কনফারেন্স অর্জনের জন্য নথির অবিচ্ছেদ্য অংশগুলিতে নির্দিষ্ট সীমাবদ্ধতা আরোপ করে দীর্ঘ সময় পরেও সংরক্ষণাগারভুক্ত ফাইলগুলি খোলার বিষয়টি নিশ্চিত করে। বিন্যাসটি এখন সমস্ত শিল্প জুড়ে ব্যাপকভাবে গৃহীত হয়। Adobe Acrobat Reader-এর মতো PDFA/A দর্শকরা নিশ্চিত করে যে এই ফর্ম্যাটে সংরক্ষিত ফাইলগুলি ভবিষ্যতেও এই স্ট্যান্ডার্ডের শেয়ার করা তথ্য অনুযায়ী খোলা যাবে।

## PDF/A সংস্করণ ##

PDF/A was accepted as ISO Standard in October 2005. তারপর থেকে, এটি ক্রমাগত বর্ধনের অধীনে রয়েছে এবং সময়ের সাথে সাথে আরও কয়েকটি মান তৈরি করা হয়েছে। সময়ের সাথে সাথে প্রকাশিত PDF/A মান সম্পর্কে তথ্য এবং তাদের বিশদ বিবরণ নিম্নরূপ:

* **PDF/A-1:** অক্টোবর 2005 সালে ISO 19005-1 হিসাবে প্রকাশিত এবং PDF 1.4 এর উপর ভিত্তি করে

* **PDF/A-2:** জুন 2011 সালে ISO 19005-2 হিসাবে প্রকাশিত এবং PDF 1.7 এর উপর ভিত্তি করে (ISO 32000-1:2008)

* **PDF/A-3:** অক্টোবর 2012 সালে ISO 19005-3 হিসাবে প্রকাশিত এবং PDF 1.7 এর উপর ভিত্তি করে (ISO 32000-1:2008)


## PDF/A-1 ##

PDF/A-1 মানটি মূল PDF 1.4 সংস্করণের উপর ভিত্তি করে ছিল। পিডিএফ/এ-1 স্ট্যান্ডার্ড পিডিএফ ফাইলগুলির জন্য দুটি স্তরের মান নির্ধারণ করে।

### PDF/A-1a ###

এটি লেভেল A-এর সাথে সামঞ্জস্যপূর্ণ এবং PDF/A-1 স্ট্যান্ডার্ডের স্পেসিফিকেশনে সমস্ত প্রয়োজনীয়তা পূরণ করে। PDF/A-1a নিশ্চিত করে যে পাঠ্য নথি থেকে নিষ্কাশনযোগ্য। এটি নিশ্চিত করে যে সমন্বিত পাঠ্য উপাদানের স্বাভাবিক পঠন প্রক্রিয়া অক্ষত থাকবে। পিডিএফ/এ পুনর্গঠন করে হ্রাসকৃত স্ক্রিনে পাঠ্য উপস্থাপনের ক্ষমতার জন্য প্রয়োজনীয়তা আরোপ করে যা ট্যাগ করা PDF নামে পরিচিত। এটি সহায়ক সফ্টওয়্যারকে অনুমতি দিয়ে শারীরিকভাবে প্রতিবন্ধী ব্যবহারকারীদের জন্য ফাইলগুলির অ্যাক্সেসযোগ্যতা বাড়ানোর উদ্দেশ্যে ছিল।

### PDF/A-1b ###

PDF/A-1b হল একটি নিম্ন স্তরের সামঞ্জস্য এবং ISO 19005 স্ট্যান্ডার্ডের সাপেক্ষে ইলেকট্রনিক নথিগুলির চাক্ষুষ উপস্থিতি নিয়ে কাজ করে। এটি নিশ্চিত করে যে পৃষ্ঠাগুলিতে পাঠ্য এবং অন্যান্য বিষয়বস্তু একইভাবে পুনরুত্পাদন করা হয়েছে। এই লেভেল বি কনফরমেন্স ন্যূনতম সম্মতি নির্দেশ করে যে একটি কনফর্মিং ফাইলের রেন্ডার করা ভিজ্যুয়াল চেহারা দীর্ঘ মেয়াদে সংরক্ষণযোগ্য।

## PDF/A-2 ##

PDF/A-2 was released by ISO Standard in July 2011 as a new standard known as ISO 32001-1. এই নতুন স্ট্যান্ডার্ডটি শুধুমাত্র 1.7 পর্যন্ত পিডিএফ সংস্করণের সমস্ত বৈশিষ্ট্য থেকে উপকৃত হয়নি, এটি একটি নতুন মান হিসাবেও চালু করা হয়েছিল। PDF/A-2 এই নতুন স্ট্যান্ডার্ডের অংশ হিসাবে নিম্নলিখিত বৈশিষ্ট্যগুলি অন্তর্ভুক্ত করেছে।

* PDF/A-2 [JPEG2000](/image/jp2/) এর সমর্থনে আসে যা স্ক্যান করা নথির ক্ষেত্রে সহায়ক।

* এটি PDF/A সংগ্রহের এমবেডিং সমর্থন করে যা অন্যান্য অনুরূপ ফাইল সহ একটি ধারক PDF তৈরি করতে ব্যবহার করা যেতে পারে

* এটি PDF/A-1 এর তুলনায় সম্পূর্ণভাবে PDF ফাইলের স্বচ্ছতা বৈশিষ্ট্য সমর্থন করে যেখানে এটি আংশিকভাবে সমর্থিত ছিল।

* PDF/A-2 ঐচ্ছিক বিষয়বস্তুর জন্য সমর্থন প্রদান করে যা ম্যাপিং অ্যাপ্লিকেশন এবং ইঞ্জিনিয়ারিং অঙ্কনের জন্য দরকারী। এগুলি স্তর হিসাবেও পরিচিত যা দেখার ব্যক্তির প্রয়োজনীয়তা অনুসারে দৃশ্যমান বা লুকানো যায়।

* এটি কাস্টম XMP মেটাডেটার জন্য প্রয়োজনীয়তা নির্দিষ্ট করে

* নিষিদ্ধ টীকা প্রকারের তালিকায় কিছু নতুন মন্তব্যের প্রকার যোগ করে। এছাড়াও, কিছু নতুন মন্তব্যের ধরন যেমন পাঠ্য সম্পাদনা মন্তব্যগুলি গ্রহণযোগ্য আইটেমগুলির তালিকায় যুক্ত করা হয়েছিল৷


## PDF/A-3 ##

PDF/A-3-এ লেভেল 2-এর সমস্ত সামঞ্জস্যের প্রয়োজনীয়তা রয়েছে এবং অতিরিক্ত ফাইল ফরম্যাট (যেমন XML, [CSV](/spreadsheet/csv/), [CAD](/cad/), [word-processing](/word-processing/) , [spreadsheet](/spreadsheet/) এবং অন্যান্যগুলি এম্বেড করার অনুমতি দেয় ) পিডিএফ/এ কনফার্মিং ডকুমেন্টে।

## তথ্যসূত্র ##

* [PDF/A - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/PDF/A)

* [সাদা কাগজ: PDF/A – দ্য বেসিক](https://www.pdf-tools.com/public/downloads/whitepapers/whitepaper-pdfa.pdf)


