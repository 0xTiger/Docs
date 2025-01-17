{
  "date": "2021-03-09",
  "keywords": [
    "TCR",
    "Psion",
    "extension",
    "format",
    "eBook"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Psion 3 সিরিজের জন্য TCR ফাইল ফরম্যাট এবং APIs সম্পর্কে জানুন যা tcr ফাইল তৈরি এবং খুলতে পারে।",
  "title": "TCR - Psion সিরিজ 3 ইবুক ফাইল",
  "linktitle": "TCR",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-tcr-bn"
    }
  },
  "lastmod": "2021-03-09"
}

## একটি TCR ফাইল কি?

90 এর দশকের গোড়ার দিকে, টিসিআর ফাইল ফর্ম্যাটটি প্রাচীন **Psion সিরিজ 3** পামটপ ডিভাইসগুলির জন্য চালু করা হয়েছিল। কোম্পানিটি তার প্ল্যাটফর্ম-নির্দিষ্ট কম্প্রেশন ব্যবহার করেছে এবং এই ফর্ম্যাটে টেক্সট ফর্ম্যাটিংয়ের জন্য খুব সীমিত সমর্থন রয়েছে। এটি একটি ZVR ভিত্তিক ফাইল ফরম্যাট এবং PalmDOC এর তুলনায় তুলনামূলকভাবে ভালো কম্প্রেশন রেট প্রদান করে। এটি ফন্টমেশিনের সাথেও খুব ভাল কাজ করে। যদিও TCR ফাইল বিন্যাসটি একটি বন্ধ ডিভাইসের অন্তর্গত, তবুও কিছু eReaders ব্যবহার করে এই ফাইল বিন্যাসটি পড়া যেতে পারে। এই ফাইল ফরম্যাটটি সুমাত্রা পিডিএফ সহ একটি ডেস্কটপে এবং উইন্ডোজ এবং লিনাক্সে ক্যালিবার অ্যাপ্লিকেশনের সাথেও দেখা যেতে পারে।

## প্রযুক্তিগত বিবরণ

যেহেতু TCR ফাইল ফরম্যাট একটি ZVR কম্প্রেসারের উপর ভিত্তি করে তৈরি করা হয়েছে যা অনেক ফাইলকে তাদের আসল আকারের প্রায় 50% কমাতে সক্ষম। ওভার দ্বারা ব্যবহৃত কম্প্রেশন স্কিমটি একটু পুরানো। সংকুচিত ফাইলটি 256টি সম্ভাব্য চিহ্নের অভিধান দিয়ে শুরু হয় যা সংকুচিত ফাইলে দেখাতে পারে। অভিধানে এই প্রতিটি চিহ্নের জন্য একটি নির্দিষ্ট বিকল্প স্ট্রিং রয়েছে। এমনকি OPL-তেও ডিকম্প্রেশন খুব দ্রুত হয়ে গেছে এবং এটি সংকুচিত ফাইলের যেকোনো সময়ে শুরু হতে পারে।

## একটি TCR ফাইল খুলতে সমস্যা ##

আপনি যদি TCR ফাইলটি খুলতে এবং চালাতে সক্ষম না হন; এর মানে এই নয় যে আপনার ডিভাইসে উপযুক্ত সফ্টওয়্যার ইনস্টল করা নেই। অন্য কিছু সমস্যা থাকতে পারে যা ফাইলটিকে সঠিকভাবে কাজ করতে বাধা দেয়। সম্ভাব্য সমস্যাগুলি নিম্নলিখিতগুলির মধ্যে একটি হতে পারে:

- একটি টিসিআর ফাইলের দুর্নীতি।
- রেজিস্ট্রি এন্ট্রিতে TCR ফাইলের ভুল লিঙ্ক।
- Deleted description of the TCR from the Windows registry
- টিসিআর ফর্ম্যাট সমর্থন করে এমন একটি অ্যাপ্লিকেশনের দূষিত ইনস্টলেশন
- অবাঞ্ছিত ম্যালওয়্যার সহ একটি সংক্রামিত TCR ফাইল।
- কম্পিউটারে টিসিআর ফাইল পরিচালনা করার জন্য পর্যাপ্ত হার্ডওয়্যার সংস্থান নেই।
- একটি TCR ফাইল খুলতে কম্পিউটার দ্বারা ব্যবহৃত ড্রাইভারগুলি পুরানো৷




## তথ্যসূত্র

* [TCR - MobileRead দ্বারা](https://wiki.mobileread.com/wiki/TCR)

* [ZVR কমপ্রেসড টেক্সট ফাইল রিডার](https://iay.org.uk/zvr/)


