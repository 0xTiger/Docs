---
date: 2019-10-11
keywords: kt, .kt, kotlin फाइल फॉर्मेट, kotlin फाइल कैसे खोलें, kotlin फाइल कैसे रन करें, .kt फाइल फॉर्मेट, kt फाइल, kotlin फाइल एक्सटेंशन, .kt एक्स्टेंशन, कोटलिन बनाम जावा
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: केटी फ़ाइल स्वरूप
linktitle: KT
description: "KT फ़ाइल स्वरूप और API के बारे में जानें जो KT फ़ाइलें बना और खोल सकते हैं।"
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## केटी फाइल क्या है? ##

कोटलिन में लिखे गए स्रोत कोड को .kt एक्सटेंशन के साथ सहेजा जाता है जिसे आमतौर पर **कोटलिन फ़ाइल एक्सटेंशन** के रूप में जाना जाता है। कोटलिन जेटब्रेन्स द्वारा [Java](/hi/programming/java/) के साथ पूरी तरह से इंटरऑपरेबल होने के लिए विकसित एक सामान्य-उद्देश्य वाली क्रॉस-प्लेटफ़ॉर्म प्रोग्रामिंग भाषा है। कोटलिन ट्रेडमार्क कोटलिन फाउंडेशन द्वारा संरक्षित है।

7 मई 2019 को Google द्वारा कोटलिन को एंड्रॉइड ऐप डेवलपमेंट के लिए पसंदीदा प्रोग्रामिंग भाषा के रूप में घोषित किया गया था। एंड्रॉइड स्टूडियो 3.0 ने अक्टूबर 2017 में एंड्रॉइड ऐप डेवलपमेंट के विकल्प के रूप में कोटलिन का समर्थन करना शुरू किया।

## कोटलिन केटी फाइल फॉर्मेट का संक्षिप्त इतिहास ##

JVM के लिए एक नई प्रोग्रामिंग भाषा के रूप में जुलाई 2011 में JetBrains द्वारा कोटलिन का अनावरण किया गया था। JetBrains के प्रमुख दिमित्री जेमेरोव ने कहा कि स्काला को छोड़कर अधिकांश भाषाओं में ऐसी विशेषताएं नहीं थीं, जिनकी वे तलाश कर रहे थे, लेकिन स्काला का धीमा संकलन एक खामी थी। कोटलिन के मुख्य लक्ष्यों में से एक जावा जितनी जल्दी संकलन करना था। फरवरी 2012 में Apache 2 लाइसेंस के तहत कोटलिन प्रोजेक्ट ओपन-सोर्स किया गया था।

कोटलिन का संस्करण 1.0 15 फरवरी 2015 को जारी किया गया था। Android ने Google I/O 2017 पर Android पर कोटलिन के लिए प्रथम श्रेणी के समर्थन की घोषणा की। कोटलिन 1.2 को 28 नवंबर 2017 को JVM और जावास्क्रिप्ट प्लेटफार्मों के बीच कोड साझा करने की क्षमता के साथ जारी किया गया था। कोटलिन 1.3 को अतुल्यकालिक प्रोग्रामिंग के समर्थन के साथ 29 अक्टूबर 2018 को जारी किया गया था। Google ने 7 मई 2019 को Android ऐप डेवलपमेंट के लिए कोटलिन को पसंदीदा प्रोग्रामिंग भाषा बनाने की घोषणा की। स्विफ्ट/ऑब्जेक्टिव-सी के साथ इंटरऑपरेबिलिटी का समर्थन करने के लिए कोटलिन 1.4 को अगस्त 2020 में कुछ मामूली बदलावों के साथ जारी किया गया था।

## कोटलिन सिंटेक्स ##

कोटलिन को जावा से बेहतर होने के लिए डिज़ाइन किया गया था, लेकिन फिर भी जावा कोड के साथ इंटरऑपरेबल होना चाहिए ताकि जावा से कोटलिन में धीरे-धीरे माइग्रेशन हो सके।

* कोटलिन में अर्धविराम वैकल्पिक हैं। बयान के अंत को इंगित करने के लिए एक नई पंक्ति पर्याप्त है।
* कोटलिन दो प्रकार के वेरिएबल्स का समर्थन करता है, केवल पढ़ने के लिए, *val* कीवर्ड द्वारा परिभाषित, और परिवर्तनशील, *var* कीवर्ड द्वारा परिभाषित।
* कक्षाएं डिफ़ॉल्ट रूप से निजी और अंतिम होती हैं। एक वर्ग से प्राप्त करने के लिए, आधार वर्ग को *खुले* कीवर्ड के साथ घोषित किया जाना चाहिए।
* कोटलिन प्रक्रियात्मक प्रोग्रामिंग का भी समर्थन करता है।
* कोटलिन कार्यक्रम का प्रवेश बिंदु जावा, सी #, आदि के समान "मुख्य" कार्य है।

### सिंटेक्स उदाहरण ###

निम्नलिखित कोटलिन सिंटैक्स का एक उदाहरण है।

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

उपरोक्त कोड में, **fun** कीवर्ड मुख्य नाम के फ़ंक्शन को परिभाषित करता है। फ़ंक्शन के अंदर, **val** कीवर्ड के साथ केवल-पढ़ने योग्य चर 'ऑडियंस' घोषित किया गया है। ** Println ** विधि का उपयोग करके, "हैलो वर्ल्ड फ्रॉम कोटलिन" कंसोल पर प्रिंट किया जाता है। चर ऑडियंस के मान को **$** चिह्न के साथ स्ट्रिंग में इंजेक्ट किया जाता है।

## कोटलिन बनाम जावा
कई उन्नत सुविधाओं की पेशकश के साथ एंड्रॉइड ऐप लिखने के लिए कोटलिन एक आधिकारिक भाषा है, लेकिन कई विशेषज्ञ जावा डेवलपर्स अभी भी कोटलिन पर स्विच करने में अपनी रुचि नहीं दिखाते हैं। उन्हें लगता है कि वे जावा के साथ ही सब कुछ कर सकते हैं। तो निम्नलिखित दो तकनीकों के बीच तुलना है जो जावा डेवलपर्स को स्विच करने के लिए राजी कर सकती है:

| पैरामीटर | जावा | कोटलिन |
|--------------------|-----------|---------------- -|
| सिंगलटन्स ऑब्जेक्ट्स | √ | √ |
| वाइल्डकार्ड प्रकार | √ | Χ |
| संकलन | बाइटकोड्स | वर्चुअल मशीन |
| लैम्ब्डा एक्सप्रेशन | Χ | √ |
| अपरिवर्तनीय ऐरे | Χ | √ |
| गैर-निजी क्षेत्र | √ | Χ |
| स्मार्ट कास्ट | Χ | √ |
| अशक्त सुरक्षा | Χ | √ |
| स्थैतिक सदस्य | √ | Χ |

## संदर्भ ##

- [कोटलिन (प्रोग्रामिंग भाषा) - विकिपीडिया](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

