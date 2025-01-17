{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "फ़ाइल", "एक्सटेंशन", "प्रारूप", "3D fbx", ""],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"JT फ़ाइल स्वरूप और API के बारे में जानें जो JT फ़ाइलें बना और खोल सकते हैं।",
  "title" :"JT - जुपिटर टेसेलेशन फ़ाइल स्वरूप",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## जेटी फ़ाइल क्या है?

**JT** (बृहस्पति टेसेलेशन) सीमेंस पीएलएम सॉफ्टवेयर द्वारा विकसित एक कुशल, उद्योग-केंद्रित और लचीला आईएसओ-मानकीकृत 3 डी डेटा प्रारूप है। एयरोस्पेस, ऑटोमोटिव उद्योग और भारी उपकरण के मैकेनिकल CAD डोमेन अपने सबसे प्रमुख 3D विज़ुअलाइज़ेशन प्रारूप के रूप में JT का उपयोग करते हैं।

जेटी प्रारूप एक दृश्य ग्राफ है जो सीएडी विशिष्ट विशेषताओं और नोड्स का समर्थन करता है। पहलू डेटा (त्रिकोण) को संग्रहीत करने के लिए परिष्कृत संपीड़न तकनीकों का उपयोग किया जाता है। यह प्रारूप दृश्य विशेषताओं, उत्पाद और निर्माण जानकारी (पीएमआई), और मेटाडेटा का समर्थन करने के लिए संरचित है। सामग्री की अतुल्यकालिक स्ट्रीमिंग के लिए एक अच्छा समर्थन है। भारी यांत्रिक उद्योग में, पेशेवर अपने सीएडी समाधान और उत्पाद जीवनचक्र प्रबंधन (पीएलएम) सॉफ्टवेयर प्रोग्राम में जटिल वस्तुओं की ज्यामिति की जांच करने के लिए जेटी फ़ाइल का उपयोग करते हैं।

जैसा कि JT लगभग सभी महत्वपूर्ण 3D CAD स्वरूपों का समर्थन करता है, इसकी असेंबली विभिन्न संयोजनों से निपट सकती है जिसे "मल्टी-सीएडी" के रूप में जाना जाता है। यह मल्टी-सीएडी असेंबली हमेशा अच्छी तरह से प्रबंधित और अद्यतित होती है क्योंकि देशी सीएडी उत्पाद विवरण फाइलों के बीच उनकी संबंधित जेटी फाइलों के साथ सिंक्रनाइज़ेशन स्वचालित रूप से होता है। JT फाइलें मूल रूप से हल्की होती हैं, इसलिए इसे इंटरनेट सहयोग के लिए उपयुक्त माना जाता है। कंपनियाँ "भारी" मूल CAD फ़ाइलों की तुलना में अधिक आसानी से मीडिया पर 3D विज़ुअलाइज़ेशन भेजकर सहयोग करती हैं। इसके अलावा, JT फ़ाइलें कई सुरक्षा सुविधाएँ सुनिश्चित करती हैं जो बौद्धिक संपदा साझाकरण को अधिक सुरक्षित बनाती हैं।

## JT फ़ाइल स्वरूप का संक्षिप्त इतिहास

