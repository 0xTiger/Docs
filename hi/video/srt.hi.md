---
date: 2019-10-11
keywords: srt, .srt, srt फ़ाइल स्वरूप, .srt फ़ाइल स्वरूप, .srt एक्सटेंशन, srt एक्सटेंशन
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "SRT फ़ाइल स्वरूप और API के बारे में जानें जो SRT फ़ाइलें बना और खोल सकते हैं।"
title: एसआरटी फ़ाइल स्वरूप
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## एसआरटी फाइल क्या है? ##

SRT (सबरिप फाइल फॉर्मेट) एक साधारण सबटाइटल फाइल है जिसे .srt एक्सटेंशन के साथ सबरिप फाइल फॉर्मेट में सेव किया जाता है। इसमें उपशीर्षक की क्रमिक संख्या, प्रारंभ और समाप्ति टाइमस्टैम्प और उपशीर्षक पाठ शामिल हैं। एसआरटी फाइलें वीडियो सामग्री के उत्पादन के बाद उपशीर्षक जोड़ना संभव बनाती हैं।

## एसआरटी फ़ाइल संरचना ##

SRT फ़ाइल में प्रत्येक उपशीर्षक के चार भाग होते हैं।

1. उपशीर्षक की संख्या या स्थिति को इंगित करने वाला एक संख्यात्मक काउंटर।
1. उपशीर्षक का प्रारंभ और समाप्ति समय --> वर्णों द्वारा अलग किया गया
1. एक या अधिक पंक्तियों में उपशीर्षक पाठ।
1. उपशीर्षक के अंत को इंगित करने वाली एक रिक्त रेखा।

### एसआरटी का उदाहरण ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

समय निर्दिष्ट करने के लिए * घंटे: मिनट: सेकंड, मिलीसेकंड (00: 00: 00,000) * प्रारूप का उपयोग किया जाता है।

## एसआरटी फाइलों का प्रारूपण ##

SRT फ़ाइलों का स्वरूपण HTML टैग्स से लिया गया है। SRT फ़ाइल के लिए फ़ॉर्मेटिंग टैग नीचे सूचीबद्ध हैं।

| प्रभाव | टैग |
| --- | --- |
|बोल्ड|**\ <b>...\</b> ** या {b}...{/b}|
|इटैलिक|**\ <i>...\</i> ** या **{i}...{/i}**|
|अंडरलाइन|**\ <u>...\</u> ** या **{u}...{/u}**|
|फ़ॉन्ट रंग|**\ <font color="white">...\</font> **|
|लाइन स्थिति|**{\a3}** (इंगित करता है कि टेक्स्ट लाइन 3 पर दिखना शुरू हो जाना चाहिए)

## सबरिप सॉफ्टवेयर ##

सबरिप एक मुफ्त सॉफ्टवेयर प्रोग्राम है जो विंडोज़ पर चलता है। यह उपशीर्षक और उनके समय को विभिन्न वीडियो प्रारूपों से निकालता है और उपशीर्षक को SRT प्रारूप में सहेजता है। सबरिप लाइव वीडियो, अन्य वीडियो फ़ाइलों और डीवीडी से उपशीर्षक निकालने के लिए ऑप्टिकल कैरेक्टर रिकग्निशन का उपयोग करता है।

## संदर्भ ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
