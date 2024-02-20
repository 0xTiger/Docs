{
  "date": "2021-04-19",
  "keywords": [
    "Blitz3D",
    "b3d",
    "file",
    "extension",
    "format",
    "blitz3d games"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "B3D ফাইল ফরম্যাট সম্পর্কে জানুন; Blitz3d গেম এবং API-এ ব্যবহৃত হয় যা B3D ফাইল খুলতে এবং তৈরি করতে পারে।",
  "title": "B3D - Blitz3D সত্তা মডেল ফাইল",
  "linktitle": "B3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-b3d-bn"
    }
  },
  "lastmod": "2021-04-19"
}

## একটি B3D ফাইল কি?

.b3d এক্সটেনশন সহ একটি ফাইল হল Blitz3D দ্বারা ব্যবহৃত একটি মডেল ফাইল যাতে অক্ষর, ভবন, ভূখণ্ড এবং অন্যান্য বস্তুর জন্য ভিডিও গেমের মডেল থাকতে পারে। Blitz3D হল একটি প্রোগ্রামিং ভাষা যা **blitz3d গেম** তৈরি করতে ব্যবহৃত হয়। Blitz3D হল একটি শক্তিশালী, নমনীয় এবং সহজে ব্যবহারযোগ্য প্রোগ্রামিং ভাষা যা ভিডিও গেম লেখার একমাত্র উদ্দেশ্যে ডিজাইন করা হয়েছে। বিকাশকারীরা শুধুমাত্র Blitz3D ব্যবহার করে অ্যাকশন প্যাকড 3D গেম, 2D পাজলার, অ্যাডভেঞ্চার, RPGS, যা কিছু তৈরি করতে পারে।

Blitz3D বেসিক প্রোগ্রামিং ভাষার উপর ভিত্তি করে; যা শিখতে এবং ব্যবহার করাও সহজ। এই সমস্ত তথ্য নতুনদের এবং আরও অভিজ্ঞ প্রোগ্রামারদের জন্য একইভাবে ব্লিটজকে আদর্শ করে তুলছে। যদিও বেশিরভাগ আধুনিক 3D ইঞ্জিনের তুলনায় এটির বৈশিষ্ট্যগুলিকে কিছুটা পুরানো বলে মনে করা হয়, তবে Blitz3D বিশ্বব্যাপী অনেক গেম প্রোগ্রামার দ্বারা ব্যবহার করা অব্যাহত রয়েছে।

## Blitz3D এর সংক্ষিপ্ত ইতিহাস

Blitz3D মূলত অন্যান্য অনুরূপ গেম-ডেভেলপমেন্ট ভাষার সাথে প্রতিদ্বন্দ্বিতা করার জন্য সেপ্টেম্বর 2001 সালে মাইক্রোসফ্ট উইন্ডোজ অপারেটিং সিস্টেমের জন্য প্রকাশ করা হয়েছিল। Blitz3D পূর্ববর্তী 2D ইঞ্জিন BlitzBasic-এর উপরে একটি আপগ্রেড সংস্করণ ছিল, যা একটি DirectX 7-ভিত্তিক 3D ইঞ্জিনের জন্য একটি API যুক্ত করার সাথে তার কমান্ড-সেটকে প্রসারিত করেছিল। Blitz3D ব্যবহারকারীদেরও BlitzMax তুলনা করা উচিত, যেটি BlitzBasic এর পরবর্তী ইঞ্জিন। BlitzMax হল Blitz3D-এর একটি জটিল কিন্তু আরও শক্তিশালী সংস্করণ, যা অবজেক্ট-ওরিয়েন্টেড প্রোগ্রামিং ভাষা সমর্থন করে। এটি একটি আপডেটেড গ্রাফিক্স এপিআই যা ইউনিকোড অক্ষর, ওপেনজিএল, এবং শুধুমাত্র উইন্ডোজের পরিবর্তে ওএসএক্স এবং লিনাক্সে রপ্তানি করে।

## B3D উদাহরণ
একটি b3d ফাইল যাতে 1 TEXS খণ্ড, 1 BRUS খণ্ড এবং 1 NODE খণ্ড রয়েছে, দেখতে এইরকম হবে:

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
একটি সাধারণ, নন-অ্যানিমেশন এবং নন-টেক্সচারযুক্ত জাল এইরকম দেখাবে:

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## তথ্যসূত্র
 * [B3D](https://moddb.fandom.com/wiki/B3D)
 * [ব্লিটজ বেসিক](https://en.wikipedia.org/wiki/Blitz_BASIC)
