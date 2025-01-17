{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR3 फ़ाइल स्वरूप - कैनन रॉ 3 छवि फ़ाइल",
  "description":"CR3 फ़ाइल स्वरूप और API के बारे में जानें जो CR3 फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## CR3 फ़ाइल क्या है?

CR3 फ़ाइल एक कैनन रॉ छवि फ़ाइल स्वरूप है जो चयनित कैनन डिजिटल कैमरों द्वारा बनाई गई है। यह कैनन द्वारा CR2 फ़ाइल स्वरूप को बदलने के लिए पेश किया गया था और इसका उपयोग कैनन के कुछ डिजिटल उपकरणों द्वारा किया जाता है। CR3 फाइलें कैमरे द्वारा कैप्चर किए गए मूल गैर-संसाधित दोषरहित छवि डेटा को संग्रहीत करती हैं। इन कच्ची छवियों का उपयोग उच्च गुणवत्ता वाली छवियां प्रदान करता है और फोटोग्राफरों को संपादन के लिए बहुत जगह देता है। मुख्य छवि डेटा के अलावा, CR3 फ़ाइलें छवि के बारे में मेटाडेटा जानकारी भी संग्रहीत करती हैं।

## CR3 फ़ाइल स्वरूप

CR3 फ़ाइलें ISO बेस मीडिया फ़ाइल स्वरूप (ISO/IEC 14496-12) में बाइनरी फ़ाइल के रूप में डिस्क में संग्रहीत की जाती हैं और इसमें कस्टम [कैनन टैग](https://exiftool.org/TagNames/Canon.html#uuid) भी शामिल हैं। इसमें [कैनन 'crx' कोडेक](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) भी शामिल है जो JPEG-LS (Rice-Golomb + RLE) का मिश्रण है। कोडिंग) और JPEG-2000 (LeGall 5/3 DWT + परिमाणीकरण)।

## CR3 कस्टम टैग

CR3 फ़ाइलों में विभिन्न उद्देश्यों के लिए कस्टम टैग होते हैं। इनमें से कुछ टैग इस प्रकार हैं।

|टैग आईडी| टैग नाम | लिखने योग्य |मूल्य / नोट्स|
---|---|---|---|
|'सीसीटीपी' |कैननसीसीटीपी| - |--> कैनन सीसीटीपी टैग|
|'सीएमटी1' |आईएफडी0| - |--> EXIF टैग|
|'CMT2' |ExifIFD| - |--> EXIF टैग|
|'CMT3' | मेकरनोटकैनन| - |--> कैनन टैग|
|'सीएमटी4' |जीपीएसइन्फो| - |--> जीपीएस टैग|
|'सीएनसीवी' |CompressorVersion| नहीं| |
|'सीएनओपी' |कैननसीएनओपी| - |--> कैनन CNOP टैग|
|'सीएनटीएच' |कैननसीएनटीएच| - |--> कैनन सीएनटीएच टैग|
|'THMB' |थंबनेलइमेज| नहीं| |

## संदर्भ

* [CR2 फ़ाइल स्वरूप](http://lclevy.free.fr/cr2/)
* [कैनन टैग](https://exiftool.org/TagNames/Canon.html#uuid)

