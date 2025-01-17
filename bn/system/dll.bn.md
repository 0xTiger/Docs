{
  "date": "2021-06-29",
  "keywords": [
    "DLL",
    "extension",
    "file",
    "format",
    "system",
    "Dynamic Link Library",
    "settings",
    "programs",
    "computer",
    "application"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "DLL - ডাইনামিক লিঙ্ক লাইব্রেরি",
  "description": "DLL ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা DLL ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "DLL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dll-bn"
    }
  },
  "lastmod": "2021-06-29"
}

## একটি DLL ফাইল কি? ##

একটি DLL ফাইল বা ডাইনামিক লিঙ্ক লাইব্রেরি হল এক ধরনের এক্সিকিউটেবল ফাইল। এটি আপনার ডিভাইসে সবচেয়ে বেশি পাওয়া এক্সটেনশন ফাইলগুলির মধ্যে একটি এবং সাধারণত আপনার উইন্ডোজের System32 ফোল্ডারে সংরক্ষণ করা হয়। ডিএলএল এক্সটেনশন ফাইলটি মাইক্রোসফ্ট দ্বারা তৈরি করা হয়েছিল এবং তাদের দ্বারা জনপ্রিয়ভাবে ব্যবহৃত হয়। এটি একটি উচ্চ জনপ্রিয়তা ব্যবহারকারী রেটিং আছে. DLL একটি শেলফ হিসাবে কাজ করে যাতে *ড্রাইভার/প্রক্রিয়া/ফাংশন/বৈশিষ্ট্য* থাকে যা উইন্ডোজ সার্ভার দ্বারা একটি প্রোগ্রাম/অ্যাপ্লিকেশনের জন্য ডিজাইন এবং প্রয়োগ করা হয়। একটি একক DLL ফাইল বিভিন্ন উইন্ডোজ প্রোগ্রামের মধ্যে শেয়ার করা যেতে পারে। এই এক্সটেনশন ফাইলগুলি আপনার ডিভাইসে উইন্ডোজ প্রোগ্রামগুলিকে মসৃণভাবে চালানোর জন্য অত্যাবশ্যক কারণ তারা প্রোগ্রামে বিভিন্ন ফাংশন যেমন ফাইল লেখা এবং পড়া, আপনার সেটআপের বাইরের অন্যান্য ডিভাইসগুলির সাথে সংযোগ স্থাপনের জন্য সক্রিয় এবং চালানোর জন্য দায়ী৷
তবে এই ফাইলগুলি শুধুমাত্র এমন একটি ডিভাইসে খোলা যেতে পারে যা উইন্ডোজের যেকোনো সংস্করণ সমর্থন করে (উইন্ডোজ 7/উইন্ডোজ 10/ইত্যাদি) এবং তাই ম্যাক ওএস সমর্থন করে এমন ডিভাইসে সরাসরি খোলা যাবে না। (যদি আপনি ম্যাক ওএসে একটি DLL ফাইল খুলতে চান, বিভিন্ন বহিরাগত অ্যাপ্লিকেশনগুলি সেগুলি খুলতে সহায়তা করতে পারে।)


## DLL ফাইল ফরম্যাট ##

DLL ফাইলটি মাইক্রোসফ্ট দ্বারা বিকশিত হয়েছে এবং এতে .dll এক্সটেনশন রয়েছে যা টাইপের প্রতিনিধিত্ব করে। এটি Windows 1.0 সার্ভারের একটি অবিচ্ছেদ্য অংশ এবং তার পরেও। এটি একটি বাইনারি ফাইল টাইপ এবং মাইক্রোসফ্ট উইন্ডোজের সমস্ত সংস্করণ দ্বারা সমর্থিত। এই ফাইল টাইপটি উইন্ডোজ প্রোগ্রামগুলির মধ্যে একটি শেয়ার্ড লাইব্রেরি সিস্টেম তৈরি করার উপায় হিসাবে তৈরি করা হয়েছিল, প্রোগ্রামগুলিকে পুনরায় লিঙ্ক করার প্রয়োজন ছাড়াই প্রোগ্রাম লাইব্রেরিতে পৃথক এবং স্বাধীন সম্পাদনা বা পরিবর্তনের অনুমতি দেওয়ার জন্য।


## DLL উদাহরণ ##

একটি DLL এন্ট্রি পয়েন্টের উদাহরণ কোড নীচে পাওয়া যাবে:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## রেফারেন্স ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
