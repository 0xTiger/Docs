{
  "date" : "2021-02-25",
  "keywords" :[ "बीडीएफ फाइल", "बीडीएफ फाइल फॉर्मेट", "बीडीएफ फाइल क्या है", "फाइल", "बीडीएफ उदाहरण", "बीडीएफ फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"बीडीएफ - ग्लिफ़ बिटमैप वितरण प्रारूप",
  "description":"बीडीएफ फ़ाइल प्रारूप और एपीआई के बारे में जानें जो बीडीएफ फाइलें बना और खोल सकते हैं।",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## बीडीएफ फाइल क्या है?
बीडीएफ फाइलें मानव पठनीय रूप हैं और आमतौर पर एएससीआईआई एन्कोडिंग में वितरित की जाती हैं। फ़ाइल संपूर्ण फ़ॉन्ट के लिए प्रासंगिक वैश्विक जानकारी के साथ शुरू होती है, इसके बाद व्यक्तियों के ग्लिफ़ के लिए जानकारी और बिटमैप होते हैं। इसमें डेटा एकल आकार के उन्मुखीकरण के लिए फ़ॉन्ट के लिए दिखाता है। एक से अधिक दिशाओं में उपयोग किए जाने वाले मेट्रिक्स को एक फ़ाइल में शामिल किया जा सकता है। BDF फ़ाइल में, प्रत्येक आइटम फ़ाइल में टेक्स्ट की एक अलग पंक्ति में समाहित है। रिक्त स्थान का उपयोग वस्तुओं को एक पंक्ति में अलग करने के लिए किया जाता है।

## बीडीएफ फ़ाइल प्रारूप
ग्लिफ़ बिटमैप वितरण प्रारूप के लिए बीडीएफ शॉर्ट्स; Adobe का स्वामित्व बिटमैप प्रकार के फ़ॉन्ट सहेजने के लिए एक फ़ाइल स्वरूप है। सामग्री कंप्यूटर के साथ-साथ मानव पठनीय होने के लिए एक टेक्स्ट फ़ाइल का रूप लेती है। बीडीएफ विशेष रूप से यूनिक्स एक्स विंडो वातावरण में उपयोग किया जाता है। इसे पीसीएफ फ़ॉन्ट प्रारूप द्वारा व्यापक रूप से प्रतिस्थापित किया गया है जिसे अधिक कुशल माना जाता है, और ओपन टाइप और ट्रू टाइप फोंट द्वारा।
### बीडीएफ फ़ाइल संरचना
BDF फ़ॉन्ट फ़ाइल में तीन खंड होते हैं:

- एक वैश्विक खंड जो एक फ़ॉन्ट में सभी ग्लिफ़ पर लागू होता है।
- प्रत्येक ग्लिफ़ के लिए एक अलग प्रविष्टि वाला एक अनुभाग।
- ENDFONT स्टेटमेंट।

## उदाहरण
एएससीआईआई कैपिटल 'ए' के लिए एक ग्लिफ़ युक्त एक उदाहरण फ़ॉन्ट यहां दिया गया है। इसकी वैश्विक घोषणाएं "STARTFONT" लाइन से शुरू होती हैं और "CHARS" लाइन के साथ समाप्त होती हैं
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## संदर्भ
* [ग्लिफ़ बिटमैप वितरण प्रारूप](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [ग्लिफ़ बिटमैप वितरण प्रारूप (बीडीएफ) विशिष्टता](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

