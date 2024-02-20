{
  "date": "2021-02-15",
  "keywords": [
    "vp6 file",
    "vp6 file format",
    "what is an vp6 file",
    "file",
    "vp6 example",
    "vp6 file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "VP6 - TrueMotion ভিডিও ফাইল",
  "description": "VP6 ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা VP6 ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "VP6",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp6-bn"
    }
  },
  "lastmod": "2021-02-16"
}

## একটি VP6 ফাইল কি?

VP6 is a lossy compression video format that was introduced by On2 technologies in May 2003. এটি V3, V4 এবং V5 সহ TrueMotion দ্বারা তৈরি করা ভিডিও কোডেক সিরিজের একটি অংশ। বিবিসি রিপোর্ট এবং কুইকলিঙ্ক সফ্টওয়্যারের মতো সম্প্রচার ক্ষেত্রের ফর্ম্যাটটি খুব শীঘ্রই ব্যবহার করা হয়েছিল। 2005 সালের জানুয়ারিতে ভিপি 7 কোডেক দ্বারা ভিপি 6-এর স্থলাভিষিক্ত হয়।

## VP6 ফাইল ফরম্যাট

Complete specifications for V6 files are not available publicly. On2 made the specifications public initially but soon these were made non-available for general users. An unofficial documentation of the VP6 file format is available at [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) that can be referred for developer's reference.

### ম্যাক্রোব্লক (MB)

MPEG-2, MPEG-4 অংশ 2 এবং 10 এর মতো, একটি VP6 ফাইলের প্রতিটি ভিডিও ফ্রেম 16x16 ম্যাক্রোব্লক (MB) এর একটি অ্যারে দিয়ে গঠিত। প্রতিটি MB নিম্নলিখিত মোডগুলির মধ্যে একটি হতে পারে:

 * ইন্ট্রা এমবি
 * ইন্টার এমবি, নাল এমভি, পূর্ববর্তী ফ্রেম রেফারেন্স
 * ইন্টার এমবি, ডিফারেনশিয়াল এমভি, পূর্ববর্তী ফ্রেম রেফারেন্স
 * ইন্টার এমবি, চার এমভি, পূর্ববর্তী ফ্রেম রেফারেন্স
 * ইন্টার এমবি, এমভি 1, পূর্ববর্তী ফ্রেম রেফারেন্স
 * ইন্টার এমবি, এমভি 2, পূর্ববর্তী ফ্রেম রেফারেন্স
 * ইন্টার এমবি, নাল এমভি, বুকমার্ক করা ফ্রেম রেফারেন্স
 * ইন্টার এমবি, ডিফারেনশিয়াল এমভি, বুকমার্ক করা ফ্রেম রেফারেন্স
 * ইন্টার এমবি, এমভি 1, বুকমার্ক করা ফ্রেম রেফারেন্স
 * ইন্টার MB, MV 2, বুকমার্ক করা ফ্রেম রেফারেন্স

### ফ্রেম হেডার

একটি VP6 এর ফ্রেম শিরোনামটি নীচে দেখানো হয়েছে যা বিগ-এন্ডিয়ান বিট প্যাকিং অনুসরণ করে।

|সিনট্যাক্স|বিটের সংখ্যা|টাইপ|সিমেন্টেক্স|
---|---|---|---|
|frame_mode|1|Enum|0x0 একটি ইন্ট্রা ফ্রেম|
|qp |6 | স্বাক্ষরবিহীন | পরিমাপকরণ প্যারামিটার বৈধ পরিসীমা 0..63|
|মার্কার| 1| ধ্রুবক| 0=VP61/62, 1=VP60|
|যদি (ফ্রেম_মোড == 0) { | 0 | |INTRA_FRAME এর সমান|
|সংস্করণ |5| ধ্রুবক| 6=VP60/61, 7=VP60(ইলেক্ট্রনিক আর্টস), 8=VP62|
|সংস্করণ2 |2| ধ্রুবক |0=VP60, 3=VP61/62|
|ইন্টারলেস |1| বুলিয়ান |সত্য (1) মানে ইন্টারলেস ব্যবহার করা হবে|
|if (মার্কার==1 বা সংস্করণ2==0) {||||
|অফসেট |16 |স্বাক্ষরবিহীন | সেকেন্ডারি বাফার অফসেট (বাফার শুরুর সাথে সম্পর্কিত বাইট)|
|}||||
|dim_y |8| স্বাক্ষরবিহীন| ভিডিওর ম্যাক্রোব্লক উচ্চতা|
|dim_x |8| স্বাক্ষরবিহীন| ভিডিওর ম্যাক্রোব্লক প্রস্থ|
|render_y |8 | স্বাক্ষরবিহীন |ভিডিওর উচ্চতা প্রদর্শন |
|render_x |8 |আনসাইন করা |ভিডিওর প্রস্থ প্রদর্শন |
|}অন্য{||||
|if (মার্কার==1 বা সংস্করণ2==0) {||||
|অফসেট |16 |আনসাইনড |সেকেন্ডারি বাফার অফসেট (বাফারের শুরুতে বাইট আপেক্ষিক)|
|}||||
|}||||

## তথ্যসূত্র

* [VP6 উইকিপিডিয়া](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

