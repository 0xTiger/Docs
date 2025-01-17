{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSU ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি OSU ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "OSU ফাইল - ওসু! স্ক্রিপ্ট ফাইল ফরম্যাট",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-bn",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## একটি OSU ফাইল কি?

একটি OSU ফাইল হল একটি গেম স্ক্রিপ্ট যা ওসুর জন্য লেখা! ছন্দ খেলা। এটিতে গেমটিতে ব্যবহৃত একটি বিটম্যাপ সম্পর্কে তথ্য রয়েছে যেমন অসুবিধার স্তর, গানটি চালানো হবে এবং হিট অবজেক্টের সময় যা প্লেয়ারকে সঙ্গীতের সাথে সিঙ্ক করতে হবে। এটি রিদম গেম প্লেয়ারদের কাস্টম চ্যালেঞ্জ ডেভেলপ করতে এবং গেম কমিউনিটির সাথে শেয়ার করতে দেয়।

**ওএসআর ফাইল ফরম্যাটের MIME প্রকার:** x-osu-বিটম্যাপ

## OSU ফাইল ফরম্যাট

OSU ফাইলগুলিকে ডিস্কে প্লেইন টেক্সট ফাইল হিসাবে সংরক্ষিত করা হয় এবং এর গঠনটি osu! দ্বারা [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)-এ খুব স্পষ্টভাবে সংজ্ঞায়িত করা হয়েছে।

### OSU ফাইলের বিভাগগুলি

একটি সাধারণ OSU ফাইলে নিম্নলিখিত বিভাগগুলি রয়েছে।

|বিভাগ |বিবরণ |সামগ্রীর প্রকার |
---|---|---|
|[সাধারণ]| বিটম্যাপ সম্পর্কে সাধারণ তথ্য| কী: মান জোড়া|
|[সম্পাদক]| বীটম্যাপ সম্পাদকের জন্য সংরক্ষিত সেটিংস| কী: মান জোড়া|
|[মেটাডেটা] |বিটম্যাপ সনাক্ত করতে ব্যবহৃত তথ্য| কী: মান জোড়া|
|[কঠিনতা] |কঠিন সেটিংস| কী: মান জোড়া|
|[ইভেন্টস]| বিটম্যাপ এবং স্টোরিবোর্ড গ্রাফিক ইভেন্ট| কমা দ্বারা পৃথক করা তালিকা|
|[টাইমিংপয়েন্টস]| সময় এবং নিয়ন্ত্রণ পয়েন্ট| কমা দ্বারা পৃথক করা তালিকা|
|[রঙ]| কম্বো এবং ত্বকের রং| কী: মান জোড়া|
|[হিটঅবজেক্টস]| বস্তুকে আঘাত করুন| কমা দ্বারা পৃথক করা তালিকা|

## তথ্যসূত্র

* [ওএসইউ! রিদম গেম](https://osu.ppy.sh/home)

* [OSU ফাইল ফরম্যাট](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


