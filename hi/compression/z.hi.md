{
  "date" : "2021-06-22",
  "keywords" :[ "जेड", "संपीड़ित", "फ़ाइल", "एक्सटेंशन", "फ़ाइल प्रारूप", "यूनिक्स", "कार्टज़"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Z संपीड़ित फ़ाइल स्वरूप",
  "description":"Z फ़ाइल स्वरूप और API के बारे में जानें जो Z फ़ाइलें बना और खोल सकता है।",
  "linktitle" : "Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-22"
}

## Z फाइल क्या है? ##

AZ फ़ाइल UNIX संपीड़ित डेटा फ़ाइलों से संबंधित फ़ाइलों की एक श्रेणी है। संपीड़ित यूनिक्स फ़ाइलें Z फ़ाइल का सबसे लोकप्रिय और व्यापक रूप से उपयोग किया जाने वाला एक्सटेंशन प्रकार हैं। Z फाइल फाइलों को फॉर्मेट करना, चलाना और खोलना आसान बनाती है क्योंकि इनका उपयोग छोटी कंप्यूटर फाइलें बनाने के लिए किया जाता है जिन्हें लिनक्स/यूनिक्स ऑपरेटिंग सिस्टम पर आसानी से चलाया जा सकता है। यह डिस्क स्थान बचाने के इच्छुक उपयोगकर्ताओं के लिए फायदेमंद है, क्योंकि बड़ी फ़ाइलों को एक Z फ़ाइल में संपीड़ित करके, उपयोगकर्ता बहुत अधिक संग्रहण स्थान बचा सकते हैं और अपनी फ़ाइलों को अधिक व्यवस्थित कर सकते हैं। इन संपीड़ित Z फ़ाइलों को "abc" नाम की फ़ाइल के लिए एक साधारण कमांड "uncompress abc.z" का उपयोग करके यूनिक्स सिस्टम में आसानी से विघटित किया जा सकता है।


## संक्षिप्त इतिहास ##

Z फ़ाइल 80 के दशक के अंत और 90 के दशक की शुरुआत में एक तेज़ संग्रहकर्ता की अटूट माँग के परिणामस्वरूप बनाई गई थी। चूंकि उस समय इंटरनेट बहुत लोकप्रिय और सुलभ नहीं था, इसलिए उपयोगकर्ताओं को बुनियादी फाइलों को साझा करने और इंटरनेट तक पहुंचने के लिए संघर्ष करना पड़ता था। ऐसा ही एक तरीका है कि उपयोगकर्ता फ़ाइलों को स्थानांतरित करने के लिए एक संग्रहकर्ता का उपयोग कर रहे थे। Z फाइल को फिल काट्ज द्वारा आर्काइवर के एक तेज और अधिक सहायक रूप के रूप में पेश किया गया था, जिसके माध्यम से बड़ी फाइलों को एक में संपीड़ित किया जा सकता था और स्थानांतरित किया जा सकता था। कार्त्ज़ द्वारा अंतिम संस्करण 1989 में एक कानूनी लड़ाई के बाद पेश किया गया था, और यह सार्वजनिक डोमेन के लिए समर्पित था, जैसा कि कार्त्ज़ द्वारा घोषित किया गया था।


## तकनीकी विशिष्टता ##

Z फाइल एक फाइल है जो आर्काइव फाइल फॉर्मेट को सपोर्ट करती है। यह पहली फ़ाइल प्रकारों में से एक है जो यूनिक्स और लिनक्स ऑपरेटिंग सिस्टम का उपयोग करके तेज़, और दोषरहित डेटा संपीड़न और डीकंप्रेसन प्रदान करता है। कुछ ऑपरेटिंग सिस्टम में, लोअरकेस Z (.z) के साथ एक फ़ाइल एक्सटेंशन एक GNU-संपीड़ित फ़ाइल का प्रतिनिधित्व करता है, जबकि अपरकेस Z (.Z) वाली फ़ाइल एक संपीड़ित फ़ाइल का प्रतिनिधित्व करती है। Z फ़ाइल के कई संस्करण हैं जो इसका समर्थन करते हैं, जैसे कि 2.0, 2.1, 4.5, 4.6, अन्य। विभिन्न Z फ़ाइल संस्करणों में विभिन्न एल्गोरिदम हैं, और सबसे लोकप्रिय एक DEFLATE है।




