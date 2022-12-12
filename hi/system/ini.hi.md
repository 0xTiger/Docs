{
  "date" : "2021-07-07",
  "keywords" :["आईएनआई", "विस्तार", "फ़ाइल", "प्रारूप", "प्रणाली", "आरंभ", "निर्देशिका विस्तार", "कार्यक्रम", "कंप्यूटर", "अनुप्रयोग"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"आईएनआई - दीक्षा फ़ाइल स्वरूप",
  "description":"INI फ़ाइल स्वरूप और API के बारे में जानें जो INI फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## आईएनआई फाइल क्या है? ##

एक INI फ़ाइल कंप्यूटर प्रोग्राम के लिए एक संदेश कॉन्फ़िगरेशन दस्तावेज़ है जिसमें विशेषताओं और अनुभागों के लिए सार्वजनिक कुंजियाँ होती हैं जो एक रूपरेखा और व्याकरण में विशेषताओं को व्यवस्थित करती हैं। ये सिस्टम फ़ाइल स्वरूप कॉन्फ़िगरेशन दस्तावेज़ MS-DOS ऑपरेटिंग सिस्टम के डायरेक्टरी एक्सटेंशन INI से अपना नाम प्राप्त करते हैं, जो दीक्षा के लिए है। इसने सॉफ्टवेयर सेटअप के इस रूप को लोकप्रिय बनाया। अन्य सॉफ़्टवेयर अनुप्रयोगों पर कई प्रोग्राम विभिन्न फ़ाइल नाम परिवर्धन का उपयोग करते हैं, जैसे CONF और [CFG](/hi/system/cfg), हालांकि प्रारूप ने कॉन्फ़िगरेशन की कई स्थितियों में एक अनौपचारिक मानक स्थापित किया है।

## आईएनआई फाइलों का संक्षिप्त इतिहास##

प्रारंभ में, विंडोज की प्रमुख प्रोग्राम कॉन्फ़िगरेशन तकनीक एक टेक्स्ट फ़ाइल प्रारूप थी जिसमें पाठ की पंक्तियाँ होती थीं, जिसमें प्रति पंक्ति एक महत्वपूर्ण जोड़ी होती थी, जो खंडों में विभाजित होती थी। डिवाइस ड्राइवर, टाइपफेस और शुरुआती लॉन्चर सभी इस प्रारूप में संग्रहीत किए गए थे। व्यक्तिगत सेटिंग्स भी आमतौर पर ऐप्स द्वारा आईएनआई फाइलों में संग्रहीत की जाती थीं।
विंडोज 3.1x तक, प्रारूप 16-बिट माइक्रोसॉफ्ट विंडोज प्लेटफॉर्म पर समर्थित था। विंडोज 95 के साथ शुरुआत करते हुए, माइक्रोसॉफ्ट ने डेवलपर्स को कॉन्फिगरेशन के लिए आईएनआई फाइलों के बजाय विंडोज रजिस्ट्री का उपयोग करने के लिए प्रोत्साहित करना शुरू किया।

## आईएनआई फ़ाइल - फ़ाइल प्रारूप निर्दिष्टीकरण

### कुंजी/गुण ###

कुंजी/संपत्ति आईएनआई फ़ाइल का सबसे बुनियादी तत्व है। एक बराबर प्रतीक (=) प्रत्येक कुंजी के नाम और मान को अलग करता है। बराबर चिह्न के बाईं ओर जहां नाम प्रदर्शित होता है। विंडोज सिस्टम में समान प्रतीक और अर्धविराम विचारशील अक्षर हैं इसलिए कुंजी में उपयोग नहीं किया जा सकता है। मूल्य में किसी भी वर्ण का उपयोग किया जा सकता है।

```
name=value
```

### खंड ###

अनुभाग टिप्पणी वर्ग कोष्ठक ([]) में अपनी लाइन पर दिखाई देती है। सेक्शन की परिभाषा के बाद, सभी कुंजियाँ उस सेक्शन से जुड़ी होती हैं। अनुभाग अगले अनुभाग पदनाम या दस्तावेज़ के अंत में समाप्त होते हैं; कोई विशिष्ट "अनुभाग का अंत" विभाजक नहीं है। अनुभागों को ढेर नहीं किया जा सकता है; उन्हें केवल एक बार नाम दिया जा सकता है और उन्हें लिंक करने की आवश्यकता नहीं है।

```
[section]
a=a
b=b
```

### बदलती विशेषताएं ###

INI फ़ाइल स्वरूप में विश्व स्तर पर स्वीकृत परिभाषा नहीं है। कई कंप्यूटर अनुप्रयोगों में पहले से उल्लिखित कार्यों के अतिरिक्त कार्य शामिल हैं। नीचे दी गई सूची में कुछ सामान्य विशेषताएं शामिल हैं जो किसी व्यक्तिगत कार्यक्रम में शामिल हो भी सकती हैं और नहीं भी।

* टिप्पणियाँ
* पलायन वर्ण
* डुप्लीकेट नाम


## आईएनआई उदाहरण ##

नमूना आईएनआई फ़ाइल निम्नानुसार दिखती है:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## संदर्भ ##

* [डीएमपी - माइक्रोसॉफ्ट](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)