इंजीनियरिंग एनिमेशन, इंक. और हेवलेट पैकार्ड जेटी के मूल डिजाइनर थे, जिन्होंने उस प्रारूप को डायरेक्ट मॉडल टूलकिट के रूप में विकसित किया था। UGS Corp. द्वारा EAI के अधिग्रहण के बाद JT UGS के सुइट का हिस्सा बन गया। 2007 की शुरुआत में, यूजीएस ने जेटी को अपने मास्टर 3डी प्रारूप के रूप में घोषित किया। उसी वर्ष, सीमेंस एजी ने यूजीएस खरीदा और सीमेंस पीएलएम सॉफ्टवेयर निकला। सीमेंस JT को सामान्य इंटरऑपरेबिलिटी प्रारूप और डेटा अभिलेखीय प्रारूप के रूप में उपयोग करता है। 2009 में, ISO ने JT विनिर्देश को ISO सार्वजनिक रूप से उपलब्ध विशिष्टता (PAS) के रूप में प्रकाशन के लिए स्वीकार किया। 2010 के मध्य में, ProSTEP iViP ने घोषणा की कि औद्योगिक स्तर पर, JT और STEP AP 242 XML को डेटा में अधिकतम लाभ प्राप्त करने के लिए एक साथ उपयोग किया जा सकता है। विनिमय परिदृश्य। 2012 में, JT को आधिकारिक तौर पर ISO-मानकीकृत (ISO 14306:2012 (ISO JT V1)) 3D विज़ुअलाइज़ेशन प्रारूप के रूप में घोषित किया गया है।

## संयुक्त फ़ाइल प्रारूप ##

JT प्रारूप में सभी वस्तुओं को एक वस्तु पहचानकर्ता के माध्यम से दर्शाया जाता है और वस्तुओं के बीच के संदर्भों को संदर्भित वस्तु के पहचानकर्ता के माध्यम से नियंत्रित किया जाता है। इन ऑब्जेक्ट संदर्भों की अखंडता को पॉइंटर्स अनस्विज़लिंग/स्विज़लिंग के माध्यम से बनाए रखा जा सकता है।

JT फ़ाइल को ब्लॉक की एक श्रृंखला के रूप में व्यवस्थित किया जाता है और हेडर ब्लॉक हमेशा फ़ाइल में डेटा का पहला ब्लॉक होता है। डेटा सेगमेंट की एक श्रृंखला और एक TOC सेगमेंट तुरंत हेडर ब्लॉक का अनुसरण करता है। एक डेटा खंड (6 एलएसजी सेगमेंट) में एक संदर्भ अनुरूप जेटी फ़ाइल हमेशा मौजूद होती है। TOC सेगमेंट में उस फ़ाइल के अन्य सभी डेटा सेगमेंट की स्थान जानकारी होती है।

{{< figure src="../JT-1.png" alt="संयुक्त फ़ाइल प्रारूप" >}}

### फ़ाइल हैडर ###

फ़ाइल हैडर JT फ़ाइल के डेटा पदानुक्रम में पहला ब्लॉक है। संस्करण की जानकारी और टीओसी स्थान की जानकारी हेडर के भीतर संलग्न है जो फ़ाइल पढ़ने में लोडर की सुविधा प्रदान करती है। फ़ाइल हेडर सामग्री को निम्नानुसार व्यवस्थित किया गया है।

### टीओसी खंड ###

TOC सेगमेंट एक फ़ाइल के भीतर मौजूद होना चाहिए और इसमें अन्य सभी डेटा सेगमेंट की पहचान और स्थान की जानकारी होनी चाहिए। TOC सेगमेंट का वास्तविक स्थान फ़ाइल हेडर के TOC ऑफ़सेट फ़ील्ड द्वारा निर्दिष्ट किया जाता है। प्रत्येक व्यक्तिगत रूप से पता करने योग्य डेटा सेगमेंट को TOC सेगमेंट में TOC प्रविष्टि द्वारा दर्शाया जाता है।

### डेटा खंड ###

JT फ़ाइल डेटा सेगमेंट के भीतर सभी संग्रहीत डेटा को परिभाषित करती है। कुछ डेटा सेगमेंट सेगमेंट के भीतर बनी हुई जानकारी के सभी डेटा बाइट्स को कंप्रेस कर सकता है। डेटा सेगमेंट में निम्नलिखित संरचना होती है:

![alt text](../JT-2.png "JT Data Segment")

निम्न तालिका विभिन्न प्रकार के डेटा खंडों का वर्णन करती है:

