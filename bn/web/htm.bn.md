{
  "date": "2019-10-11",
  "keywords": [
    "htm",
    "htm file",
    "htm file format",
    "htm file type",
    "file",
    "type",
    "what is an htm file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "HTM ফাইল ফরম্যাট",
  "description": "একটি HTM ফাইল এবং API যা সেগুলি তৈরি এবং খুলতে পারে তা শিখতে আপনার ফাইল বিন্যাস নির্দেশিকা৷",
  "linktitle": "HTM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htm-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি HTM ফাইল কি?

**.htm** এক্সটেনশন সহ ফাইলগুলি ওয়েব ব্রাউজার যেমন গুগল ক্রোম, ইন্টারনেট এক্সপ্লোরার, ফায়ারফক্স এবং আরও কয়েকটিতে প্রদর্শনের জন্য ওয়েব পৃষ্ঠাগুলি তৈরি করার জন্য হাইপারটেক্সট মার্কআপ ভাষা উপস্থাপন করে। এটি ওয়ার্ল্ড ওয়াইড ওয়েবে (WWW) অন্যদের অ্যাক্সেসের জন্য স্থির পৃষ্ঠাগুলি তৈরি করার জন্য মার্কআপগুলিকে সংজ্ঞায়িত করে৷ এই মার্কআপগুলি ব্রাউজারকে বলে যে কীভাবে একটি ওয়েব পৃষ্ঠার বিষয়বস্তু প্রদর্শন করতে হয়। এই ধরনের পৃষ্ঠাগুলিতে সাধারণ পাঠ্য, ছবি, অন্যান্য পৃষ্ঠাগুলির হাইপারলিঙ্ক, ভিডিও এবং অন্যান্য মিডিয়া তথ্য থাকতে পারে। যখন একটি ওয়েব পৃষ্ঠা প্রকাশিত হয়, তখন আপনি এর পৃষ্ঠার উৎস দেখে এর পিছনের মার্কআপ কোডটি দেখতে পারেন। আধুনিক ব্রাউজারগুলি একটি ওয়েব পৃষ্ঠার প্রতিটি বিভাগ পরিদর্শন করার অনুমতি দেয় যেখানে HTM উত্সের প্রতিটি উপ-বিভাগ বা মার্কআপ উপাদান বিশদভাবে বর্ণনা করা হয়।

## HTM এর সংক্ষিপ্ত ইতিহাস

Since its inception and first role out, the HTML specifications have been maintained by World Wide Web Consortium (W3C) since 1996. 2000 সালে, এটি একটি আন্তর্জাতিক মানও হয়ে ওঠে (ISO/IEC 15445:2000)। 1999 সালে, HTML 4.01 প্রকাশিত হয়েছিল। 2004 সালে, ওয়েব হাইপারটেক্সট অ্যাপ্লিকেশন টেকনোলজি ওয়ার্কিং গ্রুপ (WHATWG) HTML5 সংস্করণে কাজ শুরু করে যা 2008 সালে W3C-এর সাথে একটি যৌথ বিতরণযোগ্য হয়ে ওঠে। এটি 28 অক্টোবর 2014-এ সম্পূর্ণ এবং মানসম্মত হয়।

## এইচটিএমএল ফাইল ফরম্যাট

একটি HTML 4 নথি তিনটি অংশ নিয়ে গঠিত:

1. HTML সংস্করণ তথ্য ধারণকারী একটি লাইন
1. একটি ঘোষণামূলক শিরোনাম বিভাগ
1. একটি বডি, যা নথির প্রকৃত বিষয়বস্তু ধারণ করে। শরীরকে শরীরের উপাদান বা ফ্রেমসেট উপাদান দ্বারা বাস্তবায়িত করা যেতে পারে যাতে শরীরকে ফ্রেমে রাখা হয়

প্রতিটি বিভাগে সাদা স্থান, নতুন লাইন, ট্যাব এবং মন্তব্য দ্বারা নেতৃত্ব দেওয়া বা অনুসরণ করা যেতে পারে। একটি সাধারণ HTML নথির উদাহরণ নীচে দেখানো হয়েছে:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### সংস্করণ সংক্রান্ত তথ্য

কোডের প্রথম লাইন,<!DOCTYPE html> , কে ডকটাইপ ডিক্লারেশন বলা হয় এবং ব্রাউজারকে বলে যে এইচটিএমএল এর কোন সংস্করণে পেজটি লেখা হয়েছে। এইচটিএমএল এর সংস্করণের উপর নির্ভর করে, ডকুমেন্টের জন্য ব্যবহৃত ডকুমেন্ট টাইপ ডেফিনিশন (ডিটিডি) এর নামকরণ করে বিভিন্ন ডকটাইপ ঘোষণা রয়েছে। প্রতিটি ডিটিডি এটি সমর্থন করে এমন উপাদানগুলির মধ্যে অন্যদের থেকে পৃথক এবং নিম্নরূপ পৃথক:

* HTML 4.01 কঠোর - সমস্ত উপাদান এবং গুণাবলী অন্তর্ভুক্ত করে যেগুলি [অবঞ্চিত](https://www.w3.org/TR/html401/conform.html#deprecated) বা ফ্রেমসেট নথিতে প্রদর্শিত হয় না

* এইচটিএমএল 4.01 ট্রানজিশনাল - কঠোর ডিটিডি প্লাস অবচয়িত উপাদান এবং বৈশিষ্ট্যগুলির মধ্যে সবকিছু অন্তর্ভুক্ত করে (যার বেশিরভাগই ভিজ্যুয়াল উপস্থাপনা সম্পর্কিত

* এইচটিএমএল 4.01 ফ্রেমসেট - ট্রানজিশনাল ডিটিডি প্লাস ফ্রেমের সবকিছুই অন্তর্ভুক্ত করে


**HTML5**-এর জন্য, ভার্সনের তথ্য নিচে উল্লেখ করা হয়েছে।

```
<!DOCTYPE html>
```

### হেডারের তথ্য

একটি HTML নথির শিরোনামে অনেকগুলি HTML উপাদান অন্তর্ভুক্ত থাকতে পারে যা ব্রাউজার দ্বারা রেন্ডার করা হয় না। এই জাতীয় উপাদানগুলি হয় মেটাডেটা যা পৃষ্ঠা সম্পর্কে তথ্য বর্ণনা করে বা সেগুলি অন্তর্ভুক্ত করে যা CSS স্টাইলশীট বা জাভাস্ক্রিপ্ট ফাইলের মতো বাহ্যিক সংস্থান থেকে তথ্য আনতে ব্যবহৃত হয়। একটি পৃষ্ঠার শিরোনাম দ্বারা প্রতিনিধিত্ব করা হয় \<head> ট্যাগ এবং শেষ হয় \</head> ট্যাগ

পৃষ্ঠার শিরোনাম সেট করার জন্য, \<title> উপাদান শুধুমাত্র একটি যা \<head> ট্যাগের মধ্যে প্রয়োজন। এটি একটি পৃষ্ঠার শিরোনাম সনাক্ত করতে অনুসন্ধান ইঞ্জিন দ্বারা ব্যবহৃত হয়।

### শরীরের তথ্য

এটি ফাইলের প্রধান বিভাগ যাতে ফাইলের সমস্ত বিষয়বস্তু থাকে যা ব্রাউজার দ্বারা রেন্ডার করা হয়। এইচটিএমএল বডিতে মার্কআপ থাকতে পারে যা ট্যাগের আকারে বিভিন্ন বিল্ডিং ব্লককে উল্লেখ করতে পারে। এতে বিভিন্ন ধরনের তথ্য যেমন টেক্সট, ছবি, রং, গ্রাফিক্স ইত্যাদি থাকতে পারে। উপরন্তু, ব্রাউজার দ্বারা রেন্ডার করার জন্য অডিও এবং ভিডিও উপাদানগুলিও html বডিতে এম্বেড করা যেতে পারে। ভিজ্যুয়াল উপস্থাপনার জন্য আধুনিক শৈলী শীট অ্যাপ্লিকেশনের উপস্থিতিতে, BODY-এর উপস্থাপনা বৈশিষ্ট্যগুলি যেমন পটভূমির রঙ, লিঙ্কের রঙ, পাঠ্যের রঙ, ইত্যাদি অবমূল্যায়িত করা হয়েছে। সুতরাং, নীচে দেখানো স্টাইলশীট ব্যবহার করে একই প্রভাবগুলি অর্জন করা যেতে পারে:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

ইনলাইন স্টাইল শীটগুলি এম্বেড করা সহজ এবং ভিজ্যুয়াল এফেক্টগুলিতে দ্রুত অ্যাপ্লিকেশনের জন্য, বাহ্যিক স্টাইল শীটগুলি একবার স্থাপন করা এবং অনেক জায়গায় অ্যাক্সেস করা আরও সুবিধাজনক করে তোলে।

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML উপাদান

আগেই উল্লেখ করা হয়েছে, এইচটিএমএল বডির ভিতরের বিষয়বস্তু ট্যাগ দ্বারা উপস্থাপন করা হয়, যা এইচটিএমএল এলিমেন্ট নামেও পরিচিত। প্রতিটি ট্যাগের বৈশিষ্ট্যগুলির আকারে অতিরিক্ত তথ্য থাকতে পারে যা হিসাবে লেখা হয়
```
<tag attribute1#"value1" attribute2#"value2">
```
যদিও প্রতিটি ট্যাগের সাথে বৈশিষ্ট্য থাকা আবশ্যক নয়। যদি গুণাবলী উল্লেখ না করা হয়, প্রতিটি ক্ষেত্রে ডিফল্ট মান ব্যবহার করা হয়। নিচে কিছু এলিমেন্টের উদাহরণ দেওয়া হল:

#### হেডার

```
<head>
  <title>The Title</title>
</head>
```

#### শিরোনাম

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### অনুচ্ছেদ

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## তথ্যসূত্র

* [HTML নথির গ্লোবাল স্ট্রাকচার](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

