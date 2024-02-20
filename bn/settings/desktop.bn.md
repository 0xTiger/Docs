{
  "date": "2023-05-31",
  "keywords": [
"ডেস্কটপ ফাইল",
"একটি ডেস্কটপ ফাইল কি?",
"ডেস্কটপ ফাইলে কি থাকে",
"উদাহরণ ডেস্কটপ ফাইল",
"কিভাবে ডেস্কটপ ফাইল খুলবেন",
"ডেস্কটপ ফাইলের বিন্যাস কি?",
"ফাইল",
"ডেস্কটপ ফাইল এক্সটেনশন",
"এক্সটেনশন"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "ডেস্কটপ ফাইল ফরম্যাট - ডেস্কটপ এন্ট্রি ফাইল",
  "description": "DESKTOP বিন্যাস এবং API সম্পর্কে জানুন যেগুলি DESKTOP ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop-bn",
      "parent": "settings"
}
},
  "lastmod": "2023-05-31"
}

## ডেস্কটপ ফাইল কি?

একটি .desktop ফাইল হল একটি কনফিগারেশন ফাইল যা লিনাক্স ডেস্কটপ পরিবেশ দ্বারা অ্যাপ্লিকেশন শর্টকাট এবং লঞ্চারকে সংজ্ঞায়িত করতে ব্যবহৃত হয়। এটি একটি অ্যাপ্লিকেশন সম্পর্কে মেটাডেটা প্রদান করে যেমন এর নাম, আইকন, কার্যকর করার কমান্ড এবং অন্যান্য বৈশিষ্ট্য। এই ফাইলগুলি সাধারণত লিনাক্স-ভিত্তিক সিস্টেমে অ্যাপ্লিকেশন মেনু, ডেস্কটপ লঞ্চার বা প্যানেলে শর্টকাট তৈরি করতে ব্যবহৃত হয়।

## ডেস্কটপ ফাইলে কী থাকে?

একটি .desktop ফাইল নির্দিষ্ট বিন্যাস অনুসরণ করে এবং এতে বেশ কয়েকটি কী ক্ষেত্র রয়েছে:

- **[ডেস্কটপ এন্ট্রি]:** এটি .desktop ফাইলের প্রধান সেকশন হেডার।
- **নাম:** আবেদনের নাম উল্লেখ করে।
- **Comment:** Provides brief description or comment about application.
- **Exec:** অ্যাপ্লিকেশান চালু করার সময় এক্সিকিউট করার কমান্ড সংজ্ঞায়িত করে।
- **আইকন:** অ্যাপ্লিকেশনের সাথে যুক্ত আইকন ফাইলের পথ নির্দিষ্ট করে।
- **টার্মিনাল:** টার্মিনাল উইন্ডোতে অ্যাপ্লিকেশন চালানো উচিত কিনা তা নির্দিষ্ট করে।
- **প্রকার:** অ্যাপ্লিকেশন বা লিঙ্ক এর মতো এন্ট্রির ধরন নির্দিষ্ট করে।
- **Categories:** Specifies categories or groups under which the application should be displayed in the menu.
- **StartupNotify:** ডেস্কটপ পরিবেশে অ্যাপ্লিকেশনের জন্য একটি স্টার্টআপ বিজ্ঞপ্তি দেখানো উচিত কিনা তা নির্দিষ্ট করে।
- **NoDisplay:** Specifies whether application should be hidden from menus.
- **ক্রিয়া:** অতিরিক্ত ক্রিয়াগুলিকে সংজ্ঞায়িত করে যা অ্যাপ্লিকেশনে সঞ্চালিত হতে পারে যেমন একটি নির্দিষ্ট ফাইল খোলা।

## উদাহরণ ডেস্কটপ ফাইল

এখানে MyTextEditor নামক একটি কাল্পনিক পাঠ্য সম্পাদকের জন্য একটি .desktop ফাইলের একটি উদাহরণ রয়েছে:

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

এই উদাহরণে, .desktop ফাইলটি MyTextEditor অ্যাপ্লিকেশনটিকে এর সংশ্লিষ্ট বৈশিষ্ট্যগুলির সাথে সংজ্ঞায়িত করে৷ এটিতে দুটি অতিরিক্ত ক্রিয়াও রয়েছে, নতুন উইন্ডো খুলুন এবং ওপেন এক্সিস্টিং ফাইল, যা অ্যাপ্লিকেশন লঞ্চারের প্রসঙ্গ মেনু থেকে অ্যাক্সেস করা যেতে পারে।

একটি .desktop ফাইল নির্দিষ্ট ডিরেক্টরি যেমন `/usr/share/applications` বা `~/.local/share/applications`-এ রাখলে, ডেস্কটপ পরিবেশ এটিকে চিনবে এবং মেনুতে সেই অনুযায়ী অ্যাপ্লিকেশন প্রদর্শন করবে বা এটি থেকে লঞ্চ করার অনুমতি দেবে। ডেস্কটপ.

