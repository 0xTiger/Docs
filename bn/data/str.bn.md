{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR ফাইল - dBASE স্ট্রাকচার লিস্ট অবজেক্ট ফাইল - .str ফাইল কি এবং কিভাবে খুলতে হয়?",
  "description" : "STR dBASE স্ট্রাকচার লিস্ট অবজেক্ট ফাইল এবং এটি কিভাবে খুলতে হয় সে সম্পর্কে জানুন।",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-bn",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## একটি STR ফাইল কি?

STR ফাইল ফরম্যাট সাধারণত dBASE এর সাথে যুক্ত, একটি ডাটাবেস ম্যানেজমেন্ট সিস্টেম। dBASE-এ, একটি .str ফাইল সাধারণত একটি স্ট্রাকচার লিস্ট অবজেক্ট ফাইলকে উপস্থাপন করে। এই ফাইলটিতে ক্ষেত্র (কলাম) এবং তাদের বৈশিষ্ট্য সম্পর্কে তথ্য সহ একটি ডাটাবেস টেবিলের গঠন রয়েছে।

স্ট্রাকচার লিস্ট অবজেক্ট ফাইলে (.str) মেটাডেটা থাকে যেমন ফিল্ডের নাম, ডাটা টাইপ, ফিল্ডের দৈর্ঘ্য এবং ডাটাবেস টেবিলের প্রতিটি ফিল্ডের সাথে যুক্ত অন্য কোনো বৈশিষ্ট্য। এটি প্রকৃত ডেটা রেকর্ড ধারণ না করেই ডাটাবেস টেবিলের গঠন সংজ্ঞায়িত করতে ব্যবহৃত হয়।

dBASE বা অন্যান্য ডাটাবেস ম্যানেজমেন্ট টুলের মতো প্রোগ্রামগুলি ডাটাবেস টেবিলের বিন্যাস বোঝার জন্য এই ফাইলটি ব্যবহার করতে পারে এবং এই কাঠামোর উপর ভিত্তি করে অনুসন্ধান, আপডেট বা নতুন রেকর্ড তৈরি করার মতো ক্রিয়াকলাপ সম্পাদন করতে পারে।

একটি STR ফাইলে কী থাকতে পারে তার একটি প্রাথমিক উদাহরণ এখানে দেওয়া হল:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

এই উদাহরণটি চারটি ক্ষেত্র সহ একটি টেবিল বর্ণনা করে: আইডি, নাম, বয়স এবং DOB, তাদের নিজ নিজ ডেটা প্রকার এবং দৈর্ঘ্য সহ।

## কিভাবে STR ফাইল খুলবেন?

.str ফাইল খোলার প্রাথমিক উপায় হল dBASE ব্যবহার করে, বিশেষ করে উইন্ডোজ অপারেটিং সিস্টেমে। dBASE এই ফাইলগুলির বিষয়বস্তু পড়তে এবং ব্যাখ্যা করতে সক্ষম, ব্যবহারকারীদের ডাটাবেস কাঠামো দেখতে এবং কাজ করার অনুমতি দেয়।

যেহেতু .str ফাইলগুলি মূলত প্লেইন টেক্সট ফাইল যাতে ডাটাবেসের গঠন সম্পর্কে তথ্য থাকে, আপনি একটি টেক্সট এডিটর ব্যবহার করেও সেগুলি খুলতে পারেন। টেক্সট এডিটরগুলির উদাহরণগুলির মধ্যে রয়েছে Windows-এ Microsoft Notepad এবং Mac-এ Apple TextEdit। টেক্সট এডিটরে খোলা হলে, আপনি ফাইলের বিষয়বস্তু দেখতে সক্ষম হবেন, যার মধ্যে ফিল্ডের নাম, ডাটা টাইপ এবং অন্যান্য কাঠামোগত তথ্য মানব-পাঠযোগ্য বিন্যাসে রয়েছে।

## তথ্যসূত্র
* [dBase](https://en.wikipedia.org/wiki/DBase)


