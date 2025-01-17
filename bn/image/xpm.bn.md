{
  "date": "2019-10-11",
  "keywords": [
    "xpm file",
    "xpm file format",
    "what is a xpm file",
    "file",
    "xpm example",
    "xpm file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "XPM - X PixMap ফাইল ফরম্যাট",
  "description": "XPM ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি XPM ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "XPM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-xpm-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি XPM ফাইল কি?

.xpm এক্সটেনশন সহ একটি ফাইল হল একটি ইমেজ ফাইল ফরম্যাট যা এক্স উইন্ডোজ সিস্টেম ব্যবহার করত। এটি স্বচ্ছ পিক্সেল সমর্থন করে এবং সাধারণত আইকন পিক্সম্যাপ তৈরি করে। এটি একরঙা, গ্রা-স্কেল এবং কালার পিক্সম্যাপ ডেটা সমর্থন করে। এগুলি হাতে সম্পাদনাযোগ্য করার জন্য ডিজাইন করা হয়েছে এবং [C](/programming/c/) কোডে অন্তর্ভুক্ত করা যেতে পারে৷ এই উদ্দেশ্যে, XPM ফাইলগুলি প্লেইন টেক্সট ফাইল ফরম্যাটে এবং সি প্রোগ্রামিং ল্যাঙ্গুয়েজ সিনট্যাক্স অনুসরণ করে। XPM ফাইলগুলি বিভিন্ন ইমেজ দেখার অ্যাপ্লিকেশনের সাথে খোলা যেতে পারে যেমন
CorelDRAW গ্রাফিক্স স্যুট 2020, Corel PaintShop Pro, IrfanView এবং Canvas X।

## XPM ফাইল ফরম্যাট

XPM ফাইল ফরম্যাট C সিনট্যাক্স ব্যবহার করে যাতে এগুলো C এবং C++ প্রোগ্রামে একত্রিত হয়। এটি নিম্নলিখিত ছয়টি ভিন্ন বিভাগ নিয়ে গঠিত।

 * \<Values>
 * \<Colors>
 * \<Pixels>
 * \<Extensions>

বিভাগগুলি আসলে অনুসরণ করা স্ট্রিংগুলির একটি অ্যারে।

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
নিম্নে প্রতিটি সেকশনের বিশদ বিবরণ দেওয়া হল।

`<Values> ` - এই বিভাগটি এমন একটি স্ট্রিং যাতে চার বা ছয়টি পূর্ণসংখ্যা রয়েছে যা বেস 10-এ রয়েছে এবং এর সাথে মিল রয়েছে:

 * pixmap প্রস্থ এবং উচ্চতা
 * রঙের সংখ্যা
 * পিক্সেল প্রতি অক্ষরের সংখ্যা
 * ঐচ্ছিক হটস্পট স্থানাঙ্ক এবং XPMEXT ট্যাগ

`<Colors> ` - এই বিভাগে যতগুলি স্ট্রিং আছে ততগুলি রঙ রয়েছে৷ প্রতিটি স্ট্রিং নিম্নরূপ:

```
<chars>{<key><color> }+
```
`<Pixels> ` - এই বিভাগটি গঠিত<height> স্ট্রিং এবং<width> \<chars_per_pixel> চরিত্র. প্রতি<chars_per_pixel> দৈর্ঘ্যের স্ট্রিংটি পূর্বে সংজ্ঞায়িত গ্রুপগুলির মধ্যে একটি হওয়া উচিত<Colors> অধ্যায়.

`<Extension> ` - এক্সটেনশন বিভাগটি লেবেল করা আবশ্যক, যদি এটি খালি না হয়,<Values> অধ্যায়. এটি বেশ কয়েকটি নিয়ে গঠিত হতে পারে<Extension> উপধারা যা নিম্নলিখিত দুই ধরনের হতে পারে:

 * একটি স্ট্যান্ড একা স্ট্রিং নিম্নরূপ গঠিত: XPMEXT<extension-name><extension-data>
 * বা একাধিক স্ট্রিং দ্বারা গঠিত একটি ব্লক:XPMEXT<extension-name><related extension-data composed of several strings>

## তথ্যসূত্র

* [XPM - উইকিপিডিয়া](https://en.wikipedia.org/wiki/X_PixMap)

* [XPM ম্যানুয়াল](http://www.xfree86.org/current/xpm.pdf)


