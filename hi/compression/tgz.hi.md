{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGZ फ़ाइल - Gzipped टार फ़ाइल",
  "description":"टीजीजेड फ़ाइल प्रारूप और एपीआई के बारे में जानें जो टीजीजेड फाइलें बना और खोल सकते हैं।",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## टीजीजेड फाइल क्या है?

.tgz एक्सटेंशन वाली फाइल एक TAR आर्काइव फाइल होती है, जिसमें कई फाइलें और फोल्डर होते हैं, जिन्हें Gnu Zip (gzip) कम्प्रेशन सॉफ्टवेयर का उपयोग करके कंप्रेस किया गया है। एक [TAR](/hi/compression/tar/) फ़ाइल आमतौर पर इंटरनेट पर बैकअप या वितरण के लिए एकाधिक फ़ाइलों को एक फ़ाइल में जोड़ती है। यह फ़ाइल को तब तक असम्पीडित करता है जब तक कि इसे gzip सॉफ़्टवेयर का उपयोग करके संपीड़ित नहीं किया जाता है जिसके बाद यह TGZ फ़ाइल बन जाती है। TGZ फ़ाइलें, संपीड़ित फ़ाइलें होने के कारण, डिस्क पर कम जगह लेती हैं और ईमेल के माध्यम से इंटरनेट का उपयोग करके आसानी से स्थानांतरित की जा सकती हैं। कुछ एप्लिकेशन जो TGZ फाइलें खोल सकते हैं उनमें WinZip, Apple Archive Utility, 7-Zip और WinRAR शामिल हैं। TGZ फाइलें ज्यादातर UNIX और Linux सिस्टम में उपयोग की जाती हैं।

## टीजीजेड फ़ाइल प्रारूप

TGZ फ़ाइलें [GZ](/hi/compression/gz/) कम्प्रेशन एल्गोरिथम का उपयोग करके संपीड़ित बाइनरी फ़ाइलों के रूप में सहेजी जाती हैं।

## Linux पर .tgz फ़ाइल को अनपैक कैसे करें

लिनक्स/यूनिक्स ओएस पर, कमांड लाइन से टीजीजेड फाइलों को अनपैक करने के लिए निम्न कमांड का उपयोग किया जा सकता है।

```
tar zxvf tgzCompressedFile.tgz
```

उपरोक्त आदेश संपीड़ित TGZ फ़ाइल को विघटित करता है और इसकी फ़ाइलों को TAR संग्रह को डिस्क पर निकालता है।
## संदर्भ ##

* [टीजीएस](https://core.telegram.org/stickers#animated-stickers)
* [गज़िप - विकिपीडिया](https://en.wikipedia.org/wiki/Gzip)

