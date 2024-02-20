{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "WMV ফাইল ফরম্যাট",
  "description": "WMV ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি WMV ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "WMV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-wmv-bn"
    }
  },
  "lastmod": "2019-09-16"
}

## একটি WMV ফাইল কি?

অ্যাডভান্সড সিস্টেম ফরম্যাট (এএসএফ) হল একটি ডিজিটাল মাল্টিমিডিয়া কন্টেইনার যা মূলত মিডিয়া স্ট্রিম সংরক্ষণ এবং প্রেরণের জন্য ডিজাইন করা হয়েছে। Microsoft Windows Media Video (WMV) হল সংকুচিত ভিডিও বিন্যাস এবং Microsoft Windows Media Audio (WMA) হল Microsoft দ্বারা তৈরি ASF কন্টেইনারে অতিরিক্ত মেটাডেটা সহ সংকুচিত অডিও বিন্যাস। একবার WMV বা WMA ফাইলগুলি উইন্ডোজ মিডিয়া ভিডিও এবং উইন্ডোজ মিডিয়া অডিও কোডেকগুলির সাথে এনকোড করা হলে সেগুলিকে .asf এক্সটেনশন দিয়ে উপস্থাপন করা হয়। WMV ভিডিওর গুণমান বজায় রেখে একটি নেটওয়ার্কে একটি ভাল ট্রান্সমিশন হারের জন্য বড় ফাইলগুলিকে সংকুচিত করে। WMV বিশেষভাবে সমস্ত উইন্ডোজ ডিভাইসে চালানোর জন্য ডিজাইন করা হয়েছে। সোসাইটি অফ মোশন পিকচার অ্যান্ড টেলিভিশন ইঞ্জিনিয়ার্স (SMPTE) দ্বারা প্রমিতকরণের পরে, WMV এখন একটি উন্মুক্ত মান বিন্যাস হিসাবে বিবেচিত হয়।

## ইতিহাস ##

With the help of Microsoft proprietary codecs new compressed video format was developed in 1999 known as WMV7 which was based on MPEG-4 Part 2. আরও দুটি সংস্করণ যেমন WMV8 এবং 9-এ উন্নতিগুলি যোগ করা হয়েছিল। মাইক্রোসফ্ট 2003 সালে স্ট্যান্ডার্ডাইজেশনের জন্য SMPTE-তে WMV-এর একটি 9^^th^^ সংস্করণ জমা দেয় যা অবশেষে 2006 সালে SMPTE 421M নামেও VC-1 নামে পরিচিত। WMV-এর পিছনে ধারণাটি ছিল একটি মিডিয়া ফর্ম্যাট তৈরি করা যা মাইক্রোসফ্ট-সমর্থিত সমস্ত হার্ডওয়্যার এবং সফ্টওয়্যার দ্বারা সমর্থিত হতে পারে। তদুপরি, আরেকটি প্রধান উদ্দেশ্য ছিল একটি সর্বোত্তম পরিস্থিতিতে ইন্টারনেটের মাধ্যমে ভিডিও স্ট্রিমগুলি প্রেরণ করা। SMPTE থেকে প্রমিতকরণের পরে, WMV ব্লু-রে ডিস্কের জন্য একটি ভিডিও বিন্যাসে পরিণত হয়েছে।

## ফাইল ফরম্যাট স্পেসিফিকেশন

### ধারক

সাধারণত, WMV একটি ASF পাত্রে প্যাক করা হয় তবে উপরন্তু, Matroska বা AVI কন্টেইনার যথাক্রমে .mkv এবং .avi এর এক্সটেনশনের সাথে এটিকে সমর্থন করতে পারে।

### উইন্ডোজ মিডিয়া ভিডিও 9

যদিও ডিজিটাল মিডিয়ার লেখা এবং প্লেব্যাকের জন্য উইন্ডোজ মিডিয়া ভিডিও 9 সিরিজে বিভিন্ন অডিও এবং ভিডিও কোডেক উপলব্ধ রয়েছে, তবে WMV-9 কোডেক হল সর্বশেষ এবং সেরা ভিডিও কোডেক কারণ এটি খুব কম বিট রেট থেকে সর্বোত্তম কম্প্রেশন অর্জন করতে পারে অর্থাৎ 160 x 120 এ 10 Kbps থেকে 1920 x 1080 তে 4-8 Mbps তে বিভিন্ন HD ভিডিওর জন্য।

### কোডেক এর গঠন

