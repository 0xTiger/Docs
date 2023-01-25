{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "संपीड़ित", "फ़ाइल", "एक्सटेंशन", "फ़ाइल प्रारूप", "लेम्पेल-ज़िव-ओबरह्यूम"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZO फ़ाइल प्रारूप",
  "description":"LZO फ़ाइल स्वरूप और API के बारे में जानें जो LZO फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## एलजेडओ फाइल क्या है? ##

.lzo एक्सटेंशन वाली फाइल को फाइल आर्काइविंग फीचर्स के साथ जोड़ा जाता है जो कंप्रेस्ड फाइल में सभी फाइलों के आकार को कम कर सकता है। सभी संपीड़ित फ़ाइलों में एक या अधिक फ़ाइलें या विभिन्न प्रकार और आयामों की कई फ़ाइलों के साथ बाइंडरों के समूह भी शामिल हो सकते हैं। एक संपीड़ित फ़ाइल का आकार LZO संपीड़ित फ़ाइल में संग्रहीत सभी फ़ाइलों और फ़ोल्डरों के संयुक्त आकार की तुलना में छोटा होता है। सभी LZO संपीड़ित फ़ाइलें LZO प्रारूप में संग्रहीत हैं और स्पष्ट रूप से LZOP फ़ाइल संपीड़न और डीकंप्रेसन सॉफ़्टवेयर द्वारा उपयोग की जाने वाली संपीड़न सुविधाओं के साथ निष्पादित की जाती हैं। सभी संपीड़न विनिर्देशों को इस फ़ाइल संपीड़न और डीकंप्रेसन प्रोग्राम में जोड़ दिया गया है जो कि लेम्पेल-ज़िव-ओबरह्यूम फ़ाइल संपीड़न लाइब्रेरी से उत्पन्न हुआ है। तेज़ डीकंप्रेसन गति और विकसित संपीड़न अनुपात भी इन एलजेडओ फाइलों में संयुक्त हैं।

## एलजेडओ विशिष्टता ##

मार्कस फ्रांज ज़ेवर जोहान्स ओबरहुमर ने 1996 में अब्राहम लेम्पेल और जैकब ज़िव द्वारा पहले के एल्गोरिदम के आधार पर मूल "lzop" एल्गोरिथ्म विकसित किया था। यह पुस्तकालय निम्नलिखित विशेषताओं के साथ विभिन्न प्रकार के एल्गोरिदम को लागू करता है:

* DEFLATE की तुलना में तेज़ संपीड़न
*तेजी से विसंपीड़न
* अतिरिक्त बफ़र्स जो संपीड़न के दौरान आवश्यक होते हैं (संपीड़न स्तर के आधार पर 8KB या 64KB आकार के)
* स्रोत और गंतव्य बफ़र डीकंप्रेसन के लिए आवश्यक सभी मेमोरी हैं
* संपीड़न अनुपात और संपीड़न गति दोनों पर नियंत्रण प्रदान करता है

एक ब्लॉक कम्प्रेशन एल्गोरिथम के रूप में, LZO ओवरलैपिंग कम्प्रेशन के साथ-साथ इन-प्लेस डीकंप्रेसन भी करता है। अतिव्यापी संपीड़न प्राप्त करने के लिए, संपीड़न और डीकंप्रेसन दोनों के ब्लॉक आकार का मिलान होना चाहिए। LZO कम्प्रेशन एल्गोरिथम इनपुट डेटा को मैचों (एक स्लाइडिंग डिक्शनरी) और शाब्दिकों में विभाजित करता है जो मेल नहीं खाते हैं, अत्यधिक निरर्थक डेटा के साथ अच्छे परिणाम देते हैं और गैर-संपीड़ित डेटा के साथ स्वीकार्य परिणाम देते हैं, केवल असंपीड्य डेटा को मूल के 1/64 से बढ़ाते हैं। आकार।

## LZO फ़ाइल खोलने में समस्या ##

निम्नलिखित कुछ समस्याएं हैं जो LZO फ़ाइल स्वरूप के खराब काम करने का कारण हो सकती हैं:
  


* फ़ाइल दूषित हो सकती है। इस समस्या को हल करने के लिए, फ़ाइल को फिर से डाउनलोड करें या प्रेषक को फ़ाइल को फिर से भेजने के लिए कहें
*दूसरा कारण है संक्रमित फाइल इस मामले में फाइल को ठीक से स्कैन करें
* LZO फ़ाइल के अनुचित लिंक
* LZO . के विवरण को हटाना
*पर्याप्त हार्डवेयर संसाधन नहीं
*उपकरण के पुराने ड्राइवर
  


## संदर्भ ##

* [एलजेडओ - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)
