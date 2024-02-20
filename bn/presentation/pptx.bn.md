{
  "date": "2019-12-13",
  "keywords": [
    "pptx file",
    "pptx file format",
    "what is a pptx file",
    "file",
    "pptx example",
    "pptx file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "PPTX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি PPTX ফাইল তৈরি এবং খুলতে পারে।",
  "title": "PPTX - পাওয়ারপয়েন্ট প্রেজেন্টেশন ফাইল ফরম্যাট",
  "linktitle": "PPTX",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pptx-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি PPTX ফাইল কি?

পিপিটিএক্স এক্সটেনশন সহ ফাইলগুলি জনপ্রিয় মাইক্রোসফ্ট পাওয়ারপয়েন্ট অ্যাপ্লিকেশন দিয়ে তৈরি উপস্থাপনা ফাইল। প্রেজেন্টেশন ফাইল ফরম্যাট পিপিটি-এর আগের সংস্করণ থেকে ভিন্ন যা বাইনারি ছিল, পিপিটিএক্স ফরম্যাটটি মাইক্রোসফট পাওয়ারপয়েন্ট ওপেন এক্সএমএল প্রেজেন্টেশন ফাইল ফরম্যাটের উপর ভিত্তি করে তৈরি। একটি উপস্থাপনা ফাইল হল স্লাইডের একটি সংগ্রহ যেখানে প্রতিটি স্লাইডে পাঠ্য, চিত্র, বিন্যাস, অ্যানিমেশন এবং অন্যান্য মিডিয়া থাকতে পারে। এই স্লাইডগুলি কাস্টম উপস্থাপনা সেটিংস সহ স্লাইডশো আকারে দর্শকদের কাছে উপস্থাপন করা হয়।

## সংক্ষিপ্ত ইতিহাস

PPTX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. PPTX এর আগে, ব্যবহৃত সাধারণ ফাইল বিন্যাস ছিল PPT যা ছিল বিশুদ্ধ বাইনারি ফাইল বিন্যাস। নতুন ফাইলের ধরণটি ছোট ফাইলের আকার, দুর্নীতির কম পরিবর্তন এবং ভাল ফর্ম্যাট করা চিত্র উপস্থাপনের সুবিধা যুক্ত করেছে। এটি 2000 সালের প্রথম দিকে ছিল যখন মাইক্রোসফ্ট **অফিস ওপেন এক্সএমএল** এর মানকে মানিয়ে নিতে পরিবর্তন করার সিদ্ধান্ত নিয়েছিল। 2007 সাল নাগাদ, এই নতুন ফাইল ফরম্যাটটি Office 2007-এর অংশ হয়ে ওঠে এবং মাইক্রোসফট অফিসের নতুন সংস্করণেও এটি চালু করা হয়।

## PPTX ফাইল ফরম্যাট স্পেসিফিকেশন

অফিস ওপেন এক্সএমএল ফাইল ফরম্যাটের মাধ্যমে তৈরি করা ফাইল হল অন্যান্য ফাইলের সাথে XML ফাইলের একটি সংগ্রহ যা সমস্ত উপাদান ফাইলের মধ্যে লিঙ্ক প্রদান করে। এই সংগ্রহটি আসলে একটি সংকুচিত আর্কাইভ যা এর বিষয়বস্তু দেখতে বের করা যেতে পারে। এটি করার জন্য, শুধুমাত্র পিপিটিএক্স ফাইল এক্সটেনশনটি জিপ দিয়ে পুনঃনামকরণ করুন এবং এর বিষয়বস্তু পর্যবেক্ষণের জন্য এটিকে বের করুন (Microsoft-এর [PPTX file format specifications](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f) দেখুন)।

নিম্নলিখিত বিভাগগুলি প্রতিটির উপর কিছু আলোকপাত করেছে।

### [Content_Types].xml

এটিই একমাত্র ফাইল যা বেস লেভেলে পাওয়া যায় যখন জিপ বের করা হয়। এটি প্যাকেজের মধ্যে অংশগুলির জন্য বিষয়বস্তুর প্রকারগুলি তালিকাভুক্ত করে৷ প্যাকেজে অন্তর্ভুক্ত XML ফাইলগুলির সমস্ত রেফারেন্স এই XML ফাইলে উল্লেখ করা হয়েছে৷ নিচে একটি স্লাইড অংশের জন্য একটি বিষয়বস্তুর প্রকার রয়েছে:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

প্যাকেজে নতুন অংশ যোগ করার প্রয়োজন হলে, এটি নতুন অংশ যোগ করে এবং .rels ফাইলের মধ্যে যেকোনো সম্পর্ক আপডেট করার মাধ্যমে করা যেতে পারে। এটা মনে রাখতে হবে যে এই ধরনের পরিবর্তনের জন্য, Content_Types.xmlও আপডেট করতে হবে।

### \_rels (ফোল্ডার) ###

প্যাকেজের বাইরে অন্যান্য অংশ এবং সম্পদের মধ্যে সম্পর্ক সম্পর্ক অংশ দ্বারা বজায় রাখা হয়। সম্পর্ক ফোল্ডারে একটি একক XML ফাইল রয়েছে যা প্যাকেজ-স্তরের সম্পর্ক সংরক্ষণ করে। PPTX ফাইলগুলির মূল অংশগুলির লিঙ্কগুলি এই ফাইলটিতে URI হিসাবে রয়েছে৷ এই ইউআরআইগুলি প্যাকেজের সাথে প্রতিটি মূল অংশের সম্পর্কের ধরন সনাক্ত করে। এর মধ্যে রয়েছে ppt/presentation.xml হিসাবে অবস্থিত প্রাথমিক অফিস নথির সাথে সম্পর্ক এবং মূল এবং বর্ধিত বৈশিষ্ট্য হিসাবে docProps-এর মধ্যে অন্যান্য অংশ।

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

এক বা একাধিক সম্পর্কের উৎস নথির প্রতিটি অংশের নিজস্ব সম্পর্কের অংশ থাকবে যেখানে প্রতিটি সম্পর্কের অংশটি অংশটির একটি \_rels সাব-ফোল্ডারের মধ্যে পাওয়া যায় এবং এর নামের সাথে '.rels' যুক্ত করে নামকরণ করা হয়। অংশ প্রধান বিষয়বস্তুর অংশ (presentation.xml) এর নিজস্ব সম্পর্ক অংশ রয়েছে (presentation.xml.rels)। এতে বিষয়বস্তুর অন্যান্য অংশের সাথে সম্পর্ক রয়েছে যেমন slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, সেইসাথে বাহ্যিক লিঙ্কগুলির জন্য URI-এর সাথে।

#### স্পষ্ট সম্পর্ক ####

একটি সুস্পষ্ট সম্পর্কের জন্য, একটি আইডি বৈশিষ্ট্য ব্যবহার করে একটি সংস্থান উল্লেখ করা হয়<Relationship> উপাদান অর্থাৎ, উৎসের আইডি সরাসরি একটি সম্পর্ক আইটেমের আইডিতে ম্যাপ করে, টার্গেটের সুস্পষ্ট রেফারেন্স সহ।

উদাহরণস্বরূপ, একটি স্লাইডে একটি হাইপারলিঙ্ক থাকতে পারে যেমন:

```
<a:hlinkClick r:id#"rId2">
```

r:id#rId2 স্লাইডের (slide1.xml.rels) জন্য সম্পর্ক অংশের মধ্যে নিম্নলিখিত সম্পর্ক উল্লেখ করে।

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### অন্তর্নিহিত সম্পর্ক ####

একটি অন্তর্নিহিত সম্পর্কের জন্য, `এর মতো কোনো সরাসরি উল্লেখ নেই<Relationship> আইডি'। পরিবর্তে, রেফারেন্স বোঝা যায়।

### ppt ফোল্ডার ###

এটি হল প্রধান ফোল্ডার যা উপস্থাপনার বিষয়বস্তু সম্পর্কে সমস্ত বিবরণ ধারণ করে। ডিফল্টরূপে, এটিতে নিম্নলিখিত ফোল্ডার রয়েছে:

* \_rels

* থিম

* স্লাইড

* স্লাইড লেআউট

* স্লাইডমাস্টারস


এবং নিম্নলিখিত xml ফাইলগুলি:

* presentation.xml

* presProps.xml

* tableStyles.xml

* viewProps.xml


## তথ্যসূত্র ##

* [[MS-PPTX] - PPTX ফাইল ফরম্যাট](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)

* [ওপেন অফিস এক্সএমএল](http://officeopenxml.com/anatomyofOOXML-pptx.php)

