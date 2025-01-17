{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - संपीड़ित LIDAR डेटा एक्सचेंज फ़ाइल",
  "description":"LAZ फ़ाइल स्वरूप और API के बारे में जानें जो LAZ फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## LAZ फ़ाइल क्या है?

LAZ फ़ाइल स्वरूप LAS (Lidar LASer) फ़ाइल स्वरूप का एक संपीड़ित संस्करण है, जिसे विशेष रूप से लिडार बिंदु क्लाउड डेटा संग्रहीत करने के लिए डिज़ाइन किया गया है। LAZ फ़ाइलें LAS फ़ाइलों के समान डेटा और संरचना बनाए रखती हैं लेकिन मूल डेटा निष्ठा को संरक्षित करते हुए फ़ाइल आकार को कम करने के लिए दोषरहित संपीड़न तकनीकों का उपयोग करती हैं।

## LAZ फ़ाइल स्वरूप - संक्षिप्त इतिहास

TLAZ फ़ाइल प्रारूप को बड़े लिडार डेटासेट के कुशल भंडारण और ट्रांसमिशन की बढ़ती मांग को पूरा करने के लिए विकसित किया गया था। LAS फ़ाइलों को संपीड़ित करके, LAZ फ़ाइलें अपने आकार को काफी कम कर देती हैं, जिससे उन्हें प्रबंधित करना और स्थानांतरित करना आसान हो जाता है। लिडार बिंदु विशेषताओं को अधिक कॉम्पैक्ट रूप में प्रस्तुत करने के लिए एन्ट्रापी कोडिंग और चर-लंबाई एन्कोडिंग जैसे विभिन्न एल्गोरिदम के संयोजन को नियोजित करके संपीड़न प्राप्त किया जाता है।

## LAZ फ़ाइल स्वरूप

संपीड़न के बावजूद, LAZ फ़ाइलें जानकारी के किसी भी नुकसान के बिना मूल LAS डेटा को पूरी तरह से पुनर्स्थापित करने की क्षमता बरकरार रखती हैं। इसका मतलब यह है कि एक बार जब LAZ फ़ाइल विघटित हो जाती है, तो इसे असम्पीडित LAS फ़ाइल की तरह ही संसाधित और विश्लेषण किया जा सकता है। संपीड़न और डीकंप्रेसन प्रक्रिया आमतौर पर विशेष सॉफ़्टवेयर या लाइब्रेरी का उपयोग करके की जाती है जो LAZ प्रारूप का समर्थन करते हैं।

LAZ फ़ाइल प्रारूप LAS फ़ाइलों के साथ अनुकूलता बनाए रखता है, जिससे लिडार सॉफ़्टवेयर और प्रोसेसिंग टूल में अंतरसंचालनीयता सुनिश्चित होती है। इसका मतलब यह है कि जो एप्लिकेशन LAS फ़ाइलों को पढ़ और संसाधित कर सकते हैं, वे आमतौर पर बिना किसी संशोधन के LAZ फ़ाइलों को संभाल सकते हैं। इसके अतिरिक्त, LAZ फ़ाइलों में अभी भी फ़ाइल हेडर, वेरिएबल लेंथ रिकॉर्ड (VLRs), और पॉइंट डेटा रिकॉर्ड शामिल हैं, जो LAS फ़ाइलों के समान संरचना को संरक्षित करते हैं।

## LAZ फ़ाइल स्वरूप के लाभ

**फ़ाइल का आकार कम होना:** LAZ संपीड़न लिडार डेटासेट के फ़ाइल आकार को काफी कम कर देता है, जिससे उन्हें अधिक प्रबंधनीय और संग्रहीत और स्थानांतरित करना आसान हो जाता है।

**डेटा अखंडता:** एलएजेड संपीड़न दोषरहित है, जिसका अर्थ है कि विघटित डेटा मूल एलएएस डेटा की एक सटीक प्रतिकृति है, जिससे जानकारी या सटीकता का कोई नुकसान नहीं होता है।

**इंटरऑपरेबिलिटी:** LAZ फ़ाइलें LAS फ़ाइलों के साथ संगत हैं, जो मौजूदा लिडार सॉफ़्टवेयर और वर्कफ़्लो के साथ सहज एकीकरण की अनुमति देती हैं।

**कुशल प्रसंस्करण:** उनके कम आकार के कारण, एलएजेड फाइलों को अधिक तेज़ी से लोड और संसाधित किया जा सकता है, जिससे समग्र प्रसंस्करण और विश्लेषण समय में सुधार होता है।

संपीड़ित लिडार डेटा भंडारण और विनिमय के लिए एक मानक के रूप में LAZ फ़ाइल प्रारूप को लिडार समुदाय में व्यापक रूप से अपनाया गया है। यह कुशल डेटा संपीड़न और डेटा अखंडता के बीच संतुलन प्रदान करता है, जो मूल डेटा की सटीकता और गुणवत्ता को बनाए रखते हुए बड़े लिडार डेटासेट को आसानी से संभालने में सक्षम बनाता है।

## संदर्भ

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