## কিভাবে DESKTOP ফাইল খুলবেন?

বেশ কিছু সফ্টওয়্যার প্রোগ্রাম .desktop ফাইল খুলতে এবং পরিচালনা করতে পারে। এই প্রোগ্রামগুলি সাধারণত লিনাক্স-ভিত্তিক সিস্টেমে ফাইল ম্যানেজার বা ডেস্কটপ পরিবেশ। এখানে কিছু উদাহরণঃ:

- **নটিলাস (ফাইল):** জিনোম ডেস্কটপ পরিবেশের জন্য ডিফল্ট ফাইল ম্যানেজার।
- **নিমো:** দারুচিনি ডেস্কটপ পরিবেশের জন্য ফাইল ম্যানেজার।
- **ডলফিন:** কেডিই প্লাজমা ডেস্কটপ পরিবেশের জন্য ডিফল্ট ফাইল ম্যানেজার।
- **Thunar:** Xfce ডেস্কটপ পরিবেশের জন্য ডিফল্ট ফাইল ম্যানেজার।
- **KDE মেনু এডিটর:** কেডিই প্লাজমা ডেস্কটপ পরিবেশের জন্য নির্দিষ্ট একটি টুল যা আপনাকে ডেস্কটপ ফাইল দেখতে ও সম্পাদনা করতে দেয়।

এই ফাইল ম্যানেজার এবং ডেস্কটপ এনভায়রনমেন্ট .desktop ফাইলগুলি পরিচালনার জন্য গ্রাফিকাল ইন্টারফেস প্রদান করে। তারা আপনাকে .desktop ফাইলগুলির বৈশিষ্ট্যগুলি দেখতে এবং সম্পাদনা করতে, অ্যাপ্লিকেশন লঞ্চার তৈরি করতে এবং অ্যাপ্লিকেশন মেনুতে বা ডেস্কটপে শর্টকাটগুলি সংগঠিত করার অনুমতি দেয়৷

ডেস্কটপ ফাইলগুলি হল প্লেইন টেক্সট ফাইল, তাই আপনি আপনার পছন্দের টেক্সট এডিটর দিয়ে সেগুলি খুলতে ও সম্পাদনা করতে পারেন৷ শুধুমাত্র .desktop ফাইলটিতে ডান-ক্লিক করুন এবং ইনস্টল করা প্রোগ্রামগুলির তালিকা থেকে একটি পাঠ্য সম্পাদক চয়ন করতে ওপেন উইথ বা অন্য অ্যাপ্লিকেশন দিয়ে খুলুন নির্বাচন করুন।

## ডেস্কটপ ফাইলের বিন্যাস কি?

.desktop ফাইল ফরম্যাট নির্দিষ্ট কাঠামো এবং বিন্যাস অনুসরণ করে। এটি একটি প্লেইন টেক্সট ফাইল যার একটি সেট কী-মানের জোড়া অংশে সাজানো। এখানে বিন্যাসের একটি ওভারভিউ আছে:

- **বিভাগ শিরোনাম:** প্রতিটি বিভাগ শুরু হয় বর্গাকার বন্ধনী ([]) এ আবদ্ধ একটি শিরোনাম দিয়ে। প্রাথমিক বিভাগটিকে সাধারণত [ডেস্কটপ এন্ট্রি] নাম দেওয়া হয়, যেটিতে অ্যাপ্লিকেশন বা লঞ্চারের প্রধান মেটাডেটা থাকে।
- **কী-মান জোড়া:** প্রতিটি বিভাগের মধ্যে, আপনি কী-মান জোড়া ব্যবহার করে বৈশিষ্ট্যগুলি সংজ্ঞায়িত করেন৷ বিন্যাস হল কী = মান। কী বৈশিষ্ট্য সনাক্ত করে এবং মান সংশ্লিষ্ট তথ্য প্রদান করে।
- **প্রপার্টি সিনট্যাক্স:** প্রপার্টির মান স্ট্রিং, বুলিয়ান মান, ফাইল পাথ বা তালিকা সহ বিভিন্ন ধরনের হতে পারে। প্রতিটি সম্পত্তির মানের বিন্যাস তার প্রকারের উপর নির্ভর করে।
- **মন্তব্য:** আপনি '#' চিহ্ন ব্যবহার করে .desktop ফাইলে মন্তব্য অন্তর্ভুক্ত করতে পারেন। লাইনে '#' অনুসরণ করা যেকোনো কিছুকে একটি মন্তব্য হিসেবে বিবেচনা করা হয় এবং উপেক্ষা করা হয়।

## তথ্যসূত্র
* [ডেস্কটপ এন্ট্রি ফাইল](https://www.baeldung.com/linux/desktop-entry-files)

