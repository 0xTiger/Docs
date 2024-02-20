{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "পিইটি ফাইল ফরম্যাট - পপি লিনাক্স ইনস্টল প্যাকেজ ফাইল",
  "description":"PET ফাইল বিন্যাস এবং API সম্পর্কে জানুন যেগুলি PET ফাইলগুলি তৈরি এবং খুলতে পারে।",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet-bn",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## একটি লিনাক্স পিইটি ফাইল কি?

একটি PET ফাইল হল একটি অ্যাপ্লিকেশন ইনস্টলেশন প্যাকেজ ফাইল যা লিনাক্স অপারেটিং সিস্টেমের PuppyLinux ভেরিয়েন্টের সাথে তৈরি এবং ব্যবহৃত হয়। এটি একটি সংকুচিত [TGZ](/compression/tgz/) ফাইল হিসাবে তৈরি করা হয়েছে যা সংকুচিত সংরক্ষণাগারের ফাইলের আকার হ্রাস করে। PET ফাইল বিন্যাসের অখণ্ডতা md5sum চেকসাম দ্বারা নিশ্চিত করা হয় যা দূরবর্তী প্রান্তে যাচাইয়ের জন্য ফাইলের শেষে সংযুক্ত করা হয়। PET ফাইলগুলি স্ট্যান্ডার্ড TGZ ফাইল এক্সট্র্যাক্টর এবং WinRAR ব্যবহার করে বের করা যেতে পারে। PET ফাইলগুলি পুরানো [PUP](/compression/pup/) প্যাকেজ ইনস্টলেশন ফাইলগুলিকে প্রতিস্থাপন করেছে৷

## পিইটি ফাইল ফরম্যাট

পিইটি ফাইলগুলি বাইনারি ফাইল বিন্যাসে সংকুচিত সংরক্ষণাগার হিসাবে ডিস্কে সংরক্ষণ করা হয়। যাইহোক, পিইটি ফাইল ফরম্যাটের অভ্যন্তরীণ ফাইল বিন্যাসের বিবরণ জানা যায়নি। [.exe](/executable/exe/) এবং [.msi](/executable/msi/) প্যাকেজ ইনস্টলেশন ফাইলের মতো, PET ফাইলগুলি কার্যকর করা হলে একটি ইনস্টলেশন শুরু করে।

## তথ্যসূত্র

 * [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
 * [পাপিলিনাক্স পিইটি প্যাকেজগুলির সূচক](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)