WMV-9 এর একটি 8 বিট 4:2:0 অভ্যন্তরীণ রঙের বিন্যাস রয়েছে। অন্যান্য জনপ্রিয় ভিডিও কম্প্রেশন স্ট্যান্ডার্ড MPEG-1 এবং H.261 এর মতো, WMV-9 একটি ব্লক-ভিত্তিক গতি ক্ষতিপূরণ এবং স্থানিক রূপান্তর স্কিম ব্যবহার করে। সাধারণভাবে, আমরা বলতে পারি যে এই মানগুলি স্থানিক স্থানচ্যুতিকে সংকেত দিতে মোশন ভেক্টর (MV) নামক 2-ডি পরিমাণের সাহায্যে পূর্ববর্তী পুনর্গঠিত ফ্রেম থেকে ব্লক-বাই-ব্লক মোশন ক্ষতিপূরণ সম্পাদন করে। বর্তমান ব্লকটি একই আকারের পূর্ববর্তী পুনর্গঠিত ফ্রেম থেকে মানগুলির পূর্বাভাসের সাহায্যে গঠিত হয় যা গতি ভেক্টর দ্বারা বর্তমান অবস্থান থেকে স্থানচ্যুত হয়। অবশেষে, অবশিষ্ট ত্রুটিটি গতি-ক্ষতিপূরণ পূর্বাভাসিত ব্লক এবং প্রকৃত ব্লকের মধ্যে পার্থক্য হিসাবে গণনা করা হয়। এই অবশিষ্ট ত্রুটিটি একটি লিনিয়ার এনার্জি-কম্প্যাক্টিং ট্রান্সফর্ম ব্যবহার করে পরিবর্তিত হয় তারপর কোয়ান্টাইজড এবং এনট্রপি কোডেড।

Quantized transform coefficients are entropy decoded, de-quantized, and inverse transformed to produce an approximation of the residual error on the decoder side, which is then added to the motion-compensated prediction to generate the reconstruction. The high-level description of the codec is shown in the following image.

বাকি অংশে WMV-9-এর নতুন উন্নতি নিয়ে আলোচনা করা হবে যা MPEG স্ট্যান্ডার্ডের মতো বাকি ভিডিও কোডিং সমাধান থেকে এটিকে আলাদা করে। WMV-9-এ ইন্ট্রা (I), ভবিষ্যদ্বাণী করা (P), এবং দ্বি-দিকনির্দেশিকভাবে পূর্বাভাসিত (B) ফ্রেম রয়েছে। ইন্ট্রা ফ্রেমগুলি হল সেগুলি যা স্বাধীনভাবে কোড করা হয় এবং অন্য ফ্রেমের উপর নির্ভর করে না। পূর্বাভাসিত ফ্রেমগুলি এমন ফ্রেম যা অতীতের একটি ফ্রেমের উপর নির্ভর করে। একটি পূর্বাভাসিত ফ্রেমের ডিকোডিং শুধুমাত্র সাম্প্রতিক (I) ফ্রেম থেকে শুরু করে বর্তমান ফ্রেমের পূর্বের সমস্ত রেফারেন্স ফ্রেমগুলিকে ডিকোড করার পরেই ঘটতে পারে৷ B ফ্রেম হল এমন ফ্রেম যার দুটি রেফারেন্স রয়েছে—একটি সাময়িক অতীতে এবং একটি সাময়িক ভবিষ্যতে। বি ফ্রেমগুলি তাদের রেফারেন্সের পরে প্রেরণ করা হয়, যার মানে হল যে বি ফ্রেমগুলি ডিকোডিংয়ের সময় তাদের রেফারেন্সগুলি উপলব্ধ রয়েছে তা নিশ্চিত করার জন্য অর্ডারের বাইরে পাঠানো হয়। WMV-9-এ B ফ্রেমগুলি পরবর্তী ফ্রেমের জন্য রেফারেন্স হিসাবে ব্যবহৃত হয় না। এটি বি ফ্রেমগুলিকে ডিকোডিং লুপের বাইরে রাখে, যাতে ড্রিফট বা দীর্ঘমেয়াদী ভিজ্যুয়াল আর্টিফ্যাক্ট ছাড়াই বি ফ্রেমের ডিকোডিংয়ের সময় শর্টকাট নেওয়া যায়। I, P, এবং B ফ্রেমের উপরের সংজ্ঞাটি প্রগতিশীল এবং ইন্টারলেসড সিকোয়েন্স উভয়ের জন্যই ধারণ করে।

ভিডিও কোডেকগুলির কর্মক্ষমতা তাদের রেট-ডিস্টরশন (RD) প্লটের সাথে তুলনা করা হয়। এটি একটি 2-ডি বক্ররেখা যা একটি নির্দিষ্ট বিটরেটে কম্প্রেশন দ্বারা উত্পাদিত বিকৃতি দেখায়।

WMV-9 নীচে তালিকাভুক্ত বিভিন্ন কৌশল প্রবর্তনের মাধ্যমে এই সমস্যার সমাধান করেছে:

1. অভিযোজিত ব্লক আকার রূপান্তর

2. সীমিত নির্ভুলতা রূপান্তর সেট

3. মোশন ক্ষতিপূরণ

4. কোয়ান্টাইজেশন এবং ডিকোয়ান্টাইজেশন

5. উন্নত এনট্রপি কোডিং

6. লুপ ফিল্টারিং

7. উন্নত বি ফ্রেম কোডিং

8. ইন্টারলেস কোডিং

9. ওভারল্যাপ মসৃণ করা

10. কম হারের সরঞ্জাম

11. বিবর্ণ ক্ষতিপূরণ

## তথ্যসূত্র

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html )

* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)

