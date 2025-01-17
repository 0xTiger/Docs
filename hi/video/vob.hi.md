---
date: 2019-10-11
keywords: vob, .vob, vob फ़ाइल स्वरूप, .vob फ़ाइल स्वरूप, .vob एक्सटेंशन, vob एक्सटेंशन, vob वीडियो प्रारूप, vob डीवीडी फ़ाइलें
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "VOB फ़ाइल स्वरूप और API के बारे में जानें जो VOB फ़ाइलें बना और खोल सकते हैं।"
title: वीओबी फ़ाइल स्वरूप
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## वीओबी फाइल क्या है? ##

VOB फ़ाइलें आमतौर पर VIDEO_TS निर्देशिका में एक .vob एक्सटेंशन वाली DVD पर संग्रहीत की जाती हैं। VOB फ़ाइलों में वीडियो और ऑडियो डेटा के साथ-साथ मेनू और उपशीर्षक जैसे अन्य डेटा भी होते हैं। VOB MPEG-2 प्रोग्राम स्ट्रीम फॉर्मेट पर आधारित है, लेकिन निजी स्ट्रीम में इसकी अतिरिक्त सीमाएँ और विशिष्टताएँ हैं। VOB फाइलें MPEG प्रोग्राम स्ट्रीम का एक सख्त उपसमुच्चय हैं इसलिए सभी VOB फाइलें MPEG प्रोग्राम स्ट्रीम हैं लेकिन सभी MPEG प्रोग्राम स्ट्रीम VOB अनुरूप नहीं हैं।

## डीवीडी वीडियो की संरचना ##

जब एक कंप्यूटर पर एक डीवीडी खोली जाती है, तो VIDEO_TS AUDIO_TS के साथ शीर्ष स्तर की निर्देशिका होती है। AUDIO_TS खाली है और इसका उपयोग नहीं किया गया है। VIDEO_TS निर्देशिका के अंदर, VOB, BUP और IFO फ़ाइलें हैं। वीओबी फाइलों में एमपीईजी सामग्री होती है। इन्हें 1 जीबी या उससे कम आकार के टुकड़ों में तोड़ा जाता है ताकि ये सभी ऑपरेटिंग सिस्टम के अनुकूल हों। आईएफओ फाइलों में मेनू और शीर्षक संरचना के बारे में जानकारी होती है। BUK फाइलें समान नाम वाली IFO फाइलों की बैकअप फाइलें हैं। इन फ़ाइलों को भौतिक रूप से एक अलग क्षेत्र में रखने के लिए होती है ताकि यदि DVD को भौतिक क्षति के कारण IFO फ़ाइल क्षतिग्रस्त हो जाए, तो BUK फ़ाइल समान जानकारी प्रदान कर सके।

### भौतिक लेआउट ###

- डिस्क पर सभी फाइलें सन्निहित होनी चाहिए।
- संबंधित फाइलें एक दूसरे के बगल में होनी चाहिए (वीओबी, आईएफओ, बीयूपी)।
- क्रमांकित फाइलें आरोही क्रम में होनी चाहिए।

## कॉपी सुरक्षा ##

कई वीडियो डीवीडी एन्क्रिप्टेड हैं और डीवीडी से डेटा की कॉपी करने से रोकते हैं। डीवीडी के दुर्गम लीड-इन क्षेत्र में स्थित फ़ाइलों को चलाने के लिए प्रमाणीकरण और डिक्रिप्शन कुंजियों की आवश्यकता होती है। इन कुंजियों का उपयोग CSS डिक्रिप्शन सॉफ़्टवेयर द्वारा किया जाता है जो DVD प्लेयर या सॉफ़्टवेयर प्लेयर में मौजूद होता है। चाबियों के बिना, वीडियो फ़ाइलों को नहीं चलाया जा सकता क्योंकि फ़ाइलें खोले जाने पर कुंजियों का अनुरोध किया जाएगा।

## संदर्भ ##

- [वीओबी - विकिपीडिया](https://en.wikipedia.org/wiki/VOB)
- [डीवीडी-वीडियो/निर्देशिका संरचना के अंदर](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

