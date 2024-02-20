{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "EML - ইমেইল বার্তা",
  "description": "EML ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা EML ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "EML",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-eml-bn"
    }
  },
  "lastmod": "2019-09-16"
}

## একটি EML ফাইল কি?

EML ফাইল ফরম্যাট আউটলুক এবং অন্যান্য প্রাসঙ্গিক অ্যাপ্লিকেশন ব্যবহার করে সংরক্ষিত ইমেল বার্তাগুলিকে উপস্থাপন করে। RFC-822 ইন্টারনেট মেসেজ ফরম্যাট স্ট্যান্ডার্ডের সাথে সম্মতির জন্য প্রায় সমস্ত ইমেল ক্লায়েন্ট এই ফাইল ফর্ম্যাটটিকে সমর্থন করে। মাইক্রোসফ্ট আউটলুক হল EML বার্তার প্রকারগুলি খোলার জন্য ডিফল্ট সফ্টওয়্যার৷ EML ফাইলগুলি ডিস্কে সংরক্ষণের পাশাপাশি যোগাযোগ প্রোটোকল ব্যবহার করে প্রাপকদের কাছে পাঠানোর জন্য ব্যবহার করা যেতে পারে।

## EML এর সংক্ষিপ্ত ইতিহাস

EML ফাইল ফরম্যাট স্পেসিফিকেশন [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) স্ট্যান্ডার্ড ফরম্যাট অনুযায়ী উপলব্ধ। RFC-822-এর আগে, RFC-733 1982 সাল পর্যন্ত নেটওয়ার্ক মেসেজ আদান-প্রদানের নিয়মগুলি পরিচালনা করত, পূর্ববর্তীটি ARPA মান প্রতিষ্ঠার মাধ্যমে পার্শ্বীয় উন্নতি হিসাবে তৈরি করা হয়েছিল। একই সময়ে, মাইক্রোসফ্ট তার নিজস্ব ইমেল ক্লায়েন্ট অর্থাৎ আউটলুক এক্সপ্রেসের বিকাশের জন্য নিজস্ব COM মডিউল তৈরি করেছে। RFC-822 একটি মালিকানাধীন ফর্ম্যাট হিসাবে প্রতিষ্ঠিত হওয়ার পথ নিয়েছিল যখন Microsoft ওপেন স্ট্যান্ডার্ড থেকে বিচ্যুত হয়েছিল এবং [PST](/email/pst/) ফাইল ফর্ম্যাট তৈরি করেছিল যেখানে ইমেলগুলি একটি উচ্চ কাঠামোগত ডাটাবেস বিন্যাসে সংরক্ষিত হয়৷ এর ফলে মাইক্রোসফ্ট আউটলুক থেকে ইমেল ফরোয়ার্ড করার সময় নন-মাইক্রোসফ্ট ইমেল ক্লায়েন্ট ব্যবহারকারীদের সমস্যা দেখা দেয়।

এটি 2001 সালে ছিল যখন 822 মানকে 2822-এ উন্নীত করা হয়েছিল - ইন্টারনেট মেসেজ ফরম্যাট যা বর্তমানে MIME RFC-822 ফরম্যাটে EML বার্তা তৈরি, পড়া এবং পাঠানোর জন্য ব্যবহৃত হচ্ছে।

## EML ফাইল ফরম্যাট স্পেসিফিকেশন

EML ফাইল দুটি বিশিষ্ট বিভাগ নিয়ে গঠিত:

* **হেডার** - বার্তা শিরোনাম সম্পর্কে তথ্য রয়েছে

* **মেসেজ বডি** - বার্তার বিষয়বস্তু, এমবেড করা ছবি এবং সংযুক্তি অন্তর্ভুক্ত করতে পারে এমন তথ্যের সিরিজ রয়েছে


### শিরোনাম তথ্য ###

একটি EML ফাইলে হেডার তথ্য এবং ঐচ্ছিকভাবে মেসেজ বডি থাকে। EML এর প্রতিটি হেডার লাইন একটি কোলন : দ্বারা পৃথক দুটি অংশ আছে। প্রথমটিকে হেডার নাম বলা হয় এবং কোলনের পরে থাকাটিকে হেডার বডি বলা হয়। উদাহরণস্বরূপ, এই ধরনের শিরোনাম অন্তর্ভুক্ত:

* প্রেরকের ইমেল ঠিকানা

* প্রাপকের ইমেইল ঠিকানা

* ইমেইলের বিষয়

* বার্তার সময় এবং তারিখ স্ট্যাম্প


**উদাহরণ শিরোনাম**

```
From: <John@bmw.eml.light.com>

To: <Andy@fileformat.com>

Date: Thu, 8 Mar 2018 10:43:37 +0100

Subject: bmw eml light
```

### বার্তাংশ ###

EML মেসেজ বডিতে টেক্সট, হাইপারলিঙ্ক এবং অ্যাটাচমেন্ট আকারে ইমেলের প্রাথমিক তথ্য থাকে। ইমেলের বডি প্লেইন পঠনযোগ্য পাঠ্য ধারণ করতে পারে তবে এটি প্রয়োজনীয় নয়। এই ক্ষেত্রে, বার্তার অংশটি খালি হতে পারে বা এনকোড করা সংযুক্তি ডেটা থাকতে পারে।

