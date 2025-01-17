{
  "date": "2019-10-11",
  "keywords": [
    "vbproj",
    "file",
    "extension",
    "file format",
    "VB Project File",
    "Programming Guide"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "VBPROJ",
  "description": "VBPROJ ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা VBPROJ ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "VBPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vbproj-bn"
    }
  },
  "lastmod": "2020-09-10"
}

## একটি VBPROJ ফাইল কি?

.vbproj এক্সটেনশন সহ একটি ফাইল হল একটি মাইক্রোসফ্ট ভিজ্যুয়াল বেসিক প্রজেক্ট ফাইল যা মাইক্রোসফটের MSBuild ইঞ্জিন দ্বারা ভিজ্যুয়াল স্টুডিও সমাধানের মধ্যে প্রকল্পগুলি তৈরি করতে ব্যবহৃত হয়। এটি [C#](/programming/cs/) এ লেখা .NET প্রকল্পগুলির জন্য [CSPROJ](/programming/csproj/) ফাইলের অনুরূপ৷ MSBuild ইঞ্জিন VBPROJ ফাইল থেকে বিভিন্ন গ্রুপে থাকা তথ্য পড়ে এবং আউটপুট ফাইল তৈরি করে। একটি VBPROJ ফাইলে গ্লোবাল আইডেন্টিফায়ার, ক্লাস এবং প্রোপার্টি সম্পর্কিত তথ্য থাকতে পারে যা প্রোজেক্টকে সংজ্ঞায়িত করে। VBPROJ ফাইলগুলি Microsoft Visual Studio এবং Windows এবং MacOS অপারেটিং সিস্টেমের নোটপ্যাডের মতো সাধারণ পাঠ্য সম্পাদক ব্যবহার করে খোলা এবং সম্পাদনা করা যেতে পারে।

## VBPROJ ফাইল ফরম্যাট - আরও তথ্য

VBPROJ ফাইলগুলি হল পাঠ্য ফাইল যা [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019) এর উপর ভিত্তি করে [XML](/web/xml/) ফাইল বিন্যাসে লেখা হয়৷ একটি VBPROJ ফাইলে XML ট্যাগের আকারে তথ্য থাকে যা সেই নির্দিষ্ট গোষ্ঠীর সেটিংস সম্পর্কিত তথ্য সংজ্ঞায়িত করে। মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও আইডিই-তে এই সেটিং ফাইলগুলি খুলতে এবং সম্পাদনা করার জন্য অত্যন্ত সুপারিশ করা হয়।

### VBPROJ উপাদান

একটি VB সেটিংস ফাইলের উপাদান উপাদানগুলি নিম্নলিখিত ছবিতে দেখানো হয়েছে।

{{< figure src="../vbproj.png" alt="VBPROJ ফাইল ফরম্যাট" >}}

The following table gives a brief description of these elements.

|উপাদান|বর্ণনা|
---|---|
|প্রকল্প| প্রতিটি প্রোজেক্ট ফাইলের রুট এলিমেন্ট এবং প্রোজেক্ট ফাইলের জন্য XML স্কিমা সনাক্ত করার পাশাপাশি বিল্ড প্রক্রিয়ার জন্য এন্ট্রি পয়েন্টগুলি নির্দিষ্ট করার জন্য বৈশিষ্ট্যগুলি অন্তর্ভুক্ত করতে পারে|
|বৈশিষ্ট্য এবং শর্তাবলী| বৈশিষ্ট্যগুলি কী-মান জোড়া নিয়ে গঠিত এবং একটি প্রপার্টিগ্রুপ উপাদানের সাথে সংজ্ঞায়িত করা হয়। সম্পত্তি উপাদান নাম সম্পত্তি কী প্রতিনিধিত্ব করে এবং উপাদানের বিষয়বস্তু সম্পত্তি মান সংজ্ঞায়িত করে।|
|আইটেম এবং আইটেমগ্রুপ|প্রজেক্ট ফাইলের আইটেমগুলি হল বিল্ড প্রক্রিয়ার ইনপুট যেমন ফাইল-কোড ফাইল, কনফিগারেশন ফাইল, কমান্ড ফাইল এবং বিল্ড প্রক্রিয়ার অংশ হিসাবে প্রয়োজনীয় অন্যান্য। আইটেমগুলিকে একটি আইটেমগ্রুপ উপাদানের মধ্যে সংজ্ঞায়িত করা আবশ্যক৷
|লক্ষ্য এবং কাজ | একটি টাস্ক উপাদান একটি পৃথক বিল্ড নির্দেশনা (বা টাস্ক) প্রতিনিধিত্ব করে। MSBuild-এ কপি, CSC, VBC, Exec এর মতো পূর্বনির্ধারিত অনেকগুলি কাজ অন্তর্ভুক্ত রয়েছে। টাস্কগুলিকে সর্বদা একটি `টার্গেট` এলিমেন্টে থাকতে হবে যা এক বা একাধিক টাস্কের সেট যা ক্রমানুসারে সম্পাদিত হয় এবং একটি প্রজেক্ট ফাইলে একাধিক টার্গেট থাকতে পারে।|

## তথ্যসূত্র

* [প্রজেক্ট ফাইল বোঝা](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

* [MSBuild স্কিমা এলিমেন্টস](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)


