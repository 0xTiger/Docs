---
date: 2019-10-11
keywords: prc, .prc, prc file format, how to open prc files, .prc extension, prc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Pআরসি ফাইল ফর্মat
linktitle: PRC
description: Lপিআরসি ফাইল ফরম্যাট এবং এপিআই সম্পর্কে আয় করুন যা পিআরসি ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## PRC ফাইল ফরম্যাট
.prc এক্সটেনশনগুলি MobiPocket দ্বারা পণ্য প্রতিনিধিত্ব কমপ্যাক্ট 3D ফাইল বিন্যাস এবং একটি ই-বুক ফাইল বিন্যাসের জন্য ব্যবহার করা হচ্ছে।

## একটি পণ্য প্রতিনিধিত্ব কমপ্যাক্ট (PRC) ফাইল কি?

PRC (প্রোডাক্ট রিপ্রেজেন্টেশন কমপ্যাক্ট) হল একটি 3D ফাইল ফরম্যাট যা বিশেষ করে CAD (কম্পিউটার-এডেড ডিজাইন) সিস্টেম থেকে আসা 3D ডেটা সঞ্চয়, লোড এবং প্রদর্শনের জন্য অপ্টিমাইজ করা হয়। এটি একটি ক্রমিক বাইনারি ফাইল, একটি পোর্টেবল উপায়ে লেখা। PRC একটি PDF ফাইলে 3D ডেটা এম্বেড করতে ব্যবহার করা যেতে পারে। PRC CAD-এর বেশিরভাগ প্রধান নির্মাণকে সমর্থন করে যেমন সমাবেশ এবং অংশ, 3D সত্তার গাছ, সঠিক জ্যামিতি উপস্থাপনা, ত্রিভুজাকার উপস্থাপনা এবং মার্কআপ। PRC .prc এক্সটেনশন ব্যবহার করে এবং ইন্টারনেট মিডিয়া টাইপ ব্যবহার করা হয় *মডেল/prc*।

PRC হল একটি বহুমুখী ফাইল বিন্যাস যা এর ব্যবহারের উপর ভিত্তি করে হয় নিয়মিত কম্প্রেশন ব্যবহার করে সরাসরি CAD ডেটা উপস্থাপন করতে বা ফাইলের আকার কমাতে উচ্চ কম্প্রেশন ব্যবহার করে সংরক্ষণ করা যেতে পারে। পিআরসি ফরম্যাট ব্যবহার করে পিডিএফ-এ সংরক্ষিত 3D ডেটা CAM এবং CAE অ্যাপ্লিকেশনের সাথে ইন্টারঅপারেবল।

### প্রোডাক্ট রিপ্রেজেন্টেশন কমপ্যাক্ট (PRC) ফাইল ফরম্যাট স্পেসিফিকেশন

একটি পিআরসি ফাইলের একটি প্রধান শিরোনাম বিভাগ থাকে যার পরে এক বা একাধিক ফাইল কাঠামো থাকে এবং শেষে একটি মডেল ফাইল থাকে। একটি ফাইল কাঠামোর একটি শিরোনাম রয়েছে যার পরে নিম্নলিখিত ডেটা বিভাগগুলি রয়েছে:

- **গ্লোবাল**: এতে ফাইল স্ট্রাকচারের প্রতিটি ট্রি সত্তার জন্য রেফারেন্সকৃত ফাইল স্ট্রাকচার এবং রং, লাইন স্টাইল এবং সমন্বয় সিস্টেম রয়েছে।
- **Tree**: It contains a description of the tree of items like product occurrences, part definitions, representation items, and markup.
- **টেসেলেশন**: এতে গাছের পাতার সত্তার (প্রতিনিধিত্বের আইটেম এবং মার্কআপ) সমস্ত টেসেলেটেড (ত্রিভুজাকার) ডেটা থাকে।
- **জ্যামিতি**: এতে গাছের পাতার সত্তার (প্রতিনিধিত্বের আইটেম) সমস্ত সঠিক জ্যামিতি এবং টপোলজি ডেটা রয়েছে।
- **অতিরিক্ত জ্যামিতি**: এতে জ্যামিতির সারাংশ ডেটা থাকে। এটি সম্পূর্ণ জ্যামিতি লোড না করে ফাইলটিকে আংশিকভাবে লোড করার অনুমতি দেয়।

নিম্নলিখিত একটি সাধারণ PRC ফাইলের গঠন.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## PRC এক্সটেনশন সহ একটি MobiPocket ই-বুক ফাইল কি
একটি ই-বুক ফাইল ফরম্যাট যা **Mobipocket** নামে একটি ফরাসি কোম্পানি প্রবর্তন করেছে সেটিও .prc এক্সটেনশন ব্যবহার করছে। প্রাথমিকভাবে, মোবিপকেট একাধিক স্মার্ট ডিভাইস যেমন, ট্যাবলেট পিসি, পিডিএ এবং স্মার্টফোনের জন্য একটি বিনামূল্যের অ্যাপ্লিকেশন চালু করেছে। .prc এক্সটেনশনটি আসলে .mobi-এর অনুরূপ কিন্তু বিশেষ করে PDA-এর জন্য ব্যবহৃত হয় যা শুধুমাত্র **.prc** বা **.pdb** এক্সটেনশন সমর্থন করে।

### মোবিপকেট পিআরসি ফাইল ফরম্যাটের স্পেসিফিকেশন
MobiPocket PRC ফাইল ফরম্যাটটি XHTML ব্যবহার করে ওপেন ইবুক স্ট্যান্ডার্ডের উপর ভিত্তি করে তৈরি করা হয়েছে এবং এতে জাভাস্ক্রিপ্ট এবং ফ্রেম অন্তর্ভুক্ত থাকতে পারে। এমবেডেড ডাটাবেসের সাথে ব্যবহার করার জন্য নেটিভ এসকিউএল কোয়েরির জন্য সমর্থনও উপলব্ধ।

মোবিপকেট রিডারের একটি হোম পেজ লাইব্রেরি রয়েছে। পাঠকরা একটি বইয়ের যেকোনো অংশে ফাঁকা পৃষ্ঠা সন্নিবেশ করতে পারেন এবং পরিবর্তনশীল অঙ্কন যোগ করতে পারেন। টীকা, বুকমার্ক, সংশোধন, নোট এবং অঙ্কনের মতো বস্তুগুলি একক অবস্থান থেকে পরিচালনাযোগ্য। ছবিগুলিকে GIF ফর্ম্যাটে রূপান্তরিত করা হয় এবং সর্বাধিক 64K আকারের যা ছোট স্ক্রীন সহ মোবাইল ফোনের জন্য যথেষ্ট। মোবিপকেট রিডারে ইলেকট্রনিক বুকমার্ক এবং একটি অন্তর্নির্মিত অভিধান রয়েছে।

অনেক PDA, কমিউনিকেটর এবং স্মার্টফোনের জন্য পাঠক পাঠ এবং সমর্থনের জন্য একটি পূর্ণ স্ক্রীন মোড রয়েছে। মোবিপকেট পণ্যগুলি বেশিরভাগ পাম অপারেটিং সিস্টেম, উইন্ডোজ, সিম্বিয়ান, ব্ল্যাকবেরি সমর্থন করে, তবে অ্যান্ড্রয়েড নয়। পাঠক WINE ব্যবহার করে Linux বা Mac OS X এর অধীনে কাজ করে।

## তথ্যসূত্র

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparison of e-book formats - By Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

