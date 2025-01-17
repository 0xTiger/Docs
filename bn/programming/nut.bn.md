{
  "date": "2021-09-23",
  "keywords": [
    "NUT",
    "file",
    "extension",
    "file format",
    "NUT рrоgrаmming lаnguаge",
    "Programming Guide",
    "NUT example",
    "NUT file format",
    "squirrel language",
    ".nut extension file",
    "NUT files"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "NUT - কাঠবিড়ালি ভাষার ফাইল",
  "description": "NUT ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি NUT ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "NUT",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nut-bn"
    }
  },
  "lastmod": "2021-09-23"
}

## একটি NUT ফাইল কি?

NUT ফাইল ফরম্যাটটি প্রোগ্রামিং ভাষার অন্তর্গত যা কাঠবিড়ালি নামে পরিচিত। এটি একটি অবজেক্ট-ওরিয়েন্টেড, উচ্চ স্তরের এবং অপরিহার্য প্রোগ্রামিং ভাষা যা বেশিরভাগ এমবেডেড সিস্টেম এবং ভিডিও গেমগুলিতে ব্যবহৃত হয়।

কাঠবিড়ালি ভাষাটিকে একটি হালকা ওজনের স্ক্রিপ্টিং ভাষা হিসাবে বিবেচনা করা হয় যা আকার এবং ব্যান্ডউইথ অনুযায়ী সহজেই সামঞ্জস্য করা যায়। এতে স্বয়ংক্রিয় রেফারেন্স গণনা এবং মেমরিতে আবর্জনা ব্যবস্থাপনার সুবিধা জড়িত।

কাঠবিড়ালি ভাষার সিনট্যাক্স বিকাশকারীদের আকর্ষণ করে কারণ এটি সি-এর মতো এবং এতে স্ক্রিপ্টিং ভাষার বৈশিষ্ট্য জড়িত। তবে এখনও, এই উদ্দেশ্যে অন্যান্য জনপ্রিয় প্রোগ্রামিং ভাষার তুলনায় এটির বেশ কম সুবিধা রয়েছে।



## সংক্ষিপ্ত ইতিহাস ##

It was designed by Alberto Demichelis in 2003. যাইহোক, এই ভাষার একটি স্থিতিশীল সংস্করণ 2016 সালে প্রকাশিত হয়েছিল। এটি zlib/ libpng-এর লাইসেন্সের অধীনে ডিজাইন করা হয়েছিল। 2010 সালে লাইসেন্স পরিবর্তন করা হয় এবং MIT-তে স্থানান্তর করা হয়। এই ভাষাটিকে [LUA](/programming/lua/) (প্রোগ্রামিং ভাষা) এর একটি অনুপ্রাণিত সংস্করণ হিসাবে বিবেচনা করা হয়। এটিকে আরও সুবিধাজনক করতে আলবার্তো দ্বারা ডিজাইন করা ওয়েবসাইটে পূর্বের ভাষার জন্য পরামর্শের একটি তালিকা রয়েছে।


## প্রযুক্তিগত বৈশিষ্ট্য ##

কাঠবিড়ালি ভাষার বৈশিষ্ট্য এবং বৈশিষ্ট্য একাধিক। এটি ডায়নামিক টাইপিং, প্রতিনিধিদের সম্পত্তি, ক্লাস এবং ইন্টারফেসের বিভিন্ন ব্যবহার সুবিধা প্রদান করে। এই ভাষার সিনট্যাক্সের সাথে সি ভাষার সিনট্যাক্সের মিল রয়েছে। এন্ডুরো/এক্স (একটি ক্লাস্টার অ্যাপ্লিকেশন সার্ভার) এর মতো অ্যাপ্লিকেশনগুলি এই ভাষা ব্যবহার করে। যেমন কাঠবিড়ালি ভিডিও গেমগুলির জন্যও ব্যবহৃত হয়, সেগুলির মধ্যে কয়েকটি হল OpenTTD, GTA IV, ইত্যাদি।

The stable release of the language is 3.0.7. মির্থকিট নামে পরিচিত একটি টুলকিট দ্বি-মাত্রিক গেমগুলির জন্য একটি ওপেন-সোর্স এবং ক্রস-প্ল্যাটফর্ম প্রদান করতে কাঠবিড়ালি প্রোগ্রামিং ভাষা ব্যবহার করে। এই ভাষার প্রকৃতি গতিশীল এবং বেশিরভাগ বৈশিষ্ট্যই [Python](/programming/py/), LUA, ইত্যাদির মতো। এতে রেজিস্টার-ভিত্তিক VM প্রয়োগ করাও জড়িত। LUA এর তুলনায় কাঠবিড়ালির কর্মক্ষমতা ধীর।

এছাড়াও আরেকটি .nut এক্সটেনশন ফাইল টাইপ রয়েছে যার কারণে আপনার কোন NUT ফাইলটি আছে তা খুঁজে বের করতে ফাইলের আকার দেখতে হবে। কাঠবিড়ালী স্ক্রিপ্ট NUT ফাইলগুলি বেশিরভাগই 1 MB এর থেকে ছোট যেখানে ভিডিও NUT ফাইলগুলি সাধারণত 1 MB এর চেয়ে বড় হয়।


## NUT ফাইল ফরম্যাটের উদাহরণ ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## রেফারেন্স ##

* [NUT - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Squirrel_(programming_language))




