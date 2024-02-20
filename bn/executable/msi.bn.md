{
  "date": "2021-06-30",
  "keywords": [
    "msi file",
    "MSI file format",
    "what is a msi file",
    "file",
    "msi example",
    "msi file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "MSI ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা MSI ফাইল তৈরি এবং খুলতে পারে।",
  "title": "MSI - উইন্ডোজ ইনস্টলার প্যাকেজ ফাইল",
  "linktitle": "MSI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-msi-bn"
    }
  },
  "lastmod": "2021-06-30"
}

## একটি MSI ফাইল কি?
উইন্ডোজ প্রোগ্রাম ইনস্টল এবং চালু করতে ব্যবহৃত একটি MSI ফাইল; মাইক্রোসফ্ট উইন্ডোজের জন্য একটি সম্পূর্ণ প্যাকেজ যাতে একটি সাধারণ সফ্টওয়্যার প্রোগ্রামের জন্য ইনস্টলেশনের তথ্য রয়েছে, যার মধ্যে ইনস্টল করার জন্য প্রয়োজনীয় ফাইলগুলি এবং ইনস্টলেশন অবস্থান সম্পর্কে তথ্য রয়েছে। MSI ফাইলগুলিতে সফ্টওয়্যার আপডেটের জন্য প্যাকেজও থাকতে পারে। MSI ফাইলগুলি [EXE](/executable/exe/) এর মতো, কিন্তু EXE কিছু সময় ইনস্টলারের তথ্য অন্তর্ভুক্ত নাও করতে পারে এবং EXE ফাইলটি চালানোর সময় সফ্টওয়্যার প্রোগ্রাম সরাসরি চলতে পারে।

## MSI ফাইল বিন্যাস
Windows Installer আসলে একটি API (Application Programming Interface) এবং Microsoft Windows এর সফটওয়্যার উপাদান যা একটি সফটওয়্যার প্রোগ্রামের ইনস্টলেশন, অপসারণ এবং রক্ষণাবেক্ষণের জন্য ব্যবহৃত হয়। ইনস্টলেশনের তথ্য, এবং ঐচ্ছিক ফাইলগুলি, ইনস্টলেশন প্যাকেজ হিসাবে প্যাকেজ করা হয় এবং COM স্ট্রাকচার্ড স্টোরেজ হিসাবে ঢিলেঢালাভাবে রিলেশনাল ডাটাবেস তৈরি করা হয়; .msi ফাইল এক্সটেনশন সহ **MSI ফাইল** নামে সুপরিচিত। ফাইল এক্সটেনশন **.mst** সহ প্যাকেজগুলিতে Windows ইনস্টলারের **ট্রান্সফরমেশন স্ক্রিপ্ট** থাকে, **.msm** এক্সটেনশনের ফাইলগুলিতে **মার্জ মডিউল** এবং ফাইল এক্সটেনশন **.pcp** থাকে **প্যাচ তৈরির বৈশিষ্ট্য** এর জন্য ব্যবহার করা হয়। উইন্ডোজ ইনস্টলার এর আগের সংস্করণ, সেটআপ API থেকে উল্লেখযোগ্য পরিবর্তন করার পরে আরও উন্নত হয়ে ওঠে। একটি GUI ফ্রেমওয়ার্ক এবং আন-ইনস্টলেশন সিকোয়েন্সের স্বয়ংক্রিয় প্রজন্ম হল উইন্ডোজ ইনস্টলারের নতুন বৈশিষ্ট্য। এটি এখন স্ট্যান্ড-অলোন এক্সিকিউটেবল ইনস্টলার ফ্রেমওয়ার্কের বিকল্প হিসাবে বিবেচিত হয়েছে।

### MSI প্যাকেজের যৌক্তিক কাঠামো
একটি প্যাকেজ এক বা একাধিক সম্পূর্ণ পণ্যের ইনস্টলেশনকে মনোনীত করে এবং সাধারণত একটি **GUID** দ্বারা চিহ্নিত করা হয়। একটি পণ্য এক বা একাধিক উপাদান নিয়ে গঠিত এবং বিভিন্ন বৈশিষ্ট্যের মধ্যে গোষ্ঠীবদ্ধ। উইন্ডোজ ইনস্টলার একই সাথে বিভিন্ন পণ্যের মধ্যে নির্ভরতা পরিচালনা করে না। প্যাকেজগুলির যৌক্তিক কাঠামো নিম্নলিখিত উপাদানগুলি নিয়ে গঠিত:

- **পণ্য**: একটি একক, ইনস্টল করা, কার্যকারী প্রোগ্রাম বা একাধিক প্রোগ্রামের সেট একত্রে একটি পণ্য। একটি পণ্য একটি অনন্য GUID দ্বারা চিহ্নিত করা হয়.
- **বৈশিষ্ট্য**: যেকোনো সংখ্যক উপাদান এবং অন্যান্য উপ-বৈশিষ্ট্য থাকতে পারে। ছোট প্যাকেজ একটি একক বৈশিষ্ট্য গঠিত হতে পারে.
- **কম্পোনেন্ট**: কম্পোনেন্টকে উইন্ডোজ ইন্সটলার দ্বারা একটি ইউনিট হিসাবে বিবেচনা করা হয়; প্রোগ্রাম ফাইল, ফোল্ডার, রেজিস্ট্রি কী, COM উপাদান এবং শর্টকাট থাকতে পারে।
- **Key Paths**: A key path is a specific file, ODBC data source, or registry key that the package author specifies as critical for a given component.

## তথ্যসূত্র 

* [উইন্ডোজ ইনস্টলার - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Windows_Installer)


