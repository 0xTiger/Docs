{
  "date": "2019-10-11",
  "keywords": [
    "yaml",
    ".yaml",
    "what is a yaml file",
    "how to open yaml file",
    "extension",
    "file",
    "yaml file",
    "yaml file format",
    ".yaml extension",
    "yaml vs json",
    "YAML file example",
    "docker yaml file example"
  ],
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
  },
  "draft": "false",
  "toc": true,
  "description": " YAML ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা একটি YAML ফাইল তৈরি এবং খুলতে পারে।",
  "title": "YAML ফাইল ফরম্যাট",
  "linktitle": "YAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-yaml-bn"
    }
  },
  "lastmod": "2021-05-05"
}

## একটি YAML ফাইল কি? ##

**YAML ফাইল** একটি ভাষা YAML (YAML Ain't Markup Language) নিয়ে গঠিত যা একটি ইউনিকোড ভিত্তিক ডেটা-ক্রমিক ভাষা; কনফিগারেশন ফাইল, ইন্টারনেট মেসেজিং, অবজেক্ট পারসিসটেন্স ইত্যাদির জন্য ব্যবহৃত হয়। YAML তার ফাইলের জন্য .yaml এক্সটেনশন ব্যবহার করে। এর সিনট্যাক্স একটি নির্দিষ্ট প্রোগ্রামিং ভাষা থেকে স্বাধীন। মূলত, YAML মানুষের মিথস্ক্রিয়া এবং আধুনিক প্রোগ্রামিং ভাষার সাথে ভালভাবে কাজ করার জন্য ডিজাইন করা হয়েছে। নির্বিচারে নেটিভ ডেটা স্ট্রাকচারগুলিকে সিরিয়ালাইজ করার জন্য সমর্থন YAML ফাইলগুলির পাঠযোগ্যতা বাড়িয়েছে, তবে এটি পার্সিং এবং ফাইল তৈরির প্রক্রিয়াটিকে কিছুটা জটিল করে তুলেছে।

## সংক্ষিপ্ত ইতিহাস ##

YAML প্রথম 2001 সালে প্রস্তাবিত হয়েছিল এবং ক্লার্ক ইভান্স, ইঙ্গি ডট নেট এবং ওরেন বেন-কিকি দ্বারা বিকাশ করা হয়েছিল। YAML কে প্রথমে বলা হয়েছিল এখনও আরেকটি মার্কআপ ভাষা একটি মার্কআপ ভাষা হিসাবে এর উদ্দেশ্য নির্দেশ করার জন্য। ডেটা-ভিত্তিক হিসাবে এর উদ্দেশ্য নির্দেশ করার জন্য এটিকে পরবর্তীতে YAML এন্ট মার্কআপ ল্যাঙ্গুয়েজ হিসাবে পুনরায় ব্যবহার করা হয়েছিল।


## YAML ফাইল ফরম্যাট ##

YAML ফাইল নিম্নলিখিত ডেটা প্রকার নিয়ে গঠিত

- **স্ক্যালার**: স্কেলার হল স্ট্রিং, ইন্টিজার, বুলিয়ান ইত্যাদির মান।
- **সিকোয়েন্স**: সিকোয়েন্স হল একটি হাইফেন (-) দিয়ে শুরু হওয়া প্রতিটি আইটেমের তালিকা। তালিকা এছাড়াও নেস্ট করা যেতে পারে.
- **ম্যাপিং**: ম্যাপিং মান সহ কী তালিকাভুক্ত করার ক্ষমতা দেয়।

### বাক্য গঠন ###

- **হোয়াইটস্পেস**: হোয়াইটস্পেস ইন্ডেন্টেশন নেস্টিং এবং সামগ্রিক গঠন নির্দেশ করতে ব্যবহৃত হয়।

``ইয়ামল
নাম: জন স্মিথ
যোগাযোগ:
বাড়ি: 1012355532
অফিস: 5002586256
ঠিকানা:
রাস্তা: |
123 টর্নেডো অ্যালি
স্যুট 16
শহর: ইস্ট সেন্টারভিল
রাজ্য: কেএস
```

- **মন্তব্য**: মন্তব্যগুলি # চিহ্ন দিয়ে শুরু হয়।

``ইয়ামল
# এটি একটি YAML মন্তব্য
```

- **তালিকা**: হাইফেন (-) একটি পৃথক লাইনে প্রতিটি সদস্যের সাথে তালিকার সদস্যদের নির্দেশ করতে ব্যবহৃত হয়। তালিকার সদস্যদের কমা (,) দ্বারা পৃথক করা সদস্যদের সাথে বর্গাকার বন্ধনীতে ([...]) আবদ্ধ করা যেতে পারে।

``ইয়ামল
  - "ক"
  - "খ"
  - "গ"
```

``ইয়ামল
[A, B, C]
```

- **অ্যাসোসিয়েটিভ অ্যারে**: একটি অ্যাসোসিয়েটিভ অ্যারে কোঁকড়া বন্ধনী ({...}) দ্বারা বেষ্টিত। কী এবং মানগুলি কোলন(:) দ্বারা পৃথক করা হয় এবং প্রতিটি জোড়া কমা (,) দ্বারা পৃথক করা হয়।

``ইয়ামল
{নাম: জন স্মিথ, বয়স: 20}
```

- **স্ট্রিংস**: স্ট্রিং ডাবল-উদ্ধৃতি () বা একক-উদ্ধৃতি (') সহ বা ছাড়া লেখা যেতে পারে।

``ইয়ামল
নমুনা স্ট্রিং
"নমুনা স্ট্রিং"
নমুনা স্ট্রিং
```

- **স্কেলার ব্লক কন্টেন্ট**: স্কেলার কন্টেন্ট ব্লক নোটেশনে নিম্নলিখিত ব্যবহার করে লেখা যেতে পারে:
  - "**|**: সমস্ত লাইভ বিরতি উল্লেখযোগ্য।"
  - "**>**: প্রতিটি লাইন বিরতি স্থান ভাঁজ করা হয়. এটি প্রতিটি লাইনের জন্য অগ্রণী হোয়াইটস্পেস সরিয়ে দেয়।"

``ইয়ামল
তথ্য: |
YAML
(YAML মার্কআপ ভাষা নয়)
একটি ডেটা-সিরিয়ালাইজেশন ভাষা
```

``ইয়ামল
তথ্য:?
YAML (YAML মার্কআপ ভাষা নয়)
একটি ডেটা-সিরিয়ালাইজেশন ভাষা
```

- **একাধিক নথি**: একাধিক নথি একটি একক প্রবাহে তিনটি হাইফেন (---) দ্বারা পৃথক করা হয়৷ হাইফেন নথির শুরু নির্দেশ করে। নথির বিষয়বস্তু থেকে নির্দেশনা আলাদা করতেও হাইফেন ব্যবহার করা হয়। নথির শেষ তিনটি বিন্দু (...) দ্বারা নির্দেশিত হয়।

``ইয়ামল
  ---
দলিল 1
  ---
নথি 2
...
```

- **প্রকার**: মানের ধরন নির্দিষ্ট করতে, ডবল বিস্ময়বোধক চিহ্ন (!!) ব্যবহার করা হয়।

``ইয়ামল
a: !!float 123
b: !!str 123
```

- **ট্যাগ**: একটি নোটে একটি ট্যাগ বরাদ্দ করতে, একটি অ্যাম্পারস্যান্ড (&) ব্যবহার করা হয় এবং সেই নোডটিকে উল্লেখ করার জন্য, একটি তারকাচিহ্ন (*) ব্যবহার করা হয়।

``ইয়ামল
নাম: জন স্মিথ
বিল-টু: &id01
রাস্তা: |
123 টর্নেডো অ্যালি
স্যুট 16
শহর: ইস্ট সেন্টারভিল
রাজ্য: কেএস

জাহাজ থেকে: *id01
```

- **নির্দেশনা**: YAML নথির আগে একটি স্ট্রীমে নির্দেশনা দেওয়া যেতে পারে। নির্দেশাবলী একটি শতাংশ চিহ্ন (%) দিয়ে শুরু হয় এবং তারপরে নাম এবং তারপর স্পেস দ্বারা পৃথক করা পরামিতিগুলি।

``ইয়ামল
% YAML 1.2
  ---
নথি বিষয়বস্তু
```
## YAML ফাইলের উদাহরণ
এখানে আপনি নীচে একটি **ডকার ইয়ামল ফাইলের উদাহরণ** দেখতে পারেন:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML বনাম JSON
মূলত, JSON এবং YAML উভয়ই একটি মানব-পঠনযোগ্য ডেটা বিনিময় বিন্যাস প্রদানের জন্য তৈরি করা হয়েছে। YAML JSON ফর্ম্যাটের একটি সুপারসেট হিসাবে উপলব্ধি করা হয়েছে। এর মানে হল যে আমরা একটি YAML পার্সার ব্যবহার করে JSON পার্স করতে পারি। যদিও এই তত্ত্বের ব্যবহারিক বাস্তবায়ন একটু কঠিন। অতএব, YAML এবং JSON এর মধ্যে কিছু মৌলিক পার্থক্য নীচে দেওয়া হল:

|YAML| JSON|
---|---|
|সিরিয়ালাইজড ডেটা পার্স করার জটিল এবং সময় সাপেক্ষ প্রক্রিয়া |দ্রুত এবং সহজে JSON সিরিয়ালাইজড ডেটাকে এর সহজ ডিজাইনের সাথে পার্স করুন|
|কমিউনিটি সাপোর্ট| বৃহত্তর সম্প্রদায়ের সমর্থন এবং জনপ্রিয়তা|
|মন্তব্য সমর্থন করে| মন্তব্য সমর্থন করে না|
|অন্যান্য ডেটা অবজেক্টের রেফারেন্স ব্যবহার করার ক্ষমতা| অবজেক্ট রেফারেন্স সহ জটিল কাঠামো সিরিয়ালাইজ করা অসম্ভব|
|দ্বৈত স্থান অক্ষর ব্যবহার করে শ্রেণিবিন্যাস নির্দেশ করা হয়। ট্যাব অক্ষর অনুমোদিত নয়|বস্তু এবং অ্যারেগুলিকে ব্রেসিস এবং বন্ধনীতে চিহ্নিত করা হয়৷|
|স্ট্রিং কোট ঐচ্ছিক কিন্তু এটি একক এবং ডবল কোট সমর্থন করে।
|রুট নোড বৈধ ডেটা প্রকারের যেকোনো একটি হতে পারে|রুট নোড অবশ্যই একটি অ্যারে বা একটি বস্তু হতে হবে৷|


## তথ্যসূত্র ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

