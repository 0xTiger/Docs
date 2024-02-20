{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "LAZ - সংকুচিত LIDAR ডেটা এক্সচেঞ্জ ফাইল",
  "description": "LAZ ফাইল বিন্যাস এবং API সম্পর্কে জানুন যেগুলি LAZ ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "LAZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-laz-bn"
    }
  },
  "lastmod": "2023-07-18"
}

## একটি LAZ ফাইল কি?

LAZ ফাইল ফরম্যাট হল LAS (Lidar LASer) ফাইল ফরম্যাটের একটি সংকুচিত সংস্করণ, যা বিশেষভাবে লিডার পয়েন্ট ক্লাউড ডেটা সংরক্ষণের জন্য ডিজাইন করা হয়েছে। LAZ ফাইলগুলি LAS ফাইলগুলির মতো একই ডেটা এবং কাঠামো বজায় রাখে তবে মূল ডেটা বিশ্বস্ততা সংরক্ষণের সময় ফাইলের আকার হ্রাস করার জন্য ক্ষতিহীন কম্প্রেশন কৌশল ব্যবহার করে।

## LAZ ফাইল বিন্যাস - সংক্ষিপ্ত ইতিহাস

বৃহৎ লিডার ডেটাসেটগুলির দক্ষ সঞ্চয়স্থান এবং ট্রান্সমিশনের জন্য ক্রমবর্ধমান চাহিদা মোকাবেলার জন্য LAZ ফাইল বিন্যাস তৈরি করা হয়েছিল। LAS ফাইলগুলিকে সংকুচিত করার মাধ্যমে, LAZ ফাইলগুলি তাদের আকার উল্লেখযোগ্যভাবে হ্রাস করে, তাদের পরিচালনা এবং স্থানান্তর করা সহজ করে তোলে। লিডার পয়েন্ট বৈশিষ্ট্যগুলিকে আরও কমপ্যাক্ট আকারে উপস্থাপন করার জন্য এনট্রপি কোডিং এবং পরিবর্তনশীল-দৈর্ঘ্য এনকোডিংয়ের মতো বিভিন্ন অ্যালগরিদমের সংমিশ্রণ ব্যবহার করে কম্প্রেশনটি অর্জন করা হয়।

## LAZ ফাইল ফরম্যাট

সংকোচন সত্ত্বেও, LAZ ফাইলগুলি কোনও তথ্যের ক্ষতি ছাড়াই আসল LAS ডেটা সম্পূর্ণরূপে পুনরুদ্ধার করার ক্ষমতা বজায় রাখে। এর মানে হল যে একবার একটি LAZ ফাইল ডিকম্প্রেস হয়ে গেলে, এটি একটি আনকম্প্রেসড LAS ফাইলের মতো একইভাবে প্রক্রিয়া এবং বিশ্লেষণ করা যেতে পারে। কম্প্রেশন এবং ডিকম্প্রেশন প্রক্রিয়া সাধারণত বিশেষায়িত সফ্টওয়্যার বা লাইব্রেরি ব্যবহার করে সঞ্চালিত হয় যা LAZ ফর্ম্যাটকে সমর্থন করে।

LAZ ফাইল বিন্যাস LAS ফাইলগুলির সাথে সামঞ্জস্য বজায় রাখে, লিডার সফ্টওয়্যার এবং প্রক্রিয়াকরণ সরঞ্জাম জুড়ে আন্তঃকার্যযোগ্যতা নিশ্চিত করে। এর মানে হল যে অ্যাপ্লিকেশনগুলি LAS ফাইলগুলি পড়তে এবং প্রক্রিয়া করতে পারে তারা সাধারণত LAZ ফাইলগুলিকে কোনো পরিবর্তন ছাড়াই পরিচালনা করতে পারে। উপরন্তু, LAZ ফাইলগুলিতে এখনও ফাইল শিরোনাম, পরিবর্তনশীল দৈর্ঘ্য রেকর্ড (VLRs) এবং পয়েন্ট ডেটা রেকর্ড অন্তর্ভুক্ত থাকে, LAS ফাইলগুলির মতো একই কাঠামো সংরক্ষণ করে।

## LAZ ফাইল ফরম্যাটের সুবিধা

**কমিত ফাইলের আকার:** LAZ কম্প্রেশন উল্লেখযোগ্যভাবে লিডার ডেটাসেটের ফাইলের আকার হ্রাস করে, সেগুলিকে আরও পরিচালনাযোগ্য করে তোলে এবং সংরক্ষণ এবং স্থানান্তর করা সহজ করে তোলে।

**ডেটা ইন্টিগ্রিটি:** এলএজেড কম্প্রেশন ক্ষতিহীন, যার অর্থ হল ডিকম্প্রেস করা ডেটা হল আসল এলএএস ডেটার একটি সঠিক প্রতিরূপ, যাতে তথ্য বা নির্ভুলতার কোনো ক্ষতি না হয় তা নিশ্চিত করে।

**ইন্টারঅপারেবিলিটি:** এলএজেড ফাইলগুলি এলএএস ফাইলগুলির সাথে সামঞ্জস্যপূর্ণ, বিদ্যমান লিডার সফ্টওয়্যার এবং ওয়ার্কফ্লোগুলির সাথে বিরামহীন একীকরণের অনুমতি দেয়৷

**দক্ষ প্রক্রিয়াকরণ:** তাদের আকার হ্রাসের কারণে, LAZ ফাইলগুলি আরও দ্রুত লোড এবং প্রক্রিয়া করা যেতে পারে, সামগ্রিক প্রক্রিয়াকরণ এবং বিশ্লেষণের সময় উন্নত করে।

কম্প্রেসড লিডার ডেটা স্টোরেজ এবং এক্সচেঞ্জের জন্য একটি স্ট্যান্ডার্ড হিসাবে LAZ ফাইল ফর্ম্যাটটি লিডার সম্প্রদায়ে ব্যাপকভাবে গৃহীত হয়েছে। এটি দক্ষ ডেটা সংকোচন এবং ডেটা অখণ্ডতার মধ্যে একটি ভারসাম্য সরবরাহ করে, মূল ডেটার নির্ভুলতা এবং গুণমান বজায় রেখে বড় লিডার ডেটাসেটগুলির সহজ পরিচালনা সক্ষম করে।

## তথ্যসূত্র

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm