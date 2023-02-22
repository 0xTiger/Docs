{
  "date" : "2021-04-21",
  "keywords" :[ "मटर फ़ाइल", "मटर फ़ाइल स्वरूप", "मटर फ़ाइल क्या है", "फ़ाइल", "मटर उदाहरण", "मटर फ़ाइल एक्सटेंशन", "विस्तार", "प्रारूप"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - PeaZip पुरालेख फ़ाइल स्वरूप",
  "description":"PEA फ़ाइल स्वरूप और API के बारे में जानें जो PEA फ़ाइलें बना और खोल सकता है।",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## पीईए फाइल क्या है?

.pea एक्सटेंशन वाली फ़ाइल, पैक, एनक्रिप्ट, और ऑथेंटिकेट के लिए संक्षिप्त रूप, एक [ज़िप](/hi/compression/zip/) आर्काइव है जिसे [PeaZip](https://peazip.github.io/) आर्काइविंग सॉफ़्टवेयर एप्लिकेशन के साथ बनाया गया है। इसमें कम्प्रेशन और मल्टीपल वॉल्यूम आउटपुट की सुविधा है, और ऑथेंटिकेटेड एन्क्रिप्शन और क्रिप्टोग्राफी के माध्यम से एक लचीला सुरक्षा मॉडल प्रदान करता है। यह डेटा की गोपनीयता और प्रमाणीकरण दोनों प्रदान करता है। PeaZip उपयोगिता ओपन-सोर्स इंजन के रूप में उपलब्ध है जिसे आवश्यकता के अनुसार विभिन्न OS के लिए संकलित किया जा सकता है।

## पीईए फ़ाइल प्रारूप

[पीईए फ़ाइल प्रारूप विनिर्देश](https://peazip.github.io/pea_help.pdf) डेवलपर के संदर्भ के लिए सार्वजनिक रूप से उपलब्ध हैं। पीईए अभिलेखागार लचीली सुरक्षा मॉडल वाली बाइनरी फाइलें हैं और चेकसम से लेकर क्रिप्टोग्राफिक रूप से मजबूत हैश तक की अनावश्यक अखंडता जांच। यह नियंत्रित करने के लिए संचार के तीन अलग-अलग स्तरों को परिभाषित करता है:

* स्ट्रीम - वास्तविक आउटपुट डेटा स्ट्रीम जो कई इनपुट फ़ाइलों द्वारा बनाई जाती है और जिसे कई आउटपुट वॉल्यूम में लिखा जा सकता है
* ऑब्जेक्ट - .pea संग्रह को भेजी गई इनपुट फ़ाइलें और फ़ोल्डर
* वॉल्यूम - आउटपुट संग्रह फ़ाइल जिसे उपयोगकर्ता परिभाषित आकार में फैलाया जा सकता है

इनमें से हर एक वैकल्पिक है और इसे उपयोगकर्ता की आवश्यकताओं के अनुसार शामिल किया जा सकता है। पीईए फ़ाइल प्रारूप असीमित वस्तुओं वाली एकल स्ट्रीम को स्टोर कर सकता है। प्रत्येक स्ट्रीम आकार में 2^64 बाइट तक है।

पीईए फाइलें ईएक्स या एचएमएसी मोड में एईएस का उपयोग करके वैकल्पिक अखंडता जांच और प्रमाणित एन्क्रिप्शन प्रदान करती हैं, वैकल्पिक रूप से ईएक्स मोड में ट्वोफिश और सर्पेंट।

### पीईए आर्काइव हैडर

संग्रह शीर्षलेख 10 बाइट्स है और निम्नानुसार संरचित है।

|बाइट्स|विवरण|
---|---|
|1 | फ़ाइल प्रारूप के लिए मैजिक बाइट फ़ील्ड: $EA|
|1 | संस्करण संख्या|
|1 | संशोधन संख्या|
|1 | वॉल्यूम नियंत्रण योजना|
|1 | ओएस घोषित करना जहां स्ट्रीम बनाया गया था|
|1 | OS दिनांक और समय एन्कोडिंग घोषित करना|
|1 | ऑब्जेक्ट का नाम कैरेक्टर एन्कोडिंग घोषित करना|
|1 | सीपीयू प्रकार (7 बिट में एन्कोडेड) और एंडियननेस (एमएसबी में) घोषित करना |
|1 | भविष्य के उपयोग के लिए सुरक्षित|

## संदर्भ

* [पीईए फ़ाइल प्रारूप निर्दिष्टीकरण](https://peazip.github.io/pea_help.pdf)
* [पीईए फ़ाइल प्रारूप](https://peazip.github.io/pea-file-format.html#.pea_specifications)
