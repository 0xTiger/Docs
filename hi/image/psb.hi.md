{
  "date" : "2019-10-11",
  "keywords" :["पीएसबी फाइल", "पीएसबी फाइल फॉर्मेट", "पीएसबी फाइल क्या है", "फाइल", "पीएसबी उदाहरण", "पीएसबी फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - फोटोशॉप बिग इमेज फाइल फॉर्मेट",
  "description":"पीएसबी फ़ाइल प्रारूप और एपीआई के बारे में जानें जो पीएसबी फाइलें बना और खोल सकते हैं।",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## पीएसबी फाइल क्या है?
Adobe Photoshop फ़ाइलों को दो स्वरूपों में सहेजता है। 30,000 गुणा 30,000 पिक्सेल आकार वाली फ़ाइलें PSD एक्सटेंशन के साथ सहेजी जाती हैं और 300,000 गुणा 300,000 पिक्सेल तक PSD से बड़ी फ़ाइलें PSB एक्सटेंशन के साथ सहेजी जाती हैं जिन्हें "फ़ोटोशॉप बिग" कहा जाता है। अधिक विशेष रूप से, पीएसबी फाइलें 4 ईबी (4.2 अरब जीबी से अधिक) जितनी बड़ी हो सकती हैं, जिनकी छवियों की ऊंचाई और चौड़ाई 300,000 पिक्सेल तक होती है। दूसरी ओर, PSD अधिकतम 2 जीबी तक और 30,000 पिक्सेल के छवि आयाम हो सकते हैं।

PSB को फोटोशॉप के लिए बड़े प्रारूप आकार के रूप में भी जाना जाता है और यह परतों, प्रभावों और फिल्टर जैसी सभी फोटोशॉप सुविधाओं का समर्थन करता है। फोटोशॉप PSB फाइल को [PSD](/hi/image/psd/), [JPG](/hi/image/jpeg/) में बदल सकता है। , [PNG](/hi/image/png/), [EPS](/hi/page-description-language/eps/), [GIF](/hi/image/gif/) और अन्य प्रारूप भी। फोटोशॉप की वरीयताएँ संवाद बॉक्स के फ़ाइल प्रबंधन फलक की सुविधा सक्षम होने के बाद फ़ोटोशॉप बड़ा दस्तावेज़ प्रारूप उपलब्ध है।

## फ़ाइल स्वरूप जानकारी ##

फोटोशॉप फ़ाइल स्वरूप को पाँच प्रमुख भागों में विभाजित किया गया है, जिसमें कई लंबाई के मार्कर हैं जो खंडों के बीच चलते हैं।

|फ़ाइल स्वरूप
---|
| फाइल हैडर
| कलर मोड डेटा
| छवि संसाधन
|लेयर और मास्क की जानकारी
|((((
छवि डेटा
)))

### फाइल हैडर ###

फ़ाइल हेडर की लंबाई 26 बाइट्स होती है और इसमें छवि के मूल गुण होते हैं।

BYTE सिग्नेचर [4] - '8BPS' के बराबर है।

वर्ड वर्जन [2] - वर्जन नंबर, पीएसडी # 1, पीएसबी # 2।

बाइट आरक्षित [6] - आरक्षित और हमेशा शून्य।

वर्ड चैनल [2] - अल्फा चैनल सहित छवि में रंगीन चैनलों की संख्या। इसका मान 1 से 56 तक होता है।

लंबी पंक्तियां [4] - पिक्सेल में इमेज की ऊंचाई, PSD 1-30,000, PSB 1-300,000।

लंबे कॉलम [4] - पिक्सेल में इमेज की चौड़ाई, PSD 1-30,000, PSB 1-300,000।

शब्द गहराई [2] - प्रति चैनल बिट्स की संख्या। समर्थित मान 1,8,16 और 32 हैं।

वर्ड मोड [2] - फाइल का कलर मोड।

#### मोड विवरण ####


|मोड|विवरण
---|---|
|0|बिटमैप (मोनोक्रोम)
|1|ग्रे-स्केल
|2|अनुक्रमित
|3|आरजीबी
|4|सीएमवाईके
|7|मल्टीचैनल
|8|डुओटोन (हाफ़टोन)
|9|लैब

### कलर मोड डेटा ###

फाइल हेडर सेक्शन के बाद कलर मोड डेटा सेक्शन आता है। ब्लॉक एक लंबी संख्या से शुरू होता है जो बाइट्स में ब्लॉक की लंबाई देता है। रंग मोड डेटा की संरचना इस प्रकार है:

4 बाइट्स - निम्नलिखित रंग डेटा की लंबाई।

चर - रंग डेटा

यदि हेडर सेक्शन में मोड फ़ील्ड मान अनुक्रमित रंग या डुओटोन नहीं है, तो ब्लॉक की लंबाई 0 होगी और लंबाई फ़ील्ड के बाद कोई डेटा नहीं होगा।

अनुक्रमित रंग छवियों के लिए, लंबाई 768 बाइट्स होगी जिसमें 256 रंग पैलेट शामिल होंगे। डुओटोन के लिए, डेटा में स्क्रीन पैरामीटर और अन्य संबंधित जानकारी शामिल होगी।

### छवि संसाधन ###

कलर मोड डेटा सेक्शन के बाद, तीसरा ब्लॉक इमेज रिसोर्स सेक्शन है। पहले चार बाइट एक लंबी संख्या है जो ब्लॉक की लंबाई निर्दिष्ट करती है जिसके बाद संसाधन ब्लॉक की एक श्रृंखला होती है। छवि संसाधन ब्लॉक की संरचना इस प्रकार है:

बाइट प्रकार [4] - हस्ताक्षर '8बीआईएम'

वर्ड आईडी [2] - इमेज रिसोर्स आईडी। संसाधन आईडी की एक सूची है जिसे संदर्भ लिंक से देखा जा सकता है।

बाइट नाम [परिवर्तनीय] - नाम: पास्कल स्ट्रिंग समान लंबाई के साथ। ** **

लंबा आकार [4] - संसाधन डेटा का वास्तविक आकार जो बाद में आता है।

बाइट डेटा [वैरिएबल} - संसाधन डेटा। यह समान आकार बनाने के लिए गद्देदार है।

कुछ संसाधन प्रारूपों को संक्षेप में नीचे समझाया गया है:

**ग्रिड और गाइड्स रिसोर्स फॉर्मेट:** ग्रिड और गाइड्स की जानकारी रिसोर्स ब्लॉक में स्टोर की जाती है। इन संसाधन ब्लॉकों में 16 बाइट ग्रिड और गाइड हेडर होते हैं, जिसके बाद गाइड जानकारी के 5 बाइट ब्लॉक होते हैं।

**थंबनेल संसाधन प्रारूप:** थंबनेल जानकारी पूर्वावलोकन प्रदर्शन के लिए छवि संसाधन ब्लॉक में संग्रहीत की जाती है जिसमें आरजीबी में 28 बाइट हेडर और JFIF थंबनेल होते हैं।

**कलर सैंपलर्स रिसोर्स फॉर्मेट:** कलर सैंपलर्स की जानकारी इमेज रिसोर्स ब्लॉक में 8 बाइट हेडर के साथ कलर सैंपलर्स की जानकारी के वेरिएबल लेंथ ब्लॉक के साथ स्टोर की जाती है।

### परत और मुखौटा जानकारी ###

चौथा ब्लॉक परत और मुखौटा सूचना ब्लॉक है और इसमें परतों और मास्क के बारे में जानकारी शामिल है। परत की जानकारी पहले संग्रहित की जाती है और फिर जानकारी को छिपाया जाता है।

**परत जानकारी:** परत जानकारी एक लंबे मान से शुरू होती है जो परत जानकारी की लंबाई दर्शाती है। उसके बाद WORD वैल्यू काउंट है जो लेयर रिकॉर्ड्स की संख्या को फॉलो करने के लिए दिखाता है।

[8] - परतों की लंबाई

[2] - लेयर काउंट

[चर] - प्रत्येक परत के बारे में जानकारी।

[वैरिएबल] - चैनल छवि डेटा। ** **

**मुखौटा जानकारी:** मुखौटा संरचना में निम्न प्रारूप है:


|डेटा संरचना|क्षेत्र का नाम| विवरण
---|---|---|
|शब्द| ओवरले कलर स्पेस | (प्रलेखित नहीं)
|बाइट[8]| रंग घटक| 4x2 बाइट रंग घटक
|शब्द| अस्पष्टता| 0#पारदर्शी, 1#अपारदर्शी
|बाइट| मेहरबान| 0#उलटा, 1#संरक्षित, 128#संग्रहित मूल्य का उपयोग करें
|बाइट| पैडिंग| शून्य पर सेट करें

### छवि डेटा ###

अंतिम खंड में छवि पिक्सेल डेटा होता है। छवि डेटा को विमानों में अनुक्रम की एक श्रृंखला के रूप में संग्रहीत किया जाता है अर्थात पहले सभी लाल डेटा, फिर सभी हरे डेटा आदि। प्रत्येक पंक्ति के प्रारंभ में WORD प्रत्येक स्कैन लाइन से संबंधित बाइट्स में आकार दिखाता है।

[2] - संपीड़न विधि:

[वैरिएबल] - प्लानर ऑर्डर यानी RRRR, GGGG, BBBB आदि में इमेज डेटा।

संपीड़न के तरीके:

0 – Raw छवि डेटा

1 - आरएलई संपीड़ित

2 - भविष्यवाणी के बिना जिप

3 - भविष्यवाणी के साथ ज़िप करें

## संदर्भ ##

* [पीएसबी फ़ाइल प्रारूप - एडोब द्वारा] (https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [पीएसबी - विकिपीडिया] (https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)
