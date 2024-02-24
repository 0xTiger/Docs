{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"अवास्तविक स्टेटिक मेश वीपीके फ़ाइल प्रारूप और एपीआई के बारे में जानें जो वीपीके फाइलें बना और खोल सकते हैं।",
  "title" : "वीपीके फ़ाइल - अवास्तविक स्टेटिक मेश फ़ाइल",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-hi",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## वीपीके फ़ाइल क्या है?

.vpk फ़ाइल एक फ़ाइल स्वरूप है जिसका उपयोग वाल्व कॉर्पोरेशन द्वारा विकसित गेम इंजन **सोर्स इंजन** द्वारा किया जाता है। वीपीके फाइलों का उपयोग गेम सामग्री, जैसे मॉडल, बनावट और ध्वनि को पैकेज करने के लिए किया जाता है, और आमतौर पर टीम फोर्ट्रेस 2, लेफ्ट 4 डेड और काउंटर-स्ट्राइक: ग्लोबल ऑफेंसिव जैसे गेम में उपयोग किया जाता है। फ़ाइलें विभिन्न प्रकार के टूल, जैसे GCFScape और VPK टूल का उपयोग करके खोली और निकाली जा सकती हैं।

## वीपीके फ़ाइल प्रारूप - अधिक जानकारी

वीपीके फ़ाइलें बाइनरी फ़ाइलों के रूप में डिस्क पर संग्रहीत की जाती हैं। एक एकल वीपीके फ़ाइल वीपीके पैकेज का हिस्सा हो सकती है या एक स्वतंत्र कच्ची वीपीके फ़ाइल के रूप में कार्य कर सकती है। वीपीके फ़ाइल के अंदर संग्रहीत की जा सकने वाली जानकारी में मानचित्र, सामग्री, खेल सामग्री और कोरियोग्राफी दृश्य शामिल हैं।

### VPK फाइल कैसे बनाएं?

उपलब्ध टूल के आधार पर .vpk फ़ाइल बनाने के कई तरीके हैं।

1. `वीपीके टूल का उपयोग करना:` यह एक कमांड-लाइन टूल है जिसका उपयोग वीपीके फाइलें बनाने और निकालने के लिए किया जा सकता है। निम्नलिखित कमांड का उपयोग करके एक VPK फ़ाइल बनाई जा सकती है:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
यह निर्दिष्ट निर्देशिका से एक वीपीके फ़ाइल बनाएगा, और इसे निर्दिष्ट आउटपुट फ़ाइल के रूप में सहेजेगा।

1. `हैमर एडिटर का उपयोग करना:` हैमर एडिटर सोर्स एसडीके के साथ शामिल एक उपकरण है जिसका उपयोग सोर्स इंजन का उपयोग करने वाले गेम के लिए स्तर बनाने और संपादित करने के लिए किया जा सकता है। इसमें फ़ाइल सिस्टम टैब में एक फ़ोल्डर पर राइट-क्लिक करके और वीपीके बनाएं का चयन करके वीपीके फ़ाइलें बनाने की क्षमता भी शामिल है।

1. `वाल्व के वीपीके निर्माता का उपयोग करना:` यह वाल्व द्वारा विकसित एक उपकरण है जिसका उपयोग गेम सामग्री को पैकेज और वितरित करने के लिए किया जाता है। इस टूल का उपयोग VPK फ़ाइलें बनाने के लिए किया जा सकता है और यह VPK फ़ाइलें बनाने का आधिकारिक टूल भी है।

## संदर्भ

 * [वाल्व सॉफ्टवेयर](https://www.valvesoftware.com/en/)
 * [वीपीके डेवलपर के संसाधन](https://developer.valvesoftware.com/wiki/GCF)
