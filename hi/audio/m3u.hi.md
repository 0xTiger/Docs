---
date: 2019-12-13
keywords: m3u, m3u फ़ाइल स्वरूप, .m3u एक्सटेंशन, m3u मल्टीमीडिया प्लेलिस्ट, m3u प्लेलिस्ट प्रारूप
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "M3U फ़ाइल स्वरूप और API के बारे में जानें जो M3U फ़ाइलें बना और खोल सकते हैं।"
title: M3U फ़ाइल स्वरूप
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## M3U फ़ाइल क्या है? ##

M3U (MP3 URL) .m3u एक्सटेंशन के साथ संग्रहीत एक ऑडियो प्लेलिस्ट फ़ाइल है। M3U एक वास्तविक ऑडियो फ़ाइल नहीं है, यह केवल ऑडियो और कभी-कभी वीडियो फ़ाइलों की ओर इशारा करता है। M3U को Fraunhofer द्वारा Winplay3 सॉफ़्टवेयर के साथ उपयोग करने के लिए विकसित किया गया था। यह विभिन्न मीडिया प्लेयर और सॉफ्टवेयर द्वारा भी समर्थित है।

## M3U फ़ाइल स्वरूप

M3U फ़ाइल स्वरूप के लिए कोई आधिकारिक विनिर्देश नहीं है, यह एक वास्तविक मानक है। M3U एक सादा पाठ फ़ाइल है जो .m3u एक्सटेंशन का उपयोग करती है यदि टेक्स्ट स्थानीय सिस्टम के डिफ़ॉल्ट गैर-यूनिकोड एन्कोडिंग में एन्कोड किया गया है या यदि टेक्स्ट UTF-8 एन्कोडेड है तो .m3u8 एक्सटेंशन के साथ। M3U फ़ाइल में प्रत्येक प्रविष्टि निम्न में से एक हो सकती है:

- फ़ाइल के लिए पूर्ण पथ
- M3U फ़ाइल के सापेक्ष फ़ाइल पथ।
- यूआरएल

### विस्तारित M3U ###

विस्तारित M3U में, अतिरिक्त निर्देश पेश किए जाते हैं जो "#" से शुरू होते हैं और एक कोलन (:) के साथ समाप्त होते हैं यदि उनके पास पैरामीटर हैं। विस्तारित M3U के लिए निर्देशों की सूची नीचे दी गई है।

- **#EXTM3U** - यह विस्तारित M3U को इंगित करने वाला फ़ाइल हेडर है और फ़ाइल की पहली पंक्ति होनी चाहिए।
- **#EXTENC:** - टेक्स्ट एन्कोडिंग। यह फ़ाइल की दूसरी पंक्ति होनी चाहिए।
- **#EXTINF:** - ट्रैक की जानकारी और अन्य अतिरिक्त संपत्तियों के लिए उपयोग किया जाता है।
- **#प्लेलिस्ट:** - प्लेलिस्ट का शीर्षक
- **#EXTGRP:** - नाम समूहीकरण शुरू करें
- **#EXTALB:** - एल्बम की जानकारी
- **#EXTART:** - एल्बम कलाकार
- **#EXTGENRE** - एल्बम शैली
- **#EXTM3A** - एल्बम ट्रैक या अध्यायों के लिए एकल फ़ाइल प्लेलिस्ट।
- **#EXTBYT:** - फ़ाइल का आकार बाइट्स में।
- **#EXTBIN:** - बाइनरी डेटा इस प्रकार है।
- **#EXTIMG:** - लोगो, कवर या अन्य चित्र।

### एचएलएस एम3यू ###

HLS (HTTP लाइव स्ट्रीमिंग) Apple द्वारा iOS उपकरणों में ऑडियो और रेडियो स्ट्रीम करने के लिए बनाया गया था। यह UTF-8 एन्कोडेड विस्तारित M3U पर आधारित है। इसे IETF द्वारा 2017 में RFC 8216 के रूप में मानकीकृत किया गया था। HLS प्लेलिस्ट के टैग "#EXT-X-" से शुरू होते हैं। एचएलएस के लिए टैग की सूची नीचे दी गई है

