{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg ফাইল",
"cfg celestia কনফিগারেশন ফাইল",
"একটি cfg ফাইল কি?",
"কিভাবে cfg ফাইল খুলবেন",
"ফাইল",
"cfg ফাইল এক্সটেনশন",
"এক্সটেনশন"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG ফাইল ফরম্যাট - Celestia কনফিগারেশন ফাইল",
  "description": "CFG Celestia কনফিগারেশন ফাইল ফর্ম্যাট এবং APIগুলি সম্পর্কে জানুন যা CFG ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia-bn",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## একটি CFG ফাইল কি?

Celestia কনফিগারেশন ফাইল হল প্লেইন টেক্সট ফাইল যা Celestia, 3D ইউনিভার্স সিমুলেশন প্রোগ্রাম দ্বারা ব্যবহৃত হয়। Celestia কিভাবে আচরণ করে, কোন স্বর্গীয় বস্তুগুলি প্রদর্শিত হয় এবং কীভাবে প্রোগ্রাম প্রদর্শিত হয় তা কাস্টমাইজ করার জন্য এই ফাইলগুলি গুরুত্বপূর্ণ। যাইহোক, এই ফাইলগুলি সম্পাদনা করার জন্য সতর্ক মনোযোগ প্রয়োজন কারণ অনুপযুক্ত পরিবর্তন Celestia এর লোডিং প্রক্রিয়াকে ব্যাহত করতে পারে, এটি সঠিকভাবে চলতে বাধা দেয়।

## সেলেস্টিয়া

Celestia হল বিনামূল্যে, ওপেন সোর্স 3D জ্যোতির্বিদ্যা সিমুলেশন সফ্টওয়্যার যা ব্যবহারকারীদের অত্যন্ত বাস্তবসম্মত এবং ইন্টারেক্টিভ পদ্ধতিতে মহাবিশ্বকে অন্বেষণ এবং কল্পনা করতে দেয়। এটি ক্রিস লরেল দ্বারা বিকশিত হয়েছিল এবং 2000 এর দশকের শুরুতে প্রথম প্রকাশিত হয়েছিল। Celestia Windows, macOS এবং Linux অপারেটিং সিস্টেমের জন্য উপলব্ধ।

Celestia এর মূল বৈশিষ্ট্য এবং দিকগুলির মধ্যে রয়েছে:

- **বাস্তববাদী 3D ভিজ্যুয়ালাইজেশন:** Celestia আমাদের সৌরজগত, সেইসাথে নক্ষত্র, গ্যালাক্সি এবং অন্যান্য স্বর্গীয় বস্তুর বিস্তারিত এবং সঠিক উপস্থাপনা প্রদান করে। এটি দৃশ্যত নিমজ্জিত অভিজ্ঞতা তৈরি করতে উচ্চ-মানের 3D মডেল এবং টেক্সচার ব্যবহার করে।

- **বিস্তৃত মহাকাশীয় ডেটাবেস:** সফ্টওয়্যারটি নক্ষত্র, গ্রহ, চাঁদ, গ্রহাণু, ধূমকেতু এবং মহাকাশযান সহ পরিচিত মহাজাগতিক বস্তুর বিশাল বিল্ট-ইন ডাটাবেসের সাথে আসে। ব্যবহারকারীরা সহজেই এই বস্তুগুলি সনাক্ত এবং অন্বেষণ করতে পারেন।

- **বৈজ্ঞানিক নির্ভুলতা:** যদিও Celestia হল ভিজ্যুয়ালাইজেশন টুল, এটির লক্ষ্য হল উপলব্ধ বৈজ্ঞানিক তথ্যের উপর ভিত্তি করে যতটা সম্ভব নির্ভুলভাবে স্বর্গীয় বস্তু এবং ঘটনাগুলিকে উপস্থাপন করা।

## Celestia দ্বারা ব্যবহৃত ফাইল বিন্যাস

Celestia তার 3D জ্যোতির্বিদ্যা সিমুলেশনের বিভিন্ন দিকের জন্য বিভিন্ন ফাইল ফরম্যাট ব্যবহার করে। এখানে Celestia দ্বারা নিযুক্ত কিছু মূল ফাইল বিন্যাস রয়েছে:

1. **কনফিগারেশন ফাইল (.cel)**
- *বিবরণ*: প্লেইন টেক্সট ফাইল যা ব্যবহারকারীদের Celestia এর আচরণ, চেহারা এবং বিষয়বস্তু কাস্টমাইজ করার অনুমতি দেয়।
- *উদ্দেশ্য*: সেটিংস কাস্টমাইজ করা, অবস্থান সংজ্ঞায়িত করা এবং স্বর্গীয় বস্তু নির্দিষ্ট করা।

2. **3D মডেল এবং মেশ**
- *ফর্ম্যাট*: [.3ds](/3d/3ds/), [.obj](/3d/obj/), [.dae](/3d/dae/), .ac
- *বিবরণ*: সমর্থিত 3D মডেল ফাইল ফরম্যাট যা স্বর্গীয় বস্তু এবং মহাকাশযান রেন্ডার করার জন্য ব্যবহৃত হয়।
- *উদ্দেশ্য*: Celestia-এর মধ্যে 3D বস্তু প্রদর্শন করা।

3. **টেক্সচার ফাইল**
- *ফর্ম্যাট*: [.jpg](/image/jpeg/), [.png](/image/png/), [.dds](/image/dds/)
- *বিবরণ*: এই ফাইলগুলি মহাকাশীয় বস্তুগুলির জন্য পৃষ্ঠের টেক্সচার প্রদান করে।
- *উদ্দেশ্য*: বাস্তবসম্মত চেহারার জন্য 3D মডেলে টেক্সচার ম্যাপিং।

4. **স্টার ক্যাটালগ এবং ডেটা ফাইল**
- *ফর্ম্যাট*: কাস্টম ফরম্যাট, [.csv](/spreadsheet/csv/), [.tsv](/spreadsheet/tsv/)
- *বিবরণ*: নক্ষত্র এবং অন্যান্য মহাজাগতিক বস্তুর প্রতিনিধিত্ব করতে ব্যবহৃত ডেটা ফাইল, সঠিক সিমুলেশন নিশ্চিত করে।
- *উদ্দেশ্য*: স্বর্গীয় বস্তুর সঠিক উপস্থাপনা।

5. **টেক্সচার কিউব ম্যাপ**
- *বর্ণনা*: কিউব ম্যাপগুলি ছায়াপথের মতো দূরবর্তী মহাকাশীয় বস্তুর চেহারা অনুকরণ করতে ব্যবহৃত হয়।
- *উদ্দেশ্য*: বাস্তবসম্মত টেক্সচার সহ দূরবর্তী বস্তু রেন্ডার করা।

6. **স্ক্রিপ্ট ফাইল**
- *বিবরণ*: এই ফাইলগুলিতে Celestia এর স্ক্রিপ্টিং ভাষায় লেখা কাস্টম স্ক্রিপ্ট রয়েছে।
- *উদ্দেশ্য*: Celestia মহাবিশ্বের মধ্যে গতিশীল ইভেন্ট এবং অ্যানিমেশন তৈরি করতে ব্যবহারকারীদের সক্ষম করে।

## Celestia কনফিগারেশন ফাইল

Celestia কনফিগারেশন ফাইল দিয়ে আপনি কী করতে পারেন তার প্রাথমিক ওভারভিউ এখানে রয়েছে:

1. **আপনার অবস্থান নির্ধারণ করা**: আপনি অক্ষাংশ, দ্রাঘিমাংশ এবং উচ্চতার পরামিতি ব্যবহার করে পৃথিবীতে আপনার অবস্থান নির্দিষ্ট করতে পারেন। এটি Celestia আপনার অবস্থান থেকে সঠিকভাবে রাতের আকাশ প্রদর্শন করতে দেয়।

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **আপনার দেখার বিকল্পগুলি কাস্টমাইজ করা:** আপনি দেখার ক্ষেত্র, সময় সেটিংস এবং রেন্ডারিং পছন্দগুলির মতো বিভিন্ন দেখার বিকল্পগুলি সামঞ্জস্য করতে পারেন৷

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **আকাশীয় বস্তু লোড হচ্ছে:** আপনি আপনার সিমুলেশনে তারা, গ্রহ, গ্রহাণু, মহাকাশযান এবং আরও অনেক কিছুর মতো মহাকাশীয় বস্তু যোগ করতে পারেন। প্রতিটি বস্তুকে তার বৈশিষ্ট্য সহ কনফিগারেশন ফাইলে সংজ্ঞায়িত করা হয়।

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **স্পেসশিপ সংজ্ঞায়িত করা:** আপনি আপনার নিজস্ব কাল্পনিক মহাকাশযান তৈরি করতে পারেন বা অবস্থান, অভিযোজন এবং 3D মডেলের মতো পরামিতিগুলি নির্দিষ্ট করে বাস্তবগুলি ব্যবহার করতে পারেন৷

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **স্ক্রিপ্ট তৈরি করা:** আপনি গতিশীল ইভেন্ট এবং অ্যানিমেশন তৈরি করতে Celestia এর কাস্টম স্ক্রিপ্টিং ভাষায় স্ক্রিপ্ট লিখতে পারেন।

## কিভাবে CFG ফাইল খুলবেন?

প্রোগ্রামগুলি যেগুলি CFG ফাইলগুলি খোলা বা রেফারেন্স করে৷

- Celestia (ফ্রি) এর জন্য (উইন্ডোজ, ম্যাক, লিনাক্স)

## অন্যান্য CFG ফাইল

এখানে অন্যান্য ফাইলের ধরন রয়েছে যা **.cfg** ফাইল এক্সটেনশন ব্যবহার করে।

**সেটিংস**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**খেলা**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**সিস্টেম ও বিবিধ**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## তথ্যসূত্র
* [সেলেস্টিয়া](https://en.wikipedia.org/wiki/Celestia)


