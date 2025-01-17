{
  "date" : "2019-12-16",
  "keywords" :["एक्सएलएस", "फाइल", "एक्सटेंशन", "फाइल फॉर्मेट", "एक्सेल", "स्प्रेडशीट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"आपका फ़ाइल स्वरूप गाइड यह जानने के लिए कि एक XLS फ़ाइल और API क्या है जो उन्हें बना और खोल सकता है।",
  "title" :"XLS फ़ाइल स्वरूप क्या है? फ़ाइल स्वरूप विशेषज्ञों से सीखें!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## एक्सएलएस फाइल क्या है?

एक्सएलएस एक्सटेंशन वाली फाइलें एक्सेल बाइनरी फाइल फॉर्मेट का प्रतिनिधित्व करती हैं। ऐसी फ़ाइलें Microsoft Excel के साथ-साथ अन्य समान स्प्रेडशीट प्रोग्राम जैसे OpenOffice Calc या Apple Numbers द्वारा बनाई जा सकती हैं। एक्सेल द्वारा सहेजी गई फ़ाइल को वर्कबुक के रूप में जाना जाता है जहाँ प्रत्येक वर्कबुक में एक या अधिक वर्कशीट हो सकती हैं। डेटा वर्कशीट में तालिका प्रारूप में उपयोगकर्ताओं को संग्रहीत और प्रदर्शित किया जाता है और संख्यात्मक मान, पाठ डेटा, सूत्र, बाहरी डेटा कनेक्शन, चित्र और चार्ट को फैला सकता है। Microsoft Excel जैसे एप्लिकेशन आपको कार्यपुस्तिका डेटा को [PDF](/hi/pdf/), [CSV](/hi/spreadsheet/csv/), [XLSX](/hi/spreadsheet/xlsx/), [TXT](/hi/word-processing/txt/) सहित कई अलग-अलग स्वरूपों में निर्यात करने देता है, [HTML](/hi/web/html/), [XPS](/hi/page-description-language/xps/), और कई अन्य। XLS फ़ाइल स्वरूप को Microsoft Excel 2007 के रिलीज़ के साथ एक अधिक खुले और संरचित प्रारूप, XLSX के साथ बदल दिया गया था। नवीनतम संस्करण अभी भी XLS फ़ाइलों को बनाने और पढ़ने के लिए समर्थन प्रदान करते हैं, हालाँकि XLSX अब उपयोग की पहली पसंद है।

## संक्षिप्त इतिहास

XLS Microsoft द्वारा Microsoft Excel के साथ उपयोग के लिए बनाया गया था और इसे बाइनरी इंटरचेंज फ़ाइल स्वरूप (BIFF) के रूप में भी जाना जाता है। इस फ़ाइल प्रकार को पहली बार 1987 में विंडोज के लिए एक्सेल का हिस्सा बनाकर पेश किया गया था। XLS फ़ाइल प्रारूप विनिर्देशों को पहली बार जून 2008 में संशोधन 1 के रूप में सार्वजनिक किया गया था। उसके बाद, विनिर्देशों को लगातार अपडेट किया गया और नवीनतम संशोधन उपलब्ध थे। अगस्त 2018 तक है जिसे संशोधन 8.0 के रूप में चिह्नित किया गया है। XLS फ़ाइल स्वरूप के विभिन्न संस्करणों का संक्षिप्त इतिहास इस प्रकार है:

* संस्करण 7.0 (कार्यालय 95 के साथ जारी): एक्सेल का यह संस्करण सभी संस्करणों में सबसे मजबूत और तेज था और आंतरिक स्ट्रीम रीराइट्स को 32 बिट्स में अपडेट किया गया था।
* संस्करण 8 (कार्यालय 97 के साथ जारी): VBA को एक मानक भाषा के रूप में पेश किया गया था और पहली बार इस संस्करण में हटाए गए प्राकृतिक भाषा लेबल शामिल किए गए थे। इसने पहली बार एक पेपर क्लिप ऑफिस असिस्टेंट भी पेश किया।
* संस्करण 9 (कार्यालय 2000 के साथ जारी): संस्करण 9 में केवल मामूली बदलाव थे जहां पेपर क्लिप कार्यालय सहायक एक साथ कई वस्तुओं को रख सकता था जो पहले संभव नहीं थे।
* संस्करण 10 (कार्यालय XP के साथ जारी): इस संस्करण में कोई ध्यान देने योग्य सुधार नहीं था।
* संस्करण 11 (कार्यालय 2003 के साथ जारी): संस्करण 11 में प्रमुख अद्यतन, एक्सेल 2003 नई तालिकाओं का परिचय था।

## XLS फ़ाइल स्वरूप निर्दिष्टीकरण ##

[MS-CFB] में वर्णित एक मिश्रित फ़ाइल के रूप में डेटा को XLS फ़ाइल में बाइनरी स्ट्रीम के रूप में व्यवस्थित किया गया है। डेटा को कंपाउंड फ़ाइल में स्टोरेज, स्ट्रीम और सबस्ट्रीम का उपयोग करके संग्रहीत किया जाता है जिसमें कार्यपुस्तिका की सामग्री और संरचना के बारे में जानकारी होती है, जिसमें कार्यपुस्तिका डेटा जैसे कार्यपत्रक परिभाषाएँ शामिल होती हैं। प्रत्येक स्ट्रीम या सबस्ट्रीम में बाइनरी रिकॉर्ड की एक श्रृंखला होती है। प्रत्येक बाइनरी रिकॉर्ड में शून्य या अधिक संरचित फ़ील्ड होते हैं जिनमें कार्यपुस्तिका डेटा होता है। यह खंड XLS फ़ाइल संरचना का एक संक्षिप्त अवलोकन देता है, लेकिन विस्तृत फ़ाइल प्रारूप विनिर्देशों के लिए, किसी को [XLS फ़ाइल निर्माण विनिर्देश](https://msdn.microsoft.com/en-us/library/cc313154(v#office) से परामर्श करना चाहिए .12).aspx) Microsoft द्वारा दस्तावेज़।

#### स्ट्रीम और सबस्ट्रीम ####

कार्यपुस्तिका स्ट्रीम द्वारा कार्यपुस्तिका का प्रतिनिधित्व किया जाता है। कार्यपुस्तिका में प्रत्येक कार्यपत्रक को सबस्ट्रीम द्वारा दर्शाया जाता है। इसके अलावा, इसमें चार्ट शीट सबस्ट्रीम, मैक्रो शीट सबस्ट्रीम या डायलॉग शीट सबस्ट्रीम है जो ग्लोबल सबस्ट्रीम का अनुसरण करता है। कार्यपुस्तिका डेटा वाली प्रत्येक बाइनरी स्ट्रीम या सबस्ट्रीम को बाइनरी रिकॉर्ड की एक श्रृंखला के रूप में लिखा जाना चाहिए।

#### अभिलेख ####

कार्यपुस्तिका में सुविधाओं के बारे में जानकारी एक रिकॉर्ड के रूप में संग्रहीत की जाती है जो बाइट्स की एक चर-लंबाई अनुक्रम है। एक बाइनरी रिकॉर्ड में निम्नलिखित तीन घटक होते हैं:

**रिकॉर्ड प्रकार:** रिकॉर्ड प्रकार एक दो-बाइट अहस्ताक्षरित पूर्णांक है जो निर्दिष्ट करता है कि रिकॉर्ड द्वारा किस प्रकार की जानकारी निर्दिष्ट की गई है और इस रिकॉर्ड के लिए विशिष्ट रिकॉर्ड डेटा की संरचना कैसे क्रमबद्ध और संरचित है। रिकॉर्ड प्रकार के मान रिकॉर्ड गणना (सेक्शन 2.3) से एक मान होना चाहिए या रिकॉर्ड को भविष्य के रिकॉर्ड आर्किटेक्चर (सेक्शन 2.1.6) का उपयोग करना चाहिए।

**रिकॉर्ड आकार**: रिकॉर्ड आकार एक दो-बाइट अहस्ताक्षरित पूर्णांक है जो बाइट्स की संख्या निर्दिष्ट करता है जो रिकॉर्ड डेटा के कुल आकार को निर्दिष्ट करता है। रिकॉर्ड का आकार 0 से अधिक या उसके बराबर होना चाहिए और 8224 से कम या उसके बराबर होना चाहिए।

**रिकॉर्ड डेटा:** रिकॉर्ड डेटा घटक में ऐसे फ़ील्ड होते हैं जो एक विशेष रिकॉर्ड प्रकार के अनुरूप होते हैं और रिकॉर्ड के शेष भाग को शामिल करते हैं। किसी दिए गए रिकॉर्ड प्रकार के लिए फ़ील्ड का क्रम और संरचना उस रिकॉर्ड प्रकार के संबंधित अनुभाग में निर्दिष्ट हैं। रिकॉर्ड डेटा घटक का आकार रिकॉर्ड आकार के बराबर होना चाहिए। रिकॉर्ड डेटा घटक में फ़ील्ड्स में साधारण मान, मानों की सरणियाँ, कई फ़ील्ड्स की संरचनाएँ, फ़ील्ड्स की सरणियाँ और संरचनाओं की सरणियाँ हो सकती हैं।

#### सेल तालिका ####

कक्ष कार्यपुस्तिका के मूलभूत ब्लॉक हैं जो कार्यपुस्तिका की सामग्री जैसे पाठ, सूत्र और संख्यात्मक डेटा को संग्रहीत करते हैं। सेल सेल टेबल नामक डेटा संरचना के माध्यम से संग्रहीत डेटा का रिकॉर्ड बनाए रखते हैं। सेल तालिका स्वयं रिकॉर्ड के अनुक्रम में संग्रहीत होती है जो विनिर्देश दस्तावेज़ में परिभाषित सेलटेबल नियमों के अनुरूप होती है। इसमें पंक्ति ब्लॉकों की एक श्रृंखला होती है जहाँ पंक्तियों को पंक्ति ब्लॉकों में व्यवस्थित किया जाता है। प्रत्येक पंक्ति ब्लॉक में डेटा वाली पहली पंक्ति से डेटा वाली अंतिम पंक्ति तक पंक्तियाँ होती हैं।

प्रत्येक पंक्ति ब्लॉक के लिए पंक्ति रिकॉर्ड में डेटा या पंक्ति स्वरूपण सहेजा जाता है। प्रत्येक सेल जिसमें डेटा या अलग-अलग सेल फ़ॉर्मेटिंग शामिल है, एक रिकॉर्ड द्वारा दर्शाया जाता है। सेल से संबद्ध फ़ॉर्मेटिंग को अलग-अलग सेल फ़ॉर्मेटिंग, पंक्ति फ़ॉर्मेटिंग, कॉलम फ़ॉर्मेटिंग या डिफ़ॉल्ट सेल फ़ॉर्मेट से प्राप्त किया जा सकता है। फ़ॉर्मेटिंग के लिए प्राथमिकता का क्रम सर्वोच्च वरीयता के साथ व्यक्तिगत सेल फ़ॉर्मेटिंग है, उसके बाद पंक्ति फ़ॉर्मेटिंग, और फिर कॉलम फ़ॉर्मेटिंग, और फिर डिफ़ॉल्ट सेल फ़ॉर्मेट। जिन कक्षों में डेटा नहीं होता है और जिनमें व्यक्तिगत स्वरूपण नहीं होता है, वे सहेजे नहीं जाते हैं।

#### सूत्र ####

एक सूत्र एक सेल में मूल्यों, सेल संदर्भों, नामों, कार्यों या ऑपरेटरों का एक क्रम है जो एक साथ एक नया मान उत्पन्न करते हैं। फ़ार्मुलों को "पार्स किए गए भाव" के रूप में जाने जाने वाले टोकन प्रतिनिधित्व में संग्रहीत किया जाता है। प्रदर्शन और उपयोगकर्ता संपादन के लिए रनटाइम पर एक पार्स की गई अभिव्यक्ति को पाठ्य सूत्र में बदल दिया जाता है। सेल फ़ार्मुलों को फ़ॉर्मूला रिकॉर्ड द्वारा निर्दिष्ट किया जाता है। सरणी सूत्र सरणी रिकॉर्ड द्वारा निर्दिष्ट किए जाते हैं। साझा सूत्र ShrFmla रिकॉर्ड द्वारा निर्दिष्ट किए गए हैं।

#### चार्ट ####

चार्ट शीट एक चार्ट निर्दिष्ट करती है, एक ग्राफिक जो डेटा या डेटा के सेट के बीच संबंधों को दृश्य रूप में प्रदर्शित करता है, और एक चार्ट डेटा कैश, चार्ट डेटा में उपयोग किए जाने वाले डेटा की एक स्थानीय प्रति गायब है या यदि बाहरी से लिंक है डेटा स्रोत टूट गए हैं। चार्ट एक या दो-अक्ष समूहों को निर्दिष्ट करता है, अक्षों का एक सेट जिसके विरुद्ध चार्ट डेटा प्लॉट किया जाता है, और चार्ट में निर्दिष्ट श्रृंखला, ट्रेंडलाइन और त्रुटि बार का सेट। प्रत्येक अक्ष समूह एक से चार चार्ट समूहों को निर्दिष्ट करता है जो डेटा प्रदर्शित करने के लिए उपयोग किए जाने वाले विज़ुअलाइज़ेशन के प्रकार को निर्दिष्ट करते हैं। प्रत्येक श्रृंखला, ट्रेंडलाइन और त्रुटि बार एक चार्ट समूह निर्दिष्ट करता है जिससे यह जुड़ा हुआ है।

#### मेटाडेटा ####

मेटाडेटा किसी विशेष सेल या उसकी सामग्री से जुड़ा अतिरिक्त डेटा है। मेटाडेटा BIFF8 में केवल भविष्य के एक्स्टेंसिबिलिटी उद्देश्यों के लिए दर्ज किया गया है।

#### पिवट तालिकाएं ####

PivotTable उस डेटा के वितरण का अवलोकन प्राप्त करने के लिए स्रोत डेटा को सारांशित करने के लिए एक तंत्र है। PivotTable में, स्रोत डेटा के लागू होने वाले कॉलम फ़ील्ड बन जाते हैं जिनका उपयोग डेटा को सारांशित करने के लिए किया जा सकता है। जब PivotTable का स्रोत डेटा OLAP स्रोत डेटा होता है, तो OLAP पदानुक्रम और कुछ अन्य OLAP निकाय PivotTable में फ़ील्ड बन जाते हैं।
PivotTable के दो प्रमुख भाग होते हैं, PivotCache और PivotTable दृश्य। एकल गैर-OLAP PivotCache के आधार पर एकाधिक PivotTable दृश्य हो सकते हैं।

#### शैलियाँ ####

यह अवलोकन वर्णन करता है कि किसी शीट (1) में सेल के लिए फ़ॉर्मेटिंग और सुरक्षा जानकारी कैसे निर्दिष्ट की जाती है। सेल स्वरूपण गुणों के कई सेटों से बना है:

* फ़ॉन्ट गुण (बोल्ड, इटैलिक, फ़ॉन्ट रंग, फ़ॉन्ट आकार, आदि...)
* गुण भरें (अग्रभूमि रंग, पृष्ठभूमि रंग, पैटर्न, ढाल, आदि ...)
* संरेखण गुण (बाएं, केंद्र, सही संरेखण, आदि...)
* सीमा गुण (बाएं, दाएं, ऊपर, नीचे, मोटा या पतला, रंग, आदि...)
* संख्या स्वरूपण गुण (दिनांक, समय, दशमलव स्थानों की संख्या, आदि...)
* संरक्षण गुण (बंद, छिपा हुआ, आदि…)

समग्र रूप से ये गुण वर्णन करते हैं कि किसी विशेष सेल को कैसे प्रदर्शित और मुद्रित किया जाता है।

## संदर्भ ##

* [[एमएस-एक्सएलएस] - एक्सेल बाइनरी फ़ाइल स्वरूप संरचना](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[एमएस-सीएफबी] - कंपाउंड फाइल बाइनरी फाइल फॉर्मेट](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