- **EXT-X-VERSION** - मीडिया और उसके सर्वर के आधार पर फ़ाइल के संगतता संस्करण को दर्शाता है।
- **#EXT-X-START:** - प्लेलिस्ट के लिए पसंदीदा शुरुआती बिंदु को दर्शाता है।
- **#EXT-X-PLAYLIST-TYPE:** - प्लेलिस्ट का प्रकार (ईवेंट या वीओडी) प्रदान करता है।
- **#EXT-X-TARGETDURATION:** - यह अधिकतम सेगमेंट अवधि निर्दिष्ट करता है।
- **#EXT-X-मीडिया-अनुक्रम:** - यह मीडिया अनुक्रम संख्या को इंगित करता है।
- **#EXT-X-INDEPENDENT-SEGMENTS** - यह इंगित करता है कि सभी मीडिया नमूने स्वतंत्र हैं और अन्य खंडों के बिना डिकोड किए जा सकते हैं।
- **#EXT-X-मीडिया:** - इसका उपयोग उन मीडिया प्लेलिस्ट को जोड़ने के लिए किया जाता है जिनमें समान सामग्री के वैकल्पिक प्रस्तुतीकरण होते हैं।
- **#EXT-X-STREAM-INF:** - यह एक वैरिएंट स्ट्रीम निर्दिष्ट करता है जो रेंडिशन का एक हिस्सा है।
- **#EXT-X-BYTERANGE:** - इंगित करता है कि मीडिया खंड अपने URI द्वारा पहचाने गए संसाधन की एक उप-श्रेणी है।
- **#EXT-X-DISCONTINUITY** - पूर्ववर्ती और निम्नलिखित मीडिया सेगमेंट के बीच असंतुलन को दर्शाता है।
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - यह एक ही वेरियंट स्ट्रीम या अलग-अलग वेरियंट स्ट्रीम के विभिन्न रेंडिशन के बीच सिंक्रोनाइज़ेशन की अनुमति देता है।
- **#EXT-X-KEY:** - निर्दिष्ट करता है कि मीडिया सेगमेंट को कैसे डिक्रिप्ट किया जाए।
- **#EXT-X-MAP:** - निर्दिष्ट करता है कि मीडिया आरंभीकरण अनुभाग कैसे प्राप्त करें। लागू मीडिया सेगमेंट को पार्स करना आवश्यक है।
- **#EXT-X-कार्यक्रम-तिथि-समय:** - यह मीडिया सेगमेंट के पहले नमूने को एक पूर्ण तिथि और/या समय के साथ जोड़ता है।
- **#EXT-X-DATERANGE:** - यह डेटा रेंज को जोड़ता है।
- **#EXT-XI-FRAMES-only** - इंगित करता है कि प्लेलिस्ट में प्रत्येक मीडिया सेगमेंट एक एकल I-फ्रेम का वर्णन करता है।
- **EXT-XI-FRAME-STREAM-INF** - यह इंगित करता है कि प्लेलिस्ट फ़ाइल में मल्टीमीडिया प्रस्तुति के I-फ्रेम हैं।
- **#EXT-X-SESSION-DATA:** - यह मनमाने सत्र डेटा को होने देता है
एक मास्टर प्लेलिस्ट में किया गया।
- **#EXT-X-SESSION-KEY:** - यह एन्क्रिप्शन कुंजियों की अनुमति देता है। क्लाइंट पहले प्लेलिस्ट को पढ़े बिना इन चाबियों को प्रीलोड कर सकता है।
- **#EXT-X-ENDLIST** - यह इंगित करता है कि फ़ाइल में कोई और मीडिया सेगमेंट नहीं जोड़ा जाएगा।

M3U द्वारा उपयोग किए जाने वाले इंटरनेट मीडिया प्रकारों की सूची निम्नलिखित है:

- **application/vnd.apple.mpegurl**: यह M3U के लिए एकमात्र पंजीकृत मीडिया प्रकार (2009 में पंजीकृत) है जिसका उपयोग HLS अनुप्रयोगों में प्लेलिस्ट को संदर्भित करने के लिए किया जाता है।
- निम्नलिखित इंटरनेट मीडिया प्रकार गैर-एचएलएस अनुप्रयोगों द्वारा उपयोग किए जाते हैं।
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## M3U उदाहरण ##

यह M3U फ़ाइल का एक उदाहरण है।

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## संदर्भ ##

- [एम3यू - विकिपीडिया](https://en.wikipedia.org/wiki/M3U)
- [HTTP लाइव स्ट्रीमिंग](https://tools.ietf.org/html/rfc8216)

