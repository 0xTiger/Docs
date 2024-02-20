{
  "date": "2019-10-11",
  "keywords": [
    "j2c file",
    "j2c file format",
    "what is a j2c file",
    "file",
    "j2c example",
    "j2c file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "J2C",
  "description": "J2C ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা J2C ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "J2C",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2c-bn"
    }
  },
  "lastmod": "2021-02-14"
}

## একটি J2C ফাইল কি?

.j2c এক্সটেনশন সহ একটি ফাইল হল JPEG ফাইল ফরম্যাটের একটি বৈকল্পিক এবং ওয়েভলেট কম্প্রেশনের সাথে সংকুচিত হয়। এটিতে JPEG 2000 ফাইল ফরম্যাটে মার্কার এবং সেগমেন্টের প্রায় অভিন্ন সিস্টেম রয়েছে। J2C ফাইল বিন্যাসটি JPEG 2000 স্ট্যান্ডের পার্ট 1-এ সংজ্ঞায়িত করা হয়েছে যা ক্ষতিকর এবং ক্ষতিহীন উভয় কম্প্রেশন সমর্থন করে। JPEG 2000 কোডস্ট্রিমটি [JP2](/image/jp2/) বা অন্য ফাইল ফরম্যাটে এম্বেড করার জন্য ডিজাইন করা হয়েছে, যদিও এটি নিজে থেকে একটি ফাইলে প্রদর্শিত হতে পারে। Adobe Photoshop 2020, Adobe Illustrator 2020, এবং Corel Paintshop Pro ব্যবহার করে একটি J2C ফাইল খোলা যেতে পারে।

## J2C ফাইল ফরম্যাট

J2C ফাইল ফরম্যাট JPEG 2000 এর মত যা প্রায়ই .jp2 এবং .jpc হিসাবে সংরক্ষিত হয়। এটি J2C ফাইলগুলিকে XML ফর্ম্যাটে মেটাডেটা এনকোড করার একই পদ্ধতি অনুসরণ করে যেখানে স্ট্যান্ডার্ড 12234-1 Exif ট্যাগ এবং XML উপাদানগুলির মধ্যে একটি রেফারেন্স হিসাবে ব্যবহৃত হয়। এটিকে JPEG 2000 পার্ট-2 এক্সটেনশন দ্বারা আরও উন্নত করা হয়েছে যা অ্যানিমেশন মেকানিজম এবং কোড স্ট্রিম কনফিগারেশনকে একটি একক ছবিতে একত্রিত করে। এই ধরনের বর্ধিত ফাইল-ফরম্যাট ফাইলগুলি [.jpx](/image/jpx/) হিসাবে সংরক্ষিত হয়৷

### একটি JPEG2000 ফাইলের বিন্যাস

JPEG2000 এক্সটেনসিবল ফাইল ফরম্যাটের জন্য সামঞ্জস্যের উপর ভিত্তি করে বিভিন্ন অ্যাপ্লিকেশন সমর্থন করে। যদিও সহজ টাইপটিতে একটি একক চিত্র থাকতে পারে, তবে আরও জটিল প্রকারগুলি একে অপরের উপরে স্তুপীকৃত বা সময়-ভিত্তিক ক্রমযুক্ত চিত্রগুলির একটি সিরিজ অন্তর্ভুক্ত করতে পারে।

#### JP2 বক্স
এটি JP2 ফাইল ফরম্যাটের শীর্ষ-স্তরের বিল্ডিং ব্লক এবং এতে হেডারে একটি টাইপ এবং দৈর্ঘ্যের ক্ষেত্র এবং একটি ডেটা সেকশন রয়েছে। সবচেয়ে উল্লেখযোগ্য ধরনের বক্স হল সংলগ্ন কোডস্ট্রিম বক্স। এই বাক্সটি তার ডেটা বিভাগে JPEG2000 কোডস্ট্রিম সঞ্চয় করে।

#### JPEG2000 কোডস্ট্রিম

JPEG2000 CodeStream হল বাইটের একটি ক্রম যা JPEG2000 সংকুচিত চিত্রকে ডিকোড করার জন্য প্রয়োজন। যদি ফাইলটিতে এই কোডস্ট্রিম ছাড়া অন্য কিছু না থাকে তবে এটিকে একটি কাঁচা কোডস্ট্রিম ফাইল বলা হয়। সাধারণত একটি JPEG কোডস্ট্রিম হল একটি ছবিতে JPEG2000 কম্প্রেশন অ্যালগরিদমের প্রয়োগ, যদিও এটি একমাত্র উপায় নয়।

