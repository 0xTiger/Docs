{
  "date": "2021-03-18",
  "keywords": [
    "qgz file",
    "qgz file format",
    "what is an qgz file",
    "file",
    "qgz example",
    "qgz file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "title": "QGZ - কোয়ান্টাম জিআইএস সংকুচিত প্রকল্প",
  "description": "QGZ ফাইল ফরম্যাট সম্পর্কে জানুন যা শুধুমাত্র একটি সংকুচিত QGS এবং API যা QGZ ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "QGZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qgz-bn"
    }
  },
  "lastmod": "2021-03-18"
}

## একটি QGZ ফাইল কি?

**QGZ** ফাইল ফরম্যাট হল একটি সংকুচিত আর্কাইভ যাতে একটি [QGS](/gis/qgs/) ফাইল এবং একটি QGD ফাইল থাকে। যেখানে, QGD ফাইল হল qgis প্রকল্পের sqlite ডাটাবেস যা প্রকল্পের জন্য সহায়ক ডেটা নিয়ে গঠিত। যদি কোন সহায়ক তথ্য না থাকে, তাহলে QGD ফাইলটি খালি থাকবে।

## QGZ ফাইল ফরম্যাট সম্পর্কে বিশদ বিবরণ

QGZ **QGIS 3 প্রজেক্ট ফাইল ফরম্যাট** এর একটি নতুন বৈকল্পিক হিসাবে চালু করা হয়েছিল। এই বিন্যাসটি QGS xml ফাইলের জন্য একটি জিপ করা ধারক। ব্যবহারকারীরা যদি QGD বেছে নেয় যা একটি ঐচ্ছিক বিন্যাস, এই ক্ষেত্রে কন্টেইনারটি সহায়ক স্টোরেজ ডাটাবেস সংরক্ষণের জন্য উপকারী।

ক্লাসিক মোডে, সহায়ক ডাটাবেসটি xml ফাইলের সাথে .qgd এক্সটেনশন সহ একটি ফাইল হিসাবে সংরক্ষণ করা হয়। জিপ করা কন্টেইনার বাছাই করার সময়, .qgd ফাইলটি .qgz-এ অন্তর্ভুক্ত করে, এটি ব্যবহারকারীদের কোনো সমস্যা ছাড়াই সুবিধা দেয়, ব্যবহারকারীরা প্রকল্প ফাইলগুলি ভাগ করার সময় এটি মুছে ফেলতে বা অনুলিপি করতে ভুলবেন না!


## তথ্যসূত্র

* [QGZ – QGIS-এর জন্য একটি নতুন ডিফল্ট প্রকল্প ফাইল বিন্যাস](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)

* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)
