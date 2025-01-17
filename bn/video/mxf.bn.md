{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "MXF - উপাদান বিনিময় বিন্যাস",
  "keywords": [
    "MXF",
    "matroska video",
    "mkv format",
    "how to play MXF files",
    "SMPTE",
    "multimedia",
    "video"
  ],
  "description": "MXF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি MXF ফাইল তৈরি এবং খুলতে পারে৷",
  "linktitle": "MXF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mxf-bn"
    }
  },
  "lastmod": "2021-03-01"
}

## একটি MXF ফাইল কি?

.mxf এক্সটেনশন সহ একটি ফাইল হল একটি মাল্টিমিডিয়া কন্টেইনার ফর্ম্যাট যাতে ফাইল সম্পর্কে মেটাডেটা তথ্য সহ ডিজিটাল ভিডিও এবং অডিও মিডিয়া থাকে। এটি SMPTE (সোসাইটি অফ মোশন পিকচার অ্যান্ড টেলিভিশন ইঞ্জিনিয়ার্স) স্ট্যান্ডার্ড অনুসরণ করে যা মিডিয়া এবং বিনোদন শিল্পে কাজ করা ইঞ্জিনিয়ারিং, প্রযুক্তি এবং এক্সিকিউটিভদের পেশাদারদের একটি বিশ্বব্যাপী সমিতি। MXF ফাইলগুলিকে অন্য ফাইল ফরম্যাটে রূপান্তর করা যেতে পারে যেমন [AVI](/video/avi/) বা [MOV](/video/mov/)৷

## MXF ফাইল ফরম্যাট

MXF ফাইলগুলি আসলে বাইনারি ফাইল যা একটি নির্দিষ্ট বিন্যাসে বাইটের একটি ক্রম নিয়ে গঠিত। ডিকোডিং অ্যাপ্লিকেশানগুলিকে অবশ্যই এই ফর্ম্যাটের সাথে সঙ্গতিপূর্ণ হতে হবে যাতে এটি বোঝা যায় এবং এটি থেকে তথ্য বের করে৷ বিন্যাসটি নীচে বর্ণিত KLV কোডিং ব্যবহার করে পশ্চাদগামী সামঞ্জস্য না ভেঙে নতুন আইটেম যোগ করার অনুমতি দেয়।

 * কী - উপাদানটির শনাক্তকারী, একটি SMPTE ইউনিভার্সাল লেবেল (UL)
 * দৈর্ঘ্য - ডেটার দৈর্ঘ্য যা এই আইটেমটির জন্য প্রয়োজনীয় স্থানের পরিমাণ কমাতে ব্যবহৃত পরিবর্তনশীল-দৈর্ঘ্যের এনকোডিং।
 * মান - উপাদানের প্রকৃত মান।

### SMPTE ফরম্যাট স্পেসিফিকেশন

MXF ফাইল বিন্যাস নিম্নলিখিত SMPTE স্পেসিফিকেশন দ্বারা সংজ্ঞায়িত করা হয়েছে.

* SMPTE ST 377-1:2011। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) — ফাইল ফরম্যাট স্পেসিফিকেশন

* SMPTE ST 377-2 (জানুয়ারি 2012 অনুযায়ী কাজ চলছে)। MXF-এর জন্য KLV এনকোডেড এক্সটেনশন সিনট্যাক্স।

* SMPTE ST 378:2004 (সংরক্ষিত 2010)। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — অপারেশনাল প্যাটার্ন 1a (একক আইটেম, একক প্যাকেজ)

* SMPTE ST 379-1:2009। মেটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — MXF জেনেরিক কন্টেইনার

* SMPTE ST 379-2:2010। ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) -- MXF সীমাবদ্ধ জেনেরিক কন্টেইনার

* SMPTE ST 380:2004। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — বর্ণনামূলক মেটাডেটা স্কিম-1 (স্ট্যান্ডার্ড, ডাইনামিক)

* SMPTE ST 381-1:2005। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) — এমএক্সএফ জেনেরিক কন্টেইনারে (ডাইনামিক) MPEG স্ট্রীম ম্যাপিং

* SMPTE ST 381-2:2011। ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — MPEG স্ট্রীমকে MXF সীমাবদ্ধ জেনেরিক কন্টেইনারে ম্যাপ করা

* SMPTE ST 382:2007। ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — MXF জেনেরিক কন্টেইনারে AES3 স্ট্রীম এবং ব্রডকাস্ট ওয়েভ অডিও ম্যাপিং

* SMPTE ST 383:2008। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) — এমএক্সএফ জেনেরিক কন্টেইনারে ডিভি-ডিআইএফ ডেটা ম্যাপিং

* SMPTE ST 384:2005। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) — এমএক্সএফ জেনেরিক কন্টেইনারে আনকম্প্রেসড পিকচারের ম্যাপিং

* SMPTE ST 385:2004। টেলিভিশন - ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) - এমএক্সএফ জেনেরিক কন্টেইনারে SDTI-CP এসেন্স এবং মেটাডেটা ম্যাপিং

* SMPTE ST 386:2004 (সংরক্ষিত 2010)। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) — এমএক্সএফ জেনেরিক কন্টেইনারে ম্যাপিং টাইপ D-10 এসেন্স ডেটা

* SMPTE ST 387:2004 (সংরক্ষিত 2010)। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) — এমএক্সএফ জেনেরিক কন্টেইনারে ম্যাপিং টাইপ D-11 এসেন্স ডেটা

