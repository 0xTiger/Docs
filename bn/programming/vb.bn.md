{
  "date": "2019-10-11",
  "keywords": [
    "vb",
    "file",
    "extension",
    "file format",
    "Visual Basic",
    "Programming Guide"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "VB - ভিজ্যুয়াল বেসিক কোড ফাইল",
  "description": "VB ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি VB ফাইলগুলি তৈরি এবং খুলতে পারে।",
  "linktitle": "VB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vb-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি VB ফাইল কি?

একটি ভিবি ফাইল হল একটি সোর্স কোড ফাইল যা ভিজ্যুয়াল বেসিক ভাষায় তৈরি করা হয়েছে যা .NET অ্যাপ্লিকেশনগুলির বিকাশের জন্য মাইক্রোসফ্ট দ্বারা তৈরি করা হয়েছিল। ভিন্ন সিনট্যাক্স সহ আরেকটি অনুরূপ ভাষা হল C# যার ফাইলগুলি [.CS](/programming/cs/) ফাইল এক্সটেনশনের সাথে সংরক্ষিত হয়। ফাইল ফরম্যাট কোড লেখার জন্য নিম্ন-স্তরের প্রোগ্রামিং ভাষা প্রদান করে যা EXE বা DLL আকারে চূড়ান্ত আউটপুট ফাইল তৈরি করতে কম্পাইল করা হয়। এগুলি মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও দিয়ে তৈরি এবং কম্পাইল করা যেতে পারে। মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও এক্সপ্রেস এই ধরনের ফাইল তৈরি এবং আপডেট করতে ব্যবহার করা যেতে পারে যা একটি বিনামূল্যের IDE। একটি সাধারণ ভিজ্যুয়াল স্টুডিও প্রজেক্ট [solution](/programming/sln/) VB ভাষা দিয়ে তৈরি করা হয় এই ধরনের এক বা একাধিক ফাইল নিয়ে গঠিত। সংকলনে অন্তর্ভুক্তির জন্য চিহ্নিত ফাইলগুলি [CSPROJ](/programming/csproj/) ফাইলে তালিকাভুক্ত করা হয়েছে যা প্রকল্পের অংশ এবং কম্পাইলারকে চিহ্নিত ফাইলগুলি ব্যবহার করতে বলে৷

## VB ফাইল ফরম্যাট - আরও তথ্য

VB ফাইলগুলি হল পাঠ্য ভিত্তিক ফাইল বিন্যাস যা সম্পাদনার জন্য যেকোনো পাঠ্য সম্পাদকে খোলা যেতে পারে। যাইহোক, সঠিক সিনট্যাক্স হাইলাইটিং সহ একটি সমর্থিত IDE-তে খোলা হলে, কোডটি পড়া এবং সাজানো সহজ। একটি সাধারণ VB ফাইলে রয়েছে:

* নামস্থান ঘোষণা - নির্দিষ্ট নামস্থান দ্বারা সংজ্ঞায়িত একটি নির্দিষ্ট কার্যকারিতা উল্লেখ করার জন্য

* ভেরিয়েবল ঘোষণা - নির্দিষ্ট বাস্তবায়নের জন্য শ্রেণি স্তরের ভেরিয়েবল ঘোষণা করা

* পদ্ধতি ঘোষণা - নির্দিষ্ট কার্যকারিতার জন্য পদ্ধতি ঘোষণা ঘোষণা করা


## ভিবি ফাইল ফরম্যাটের উদাহরণ

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



