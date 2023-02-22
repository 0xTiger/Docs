{
  "date" : "2021-03-08",
  "keywords" :[ "आरबी", "नुवो मीडिया का रॉकेट ईबुक डिवाइस", "फाइल", "एक्सटेंशन", "फॉर्मेट", "ईबुक"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"नूवो मीडिया के रॉकेट ईबुक डिवाइस और एपीआई के लिए आरबी फ़ाइल प्रारूप के बारे में जानें जो आरबी फाइलें बना और खोल सकते हैं।",
  "title" :"आरबी - रॉकेट ईबुक फ़ाइल",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## आरबी फाइल क्या है?

.rb एक्सटेंशन वाली फ़ाइल में Rocket eBook सामग्री होती है। रॉकेट ईबुक वास्तव में नुवो मीडिया द्वारा बनाया गया एक उपकरण है; उन्होंने 1998 में इस उपकरण को जारी किया। हालांकि रॉकेट ईबुक छवियों को प्रदर्शित करने में सक्षम है, लेकिन केवल काले और सफेद प्रदर्शन में। इसमें 4.5 x 3 इंच की टच स्क्रीन पर 106 डीपीआई या 480 x 320 पिक्सल की स्क्रीन है। रॉकेट ईबुक आरबी फाइल फॉर्मेट में ईबुक डाउनलोड करने के लिए सीरियल पोर्ट कनेक्शन के जरिए कंप्यूटर से जुड़ता है। आरबी फाइलें डीआरएम का उपयोग करने में सक्षम हैं लेकिन आधुनिक ईबुक में इस तकनीक का उपयोग नहीं किया जा रहा है। आरबी फ़ाइल में पारंपरिक रूप से छवियों के साथ एक HTML फ़ाइल और सभी मेटाडेटा (.info) के साथ एक छद्म-ओपीएफ फ़ाइल होती है।

## आरबी फ़ाइल प्रारूप की तकनीकी विशिष्टता ##

फ़ाइल के पहले 4 बाइट्स में एक मैजिक नंबर (हेक्स में) दिखाई देता है: B0 0C B0 0C।

ऐसा प्रतीत होता है कि अगले दो बाइट्स एक संस्करण संख्या हैं, जैसे "02 00", जो प्रमुख संस्करण 2 और लघु संस्करण 0 के लिए है।

अगले चार बाइट्स में "NUVO" टेक्स्ट होता है, इसके बाद 00h के 4 बाइट्स होते हैं।

अगली 4-बाइट वह तिथि है जब पुस्तक बनाई गई थी, जिसे एक int16 के रूप में एन्कोड किया गया था। यह हमें ऑफसेट 0Eh पर रखता है। ORocketLibrary के पुराने संस्करण ने वर्ष के पूर्ण मान को कूटबद्ध किया (अर्थात, 1999 "CF 07", 2000 "D0 07" था)। हाल के संस्करण में, tm_year शब्दशः संग्रहीत है, अर्थात वर्ष 2000 के लिए 100 ("64 00")। वर्ष के बाद एक int8 1-रिश्तेदार महीने की संख्या का प्रतिनिधित्व करता है, और एक int8 महीने के दिन का प्रतिनिधित्व करता है।

अगले 6 बाइट्स 00h हैं। समय निर्धारण के लिए, इन्हें आरक्षित किया जा सकता है।

"सामग्री की तालिका" का पूर्ण ऑफसेट ऑफसेट 18h पर int32 में निहित है।

इसके बाद एक int32 है जिसमें .rb फ़ाइल की लंबाई है। इसका उपयोग यह निर्धारित करने के लिए किया जाता है कि फाइलें पूर्ण हैं या नहीं।

बाइट्स का यह पूरा हिस्सा (20h से 128h) केवल एन्क्रिप्टेड शीर्षक के लिए आवश्यक प्रतीत होता है। गैर-एन्क्रिप्टेड शीर्षकों में, वे हमेशा शून्य होते हैं।

ज्यादातर मामलों में, सामग्री की तालिका इस प्रकार है (ऑफ़सेट 128 पर)। यह टीओसी में "पेज" प्रविष्टियों (.आरबी-फाइल सेक्शन) की संख्या की एक int32 गणना के साथ शुरू होता है। प्रत्येक प्रविष्टि में एक नाम होता है (32 बाइट्स के लिए शून्य-गद्देदार), उसके बाद 3 int32s: डेटा खंड की लंबाई, .rb फ़ाइल में स्थिति और इस प्रविष्टि के लिए एक ध्वज। आज तक, ज्ञात मान हैं: 1 (एन्क्रिप्टेड), 2 (सूचना पृष्ठ), और 8 (अपस्फीति)। यह सुनिश्चित करने के लिए कि वे सभी अद्वितीय हैं, सभी नाम आवश्यकतानुसार तैयार किए गए हैं।

## संदर्भ

* [ई-रीडर - MobileRead द्वारा](https://en.wikipedia.org/wiki/E-reader)