* SMPTE ST 388:2004 (সংরক্ষিত 2010)। টেলিভিশন - ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) - এমএক্সএফ জেনেরিক কন্টেইনারে এ-ল কোডেড অডিও ম্যাপিং

* SMPTE ST 389:2005। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — MXF জেনেরিক কন্টেইনার রিভার্স প্লে সিস্টেম এলিমেন্ট

* SMPTE ST 390:2011। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) — বিশেষায়িত অপারেশনাল প্যাটার্ন "এটম" (একটি আইটেমের সরলীকৃত প্রতিনিধিত্ব)

* SMPTE ST 391:2004 (সংরক্ষিত 2010)। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — অপারেশনাল প্যাটার্ন 1b (একক আইটেম, গ্যাঞ্জেড প্যাকেজ)

* SMPTE ST 392:2004। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — অপারেশনাল প্যাটার্ন 2a (প্লে-লিস্ট আইটেম, একক প্যাকেজ)

* SMPTE ST 393:2004। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — অপারেশনাল প্যাটার্ন 2b (প্লে-লিস্ট আইটেম, গ্যাংড প্যাকেজ)

* SMPTE ST 394:2006। টেলিভিশন - ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) - এমএক্সএফ জেনেরিক কন্টেইনারের জন্য সিস্টেম স্কিম 1

* SMPTE ST 405:2006। টেলিভিশন — ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (এমএক্সএফ) — এমএক্সএফ জেনেরিক কনটেইনার সিস্টেম স্কিম 1 এর জন্য উপাদান এবং স্বতন্ত্র ডেটা আইটেম

* SMPTE ST 407:2006। টেলিভিশন — MXF — অপারেশনাল প্যাটার্নস 3a এবং 3b

* SMPTE ST 408:2006। টেলিভিশন — MXF — অপারেশনাল প্যাটার্নস 1c, 2c, এবং 3c

* SMPTE ST 410: 2008. ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট - জেনেরিক স্ট্রিম পার্টিশন।

* SMPTE ST 422:2006। ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট — MXF জেনেরিক কন্টেইনারে JPEG2000 কোডস্ট্রিম ম্যাপিং

* SMPTE ST 429.4:2006। ডি-সিনেমা প্যাকেজিং — MXF JPEG 2000 অ্যাপ্লিকেশন

* SMPTE ST 429.5:2006। ডি-সিনেমা প্যাকেজিং — টাইমড টেক্সট ট্র্যাক ফাইল

* SMPTE ST 429.6:2006। ডি-সিনেমা প্যাকেজিং — MXF ট্র্যাক ফাইল এসেন্স এনক্রিপশন

* SMPTE ST 434:2006। মেটেরিয়াল এক্সচেঞ্জ ফরম্যাট — মেটাডেটা এবং ফাইল স্ট্রাকচার তথ্যের জন্য XML এনকোডিং

* SMPTE ST 436:2006। টেলিভিশন — VBI লাইন এবং আনুষঙ্গিক ডেটা প্যাকেটের জন্য MXF ম্যাপিং

* SMPTE ST 2019-4:2009। MXF জেনেরিক কন্টেইনারে VC-3 কোডিং ইউনিট ম্যাপিং

* SMPTE ST 2037:2009। MXF জেনেরিক কন্টেইনারে VC-1 ম্যাপিং

* SMPTE RP 2008:2008। ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট — MXF জেনেরিক কন্টেইনারে AVC স্ট্রীম ম্যাপিং

* SMPTE RP 2057:2011। MXF-এ টেক্সট-ভিত্তিক মেটাডেটা ক্যারেজ

* SMPTE EG 41:2004। মেটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — ইঞ্জিনিয়ারিং গাইডলাইন। দ্রষ্টব্য: জানুয়ারী 2012 এ পরামর্শ করার সময় এই নথিটি SMPTE ওয়েব সাইটে আর তালিকাভুক্ত ছিল না।

* SMPTE EG 42:2004। ম্যাটেরিয়াল এক্সচেঞ্জ ফরম্যাট (MXF) — MXF বর্ণনামূলক মেটাডেটা

* SMPTE RDD 3:2008। e-VTR MXF ইন্টারঅপারেবিলিটি স্পেসিফিকেশন

* SMPTE RDD 9-2009। Sony MPEG লং GOP পণ্যের MXF ইন্টারঅপারেবিলিটি স্পেসিফিকেশন

* SMPTE মেটাডেটা রেজিস্ট্রি স্প্রেডশীট মেনু।


### MXF স্ট্রাকচারাল মেটাডেটা

কাঠামোগত মেটাডেটা একটি MXF ফাইলে মৌলিক কারণ এতে ফাইলের বিষয়বস্তু সম্পর্কে দরকারী তথ্য রয়েছে। MXF মেটাডেটাতে ফ্রেম রেট, ফ্রেমের আকার, ফাইল তৈরির তারিখ এবং কাস্টম পরিবর্তনের তারিখের মতো তথ্য থাকে। স্ট্রাকচারাল মেটাডেটা একটি MXF ফাইলের গঠন এবং ক্ষমতা বর্ণনা করে যার মধ্যে টেকনিক্যালি বিভিন্ন প্রয়োজনীয় উপাদান বর্ণনা করা এবং আউটপুট টাইমলাইন কীভাবে তৈরি করা হয়েছে তা বোঝায়।

## তথ্যসূত্র

 * [MXF - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Material_Exchange_Format)
 * [MXF - Progress Report](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
 * [MXF এর জন্য ওপেনসোর্স C++ লাইব্রেরি](http://www.freemxf.org/)

