{
  "date": "2023-09-05",
  "keywords": [
"জেট",
"জেট ফাইল",
"একটি জেট ফাইল কি",
"JET Microsoft Access ডাটাবেস ফাইল",
"কিভাবে জেট ফাইল খুলতে হয়",
"ফাইল",
"জেট ফাইল এক্সটেনশন",
"এক্সটেনশন"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "জেইটি ফাইল ফরম্যাট - মাইক্রোসফ্ট জেইটি ডাটাবেস ফাইল",
  "description": "জেইটি ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি জেইটি ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "JET",
  "menu": {
    "docs": {
      "identifier": "database-jet-bn",
      "parent": "database"
}
},
  "lastmod": "2023-09-05"
}

## একটি JET ফাইল কি?

একটি জেইটি ডাটাবেস ফাইল, যা মাইক্রোসফ্ট অ্যাকসেস ডাটাবেস ফাইল নামেও পরিচিত, এটি একটি জনপ্রিয় ডাটাবেস ম্যানেজমেন্ট সিস্টেম (DBMS) Microsoft Access দ্বারা ব্যবহৃত একটি ফাইল বিন্যাস। JET এর অর্থ জয়েন্ট ইঞ্জিন প্রযুক্তি, যা মাইক্রোসফ্ট অ্যাক্সেস ব্যবহার করা ডেটাবেস ইঞ্জিনের আসল নাম ছিল। অ্যাক্সেসের পরবর্তী সংস্করণগুলি বিভিন্ন ডাটাবেস ইঞ্জিন ব্যবহার করেছে, তবে জেইটি ডাটাবেস শব্দটি এখনও অ্যাক্সেস ডাটাবেস বোঝাতে ব্যবহৃত হয়।

এখানে JET ডাটাবেস ফাইল সম্পর্কে কিছু মূল বিষয় রয়েছে:

- **ফাইল এক্সটেনশন:** জেইটি ডাটাবেস ফাইলগুলিতে সাধারণত অ্যাক্সেসের পুরানো সংস্করণগুলির জন্য .mdb এর একটি ফাইল এক্সটেনশন থাকে (অ্যাক্সেস 2003 এবং পূর্ববর্তী) এবং নতুন সংস্করণগুলির জন্য .accdb (অ্যাক্সেস 2007 এবং পরবর্তী)। .mdb ফাইলগুলি পুরানো JET ডাটাবেস ইঞ্জিন ব্যবহার করে, যখন .accdb ফাইলগুলি নতুন ACE (Access Database Engine) প্রযুক্তি ব্যবহার করে৷

- **রিলেশনাল ডাটাবেস:** জেইটি ডাটাবেস হল রিলেশনাল ডাটাবেস, যার মানে তারা তাদের মধ্যে সংজ্ঞায়িত সম্পর্ক সহ টেবিলে ডেটা সঞ্চয় করে। ব্যবহারকারীরা এসকিউএল (স্ট্রাকচার্ড কোয়েরি ল্যাঙ্গুয়েজ) ব্যবহার করে বা অ্যাক্সেস গ্রাফিকাল ইন্টারফেসের মাধ্যমে ডেটা তৈরি, পরিবর্তন এবং অনুসন্ধান করতে পারে।

- **Data Storage:** JET databases can store a wide range of data types, including text, numbers, dates, images, and more. They can also handle complex data structures and relationships between tables.

- **মাল্টি-ইউজার অ্যাক্সেস:** জেইটি ডাটাবেসগুলি মাল্টি-ইউজার অ্যাক্সেস সমর্থন করে, একাধিক ব্যবহারকারীকে একই সাথে ডাটাবেসের সাথে কাজ করার অনুমতি দেয়, যদিও বড় আকারের অ্যাপ্লিকেশনগুলির জন্য স্কেলেবিলিটি এবং কর্মক্ষমতার ক্ষেত্রে সীমাবদ্ধতা থাকতে পারে।

- **ইন্টিগ্রেশন:** এক্সেস ডেটাবেসগুলিকে এক্সেল এবং আউটলুকের মতো অন্যান্য মাইক্রোসফ্ট অফিস অ্যাপ্লিকেশনগুলির সাথে একীভূত করা যেতে পারে, যা ব্যবহারকারীদের জন্য বিভিন্ন প্রোগ্রামের মধ্যে ডেটা বিনিময় করতে সুবিধাজনক করে তোলে।

## জেইটি ডাটাবেস সম্পর্কে তথ্য

**জেট ইঞ্জিনের ইতিহাস:**

জেইটি (জয়েন্ট ইঞ্জিন টেকনোলজি) ডাটাবেস ইঞ্জিন মূলত মাইক্রোসফ্ট 1990 এর দশকের গোড়ার দিকে মাইক্রোসফ্ট অ্যাক্সেসে ব্যবহারের জন্য তৈরি করেছিল। ইঞ্জিনটি একটি হালকা ওজনের, ডেস্কটপ-ভিত্তিক ডাটাবেস সমাধান হিসাবে ডিজাইন করা হয়েছিল যা বিভিন্ন মাইক্রোসফ্ট পণ্যগুলিতে একত্রিত করা যেতে পারে।

**জেইটি ডাটাবেসের উপাদান**

- **টেবিল:** JET ডাটাবেসগুলি টেবিলে ডেটা সঞ্চয় করে, যা সারি এবং কলামে সংগঠিত রেকর্ডের সংগ্রহ।
- **কোয়েরি:** ব্যবহারকারীরা এসকিউএল (স্ট্রাকচার্ড কোয়েরি ল্যাঙ্গুয়েজ) ব্যবহার করে টেবিল থেকে ডেটা বের করতে, ফিল্টার করতে এবং ম্যানিপুলেট করার জন্য প্রশ্ন তৈরি করতে পারে।
- **ফর্ম:** অ্যাক্সেস একটি ফর্ম ডিজাইনার প্রদান করে যা ব্যবহারকারীদের কাস্টম ডেটা ইনপুট এবং প্রদর্শন ফর্ম তৈরি করতে দেয়৷
- **রিপোর্ট:** ব্যবহারকারীরা ডাটাবেসে সংরক্ষিত ডেটা থেকে পেশাদার চেহারার প্রতিবেদন তৈরি করতে পারে।
- **ম্যাক্রো এবং VBA:** ব্যবহারকারীরা কাজগুলিকে স্বয়ংক্রিয় করতে এবং ম্যাক্রো ব্যবহার করে বা VBA কোড লিখে কাস্টম কার্যকারিতা যোগ করতে পারে৷

**তথ্যের ধরণ**

জেইটি ডাটাবেসগুলি বিভিন্ন ধরণের ডেটা সমর্থন করে, যার মধ্যে রয়েছে:

- **টেক্সট:** আলফানিউমেরিক অক্ষর সংরক্ষণের জন্য।
- **সংখ্যা:** সাংখ্যিক মানের জন্য।
- **Date/Time:** For date and time values.
- **মেমো:** দীর্ঘ পাঠ্য বা নোটের জন্য।
- **হাইপারলিঙ্ক:** ওয়েব লিঙ্ক এবং ইমেল ঠিকানার জন্য।
- **সংযুক্তি:** ফাইল এবং সংযুক্তি সংরক্ষণের জন্য।

## কিভাবে JET ফাইল খুলবেন?

যে প্রোগ্রামগুলি জেইটি ফাইলগুলি খুলতে বা রেফারেন্স করে সেগুলি অন্তর্ভুক্ত করে

- Microsoft Access 365 (ফ্রি ট্রায়াল)

## অন্যান্য JET ফাইল

- [JET - The Jackbox Party Pack Settings](/settings/jet/)


## তথ্যসূত্র
* [ডেটাবেস ইঞ্জিন অ্যাক্সেস করুন](https://en.wikipedia.org/wiki/Access_Database_Engine)

