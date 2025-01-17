{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Microsoft OneNote फ़ाइल स्वरूप",
  "description":"ONETOC2 फ़ाइल स्वरूप और API के बारे में जानें जो ONETOC2 फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## ONETOC2 क्या है? ##

जिन लोगों ने [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-takeing-app) ऐप्लिकेशन के साथ काम किया है, उन्होंने नोटबुक फ़ोल्डर में .onetoc2 फ़ाइलों की उपस्थिति देखी होगी। Microsoft OneNote एक नोटबुक में विभिन्न नोट-लेने वाले अनुभागों के क्रम के बारे में एक अनुक्रमणिका रखने के लिए सामग्री तालिका के रूप में बाइनरी .onetoc2 फ़ाइल बनाता है। एक नोटबुक अनुभाग फ़ाइलों का एक संग्रह है जो एक ही निर्देशिका में संग्रहीत हैं। .onetoc2 फ़ाइल गुणों के संग्रह का उपयोग सेटिंग्स निर्दिष्ट करने के लिए करती है जैसे नोटबुक के भीतर अनुभागों का क्रम और नोटबुक का रंग।

जब आप OneNote 2016 में एक नोटबुक बनाते हैं, तो यह स्वचालित रूप से नए 2010-2016 फ़ाइल स्वरूप में सहेजी जाती है। यदि आप चाहते हैं कि OneNote 2016 की सभी सुविधाएँ, जैसे गणित के समीकरण और लिंक्ड नोट्स ठीक से काम करें, तो आपको इस प्रारूप की आवश्यकता होगी।

## ONETOC2 फ़ाइल स्वरूप ##

.onetoc2 फ़ाइल प्रारूप को OneNote संशोधन स्टोर फ़ाइल स्वरूप के रूप में दर्शाया गया है और यह संरचनाओं का एक संग्रह है जो क्रॉस-रेफ़रेंस्ड ऑब्जेक्ट स्पेस में व्यवस्थित एक संशोधन स्टोर निर्दिष्ट करता है, जिसमें संपत्ति सेट के साथ ऑब्जेक्ट होते हैं, और एसिंक्रोनस में फ़ाइल अखंडता सुनिश्चित करने के लिए लेनदेन लॉग होता है। लिखता है। .onetoc2 फ़ाइल प्रारूप के लिए पूर्ण विनिर्देश उपलब्ध हैं [ऑनलाइन](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) और अनुप्रयोगों के विकास के लिए संदर्भित किया जा सकता है .

### फ़ाइल संरचना ###

एक पुनरीक्षण स्टोर फ़ाइल **शीर्षलेख** संरचना से शुरू होनी चाहिए। फ़ाइल के शेष भाग को बाइट्स के ब्लॉक में विभाजित किया गया है, जहाँ प्रत्येक ब्लॉक का आकार और संरचना उस फ़ील्ड द्वारा निर्दिष्ट किया जाता है जो इसे संदर्भित करता है। एक ब्लॉक पहुंच योग्य है यदि इसे ** हैडर ** संरचना द्वारा संदर्भित किया जाता है, या यदि इसे किसी अन्य पहुंच योग्य ब्लॉक में किसी फ़ील्ड द्वारा संदर्भित किया जाता है। **शीर्षलेख** संरचना के बाहर डेटा और किसी भी पहुंच योग्य ब्लॉक को अनदेखा किया जाना चाहिए।

सभी संरचनाएं 1-बाइट सीमाओं पर संरेखित होती हैं। जब तक अन्यथा निर्दिष्ट न हो, सभी पूर्णांकों पर हस्ताक्षर किए जाते हैं। जब तक अन्यथा निर्दिष्ट न किया जाए, सभी फ़ील्ड [थोड़ा-एंडियन](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) हैं।

#### हैडर ####

.ONE फ़ाइल के शीर्षलेख में ऐसे खंड शामिल हैं जिनमें फ़ाइल जानकारी के प्रतिनिधित्व के लिए अलग-अलग अद्वितीय आईडी और फ़ील्ड शामिल हैं:

`guidFileType (16 बाइट्स):` एक GUID जो संशोधन स्टोर फ़ाइल के प्रकार को निर्दिष्ट करता है। निम्न तालिका से मानों में से एक होना चाहिए।

|फ़ाइल स्वरूप|मान
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 बाइट्स):` एक GUID जो इस पुनरीक्षण स्टोर फ़ाइल की पहचान निर्दिष्ट करता है। विश्व स्तर पर अद्वितीय होना चाहिए।

`guidLegacyFileVersion (16 बाइट्स):` "{00000000-0000-0000-0000-000000000000}" होना चाहिए और इसे अनदेखा किया जाना चाहिए।

`guidFileFormat (16 बाइट्स):` एक GUID जो निर्दिष्ट करता है कि फ़ाइल एक पुनरीक्षण स्टोर फ़ाइल है। "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}" होना चाहिए।

`ffvLastCodeThatWroteToThisFile (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक। फ़ाइल प्रकार के आधार पर निम्न तालिका में मानों में से एक होना चाहिए।

|फ़ाइल स्वरूप|मान
--- | --- |
|.एक|0x0000002ए
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक। इस फ़ाइल के फ़ाइल स्वरूप के आधार पर, निम्न तालिका में मानों में से एक होना चाहिए।


|फ़ाइल स्वरूप|मान
--- | --- |
|.एक|0x0000002ए
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक। इस फ़ाइल के फ़ाइल स्वरूप के आधार पर, निम्न तालिका में मानों में से एक होना चाहिए।
:


|फ़ाइल स्वरूप|मान
--- | --- |
|.एक|0x0000002ए
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक। इस फ़ाइल के फ़ाइल स्वरूप के आधार पर, निम्न तालिका में मानों में से एक होना चाहिए।


|फ़ाइल स्वरूप|मान
--- | --- |
|.एक|0x0000002ए
|.onetoc2|0x0000001B

## संदर्भ ##

* [[MS-ONESTORE] - OneNote फ़ाइल स्वरूप](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [माइक्रोसॉफ्ट वनोट - विकिपीडिया](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

