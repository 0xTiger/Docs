{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"सीपीआईओ फ़ाइल - यूनिक्स सीपीआईओ पुरालेख फ़ाइल स्वरूप",
  "description":"जानना सीखें कि सीपीआईओ फ़ाइल और एपीआई क्या है जो सीपीआईओ फाइलें बना और खोल सकती है।",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## सीपीआईओ फ़ाइल क्या है?

सीपीआईओ फ़ाइल यूनिक्स के कॉपी इन कॉपी आउट (सीपीआईओ) प्रारूप में बनाई गई एक संग्रह फ़ाइल है। यह TAR फ़ाइल स्वरूप के समान है, सिवाय इसके कि यह असंपीड़ित है। सीपीआईओ फ़ाइलें डिवाइस फ़ाइलों, प्रतीकात्मक लिंक और विस्तारित फ़ाइल विशेषताओं को संग्रहीत कर सकती हैं।

## सीपीआईओ फ़ाइल प्रारूप

एक सीपीआईओ संग्रह एक बाइनरी फ़ाइल के रूप में बनाया जाता है जो मानव-पठनीय नहीं है। यह फाइलों और निर्देशिकाओं के संग्रह को संग्रहीत करता है। सीपीआईओ संग्रह की सामग्री की पहचान फ़ाइल नाम, अनुमतियाँ, स्वामित्व और टाइमस्टैम्प जैसी मेटाडेटा जानकारी से की जाती है। यह मेटाडेटा जानकारी सिस्टम द्वारा पार्श्व पहुंच के लिए संग्रह फ़ाइल में भी संग्रहीत की जाती है।

## सीपीआईओ पुरालेख का प्रारूप

एक सीपीआईओ फ़ाइल में एक या अधिक सम्मिलित सदस्य फ़ाइलें शामिल होती हैं। संग्रह में प्रत्येक फ़ाइल में वैकल्पिक रूप से एक हेडर होता है जिसके बाद हेडर में उल्लिखित फ़ाइल सामग्री होती है। संग्रह के अंत में एक और हेडर है जिसे TRAILER!! नामक एक खाली फ़ाइल द्वारा वर्णित किया गया है।

### सीपीआईओ अभिलेखागार के प्रकार

सीपीआईओ अभिलेख दो प्रकार के होते हैं। ये केवल हेडर की शैली में भिन्न हैं।

* एएससीआईआई अभिलेखागार - इन सीपीआईओ अभिलेखागार में एक प्रिंट करने योग्य हेडर होता है जो सीपीआईओ संग्रह का हिस्सा बन जाता है यदि संग्रह में एएससीआईआई फाइलें शामिल हैं
* बाइनरी आर्काइव्स - इन सीपीआईओ आर्काइव्स में बाइनरी हेडर हैं।

## सीपीआईओ पुरालेख के साथ कार्य करना

### सीपीआईओ अभिलेखागार कैसे बनाएं?

आप **cpio** कमांड का उपयोग करके यूनिक्स जैसी प्रणालियों पर एक सीपीआईओ बना सकते हैं। निम्न आदेश वर्तमान निर्देशिका और उसकी उपनिर्देशिकाओं में सभी फ़ाइलों और निर्देशिकाओं को ढूंढेगा। यह आउटपुट फिर सीपीआईओ कमांड के लिए पाइप है जो Archive.cpio नामक एक नया सीपीआईओ संग्रह उत्पन्न करेगा।

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### सीपीआईओ अभिलेखागार से फ़ाइलें कैसे निकालें?

निम्न आदेश मौजूदा संग्रह से फ़ाइलें निकालता है।

```
cpio -id < archive_cpio.cpio
```
यह मानक इनपुट से Archive.cpio फ़ाइल को पढ़ेगा और फ़ाइलों को वर्तमान निर्देशिका में निकालेगा।


## संदर्भ

* [सीपीआईओ - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/Cpio)
* [सीपीआईओ फ़ाइल प्रारूप](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

