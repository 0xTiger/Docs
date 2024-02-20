{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "বিএমএল ফাইল ফরম্যাট - বিন মার্কআপ ল্যাঙ্গুয়েজ ফাইল",
  "description": "বিএমএল ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা বিএমএল ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "BML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-bml-bn"
    }
  },
  "lastmod": "2021-08-12"
}

## একটি BML ফাইল কি?

.bml এক্সটেনশন সহ একটি ফাইল হল একটি বিন মার্কআপ ল্যাঙ্গুয়েজ ফাইল যা জাভা অ্যাপ সমর্থন করার জন্য জাভা ক্লাস সংরক্ষণ করে। এটি জাভা অবজেক্ট এবং পদ্ধতিতে অ্যাক্সেসের অনুমতি দেয় এবং জাভা ক্লাস ব্যবহার করে নতুন কার্যকারিতা তৈরি করতে হবে না। এটি নির্দিষ্ট করে যে কীভাবে উপাদানগুলি দরকারী কাজগুলি সম্পাদনের জন্য একে অপরের সাথে সংযুক্ত থাকে। BML গঠন এবং উপাদান সম্পর্ক বর্ণনা করার জন্য IBM alphaWorks দ্বারা তৈরি করা হয়েছিল। ওয়েব ব্রাউজার, মাইক্রোসফ্ট নোটপ্যাড এবং নোটপ্যাড++ এর মতো যেকোন টেক্সট এডিটর ব্যবহার করে BML ফাইল খোলা এবং দেখা যায়।

## BML ফাইল ফরম্যাট

IBM alphaworks ওয়েবসাইট BML এর দুটি বাস্তবায়ন প্রদান করেছে। প্রথম বাস্তবায়ন হল একটি দোভাষী যা কাঙ্খিত বিন অনুক্রম তৈরি করার জন্য একটি BML স্ক্রিপ্ট 'বাজায়'। দ্বিতীয় বাস্তবায়ন হল একটি কম্পাইলার যা যেকোনো BML স্ক্রিপ্টকে প্রতিফলন-মুক্ত জাভা কোডে কম্পাইল করে। এটি এই অর্থে সুবিধাজনক যে এটি 'নিয়মিত' জাভা কোডে কম্পাইল করার অতিরিক্ত ক্ষমতা সহ এই নির্দিষ্ট উদ্দেশ্যে ডিজাইন করা একটি ভাষা ব্যবহার করে অ্যাপ্লিকেশনটির আন্তঃ-কম্পোনেন্ট কাঠামো ক্যাপচার করার অনুমতি দেয়।

## বিএমএল ট্যাগ

BML ভাষায় ব্যবহৃত কিছু ট্যাগের ব্যাখ্যা নিচে দেওয়া হল:

### দ্য<bean> ট্যাগ:

দ্য<bean> উপাদান নতুন মটরশুটি তৈরি করতে বা নাম অনুসারে মটরশুটি দেখতে ব্যবহার করা হয়। দ্য<bean> ট্যাগ ফরম্যাটের:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
ট্যাগের আইডি জাভাবিনের জন্য অবজেক্ট রেজিস্ট্রির সাথে যুক্ত।

### দ্য<string> ট্যাগ

স্ট্রিং ট্যাগ দুটি উপায়ে ব্যবহার করা যেতে পারে:

 1. একটি অ-খালি স্ট্রিং তৈরি করতে:

```
<string [value = "value of string"]> [value of string]
</string>
```
 2. একটি খালি স্ট্রিং তৈরি করতে:

```
<string/>
```
## তথ্যসূত্র

* [Object-Oriented Messaging with XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [দ্য ফিজিক্যাল মার্কআপ ল্যাঙ্গুয়েজ](http://web.mit.edu/mecheng/pml/standards.htm)


