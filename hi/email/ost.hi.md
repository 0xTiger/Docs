{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ओएसटी - आउटलुक स्टोरेज फाइल फॉर्मेट",
  "description":"OST फ़ाइल स्वरूप और API के बारे में जानें जो OST फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## OST फाइल क्या है?

OST या ऑफ़लाइन संग्रहण फ़ाइलें Microsoft Outlook का उपयोग करके Exchange सर्वर के साथ पंजीकरण करने पर स्थानीय मशीन पर ऑफ़लाइन मोड में उपयोगकर्ता के मेलबॉक्स डेटा का प्रतिनिधित्व करती हैं। यह सर्वर से कनेक्ट होने पर माइक्रोसॉफ्ट आउटलुक के पहले उपयोग पर स्वचालित रूप से बनाया जाता है। एक बार फ़ाइल बन जाने के बाद, डेटा को ईमेल सर्वर के साथ सिंक्रोनाइज़ किया जाता है ताकि ईमेल सर्वर से डिस्कनेक्ट होने की स्थिति में यह ऑफ़लाइन भी उपलब्ध हो। OST फ़ाइलें उपयोगकर्ता मेलबॉक्स आइटम जैसे ईमेल, संपर्क, कैलेंडर जानकारी, नोट्स, कार्य और अन्य समान डेटा कर सकती हैं। उपयोगकर्ता सर्वर से कनेक्शन के अभाव में भी OST फ़ाइल में ईमेल और अन्य डेटा आइटम बना सकते हैं, लेकिन ये सर्वर के साथ सिंक्रनाइज़ नहीं होंगे। एक बार कनेक्शन स्थापित हो जाने के बाद, स्थानीय फ़ाइल को फिर से सर्वर के साथ सिंक्रनाइज़ किया जाता है ताकि सर्वर और स्थानीय प्रतिलिपि दोनों समान स्तर की जानकारी पर हों।

## ओएसटी फ़ाइल प्रारूप

OST (ऑफलाइन स्टोरेज टेबल) और [PST](/hi/email/pst/) (पर्सनल स्टोरेज टेबल) फाइल फॉर्मेट में पर्सनल फोल्डर फाइल (PFF) फॉर्मेट होता है जो यूजर के ईमेल, कॉन्टैक्ट्स और अपॉइंटमेंट्स को स्टोर करने से मेल खाता है। PFF फ़ाइल में डेटा को सभी तिथियों और समय के साथ छोटे-एंडियन में संग्रहीत किया जाता है, जिसे UTC में FILETIME के रूप में दर्शाया जाता है। [MS-PST] दो प्रकार के PFF को परिभाषित करता है:

* 32-बिट एएनएसआई प्रारूप
* 64-बिट यूनिकोड प्रारूप

PST फ़ाइल स्वरूप [विनिर्देश](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx), जैसा कि Microsoft से उपलब्ध है, OST फ़ाइल स्वरूप पर भी मुफ़्त में लागू होता है और ओपन स्पेसिफिकेशन प्रॉमिस के जरिए अपरिवर्तनीय पेटेंट लाइसेंसिंग। इसमें निम्नलिखित अलग-अलग तत्व होते हैं:

* फ्ले हेडर
* फ़ाइल हेडर डेटा
* सूचकांक शाखा नोड
* इंडेक्स लीफ नोड
* (फ़ाइल) ऑफ़सेट इंडेक्स
* (आइटम) डिस्क्रिप्टर इंडेक्स
* स्थानीय वर्णनकर्ता
* आइटम तालिका प्रकार

### हैडर सूचना

OST फ़ाइल की HEADER संरचना फ़ाइल की शुरुआत में 0 ऑफ़सेट पर स्थित होती है। इसमें OST फ़ाइल के बारे में मेटाडेटा जानकारी और ऊपर वर्णित NDB परत डेटा संरचनाओं तक पहुँचने के लिए ROOT जानकारी शामिल है। OST फ़ाइल स्वरूप के यूनिकोड और ANSI संस्करणों के लिए HEADER संरचना भिन्न है।

हेडर एक 4-बाइट जादुई शब्द **!BDN** से शुरू होता है, जिसे बाइट्स (0x21, 0x42, 0x44, 0x4E) द्वारा दर्शाया जाता है। एक और 2-बाइट्स मैजिक नंबर, **SM** (0x53, 0x4D), फ़ाइल की शुरुआत से ऑफसेट 8 पर स्थित है। संस्करण की जानकारी (एएनएसआई या यूनिकोड) फ़ाइल की शुरुआत से 10 के ऑफसेट पर है। हेक्स मान (0x17) यूनिकोड OST फ़ाइल को निर्दिष्ट करता है जबकि 0x0E या 0x0F ANSI फ़ाइल स्वरूप का प्रतिनिधित्व करता है।

|फ़ील्ड|विवरण
---|---|
|dwMagic (4 बाइट्स)|होना चाहिए "{ 0x21, 0x42, 0x44, 0x4E} ("!BDN")"
|dwCRCPartial (4 बाइट्स)|wMagicClient से शुरू होने वाले डेटा के 471 बाइट्स का 32-बिट CRC मान (0ffset 0x0008)
|wMagicClient (2 बाइट्स)|"{0x53, 0x4D}" होना चाहिए।
|wVer (2 बाइट्स)|फ़ाइल प्रारूप संस्करण। यदि फ़ाइल एक ANSI PST फ़ाइल है, तो यह मान 14 या 15 होना चाहिए, और यदि फ़ाइल एक यूनिकोड PST फ़ाइल है, तो यह मान 23 होना चाहिए।
|wVerClient (2 बाइट्स)|क्लाइंट फ़ाइल स्वरूप संस्करण। इस दस्तावेज़ में वर्णित प्रारूप से संबंधित संस्करण 19 है। इस दस्तावेज़ पर आधारित एक नई पीएसटी फ़ाइल के रचनाकारों को इस मान को 19 तक प्रारंभ करना चाहिए।
|bPlatformCreate (1 बाइट)|यह मान 0x01 पर सेट होना चाहिए।
|bPlatformAccess (1 बाइट)|यह मान 0x01 पर सेट होना चाहिए।
|dwReserved (8 बाइट्स)|
|bidUnused (केवल 8 बाइट्स यूनिकोड)|यूनिकोड PST फ़ाइल स्वरूप बनाए जाने पर अप्रयुक्त पैडिंग जोड़ा गया।
|bidNextP (यूनिकोड: 8 बाइट्स; ANSI: 4 बाइट्स)|अगला पेज BID। पृष्ठों में बिडइंडेक्स मान आवंटित करने के लिए एक विशेष काउंटर होता है। पृष्ठों के लिए बोली के लिए बोली सूचकांक का मूल्य इस काउंटर से आवंटित किया जाता है।
|bidNextB (केवल 4 बाइट्स ANSI): |अगली बोली। यह मान मोनोटोनिक काउंटर है जो इंगित करता है कि अगले आवंटित ब्लॉक के लिए बोली लगाई जानी है। BID मान 4 की वृद्धि में आगे बढ़ते हैं। अधिक विवरण के लिए, खंड 2.2.2.2 देखें।
|dwUnique (4 बाइट्स)|यह एक नीरस रूप से बढ़ता हुआ मान है जिसे हर बार PST फ़ाइल की HEADER संरचना को संशोधित करने पर संशोधित किया जाता है। इस मान का कार्य एक अद्वितीय मान प्रदान करना है, और यह सुनिश्चित करना है कि प्रत्येक शीर्षलेख संशोधन के बाद HEADER CRCs अलग हैं।
|rgnid[] (128 बाइट्स)|32 NID की एक निश्चित सरणी, प्रत्येक 32 संभावित NID_TYPEs (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE) में से एक के अनुरूप है।
|qwअप्रयुक्त (8 बाइट्स)|अप्रयुक्त स्थान; शून्य पर सेट होना चाहिए। केवल यूनिकोड पीएसटी फ़ाइल स्वरूप।
|रूट (यूनिकोड: 72 बाइट्स; एएनएसआई: 40 बाइट्स)|एक रूट संरचना (खंड 2.2.2.5)।
|dwAlign (4 बाइट्स)|अप्रयुक्त संरेखण बाइट्स; शून्य पर सेट होना चाहिए। केवल यूनिकोड पीएसटी फ़ाइल स्वरूप।
|rgbFM (128 बाइट्स)|बहिष्कृत FMap। इसका अब उपयोग नहीं किया जाता है और इसे 0xFF से भरा जाना चाहिए। पाठकों को इन बाइट्स के मूल्य को अनदेखा करना चाहिए।
|rgbFP (128 बाइट्स)|बहिष्कृत FPMap। इसका अब उपयोग नहीं किया जाता है और इसे 0xFF से भरा जाना चाहिए। पाठकों को इन बाइट्स के मूल्य को अनदेखा करना चाहिए।
|bSentinel (1 बाइट)|0x80 पर सेट होना चाहिए।
|bCryptMethod (1 बाइट)|यह दर्शाता है कि PST फ़ाइल में डेटा कैसे एन्कोड किया गया है। पूर्व-निर्धारित मानों में से एक पर सेट होना चाहिए (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC)।
|rgbआरक्षित (2 बाइट्स)| सुरक्षित; शून्य पर सेट होना चाहिए।
|bidNextB (8 बाइट्स)|अगले उपलब्ध BID मान को दर्शाता है। केवल यूनिकोड पीएसटी फ़ाइल स्वरूप।
|bidNextB (केवल यूनिकोड: 8 बाइट्स)|अगली बोली। यह मान मोनोटोनिक काउंटर है जो अगले आवंटित ब्लॉक के लिए बोली लगाने के लिए इंगित करता है। BID मान 4 की वृद्धि में आगे बढ़ते हैं। अधिक विवरण के लिए, खंड 2.2.2.2 देखें।
|dwCRCFपूर्ण (4 बाइट्स)|516 बाइट्स डेटा का 32-बिट CRC मान wMagicClient से लेकर बोलीनेक्स्टबी तक, समावेशी है। केवल यूनिकोड पीएसटी फ़ाइल स्वरूप।
|ullReserved (8 बाइट्स)|आरक्षित; शून्य पर सेट होना चाहिए। केवल एएनएसआई पीएसटी फ़ाइल स्वरूप।
|dwReserved (4 बाइट्स)|आरक्षित; शून्य पर सेट होना चाहिए। केवल एएनएसआई पीएसटी फ़ाइल स्वरूप।
|rgbReserved2 (3 बाइट्स)|
|bआरक्षित (1 बाइट) |
|rgbReserved3 (32 बाइट्स) |

## संदर्भ

* [आउटलुक पर्सनल फोल्डर्स (.ost) फाइल फॉर्मेट](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [व्यक्तिगत फ़ोल्डर फ़ाइल प्रारूप निर्दिष्टीकरण](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)
