{
  "date": "2021-06-16",
  "keywords": [
    "LZO",
    "Compressed",
    "File",
    "Extension",
    "File Format",
    "Lempel-Ziv-Oberhume"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "LZO ফাইল ফরম্যাট",
  "description": "LZO ফাইল বিন্যাস এবং API সম্পর্কে জানুন যেগুলি LZO ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "LZO",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lzo-bn"
    }
  },
  "lastmod": "2021-06-16"
}

## একটি LZO ফাইল কি? ##

.lzo এক্সটেনশন সহ একটি ফাইল ফাইল সংরক্ষণাগার বৈশিষ্ট্যগুলির সাথে মিলিত হয় যা সংকুচিত ফাইলের সমস্ত ফাইলের আকার হ্রাস করতে পারে। সমস্ত সংকুচিত ফাইলে এক বা একাধিক ফাইল বা এমনকি বাইন্ডারের গ্রুপগুলি বিভিন্ন ধরণের এবং মাত্রার বিভিন্ন ফাইলের সাথে থাকতে পারে। একটি LZO সংকুচিত ফাইলে সংরক্ষিত সমস্ত ফাইল এবং ফোল্ডারের যৌথ আকারের তুলনায় একটি সংকুচিত ফাইলের আকার ছোট। সমস্ত LZO সংকুচিত ফাইলগুলি LZO বিন্যাসে সংরক্ষণ করা হয় এবং LZOP ফাইল কম্প্রেশন এবং ডিকম্প্রেশন সফ্টওয়্যার দ্বারা ব্যবহৃত কম্প্রেশন বৈশিষ্ট্যগুলির সাথে স্পষ্টভাবে কার্যকর করা হয়। সমস্ত কম্প্রেশন স্পেসিফিকেশন এই ফাইল কম্প্রেশন এবং ডিকম্প্রেশন প্রোগ্রামে একত্রিত করা হয়েছে যা Lempel-Ziv-Oberhume ফাইল কম্প্রেশন লাইব্রেরি থেকে উদ্ভূত হয়েছে। দ্রুততর ডিকম্প্রেশন গতি এবং উন্নত কম্প্রেশন অনুপাতগুলিও এই LZO ফাইলগুলিতে একত্রিত হয়।

## LZO স্পেসিফিকেশন ##

Markus Franz Xaver Johannes Oberhumer developed the original "lzop" algorithm, based on earlier algorithms by Abraham Lempel and Jacob Ziv, in 1996. এই লাইব্রেরি নিম্নলিখিত বৈশিষ্ট্য সহ বিভিন্ন অ্যালগরিদম প্রয়োগ করে:

* ডিফ্লেটের চেয়ে দ্রুত কম্প্রেশন

* দ্রুত ডিকম্প্রেশন

* অতিরিক্ত বাফার যা কম্প্রেশনের সময় প্রয়োজন (8KB বা 64KB আকারের, কম্প্রেশন স্তরের উপর নির্ভর করে)

* উৎস এবং গন্তব্য বাফারগুলি ডিকম্প্রেশনের জন্য প্রয়োজনীয় সমস্ত মেমরি

* কম্প্রেশন অনুপাত এবং কম্প্রেশন গতি উভয়ের উপর নিয়ন্ত্রণ প্রদান করে


একটি ব্লক কম্প্রেশন অ্যালগরিদম হিসাবে, LZO ওভারল্যাপিং কম্প্রেশনের পাশাপাশি ইন-প্লেস ডিকম্প্রেশন সঞ্চালন করে। ওভারল্যাপিং কম্প্রেশন অর্জন করতে, কম্প্রেশন এবং ডিকম্প্রেশন উভয়ের ব্লক সাইজ অবশ্যই মিলবে। LZO কম্প্রেশন অ্যালগরিদম ইনপুট ডেটাকে মিল (একটি স্লাইডিং অভিধান) এবং মেলে না এমন আক্ষরিকগুলিতে বিভক্ত করে, যা অত্যন্ত অপ্রয়োজনীয় ডেটা সহ ভাল ফলাফল দেয় এবং অ-সংকোচনযোগ্য ডেটা সহ গ্রহণযোগ্য ফলাফল দেয়, শুধুমাত্র অসংকোচযোগ্য ডেটা মূলের 1/64 বৃদ্ধি করে আকার

## একটি LZO ফাইল খুলতে সমস্যা ##

নিম্নোক্ত কয়েকটি সমস্যা যা LZO ফাইল ফরম্যাটের দুর্বল কাজের কারণ হতে পারে:
  
* ফাইলটি দূষিত হতে পারে। এই সমস্যাটি সমাধান করতে, ফাইলটি আবার ডাউনলোড করুন বা প্রেরককে ফাইলটি আবার পাঠাতে বলুন
* দ্বিতীয় কারণ হল সংক্রমিত ফাইল এই ক্ষেত্রে ফাইলটি সঠিকভাবে স্ক্যান করুন
* LZO ফাইলের অনুপযুক্ত লিঙ্ক
  *	 Removal of the description of the LZO 
* পর্যাপ্ত হার্ডওয়্যার সংস্থান নেই
* যন্ত্রপাতির পুরানো ড্রাইভার
  
## তথ্যসূত্র ##

* [LZO - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