মেসেজ বডির বিষয়বস্তু তার বিষয়বস্তু-প্রকার দ্বারা বর্ণনা করা হয় যা রিডিং অ্যাপ্লিকেশনগুলিকে সংশ্লিষ্ট ফরম্যাটে তথ্য পড়তে সক্ষম করে। এটি আসলে একটি নথির প্রকৃতি এবং বিন্যাস প্রতিনিধিত্ব করে। একটি MIME প্রকার বা বিষয়বস্তু-টাইপের গঠন খুবই সহজ; এটি একটি টাইপ এবং একটি সাবটাইপ নিয়ে গঠিত, দুটি স্ট্রিং, একটি '/' দ্বারা বিভক্ত। কোন স্থান অনুমোদিত নয়. `টাইপ` বিভাগকে প্রতিনিধিত্ব করে এবং এটি একটি বিচ্ছিন্ন বা একাধিক অংশ হতে পারে। 'সাবটাইপ' প্রতিটি প্রকারের জন্য নির্দিষ্ট। বিষয়বস্তু-প্রকারের শ্রেণীভুক্ত প্রকারের তালিকাটি দীর্ঘ কিন্তু কিছু গুরুত্বপূর্ণ বিষয়বস্তুর প্রকার নিম্নরূপ:


|**প্রকার**|**বিবরণ**|**উপপ্রকারের উদাহরণ**
---|---|---|
|পাঠ্য|মানব-পাঠ্য
|ইমেজ
|audio|যেকোনো অডিও ফাইল ফরম্যাট|audio/mdi, audio/wav প্রতিনিধিত্ব করে
|অ্যাপ্লিকেশন

### EML বডিতে সংযুক্তির প্রতিনিধিত্ব

EML বডিতে প্রতিটি বিষয়বস্তুর প্রকারের সীমানা রয়েছে যা এতে রয়েছে। বার্তার অংশে সংযুক্তিটি নিম্নলিখিত উদাহরণে দেখানো হয়েছে তার বিষয়বস্তু-প্রকার এবং বিষয়বস্তু-স্বভাব দ্বারা চিহ্নিত করা হয়:

বিষয়বস্তু-প্রকার: পাঠ্য/সরল; charset#windows-1252; name#apple app store.txt
বিষয়বস্তু-স্বভাব: সংযুক্তি; filename#apple app store.txt
বিষয়বস্তু-স্থানান্তর-এনকোডিং: base64
এক্স-অ্যাটাচমেন্ট-আইডি: f_jkhztmd02

যেমনটি দেখা যায়, সংযুক্তিতে সেট করা বিষয়বস্তু-ডিসপোজিশন সংযুক্তি তথ্য যেমন সংযুক্তি ফাইলের নাম এবং স্থানান্তর এনকোডিং পাওয়ার জন্য রিডিং অ্যাপ্লিকেশনগুলিকে সক্ষম করে। সংযুক্তি শিরোলেখ তথ্য এনকোড করা সংযুক্তি বিষয়বস্তু দ্বারা অনুসরণ করা হয় যা পড়তে হবে।

#### সংযুক্তি হিসাবে স্প্রেডশীটের উদাহরণ

বিষয়বস্তু-প্রকার: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; নাম#ইংরেজি_spodr.xlsx
বিষয়বস্তু-স্বভাব: সংযুক্তি; ফাইলের নাম#ইংরেজি_spodr.xlsx
বিষয়বস্তু-স্থানান্তর-এনকোডিং: base64
এক্স-অ্যাটাচমেন্ট-আইডি: f_jkhztmd43

## কিভাবে একটি EML ফাইল খুলবেন

আপনি বিভিন্ন ইমেল প্রোগ্রাম ব্যবহার করে EML ফাইল খুলতে পারেন যেমন:

 * **ম্যাকোসে অ্যাপল মেল**
 * **মোজিলা থান্ডারবার্ড**
 * **মাইক্রোসফ্ট আউটলুক**

EML ফাইলগুলি প্লেইন টেক্সট ফরম্যাটে সংরক্ষিত হয় এবং আপনি এই EML ফাইলগুলিকে জনপ্রিয় টেক্সট এডিটর যেমন **TextEdit** macOS-এ এবং **Microsoft Notepad** দিয়ে Windows OS-এ খুলতে পারেন।

## কিভাবে একটি EML ফাইল রূপান্তর করতে হয়

আপনি অ্যাপল মেল এবং মাইক্রোসফ্ট আউটলুকের মতো অ্যাপ্লিকেশনগুলির সাথে EML ফাইলগুলিকে অন্য কয়েকটি ফর্ম্যাটে রূপান্তর করতে পারেন।

উদাহরণস্বরূপ, মাইক্রোসফ্ট আউটলুক EML ফাইলকে নিম্নলিখিত ফর্ম্যাটে রূপান্তর করতে পারে:

**[.MSG](/eml/msg/)** - Microsoft Outlook মেসেজ ফরম্যাট
**[.PDF](/pdf/)** - প্রোটেবল ডকুমেন্ট ফরম্যাট

## তথ্যসূত্র

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

