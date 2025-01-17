{
  "date": "2019-12-10",
  "keywords": [
    "XLTM",
    "file",
    "extension",
    "file format",
    "Excel Open XML Macro",
    "Spreadsheet"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "একটি XLTM ফাইল এবং APIগুলি কী তা জানার জন্য আপনার ফাইল বিন্যাস নির্দেশিকা যা সেগুলি তৈরি করতে এবং খুলতে পারে৷",
  "title": "একটি XLTM ফাইল কি?",
  "linktitle": "XLTM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xltm-bn"
    }
  },
  "lastmod": "2019-12-10"
}

## একটি XLTM ফাইল কি?

XLTM ফাইল এক্সটেনশন সেই ফাইলগুলিকে উপস্থাপন করে যা মাইক্রোসফ্ট এক্সেল দ্বারা ম্যাক্রো-সক্ষম টেমপ্লেট ফাইল হিসাবে তৈরি করা হয়। XLTM ফাইলগুলি গঠনে [XLTX](/spreadsheet/xltx/) এর অনুরূপ যা পরবর্তীতে ম্যাক্রো দিয়ে টেমপ্লেট ফাইল তৈরি করা সমর্থন করে না৷ এই ধরনের টেমপ্লেট ফাইলগুলি তখন একই রকম XLSX ফাইল তৈরি করার সুবিধার্থে ম্যাক্রোগুলির সাথে লেআউট, বিন্যাসকরণ এবং অন্যান্য সেটিংস তৈরি এবং সেট করতে ব্যবহৃত হয়।

## সংক্ষিপ্ত ইতিহাস ##

এটি 2000 সালের প্রথম দিকে ছিল যখন মাইক্রোসফ্ট **অফিস ওপেন এক্সএমএল** এর মানকে মানিয়ে নিতে পরিবর্তন করার সিদ্ধান্ত নিয়েছিল। এই নতুন স্ট্যান্ডার্ডের অধীনে বিভিন্ন ধরণের নথিগুলিকে তাদের এক্সটেনশনগুলিতে X যুক্ত করে চিহ্নিত করা হয়েছিল, যেখানে X XML-এর জন্য। 2007 সাল নাগাদ, এই নতুন ফাইল ফরম্যাটটি Office 2007-এর অংশ হয়ে ওঠে এবং মাইক্রোসফট অফিসের নতুন সংস্করণেও এটি চালু করা হয়। নতুন ফাইলের ধরণটি ছোট ফাইলের আকার, দুর্নীতির কম পরিবর্তন এবং ভাল ফর্ম্যাট করা চিত্র উপস্থাপনের সুবিধা যুক্ত করেছে।

## XLTM ফাইল ফরম্যাট স্পেসিফিকেশন ##

XLTM ফাইলগুলি Office OpenXML ফাইল ফর্ম্যাটের উপর ভিত্তি করে এবং ফাইলের আকার কমাতে XML এবং [ZIP](/compression/zip/) ব্যবহার করে৷ ফাইলটিতে ডাবল ক্লিক করে মাইক্রোসফ্ট এক্সেল দিয়ে খোলা যাবে। একটি XLTM ফাইল ফরম্যাটে ফাইলের সংগঠন জিপ-এ ফাইলের নাম পরিবর্তন করে এবং তারপর ডিস্কে এর বিষয়বস্তু বের করে পর্যবেক্ষণ করা যেতে পারে।

### [Content_Types].xml ###

এটিই একমাত্র ফাইল যা বেস লেভেলে পাওয়া যায় যখন জিপ বের করা হয়। এটি প্যাকেজের মধ্যে অংশগুলির জন্য বিষয়বস্তুর প্রকারগুলি তালিকাভুক্ত করে৷ প্যাকেজে অন্তর্ভুক্ত XML ফাইলগুলির সমস্ত রেফারেন্স এই XML ফাইলে উল্লেখ করা হয়েছে৷

### \_rels (ফোল্ডার) ###

এটি হল সম্পর্ক ফোল্ডার যাতে একটি একক XML ফাইল থাকে যা প্যাকেজ-স্তরের সম্পর্কগুলি সঞ্চয় করে। Xltx ফাইলগুলির মূল অংশগুলির লিঙ্কগুলি এই ফাইলটিতে URI হিসাবে রয়েছে৷ এই ইউআরআইগুলি প্যাকেজের সাথে প্রতিটি মূল অংশের সম্পর্কের ধরন সনাক্ত করে। এর মধ্যে xl/workbook.xml হিসাবে অবস্থিত প্রাথমিক অফিস নথির সাথে সম্পর্ক এবং ডকপ্রপসের মধ্যে মূল অ্যাডএন এক্সটেন্ডেড বৈশিষ্ট্য হিসাবে অন্যান্য অংশ অন্তর্ভুক্ত রয়েছে।

### ডকপ্রপস ###

এই ফোল্ডারে সামগ্রিক নথির বৈশিষ্ট্য রয়েছে। এর মধ্যে রয়েছে মূল বৈশিষ্ট্যের একটি সেট, বর্ধিত বা অ্যাপ্লিকেশন-নির্দিষ্ট বৈশিষ্ট্যের একটি সেট এবং নথির একটি থাম্বনেইল পূর্বরূপ। একটি ফাঁকা ওয়ার্কবুকের এই ফোল্ডারে app.xml এবং core.xml নামে দুটি ফাইল রয়েছে। core.xml-এ লেখক, তৈরি ও সংরক্ষিত এবং পরিবর্তিত হওয়ার মতো তথ্য রয়েছে। App.xml ফাইলের বিষয়বস্তু সম্পর্কে তথ্য রয়েছে।

### xl (ফোল্ডার) ###

এটি হল মূল ফোল্ডার যা ওয়ার্কবুকের বিষয়বস্তু সম্পর্কে সমস্ত বিবরণ ধারণ করে। ডিফল্টরূপে, এটিতে নিম্নলিখিত ফোল্ডার রয়েছে:

* \_rels

* থিম

* ওয়ার্কশীট


এবং নিম্নলিখিত xml ফাইলগুলি:

* styles.xml

* workbook.xml


## তথ্যসূত্র ##

* [MS-XLSX ফাইল ফরম্যাট](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [ওপেন অফিস এক্সএমএল](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


