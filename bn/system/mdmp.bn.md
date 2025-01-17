{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "MDMP ফাইল - উইন্ডোজ মিনিডাম্প ফাইল ফরম্যাট",
  "description": "MDMP ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি MDMP ফাইল তৈরি এবং খুলতে পারে৷",
  "linktitle": "MDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-mdmp-bn"
    }
  },
  "lastmod": "2022-08-19"
}

## একটি MDMP ফাইল কি?

একটি MDMP ফাইল মাইক্রোসফ্ট উইন্ডোজের একটি অ্যাপ্লিকেশনের মেমরি ডাম্প যা অ্যাপ্লিকেশনটি অস্বাভাবিকভাবে বন্ধ হয়ে গেলে বা ক্র্যাশ হলে তৈরি হয়। এতে তথ্য এবং ডেটা ডাম্প রয়েছে যা ক্র্যাশের কারণ ডিবাগ করতে ব্যবহার করা যেতে পারে। MDMP ফাইলগুলি জাভা, C++, .NET এবং অন্যদের মতো যেকোন প্ল্যাটফর্ম দ্বারা তৈরি করা অ্যাপ্লিকেশনগুলিতে প্রযোজ্য। MDMP ছাড়াও,

যে অ্যাপ্লিকেশনগুলি MDMP ফাইলগুলি খুলতে পারে তার মধ্যে Microsoft Visual Studio Debugger অন্তর্ভুক্ত।

## MDMP ফাইল ফরম্যাট

MDMP ফাইলগুলি ডিস্কে বাইনারি ফাইল হিসাবে সংরক্ষণ করা হয় এবং মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও ডিবাগার দিয়ে খোলা যায়। ক্র্যাশের কারণ শনাক্ত করতে সাহায্য করার জন্য এতে নিম্নলিখিত তথ্য রয়েছে৷

 * স্টপ বার্তার বিশদ বিবরণ, এর পরামিতি এবং অন্যান্য ডেটা
 * লোড করা ড্রাইভারের তালিকা
 * যে প্রসেসর কাজ করা বন্ধ করে দিয়েছে তার জন্য প্রসেসর প্রসঙ্গ (PRCB)
 * প্রক্রিয়া তথ্য এবং কার্নেল প্রসঙ্গ (EPROCESS) যে প্রক্রিয়াটি বন্ধ হয়ে গেছে তার জন্য
 * থেমে যাওয়া থ্রেডের জন্য তথ্য এবং কার্নেল প্রসঙ্গ (ETHREAD) প্রক্রিয়া করুন
 * থেমে যাওয়া থ্রেডের জন্য কার্নেল-মোড কল স্ট্যাক

এই তথ্যটি কী ঘটেছে তা খুঁজে বের করতে, সমস্যার সমাধান করতে এবং এটিকে আবার ঘটতে বাধা দিতে সাহায্য করে।

### মিনিডাম্প বিশ্লেষণ করুন

একটি মেমরি ডাম্প ফাইল তৈরি করতে উইন্ডোজের বুট ভলিউমে একটি পেজিং ফাইল প্রয়োজন। পেজিং ফাইলটি বুট ভলিউমে তৈরি করা হয় এবং এর আকার কমপক্ষে 2 মেগাবাইট (MB) হওয়া উচিত। একটি অ্যাপ্লিকেশন ক্র্যাশ হলে ডাম্প ফাইল তৈরি হয়। দ্বিতীয় সমস্যার ক্ষেত্রে, একটি দ্বিতীয় ছোট মেমরি ডাম্প ফাইল তৈরি করা হয় যখন আগেরটি সংরক্ষণ করা হয়। কোনো ওভাররাইটিং এড়াতে ডাম্প ফাইলের নামটি আলাদা।

উইন্ডোজ %SystemRoot%\Minidump ফোল্ডারে সমস্ত মেমরি ডাম্প ফাইলের একটি তালিকা রাখে। আপনি নীচের ধাপে তালিকাভুক্ত MDMP ফাইলগুলিকে ভিজ্যুয়াল স্টুডিও ডিবাগারে চালিয়ে বিশ্লেষণ করতে পারেন।

## আমি কিভাবে ভিজ্যুয়াল স্টুডিওতে একটি MDMP ফাইল খুলব?

নিম্নলিখিত পদক্ষেপগুলি ভিজ্যুয়াল স্টুডিওতে একটি MDMP ফাইল খুলতে ব্যবহার করা যেতে পারে।

 * ভিজ্যুয়াল স্টুডিওতে, ফাইল মেনু থেকে, ওপেন | নির্বাচন করুন ক্র্যাশ ডাম্প .
 * আপনি যে ডাম্প ফাইলটি খুলতে চান সেটিতে নেভিগেট করুন।
 * খুলুন নির্বাচন করুন।

## রেফারেন্স

* [একটি ক্র্যাশ ঘটলে উইন্ডোজ দ্বারা তৈরি করা ছোট মেমরি ডাম্প ফাইল কীভাবে পড়বেন](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -ফাইল)


