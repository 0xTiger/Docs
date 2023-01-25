{
  "date" : "2020-11-11",
  "keywords" :[ "डीटीएसएक्स", "एक्सटेंशन", "फाइल", "फाइल फॉर्मेट", "डेटाबेस फाइल टाइप", "डेटाबेस फाइल फॉर्मेट", "डेटाबेस फाइल्स"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DTSX फ़ाइल स्वरूप और API के बारे में जानें जो DTSX फ़ाइलें बना और खोल सकते हैं।",
  "title" :"DTSX फ़ाइल स्वरूप - SQL सर्वर DTS सेटिंग्स फ़ाइल",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## डीटीएसएक्स फ़ाइल क्या है?

.dtsx (डेटा ट्रांसफ़ॉर्मेशन सर्विसेज पैकेज XML) एक्सटेंशन वाली फ़ाइल एक डेटा ट्रांसफ़ॉर्मेशन सर्विसेज (DTS) फ़ाइल है जिसका उपयोग Microsoft SQL द्वारा एक डेटाबेस से दूसरे डेटाबेस में डेटा स्थानांतरण के लिए डेटा माइग्रेशन चरणों/नियमों के संदर्भ में किया जाता है। इसमें परिवर्तन और किसी भी वैकल्पिक प्रसंस्करण चरण शामिल हैं जो मूल और गंतव्य बिंदुओं के बीच डेटा स्थानांतरण के दौरान आवश्यक हो सकते हैं। SQL सर्वर इंटीग्रेशन सर्विसेज (SSIS), Microsoft SQL सर्वर का एक घटक, डेटाबेस सर्वरों के बीच डेटा के प्रसंस्करण के चरणों की पहचान करने के लिए DTSX फ़ाइलों का उपयोग करता है। DTSX फाइलें Microsoft SQL Server 2019 के साथ खोली जा सकती हैं।

## डीटीएसएक्स फ़ाइल प्रारूप

इस ऑपरेशन के दौरान डेटा की अखंडता सुनिश्चित करने के लिए डेटाबेस सर्वर के बीच डेटा आंदोलन के लिए नियमों और प्रसंस्करण चरणों की आवश्यकता होती है। एसएसआईएस यह सुनिश्चित करता है कि उद्यम में विभिन्न स्रोतों से डेटा को स्थानांतरित करने और अनुरूप बनाने के लिए ये सभी गतिविधियां आसानी से हो सकें। यही वह जगह है जहां डीटीएसएक्स आता है जो एसएसआईएस द्वारा उपयोग की जाने वाली संरचनाओं को उन चरणों को स्थापित करने के लिए परिभाषित करता है जहां डेटा को संसाधित किया जा सकता है क्योंकि यह इन चरणों के माध्यम से होता है।

DTSX द्वारा वर्णित डेटा प्रवाह निम्न छवि में दिखाया गया है।

{{< figure src="../DataFlowDTSX.png" alt="डेटा प्रवाह DTSX" >}}

DTSX [XML](/hi/web/xml/)-आधारित है और [MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-) में प्रलेखित है। 4b5b-a388-aa3c65aec1dd)। डीटीएसएक्स एक्सएमएल की बढ़ी हुई रिफैक्टरिंग डीटीएसएक्स 2.0 है जिसमें संरचनाओं के लिए नई विशेषताएं शामिल हैं, नामित गुणों को मूल एक्सएमएल विशेषताओं के रूप में बदलना, अधिकांश विशेषता मानों के लिए डिफ़ॉल्ट निर्दिष्ट करना, और मूल तत्व के अंदर दोहराए गए तत्वों की नियुक्ति शामिल है। DTSX संरचनाओं का वर्णन इन [XML योजनाओं](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) का उपयोग करके किया गया है और संरचनात्मक प्रारूप है सेलर-टेक्स्ट एक्सएमएल।

## संदर्भ

* [डीटीएसएक्स प्रारूप - माइक्रोसॉफ्ट](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [डीटीएसएक्स 2 प्रारूप - माइक्रोसॉफ्ट द्वारा](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)