#### টালি যন্ত্রাংশ ####

একটি JPEG2000 এনকোডেড ইমেজ প্যাকেট নামক ডেটা ইউনিটের একটি সংগ্রহ। এই প্যাকেটগুলিকে টাইল-পার্টস বলে প্যাকেট গ্রুপের ভিতরে কোডস্ট্রিমে রক্ষণাবেক্ষণ করা হয়। একটি ইমেজ এনকোড করার আগে, এনকোডার ছবিটিকে ব্লকের একটি আয়তক্ষেত্রাকার গ্রিডে ভাগ করে, যাকে টাইলস বলা হয় যেখানে প্রতিটি টাইল অন্য টাইলস নির্বিশেষে আলাদাভাবে এনকোড করা হয়।

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 ফাইল ফরম্যাট" >}}

## J2C কম্প্রেশন
JPEG 2000 ওয়েভলেট কম্প্রেশন প্রযুক্তি ব্যবহার করে এটিকে দ্রুত করে তোলে এই সত্যের উপর ভিত্তি করে যে ভিউপোর্ট বা উইন্ডোতে ভিউয়ার যে ছবি প্রদর্শন করে তাতে অপেক্ষাকৃত কম পিক্সেল দেখানো হয়। এটি এই সত্য দ্বারা জোর দেওয়া যেতে পারে যে খুব বড় আকারের চিত্রগুলির জন্য (গিগাবাইটে) শুধুমাত্র কয়েক মেগাবাইট পিক্সেল পর্দায় উপস্থিত হবে। এটি ছবি ডেটার শুধুমাত্র সেই অংশটি দ্রুত আনয়ন এবং রেন্ডার করতে সাহায্য করে যা ডিসপ্লে পিক্সেলগুলি পূরণ করতে প্রয়োজন। এটির জন্য উচ্চ-গতির ডিকম্প্রেশন প্রযুক্তিরও প্রয়োজন হয় যাতে উড়ে যাওয়ার জন্য প্রয়োজনীয় চিত্র তৈরির জন্য ছবি তোলার প্রক্রিয়াকে দ্রুততর করা যায়।

J2C দ্রুত ডিকম্প্রেশনের সুবিধা নেয় এবং স্ক্রীনে দৃশ্যমান চিত্রগুলির অংশ দ্রুত রেন্ডার করার জন্য পিক্সেল ডেটার জন্য শুধুমাত্র প্রয়োজনীয় তথ্য নিয়ে আসে। J2C প্রাথমিকভাবে ডেটা দেখার জন্য এবং এটি সম্পাদনা না করার জন্য ডিজাইন করা হয়েছে।

## J2C সনাক্তকরণ
JPEG 2000 ফাইলে স্বাক্ষর বাইট আছে `FF 4F FF 51`।

### মাইমের প্রকারভেদ
JPEG 2000 ফাইলগুলির জন্য নিবন্ধিত মাইমের প্রকারগুলি অন্তর্ভুক্ত:
  * image/j2c
  * image/jpx
  * ছবি/জেপিএম
  * ভিডিও/এমজে২

## JPEG স্ট্যান্ডার্ডের উপর উন্নতি
JPEG স্ট্যান্ডার্ডের উপর উন্নতির মধ্যে রয়েছে:
  * উচ্চতর কম্প্রেশন কর্মক্ষমতা
  * একাধিক রেজোলিউশন উপস্থাপনা
  * পিক্সেল এবং রেজোলিউশন নির্ভুলতা দ্বারা প্রগতিশীল সংক্রমণ
  * ক্ষতিহীন বা ক্ষতিকর কম্প্রেশনের পছন্দ
  * ত্রুটি স্থিতিস্থাপকতা, নমনীয় ফাইল বিন্যাস
  * উচ্চ গতিশীল পরিসীমা সমর্থন
  * পার্শ্ব চ্যানেল স্থানিক তথ্য

## তথ্যসূত্র ##
  * [টাউবম্যান, ডেভিড; মার্সেলিন, মাইকেল (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)
