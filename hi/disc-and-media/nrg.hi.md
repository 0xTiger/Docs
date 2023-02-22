{
  "date" : "2021-08-16",
  "keywords" :[ "एनआरजी फाइल", "एनआरजी फाइल फॉर्मेट", "एनआरजी फाइल क्या है", "फाइल", "एनआरजी उदाहरण", "एनआरजी फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट", "एनआरजी फूटर", "फाइल एनआरजी का प्रारूप", "नीरो बर्निंग रोम", "नीरो एजी"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"एनआरजी फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एनआरजी फाइलें बना और खोल सकते हैं।",
  "title" :"एनआरजी - डिस्क छवि फ़ाइल स्वरूप",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## एनआरजी फाइल क्या है?

एक ऑप्टिकल डिस्क के उपयोग द्वारा बनाई गई छवि फ़ाइल स्वरूप को एक NRG फ़ाइल स्वरूप माना जाता है। यह प्रारूप विशेष रूप से Nero द्वारा Nero Burning ROM की उपयोगिता के लिए बनाया गया है। डिस्क छवियों के भंडारण के लिए, इस प्रारूप का उपयोग माना जाता है क्योंकि यह इन विशिष्ट फ़ाइलों के लिए उपयुक्त है। ये फाइलें सीडी या डीवीडी की एक सटीक प्रति के रूप में हो सकती हैं या इनमें कई फाइलें हो सकती हैं जिन्हें डिस्क के रूप में माउंट किया जा सकता है। अन्य अधिक लोकप्रिय फ़ाइल स्वरूप जैसे [ISO](/hi/compression/iso/) फ़ाइल स्वरूप वे हैं जिनमें इन फ़ाइलों को कुछ बुनियादी उपयोगिताओं में परिवर्तित किया जा सकता है। अधिकतर, एनआरजी फाइलों का उपयोग बैकअप या कुछ महत्वपूर्ण डेटा या डिस्क की प्रतियां बनाने के लिए किया जाता है।

## एनआरजी फ़ाइल प्रारूप ##

यह फ़ाइल स्वरूप Nero AG द्वारा डिस्क छवि प्रारूप के रूप में विकसित किया गया था। इसमें Nero Burning ROM उपयोगिता की विशिष्ट संपत्ति थी क्योंकि इसे डिस्क छवियों को संग्रहीत करने के लिए विकसित किया गया था। इसका पहला संस्करण मानों को 32-बिट पूर्णांक के रूप में संग्रहीत करने के लिए निर्दिष्ट किया गया था। हालाँकि, इसका दूसरा संस्करण लॉन्च किया गया था और इसमें 64-बिट पूर्णांकों के लिए समर्थन शामिल था।

## तकनीकी विनिर्देश ##

फ़ाइल की शुरुआत में, यह प्रारूप अपने डेटा को हेडर के रूप में संग्रहीत नहीं करता है। एक पादलेख की तरह, यह फ़ाइल के अंत में संलग्न होता है। IFF के विखंडू के रूप में, छवि की जानकारी संग्रहीत की जाती है। फ़ाइल के अंतिम 8 बाइट्स से 12 बाइट्स पर NRG फ़ुटर को पढ़कर पहले चंक की ऑफ़सेट प्राप्त की जा सकती है। एनआरजी फ़ाइल प्रारूप के सभी संस्करणों में, खंड, डीएओआई, सीडी पाठ, सत्र सूचना मीडिया प्रकार, डिस्क जानकारी, रेलो और इसके साथ संलग्न श्रृंखला का अंत है। बाइट ऑर्डर बड़ा-एंडियन है और भंडारण के समय सभी पूर्णांक मान अहस्ताक्षरित हैं।

### मुख्य भाग ###

#### क्यू पत्र ####

यह क्यू शीट सभी एनआरजी फाइल प्रारूप संस्करणों में आसानी से उपलब्ध है। **CUEX** का हिस्सा निश्चित आकार के संयोजन के ब्लॉक का मतलब है और इनमें से प्रत्येक क्यू बिंदु का प्रतिनिधित्व करता है।

#### डीएओ सूचना ####

यह जानकारी सभी एनआरजी प्रारूप संस्करणों में भी मौजूद है। **DAOI** के भाग प्रासंगिक विशिष्ट जानकारी को 2 भागों में संग्रहीत करते हैं। इसके पहले भाग में केवल सत्र-विशिष्ट डेटा होता है। इसका दूसरा भाग ट्रैकिंग से संबंधित ग्रे जानकारी को दोहराता है और यह प्रत्येक ट्रैक के लिए केवल एक बार होता है।

#### सीडी-पाठ ####

यह एनआरजी के दूसरे संस्करण में उपलब्ध है। **सीडीटीएक्स** के हिस्से में सीडी-टेक्स्ट पैक का कच्चा संयोजन होता है जिसमें प्रत्येक के लिए 18 बाइट्स होते हैं।

#### विस्तारित ट्रैक जानकारी ####

यह NRG के फ़ाइल स्वरूप के प्रत्येक संस्करण में उपलब्ध है। इन हिस्सों का उपयोग एक बार सत्र ट्रैक के लिए ट्रैकिंग जानकारी संग्रहीत करने के लिए किया जाता है। यह डेटा प्रत्येक ट्रैक के मामले में केवल एक बार दोहराया जाता है।

#### सत्र की जानकारी ####

यह NRG के फ़ाइल स्वरूप के प्रत्येक संस्करण में भी उपलब्ध है। सत्र भाग की जानकारी का उपयोग सत्र की छवि को जल्दी से स्कैन करने और फिर गिनती को ट्रैक करने के लिए किया जाना चाहिए।

#### श्रृंखला का अंत ####

अंत के चंक का मतलब यह संकेत है कि अब कोई और हिस्सा नहीं है जिसे पढ़ने की जरूरत है और यह एनआरजी के सभी संस्करणों में भी उपलब्ध है।


## संदर्भ ##

* [एनआरजी - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/NRG_(file_format))