|नाम|विवरण
---|---|
|LSG खंड| इसमें LSG (निर्देशित चक्रीय ग्राफ संरचना) बनाने के लिए निर्देशित संदर्भों के माध्यम से जुड़ी वस्तुओं का एक संग्रह शामिल है।
|शेप एलओडी खंड|ज्यामितीय आकृतियों के लिए परिभाषित डेटा शामिल है (जैसे कोने, मानक, बहुभुज, आदि)
|JT B-Rep Segment|JT B-Rep फ़ॉर्मेट में एक व्यक्तिगत हिस्से के लिए सटीक ज्यामितीय सीमा का प्रतिनिधित्व करने के लिए डेटा के लिए तत्व होना।
|XT बी-प्रतिनिधि खंड|डेटा के लिए सीमा प्रतिनिधित्व प्रारूप में एक व्यक्तिगत हिस्से के लिए सटीक ज्यामितीय सीमा का प्रतिनिधित्व करने के लिए तत्व होना
|वायरफ्रेम खंड|डेटा किसी विशेष हिस्से के लिए सटीक 3डी वायरफ्रेम का प्रतिनिधित्व करता है, इस खंड में निहित एक तत्व द्वारा परिभाषित किया गया है।
|मेटा डेटा सेगमेंट|मेटाडेटा को अलग-अलग एड्रेसेबल सेगमेंट में स्टोर करने की अनुमति देता है।
|JT ULP खंड|JT ULP प्रारूप में एक व्यक्तिगत हिस्से के लिए अर्ध-सटीक ज्यामितीय सीमा का प्रतिनिधित्व करने के लिए डेटा के लिए तत्व होना।
|JT LWPA खंड|एक विशेष भाग के लिए एक तत्व परिभाषित विश्लेषणात्मक डेटा शामिल है। LWPA विश्लेषणात्मक सतहों के संग्रह को भाग की बी-प्रतिनिधि परिभाषा में संलग्न करता है।

## संपीड़न ##

3D मॉडल की ट्रांसमिशन और स्टोरेज आवश्यकताएं अधिक मांग वाली हैं, इसलिए JT फाइलें संपीड़न का लाभ उठा सकती हैं। एक JT डेटा मॉडल अलग-अलग संपीड़न तकनीक का उपयोग करके विभिन्न फ़ाइलों से बना हो सकता है लेकिन संपीड़न प्रक्रिया JT डेटा उपयोगकर्ता के लिए पारदर्शी होती है।

अब तक, JT ओपन टूलकिट (एक मानक के रूप में) और उन्नत संपीड़न JT फ़ाइलों द्वारा उपयोग की जाने वाली दो संपीड़न तकनीकें हैं। JT ओपन टूलकिट एक आसान, दोषरहित संपीड़न एल्गोरिथ्म का उपयोग करता है, जबकि उन्नत संपीड़न एक अधिक परिष्कृत, डोमेन-विशिष्ट संपीड़न तकनीक को नियोजित करता है जिससे हानिपूर्ण ज्यामिति संपीड़न होता है। क्लाइंट एप्लिकेशन मानक संपीड़न का उपयोग करने के बजाय उन्नत संपीड़न पसंद करते हैं, क्योंकि उन्नत संपीड़न काफी उच्च संपीड़न अनुपात उत्पन्न करता है। सामान्य JT फ़ाइल देखने के अनुप्रयोगों के साथ पश्चगामी संगतता मानक संपीड़न के प्रावधान के माध्यम से बनाए रखी जाती है। संपीड़न प्रपत्र JT फ़ाइल स्वरूप संस्करण के साथ संगत होना चाहिए जिसे तब देखा जा सकता है जब कोई JT फ़ाइल पाठ संपादक का उपयोग करके खुलती है और ASCII शीर्षलेख जानकारी के भीतर संलग्न होती है।

## संदर्भ ##

* [जेटी फ़ाइल प्रारूप संदर्भ](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [जेटी (विज़ुअलाइज़ेशन प्रारूप)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

