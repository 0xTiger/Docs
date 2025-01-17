{
  "date" : "2021-04-08",
  "keywords" :[ "डेब फाइल", "डेब फाइल फॉर्मेट", "एक डिबेट फाइल क्या है", "फाइल", "डेब उदाहरण", "डेब फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - बज़िप कंप्रेस्ड टार आर्काइव",
  "description":"DEB फ़ाइल स्वरूप और API के बारे में जानें जो DEB फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## डीईबी फाइल क्या है?

.deb एक्सटेंशन वाली फाइल एक डेबियन बाइनरी पैकेज फाइल फॉर्मेट है जो लिनक्स ओएस पर सॉफ्टवेयर पैकेज के वितरण के लिए उपलब्ध है। इसमें दो [TAR](/hi/compression/tar/) संग्रह फ़ाइलें होती हैं। डीपीकेजी डीईबी पैकेज को पढ़ने और स्थापित करने के लिए तंत्र प्रदान करता है। एपीटी पैकेज सॉफ्टवेयर प्रबंधन इंटरफेस का उपयोग करके डीईबी पैकेज स्थापित किए जा सकते हैं। डीईबी फाइलों में इंटरनेट मीडिया प्रकार `application/vnd.debian.binary-package` होता है।

## डीईबी फ़ाइल प्रारूप

एक DEB फ़ाइल में दो [TAR](/hi/compression/tar/) संग्रह फ़ाइलें होती हैं। एक संग्रह में नियंत्रण की जानकारी होती है और दूसरे में इंस्टॉल करने योग्य डेटा होता है।

### पैकेज संगठन

DEB फ़ाइल एक **ar** संग्रह फ़ाइल है जिसका जादुई मान `!<arch> `. डेबियन 0.93 के बाद से, डीईबी फाइलों के संग्रह तंत्र में एक विशिष्ट क्रम में तीन फाइलें होती हैं।

1. `डेबियन बाइनरी` - इसमें लाइनों की एक श्रृंखला होना तय है, जो नई लाइनों से अलग होती है। वर्तमान में, केवल एक पंक्ति मौजूद है जो संस्करण संख्या का वर्णन करती है। वर्तमान संस्करण संख्या 2.0 है।
1. `कंट्रोल आर्काइव` - इसमें एक control.tar संग्रह होता है जिसमें रखरखाव स्क्रिप्ट और पैकेज के बारे में मेटा-सूचना जैसे पैकेज नाम, संस्करण, निर्भरता और रखरखाव है।
1. `डेटा आर्काइव` - यह data.tar नाम का एक टार आर्काइव है और इसमें वास्तविक इंस्टाल करने योग्य मीडिया फाइलें होती हैं। संग्रह को gz, bz2, lzma या xz के साथ संपीड़ित किया जा सकता है, और डेटा संग्रह का फ़ाइल एक्सटेंशन तदनुसार बदलता है।

### नियंत्रण संग्रह

नियंत्रण संग्रह में निम्नानुसार सामग्री शामिल हो सकती है।

* `नियंत्रण` - इसमें पैकेज का संक्षिप्त विवरण के साथ-साथ अन्य जानकारी जैसे इसकी निर्भरताएं शामिल हैं।
* `md5sums` - इसमें भ्रष्ट या अधूरी फाइलों का पता लगाने के लिए पैकेज में सभी फाइलों के एमडी 5 चेकसम शामिल हैं।
* `conffiles` - यह पैकेज की फाइलों को सूचीबद्ध करता है जिन्हें कॉन्फ़िगरेशन फाइलों के रूप में माना जाना चाहिए। जब तक निर्दिष्ट न किया गया हो, कॉन्फ़िगरेशन फ़ाइलें अद्यतन के दौरान अधिलेखित नहीं होती हैं।
* `preinst`, postinst, prerm और postrm - वैकल्पिक स्क्रिप्ट जो पैकेज को स्थापित करने या हटाने से पहले या बाद में निष्पादित की जाती हैं
* `कॉन्फ़िगरेशन` एक वैकल्पिक स्क्रिप्ट है जो डेबकॉन्फ़ कॉन्फ़िगरेशन तंत्र का समर्थन करती है।
* `shlibs` - यह साझा पुस्तकालय निर्भरताओं की एक सूची है।

## संदर्भ

* [डीईबी - विकिपीडिया](https://en.wikipedia.org/wiki/Deb_(file_format))
* [डेबियन बाइनरी पैकेज फॉर्मेट](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

