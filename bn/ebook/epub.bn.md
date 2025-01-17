{
  "date": "2019-12-12",
  "keywords": [
    "EPUB",
    "file",
    "extension",
    "format",
    "E-Book",
    "Digital book"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "EPUB ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি EPUB ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "title": "একটি EPUB ফাইল কি?",
  "linktitle": "EPUB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-epub-bn"
    }
  },
  "lastmod": "2019-12-12"
}

## একটি EPUB ফাইল কি?

.epub এক্সটেনশন সহ ফাইলগুলি হল একটি ই-বুক ফাইল ফর্ম্যাট যা প্রকাশক এবং ভোক্তাদের জন্য একটি মানক ডিজিটাল প্রকাশনা বিন্যাস প্রদান করে৷ ফরম্যাটটি এতটাই সাধারণ হয়ে উঠেছে যে এটি অনেক ই-রিডার এবং সফ্টওয়্যার অ্যাপ্লিকেশন দ্বারা সমর্থিত। উদাহরণস্বরূপ, Mac OS-এ, আগে থেকে ইনস্টল করা **Books** সফ্টওয়্যার এই ধরনের ফাইল খোলার জন্য সমর্থন প্রদান করে। এছাড়াও, স্মার্টফোন, ট্যাবলেট এবং কম্পিউটারের জন্য প্রচুর সামঞ্জস্যপূর্ণ সফ্টওয়্যার উপলব্ধ রয়েছে। EPUB ফাইলের মানগুলি [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF) দ্বারা বজায় থাকে৷ EPUB 3 সংস্করণটি বুক ইন্ডাস্ট্রি স্টাডি গ্রুপ (BISG) দ্বারাও অনুমোদিত, যা কন্টেন্ট প্যাকেজিংয়ের জন্য মানসম্মত সেরা অনুশীলন, গবেষণা, তথ্য এবং ইভেন্টগুলির জন্য একটি নেতৃস্থানীয় বই বাণিজ্য সমিতি।

## EPUB ফাইল ফরম্যাটের সংক্ষিপ্ত ইতিহাস

* **অক্টোবর 2007** - EPUB 2.0 অনুমোদিত হয়েছে

* **সেপ্টেম্বর 2010** - রক্ষণাবেক্ষণ আপডেট প্রকাশিত হয়েছে

* **অক্টোবর 2011** - EPUB 3.0 স্পেসিফিকেশন কার্যকর হয়েছে

* **জুন 2014** - 3.0 সংস্করণের পরিবর্তে ছোটখাট রক্ষণাবেক্ষণ আপডেট প্রকাশ করা হয়েছে

* **জানুয়ারি 2017** - EPUB 3.1 কার্যকর হয়েছে


## EPUB ফাইল ফরম্যাট

EPUB ফাইল ফরম্যাট হল একটি সংরক্ষণাগার যাকে [ZIP](/compression/zip/) এক্সটেনশনে পুনঃনামকরণ করা যেতে পারে এবং যেকোন আর্কাইভ এক্সট্র্যাক্টর দিয়ে আর্কাইভ এক্সট্র্যাক্ট করে এর বিষয়বস্তু দেখা যেতে পারে। এটি একটি খোলা XML-ভিত্তিক বিন্যাস এবং এতে HTML ফাইল, ছবি, CSS শৈলী শীট এবং অন্যান্য উপাদান রয়েছে। এটিকে অনেকগুলি সফ্টওয়্যার অ্যাপ্লিকেশন এবং API-এর মাধ্যমে PDF, Mobi এবং অন্যান্য ফাইল ফরম্যাটে রূপান্তর করা যেতে পারে।

{{< figure src="../epub.png" alt="EPUB ফাইল ফরম্যাট" >}}

**EPUB ই-বুক ম্যাক ওএস বুকস অ্যাপ্লিকেশনের সাথে খোলা হয়েছে**

EPUB ফাইল বিন্যাস তিনটি উন্মুক্ত মান অনুসরণের উপর ভিত্তি করে।

### ওপেন পাবলিক স্ট্রাকচার (OPS) ###

একটি EPUB 2.0 ফাইল একটি প্রকাশনার বিষয়বস্তু তৈরি করতে XHTML 1.1 ব্যবহার করে। সংক্ষেপে এর মানে হল যে একটি EPUB ফাইল এক বা একাধিক ওয়েব পৃষ্ঠা নিয়ে গঠিত। যদিও আপনি একটি বই বা সংবাদপত্রের সম্পূর্ণ বিষয়বস্তু একটি একক পৃষ্ঠায় অন্তর্ভুক্ত করতে পারেন, তবে কর্মক্ষমতা এবং সামঞ্জস্যতার কারণে এই ধরনের ফাইল 300K এর বেশি না হওয়াই ভালো। নিয়মিত ওয়েব পৃষ্ঠাগুলির মতোই, ক্যাসকেডিং স্টাইল শীট (সিএসএস) ব্যবহার করে স্টাইলিং এবং বিন্যাস সংজ্ঞায়িত করা হয়। EPUB ফাইলগুলিতে CSS2 এর একটি সাবসেট (সীমিত সিরিজের কমান্ড) ব্যবহার করা প্রয়োজন। CSS3 এর অনেক নতুন বৈশিষ্ট্য, যেমন গোলাকার বাক্স বা ড্রপ শ্যাডো, এখনও উপলব্ধ নয়। পশ্চাদগামী সামঞ্জস্যের জন্য, একজন সৃষ্টিকর্তা সামগ্রী এনকোড করতে XHTML এর পরিবর্তে DTBook ব্যবহার করতে পারেন।

### ওপেন প্যাকেজিং ফরম্যাট (OPF) ###

স্পেক্সের এই অংশটি মেটাডেটা (লেখক এবং প্রকাশক কে, শিরোনাম কি,..), ম্যানিফেস্ট (একটি ইপাব ফাইলের মধ্যে থাকা সমস্ত ফাইলের তালিকা) এবং বিষয়বস্তুর সারণীর মতো কাঠামোগত তথ্য নিয়ে কাজ করে। এই সমস্ত ডেটা XML ব্যবহার করে এমবেড করা হয়।

### ওপেন কন্টেইনার ফরম্যাট (OCF) ###

As the above descriptions should have made it clear an EPUB document consists of a series of files. The OCF specs define how all those files end up being packaged in one single container file. ZIP compression is used for this.

## সমর্থিত ইমেজ ফাইল ফরম্যাট ##

EPUB ফাইল ফরম্যাট নিম্নলিখিত ইমেজ ফাইল ফরম্যাট সমর্থন করে।

* [GIF](/image/gif/)

* [JPG](/image/jpeg/)

* [PNG](/image/png/)

* [SVG](/page-description-language/svg/)

## তথ্যসূত্র ##
* [EPUB - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/EPUB)
