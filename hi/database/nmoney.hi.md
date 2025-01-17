{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NMONEY फ़ाइल स्वरूप और API के बारे में जानें जो NMONEY फ़ाइलें बना और खोल सकते हैं।",
  "title" :"NMONEY फ़ाइल - डेनारो खाता फ़ाइल स्वरूप",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## NMONEY फ़ाइल क्या है?

NMONEY फ़ाइल एक वित्तीय डेटा भंडारण डेटाबेस फ़ाइल है जिसमें वित्तीय लेनदेन का ट्रैक रिकॉर्ड होता है। इसे Nickvision द्वारा विकसित किया गया था और इसका उपयोग Nickvision Denaro सॉफ़्टवेयर में किया गया था जो एक व्यक्तिगत वित्तीय सॉफ़्टवेयर एप्लिकेशन है। NOMONEY फ़ाइल के अंदर संग्रहीत डेटा में किसी खाते के क्रेडिट और डेबिट लेनदेन की जानकारी शामिल होती है।

NOMONEY फ़ाइलें [Github](https://github.com/NickvisionApps/Denaro) एप्लिकेशन से खोली जा सकती हैं।

## डेनारो सॉफ्टवेयर के बारे में

डेनारो को शुरुआत में [निकविज़न](https://nickvision.org/) द्वारा एक उत्पाद के रूप में विकसित किया गया था जिसे बाद में [Github](https://github.com/NickvisionApps/Denaro) पर होस्ट किए गए एक ओपन-सोर्स सॉफ़्टवेयर ऐप में बदल दिया गया था। . तब से ऐप को केवल Github पर संशोधित और अपडेट किया गया है। ऐप को विंडोज़ ऐप एसडीके (इस समय विनयूआई 3) के साथ विंडोज़ यूआई में सी# में विकसित किया गया है।

### डेनारो द्वारा प्रस्तुत सुविधाएँ

* इसके सबसे लोकप्रिय और परिचित टैब इंटरफ़ेस के साथ एक साथ कई खाते प्रबंधित करें
* लेनदेन को प्रकार, समूह या तिथि के अनुसार फ़िल्टर करें
* हर महीने होने वाले बिल जैसे लेन-देन को दोहराएँ
* एक खाते से दूसरे खाते में पैसे ट्रांसफर करें
* किसी खाते से डेटा को CSV फ़ाइल के रूप में निर्यात करें और किसी खाते में लेनदेन जोड़ने के लिए CSV, OFX या QIF फ़ाइल आयात करें

## डेनारो फ़ाइल स्वरूप - अधिक जानकारी

डेनारो फ़ाइलें बाइनरी फ़ाइल स्वरूप में डिस्क में सहेजी जाती हैं। वित्तीय डेटा को **.SQLITE3** फ़ाइल स्वरूप में डेटाबेस फ़ाइल के रूप में संग्रहीत किया जाता है। SQLITE एक हल्की SQL डेटाबेस फ़ाइल है जो SQLite सॉफ़्टवेयर के साथ बनाई गई है। यह स्व-निहित डेटाबेस इंजन प्रदान करता है जो पूरी तरह से विशेषीकृत और अत्यधिक विश्वसनीय डेटाबेस प्रदान करने में सक्षम है। SQLite डेटाबेस फ़ाइलों का उपयोग केवल नेटवर्क पर इन फ़ाइलों का आदान-प्रदान करके सिस्टम के बीच समृद्ध सामग्री साझा करने के लिए किया जा सकता है। C, [C#](/hi/programming/cs/), [C++](/hi/programming/cpp/), [Java](/hi/programming/java/), [PHP](/hi/programming/) जैसी प्रोग्रामिंग भाषाओं के लिए SQLite बाइंडिंग मौजूद हैं php/), और कई अन्य।

## संदर्भ

* [निकविज़न](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

