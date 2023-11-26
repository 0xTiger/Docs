{
"date": "2023-09-27",
  "keywords": [
"सीएफजी",
"सीएफजी फ़ाइल",
"cfg mame कॉन्फ़िगरेशन फ़ाइल",
"सीएफजी फ़ाइल क्या है",
"सीएफजी फ़ाइल कैसे खोलें",
"फ़ाइल",
"सीएफजी फ़ाइल एक्सटेंशन",
"विस्तार"
],
  "author": {
"display_name": "शकील फ़ैज़"
},
"draft": "false",
"toc": true,
"title": "CFG फ़ाइल स्वरूप - MAME कॉन्फ़िगरेशन फ़ाइल",
  "description":"CFG MAME कॉन्फ़िगरेशन फ़ाइल प्रारूप और API के बारे में जानें जो CFG फ़ाइलें बना और खोल सकते हैं।",
"linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
"पैरेंट": "सेटिंग्स"
}
},
"lastmod": "2023-09-27"
}

## सीएफजी फ़ाइल क्या है?

CFG फ़ाइल एक XML कीबोर्ड कॉन्फ़िगरेशन फ़ाइल है जिसका उपयोग MAME आर्केड वीडियो गेम एमुलेटर द्वारा किया जाता है। यह खिलाड़ी की प्राथमिकताओं के अनुरूप कीबोर्ड नियंत्रण और हॉटकी को अनुकूलित करने के लिए महत्वपूर्ण घटक है। ये फ़ाइलें मैपिंग और सेटिंग्स संग्रहीत करती हैं जो यह निर्धारित करती हैं कि गेम खेलते समय कीबोर्ड एमुलेटर के साथ कैसे इंटरैक्ट करता है। इस फ़ाइल को संपादित करके, उपयोगकर्ता गेम के भीतर कार्यों, जैसे सिक्का प्रविष्टि, प्रारंभ, आंदोलन और विभिन्न अन्य कार्यों के लिए विशिष्ट कीबोर्ड कुंजी निर्दिष्ट करके अपने गेमिंग अनुभव को अनुकूलित कर सकते हैं।

## MAME कॉन्फ़िगरेशन फ़ाइल

MAME, जिसका अर्थ है **मल्टीपल आर्केड मशीन एमुलेटर**, एक सॉफ्टवेयर एप्लिकेशन है जो आपको अपने कंप्यूटर पर आर्केड गेम का अनुकरण करने और खेलने की अनुमति देता है। MAME अपने व्यवहार और सेटिंग्स को अनुकूलित करने के लिए कॉन्फ़िगरेशन फ़ाइलों का उपयोग करता है। ये कॉन्फ़िगरेशन फ़ाइलें आमतौर पर आपकी MAME निर्देशिका के भीतर `cfg` फ़ोल्डर में स्थित होती हैं।

यहां मुख्य कॉन्फ़िगरेशन फ़ाइलें हैं जिनका सामना आपको MAME को सेट और कॉन्फ़िगर करते समय मिल सकता है:

1. **mame.ini:** यह MAME के लिए मुख्य कॉन्फ़िगरेशन फ़ाइल है। इसमें वैश्विक सेटिंग्स शामिल हैं जो सभी खेलों पर लागू होती हैं। आप इस फ़ाइल को अपने MAME इंस्टॉलेशन की रूट डायरेक्टरी में पा सकते हैं।

1. **default.cfg:** यह फ़ाइल उन सभी खेलों के लिए डिफ़ॉल्ट सेटिंग्स संग्रहीत करती है जिनकी अपनी कॉन्फ़िगरेशन फ़ाइलें नहीं होती हैं। इसका उपयोग गेम-विशिष्ट सेटिंग्स के लिए फ़ॉलबैक के रूप में किया जाता है।

1. **गेम-विशिष्ट.सीएफजी:** इन फ़ाइलों का उपयोग अलग-अलग गेम के लिए सेटिंग्स संग्रहीत करने के लिए किया जाता है। इनका नाम आम तौर पर उस गेम की ROM फ़ाइल के नाम पर रखा जाता है जिससे वे मेल खाते हैं। उदाहरण के लिए, यदि आपके पास "pacman.zip" नामक गेम है, तो इसके लिए कॉन्फ़िगरेशन फ़ाइल "pacman.cfg" होगी।

यहां कुछ सामान्य सेटिंग्स दी गई हैं जो आपको MAME कॉन्फ़िगरेशन फ़ाइल में मिल सकती हैं।

1. **रोमपाथ:** वह निर्देशिका निर्दिष्ट करता है जहां आपके आर्केड गेम रोम स्थित हैं।

1. **cfg_directory:** वह निर्देशिका निर्दिष्ट करती है जहां गेम-विशिष्ट कॉन्फ़िगरेशन फ़ाइलें संग्रहीत की जाती हैं।

1. **nvram_directory:** वह निर्देशिका निर्दिष्ट करती है जहां गैर-वाष्पशील RAM (NVRAM) फ़ाइलें संग्रहीत की जाती हैं। एनवीआरएएम उच्च स्कोर और अन्य गेम-विशिष्ट डेटा संग्रहीत करता है।

1. **artwork_directory:** वह निर्देशिका निर्दिष्ट करती है जहां कलाकृति फ़ाइलें (जैसे बेज़ेल्स, मार्कीज़ और फ़्लायर्स) संग्रहीत की जाती हैं।

