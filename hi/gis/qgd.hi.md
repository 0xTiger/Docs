{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "क्यूजीडी", "क्यूजीआईएस प्रोजेक्ट का स्क्लाइट डेटाबेस", "एक्सटेंशन", "फॉर्मेट", "क्यूजीआईएस", "ऑक्सिलरी डेटाबेस", "क्यूजीडी फाइल क्या है"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - QGIS प्रोजेक्ट का स्क्लाइट डेटाबेस",
  "description":"क्यूजीडी के बारे में जानें जो क्यूजीआईएस प्रोजेक्ट और एपीआई का एक एसक्लाइट डेटाबेस है जो क्यूजीडी फाइलें बना और खोल सकता है।",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## QGD फ़ाइल क्या है?

एक्सटेंशन वाली फ़ाइल .QGD फ़ाइल वास्तव में **QGIS** प्रोजेक्ट का संबद्ध sqlite डेटाबेस है जो प्रोजेक्ट के लिए सहायक डेटा को समायोजित करता है। यदि परियोजना के लिए कोई सहायक डेटा नहीं होगा, तो QGD फ़ाइल खाली रहेगी।

## QGD फ़ाइल स्वरूप के बारे में विवरण

क्लासिक मोड में, सहायक डेटाबेस को xml फ़ाइल के साथ .qgd एक्सटेंशन वाली फ़ाइल के रूप में सहेजा जाता है। **सहायक डेटाबेस** सिस्टम वैकल्पिक तरीके से सिस्टम में डेटा को पढ़ने और लिखने की अनुमति देता है। QGZ बनाते समय जो एक ज़िप्ड कंटेनर है, .qgd फ़ाइल .qgz में शामिल हो जाती है।

## ऑक्जिलरी डेटाबेस क्या है?
सहायक डेटाबेस वास्तव में एक स्टैंडबाय डीबी सिस्टम है जो लक्ष्य डेटाबेस के दोहराव की प्रतिक्रिया के रूप में बनाया गया है। सहायक डेटाबेस वास्तव में एक डुप्लिकेट डेटाबेस का मामला है, वह डेटाबेस होगा जिसे आप डुप्लिकेट कर रहे हैं। उदाहरण के लिए यदि आप डुप्लीकेट डेटाबेस का उपयोग करके एक स्टैंडबाय डेटाबेस सेटअप करते हैं, तो स्रोत डेटाबेस लक्ष्य होगा और स्टैंडबाय डेटाबेस को सहायक के रूप में जाना जाएगा।


## संदर्भ

* [QGZ - QGIS के लिए एक नया डिफ़ॉल्ट प्रोजेक्ट फ़ाइल स्वरूप](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [क्यूजीआईएस फ़ाइल प्रारूप](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)
