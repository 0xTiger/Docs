{
  "date": "2022-05-09",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "PYC ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি PYC ফাইল তৈরি এবং খুলতে পারে।",
  "title": "PYC ফাইল ফরম্যাট- পাইথন কম্পাইল করা ফাইল",
  "linktitle": "PYC",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-pyc-bn"
    }
  },
  "lastmod": "2022-05-09"
}

## একটি PYC ফাইল কি?

একটি PYC ফাইল হল পাইথন প্রোগ্রামিং ভাষায় লেখা সোর্স কোড থেকে তৈরি করা একটি সংকলিত আউটপুট ফাইল। যখন PY ফাইলটি পাইথন ইন্টারপ্রেটার ব্যবহার করে চালানো হয়, তখন এটি সম্পাদনের জন্য বাইটকোডে রূপান্তরিত হয়। একই সময়ে, কম্পাইল করা বাইটকোডও .pyc ফাইল হিসাবে সংরক্ষণ করা হয় যাতে প্রযোজ্য হলে পরবর্তী সময়ে ক্যাশে থেকে পুনরায় ব্যবহার করা যায়।

## পিওয়াইসি ফাইল ফরম্যাটের কাঠামো

পিওয়াইসি ফাইলগুলি বাইটকোডে রয়েছে এবং তাদের ফাইল ফর্ম্যাট স্পেসিফিকেশন সর্বজনীনভাবে উপলব্ধ নয়৷ যাইহোক, কিছু উত্স দ্বারা তদন্ত দেখায় যে [structure of a PYC file](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) এর মধ্যে রয়েছে:

 * `একটি চার-বাইটের ম্যাজিক নম্বর` - শুধু দুটি বাইট যা মার্শালিং কোডে প্রতিটি পরিবর্তনের সাথে পরিবর্তিত হয় এবং তারপরে 0d0a এর দুটি বাইট।
 * `একটি চার-বাইট পরিবর্তন টাইমস্ট্যাম্প` - উৎস ফাইলের ইউনিক্স পরিবর্তন টাইমস্ট্যাম্প যা .pyc তৈরি করেছে, যাতে উৎস পরিবর্তন হলে এটি পুনরায় সংকলিত করা যায়।
 * `একটি মার্শালড কোড অবজেক্ট` - কোড অবজেক্টের marshal.dump এর আউটপুট যা উৎস ফাইল কম্পাইল করার ফলে।

## FAQs

1. **কীভাবে একটি পিওয়াইসি ফাইল তৈরি হয়?** পাইথন ইন্টারপ্রেটার ব্যবহার করে পাইথন সোর্স কোড কম্পাইল করা হলে একটি পিওয়াইসি ফাইল তৈরি হয়। সংকলিত কোডটি তখন PYC ফাইলে সংরক্ষণ করা হয়।

1. **PYC কি py এর চেয়ে দ্রুত?** PYC ফাইলগুলি পাইথন সোর্স কোড কম্পাইল করার পরে সংরক্ষণ করা হয়। যেহেতু এইগুলি ইতিমধ্যেই ব্যাখ্যা করা হয়েছে, এই ফাইলগুলি .py ফাইলগুলির চেয়ে দ্রুততর৷

1. **py এবং pyc ফাইলের মধ্যে পার্থক্য কী?** PY ফাইলগুলিতে একটি প্রোগ্রামের জন্য পাইথন সোর্স কোড ফাইল থাকে, যখন .pyc ফাইলগুলিতে একটি অ্যাপ্লিকেশনের ব্যাখ্যা করা বাইটকোড থাকে।

1. **PYC কি একটি বাইনারি ফাইল?** হ্যাঁ, PYC ফাইল হল একটি বাইনারি ফাইল যাতে একটি 4-বাইট ম্যাজিক নম্বর, একটি 4-বাইট পরিবর্তন টাইমস্ট্যাম্প এবং একটি মার্শাল্ড কোড অবজেক্ট থাকে।

1. **আমরা কি .pyc কে .py তে রূপান্তর করতে পারি?** হ্যাঁ, pyc ফাইলগুলিকে py তে রূপান্তর করা সম্ভব। ডিকম্পাইলার যেমন Decompyle++ কম্পাইল করা পাইথন বাইট-কোডকে আবার বৈধ এবং মানব-পাঠযোগ্য পাইথন সোর্স কোডে অনুবাদ করতে ব্যবহার করা যেতে পারে।

## তথ্যসূত্র

* [.pyc ফাইলের গঠন](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)