1. **नमूनापथ:** उस निर्देशिका को निर्दिष्ट करता है जहां नमूना ध्वनि फ़ाइलें स्थित हैं।

1. **चीटपाथ:** उस निर्देशिका को निर्दिष्ट करता है जहां चीट फ़ाइलें स्थित हैं।

आप विभिन्न अन्य सेटिंग्स जैसे वीडियो और ऑडियो विकल्प, नियंत्रण और इनपुट डिवाइस भी कॉन्फ़िगर कर सकते हैं। इन सेटिंग्स को संशोधित करने के लिए, आप टेक्स्ट एडिटर में कॉन्फ़िगरेशन फ़ाइल खोल सकते हैं और आवश्यक परिवर्तन कर सकते हैं।

## माँ

MAME, जिसका अर्थ है **"मल्टीपल आर्केड मशीन एमुलेटर,"** एक सॉफ्टवेयर एप्लिकेशन है जिसे पुरानी आर्केड मशीनों और आर्केड गेम कंसोल के हार्डवेयर का अनुकरण और प्रतिलिपि बनाने के लिए डिज़ाइन किया गया है। यह उपयोगकर्ताओं को आधुनिक कंप्यूटर और अन्य संगत उपकरणों पर क्लासिक आर्केड गेम की विशाल लाइब्रेरी खेलने की अनुमति देता है। MAME एक ओपन-सोर्स प्रोजेक्ट है और आर्केड गेमिंग के समृद्ध इतिहास को संरक्षित करने और उसका आनंद लेने के लिए एमुलेटर बन गया है।

1. **अनुकरण:** MAME का प्राथमिक उद्देश्य आर्केड मशीनों के हार्डवेयर का सटीक अनुकरण करना है, जिसमें उनकी केंद्रीय प्रसंस्करण इकाइयां (सीपीयू), ध्वनि चिप्स, ग्राफिक्स चिप्स और इनपुट डिवाइस शामिल हैं। सटीकता का यह स्तर यह सुनिश्चित करता है कि गेम यथासंभव मूल आर्केड अनुभव के करीब हों।

1. **संगतता:** MAME आर्केड गेम ROM की विस्तृत श्रृंखला का समर्थन करता है, जो इसे उपलब्ध सबसे व्यापक आर्केड एमुलेटरों में से एक बनाता है। यह विभिन्न आर्केड प्लेटफार्मों से गेम चला सकता है जिसमें 70, 80, 90 के दशक के क्लासिक गेम और यहां तक कि कुछ हालिया आर्केड शीर्षक भी शामिल हैं।

1. **संरक्षण:** MAME के प्राथमिक मिशनों में से एक आर्केड गेमिंग के इतिहास को संरक्षित करना है। आर्केड हार्डवेयर का सटीक अनुकरण करके, MAME क्लासिक गेम के नुकसान को रोकने में मदद करता है और यह सुनिश्चित करता है कि आने वाली पीढ़ियां उन्हें उसी तरह अनुभव कर सकें जैसा उनका मूल रूप से इरादा था।

1. **फ्रंट-एंड:** कई उपयोगकर्ता फ्रंट-एंड एप्लिकेशन का उपयोग करते हैं जो MAME के माध्यम से गेम को प्रबंधित और लॉन्च करने के लिए ग्राफिकल इंटरफ़ेस प्रदान करते हैं। ये फ्रंट-एंड MAME की गेम्स की व्यापक लाइब्रेरी को नेविगेट करना आसान बनाते हैं।

## सीएफजी फ़ाइल कैसे खोलें?

प्रोग्राम जो CFG फ़ाइलें खोलते या संदर्भित करते हैं

- MAME (फ्री) (विंडोज़)
- एक्स्ट्रामैम (परीक्षण)
- मैकमैम (मैक)

## अन्य सीएफजी फ़ाइलें

यहां अन्य फ़ाइल प्रकार हैं जो **.cfg** फ़ाइल एक्सटेंशन का उपयोग करते हैं।

**समायोजन**
- [सीएफजी - सेलेस्टिया कॉन्फ़िगरेशन फ़ाइल](/hi/सेटिंग्स/सीएफजी-सेलेस्टिया/)
- [सीएफजी - सिट्रिक्स सर्वर कनेक्शन फ़ाइल](/hi/सेटिंग्स/सीएफजी-सिट्रिक्स/)
- [CFG - MAME कॉन्फ़िगरेशन फ़ाइल](/hi/सेटिंग्स/cfg-mame/)
- [सीएफजी - लाइटवेव कॉन्फ़िगरेशन फ़ाइल](/hi/सेटिंग्स/सीएफजी-लाइटवेव/)

**खेल**
- [सीएफजी - वेस्नोथ मार्कअप लैंग्वेज फ़ाइल](/hi/गेम/सीएफजी-वेस्नोथ/)
- [CFG - MUGEN कॉन्फ़िगरेशन फ़ाइल](/hi/game/cfg-mugen/)
- [सीएफजी - स्रोत इंजन कॉन्फ़िगरेशन फ़ाइल](/hi/गेम/सीएफजी-सोर्सइंजिन/)

**सिस्टम एवं विविध**
- [सीएफजी - सीएफजी फ़ाइल](/hi/सिस्टम/सीएफजी/)
- [CFG - Cal3D मॉडल कॉन्फ़िगरेशन फ़ाइल](/hi/misc/cfg-cal3d/)

## संदर्भ
* [MAME](https://en.wikipedia.org/wiki/MAME)
