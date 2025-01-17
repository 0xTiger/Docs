{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एक - माइक्रोसॉफ्ट वनोट फ़ाइल स्वरूप",
  "description":"एक फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एक फाइल बना और खोल सकता है।",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## एक .ONE फ़ाइल क्या है? ##

.ONE एक्सटेंशन द्वारा दर्शाई गई फ़ाइल Microsoft OneNote एप्लिकेशन द्वारा बनाई गई है। OneNote आपको एप्लिकेशन का उपयोग करके जानकारी एकत्र करने देता है जैसे कि आप नोट्स लेने के लिए अपने ड्राफ्ट पैड का उपयोग कर रहे हों। OneNote फ़ाइलों में विभिन्न तत्व हो सकते हैं जिन्हें दस्तावेज़ पृष्ठों पर गैर-निश्चित स्थानों पर रखा जा सकता है। इन तत्वों में टेक्स्ट, डिजीटल हैंडराइटिंग, और इमेज, ड्रॉइंग और मल्टीमीडिया (ऑडियो/वीडियो) क्लिप सहित अन्य एप्लिकेशन से कॉपी किए गए ऑब्जेक्ट हो सकते हैं। Microsoft अब Office365 के भाग के रूप में OneNote का ऑनलाइन संस्करण प्रदान करता है जहाँ नोट्स इंटरनेट पर अन्य OneNote उपयोगकर्ताओं के साथ साझा किए जा सकते हैं।

## .ONE फ़ाइल स्वरूप निर्दिष्टीकरण ##

OneNote फ़ाइल स्वरूप डिजिटल नोटों को अनुभागों और पृष्ठों के श्रेणीबद्ध सेट के रूप में प्रस्तुत करने का प्रभावी तरीका प्रदान करता है. प्रत्येक पृष्ठ में फ़ाइल स्वरूप दस्तावेज़ ऑब्जेक्ट मॉडल (DOM) द्वारा प्रतिनिधित्व के लिए एक विशिष्ट संरचना में उपयोगकर्ता-परिभाषित सामग्री होती है। इस प्रारूप के लिए डेटा मॉडल नीचे सचित्र है।

### संरचना अवलोकन ###

जैसा कि OneNote फ़ाइल स्वरूप के लिए डेटा मॉडल में दिखाया गया है, OneNote दस्तावेज़ में विभिन्न तत्व होते हैं।

#### खंड ####

अनुभाग किसी OneNote फ़ाइल का सबसे शीर्ष कंटेनर होता है जिसमें आगे विभिन्न तत्व शामिल होते हैं जैसे:

* पन्ने
* मेटाडेटा
* गुण

मेटाडेटा और गुणों में अनुभाग का नाम, अनुभाग में शामिल पृष्ठों की पहचान और उन पृष्ठों के प्रकट होने का क्रम शामिल है। "सेक्शन" शब्द उन सभी पेजों को संदर्भित करता है जो एक सेक्शन में हैं और OneNote® संशोधन स्टोर फ़ाइल में उस डेटा का प्रतिनिधित्व करते हैं, जिसमें एक .one फ़ाइल नाम एक्सटेंशन है।

#### पृष्ठ ####

OneNote दस्तावेज़ में उपयोगकर्ता-परिभाषित सामग्री पृष्ठ के अंदर समाहित है। पृष्ठ की जानकारी में पाठ, सूचियाँ, तालिकाएँ, पृष्ठ शीर्षक, चित्र और नोट टैग शामिल हैं। एक पृष्ठ में आउटलाइन ऑब्जेक्ट होते हैं जिनमें अधिकांश निहित ऑब्जेक्ट जोड़े जाते हैं। प्रत्येक पृष्ठ को सार्थक प्रतिनिधित्व के लिए एक नाम दिया जा सकता है और वस्तुओं को सीधे पृष्ठों में भी जोड़ा जा सकता है। एक पृष्ठ में एक पदानुक्रमित प्रणाली में उप-पृष्ठ भी शामिल हो सकते हैं।

#### गुण और संपत्ति सेट ####

OneNote सामग्री में गुण, गुण सेट और फ़ाइल डेटा ऑब्जेक्ट होते हैं। एक संपत्ति सेट गुणों का संग्रह है जो किसी प्रकार की सामग्री का प्रतिनिधित्व करता है। फ़ाइल डेटा ऑब्जेक्ट बाइनरी डेटा का एक ब्लॉक है जिसमें चित्र, एम्बेडेड फ़ाइलें या ऑडियो/वीडियो सामग्री होती है।

#### वननोट नोटबुक ####

एक नोटबुक अनुभाग फ़ाइलों का एक संग्रह है जो एक ही निर्देशिका में संग्रहीत हैं। संपत्तियों के एक संग्रह का उपयोग सेटिंग्स को निर्दिष्ट करने के लिए किया जाता है जैसे कि नोटबुक के भीतर अनुभागों का क्रम और नोटबुक का रंग।

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

|फ़ाइल स्वरूप|मान
--- | --- |
|.एक|0x0000002ए
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक। इस फ़ाइल के फ़ाइल स्वरूप के आधार पर, निम्न तालिका में मानों में से एक होना चाहिए।

|फ़ाइल स्वरूप|मान
--- | --- |
|.एक|0x0000002ए
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 बाइट्स):` एक **FileChunkReference32** संरचना जिसमें "fcrZero" का मान होना चाहिए।

`fcrLegacyTransactionLog (8 बाइट्स):` एक **FileChunkReference32** संरचना जो "fcrNil" होनी चाहिए।

`cTransactionsInLog (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक जो लेन-देन लॉग में लेनदेन की संख्या निर्दिष्ट करता है। शून्य नहीं होना चाहिए।

`cbLegacyExpectedFileLength (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक जो शून्य होना चाहिए, और इसे अनदेखा किया जाना चाहिए।

`आरजीबीप्लेसहोल्डर (8 बाइट्स):` एक अहस्ताक्षरित पूर्णांक जो शून्य होना चाहिए, और इसे अनदेखा किया जाना चाहिए।

`fcrLegacyFileNodeListRoot (8 बाइट्स):` एक **FileChunkReference32** संरचना जो "fcrNil" होनी चाहिए।

`cbLegacyFreeSpaceInFreeChunkList (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक जो शून्य होना चाहिए, और इसे अनदेखा किया जाना चाहिए।

`FNeedsDefrag (1 बाइट):` को अनदेखा किया जाना चाहिए।

`FRepairedFile (1 बाइट):` को अनदेखा किया जाना चाहिए।

`fNeedsGarbageCollect (1 बाइट):` को अनदेखा किया जाना चाहिए।

`FHasNoEmbeddedFileObjects (1 बाइट):` एक अहस्ताक्षरित पूर्णांक जो शून्य होना चाहिए, और इसे अनदेखा किया जाना चाहिए।

`guidAncestor (16 बाइट्स):` एक GUID जो सामग्री फ़ाइल की तालिका के **Header.guidFile** फ़ील्ड को निर्दिष्ट करता है, जो निम्न तालिका द्वारा दिया गया है:


|सामग्री फ़ाइल प्रारूप की तालिका|सामग्री फ़ाइल की तालिका का स्थान
--- | --- |
|अनुभाग फ़ाइल - .एक|सामग्री फ़ाइल की तालिका इस फ़ाइल के समान निर्देशिका में स्थित है।
|सामग्री की तालिका फ़ाइल - .onetoc2|सामग्री की तालिका फ़ाइल इस फ़ाइल की मूल निर्देशिका में स्थित है।

यदि GUID {00000000-0000-0000-0000-000000000000} है, तो यह फ़ील्ड सामग्री फ़ाइल की तालिका का संदर्भ नहीं देती है।

`crcName (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक जो इस पुनरीक्षण स्टोर फ़ाइल के नाम का CRC मान निर्दिष्ट करता है। नाम इसके विस्तार के साथ फ़ाइल नाम का यूनिकोड प्रतिनिधित्व है और अंत में एक अतिरिक्त अशक्त वर्ण है। इस CRC की गणना हमेशा .one फ़ाइल के लिए CRC एल्गोरिथम का उपयोग करके की जाती है, इस संशोधन स्टोर फ़ाइल प्रारूप की परवाह किए बिना।

`fcrHashedChunkList (12 बाइट्स):` एक **FileChunkReference64x32** संरचना जो हैश की गई चंक सूची में पहले **FileNodeListFragment** के संदर्भ को निर्दिष्ट करती है। यदि **FileChunkReference64x32** संरचना का मान "fcrZero" या "fcrNil" है, तो हैश की गई चंक सूची मौजूद नहीं है।

`fcrTransactionLog (12 बाइट्स):` एक **FileChunkReference64x32** संरचना जो लेनदेन लॉग में पहली **TransactionLogFragment** संरचना के संदर्भ को निर्दिष्ट करती है। **FcrTransactionLog** फ़ील्ड का मान "fcrZero" नहीं होना चाहिए और "fcrNil" नहीं होना चाहिए।

`fcrFileNodeListRoot (12 बाइट्स):` एक **FileChunkReference64x32** संरचना जो रूट फ़ाइल नोड सूची के संदर्भ को निर्दिष्ट करती है। **FcrFileNodeListRoot** फ़ील्ड का मान "fcrZero" नहीं होना चाहिए और "fcrNil" नहीं होना चाहिए।

`fcrFreeChunkList (12 बाइट्स):` एक **FileChunkReference64x32** संरचना जो पहले **FreeChunkListFragment** संरचना के संदर्भ को निर्दिष्ट करती है। यदि **FileChunkReference64x32** संरचना का मान "fcrZero" या "fcrNil" है, तो मुक्त हिस्सा सूची मौजूद नहीं है।

`cbExpectedFileLength (8 बाइट्स):` एक अहस्ताक्षरित पूर्णांक जो इस पुनरीक्षण स्टोर फ़ाइल के बाइट्स में आकार निर्दिष्ट करता है।

`cbFreeSpaceInFreeChunkList (8 बाइट्स):` एक अहस्ताक्षरित पूर्णांक जो बाइट्स में मुक्त चंक सूची द्वारा निर्दिष्ट मुक्त स्थान के आकार को निर्दिष्ट करना चाहिए।

`guidFileVersion (16 बाइट्स):` एक GUID। जब **cTransactionsInLog** फ़ील्ड या **guidDenyReadFileVersion** फ़ील्ड का मान बदला जा रहा हो, तो **guidFileVersion** को एक नए GUID में बदला जाना चाहिए।

`nFileVersionGeneration (8 बाइट्स):` एक अहस्ताक्षरित पूर्णांक जो फ़ाइल को बदलने की संख्या को निर्दिष्ट करता है। **guidFileVersion** फ़ील्ड में परिवर्तन होने पर वृद्धि अवश्य की जानी चाहिए।

`guidDenyReadFileVersion (16 बाइट्स):` एक GUID। जब फ़ाइल की मौजूदा सामग्री को बदला जा रहा हो, फ़ाइल की **शीर्षक** संरचना और अप्रयुक्त स्टोरेज ब्लॉक को छोड़कर, **guidDenyReadFileVersion** को एक नए GUID में बदला जाना चाहिए।

`grfDebugLogFlags (4 बाइट्स):` शून्य होना चाहिए। नजरअंदाज किया जाना चाहिए।

`fcrDebugLog (12 बाइट्स):` एक **FileChunkReference64x32** संरचना जिसका मान "fcrZero" होना चाहिए। नजरअंदाज किया जाना चाहिए।

`fcrAllocVerificationFreeChunkList (12 बाइट्स):` एक **FileChunkReference64x32** संरचना जो "fcrZero" होनी चाहिए। नजरअंदाज किया जाना चाहिए।

`bnCreated (4 बाइट्स):` एक अहस्ताक्षरित पूर्णांक जो इस संशोधन स्टोर फ़ाइल को बनाने वाले एप्लिकेशन की बिल्ड संख्या निर्दिष्ट करता है। नजरअंदाज किया जाना चाहिए।

`bnLastWroteToThisFile (4 बाइट्स):' एक अहस्ताक्षरित पूर्णांक जो उस एप्लिकेशन की बिल्ड संख्या को निर्दिष्ट करता है जो इस पुनरीक्षण स्टोर फ़ाइल को अंतिम बार लिखा गया था। नजरअंदाज किया जाना चाहिए।

`bnOldestWritten (4 बाइट्स):' एक अहस्ताक्षरित पूर्णांक जो इस संशोधन स्टोर फ़ाइल को लिखने वाले सबसे पुराने एप्लिकेशन की बिल्ड संख्या निर्दिष्ट करता है। नजरअंदाज किया जाना चाहिए।

`bnNewestWritten (4 बाइट्स):' एक अहस्ताक्षरित पूर्णांक जो इस संशोधन स्टोर फ़ाइल में लिखे गए नवीनतम एप्लिकेशन की बिल्ड संख्या निर्दिष्ट करता है। नजरअंदाज किया जाना चाहिए।

`rgbReserved (728 बाइट्स):` शून्य होना चाहिए। नजरअंदाज किया जाना चाहिए।

## संदर्भ ##

* [[MS-ONESTORE] - OneNote फ़ाइल स्वरूप](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [माइक्रोसॉफ्ट वनोट - विकिपीडिया](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

