{
  "date" : "2021-03-11",
  "keywords" :[ "एपीएनएक्स", "अमेज़ॅन पेज नंबर इंडेक्स", "एक्सटेंशन", "फाइल", "फॉर्मेट", "ईबुक", "अमेज़ॅन किंडल"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"अमेज़ॅन एपीएनएक्स फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एपीएनएक्स फाइलें बना और खोल सकते हैं।",
  "title" :"एपीएनएक्स - अमेज़ॅन पेज नंबर इंडेक्स",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## एपीएनएक्स फाइल क्या है? ##

Amazon पेज नंबर इंडेक्स फ़ाइल जो .apnx एक्सटेंशन का उपयोग करती है, एक ईबुक फ़ाइल प्रकार है; Amazon Kindle द्वारा उपयोग किया जाता है। इन फ़ाइलों को वास्तव में किंडल उपकरणों द्वारा उपयोग की जाने वाली पेजिनेशन फ़ाइलों के रूप में जाना जाता है। इसलिए APNX फाइलें आमतौर पर किंडल ई-बुक्स के पन्नों को चिह्नित करने के लिए बनाई जाती हैं। Amazon Kindle डिवाइस पर पेजिनेशन फीचर 3.1 फर्मवेयर के बाद से शुरू किया गया है। यह पेज इंडेक्स के लिए APNX फाइल को देखता है और फिर इसे मूल प्रिंट बुक में पेज नंबरों के साथ मैप करता है। इन फ़ाइलों को Amazon eBooks फ़ाइलों के साथ जलाने वाले उपकरणों में सहेजा जाता है। आप APNX फ़ाइलें खोल या संपादित नहीं कर सकते।

## APNX फ़ाइल स्वरूप विनिर्देश ##

### विन्यास

|बाइट्स| सामग्री| टिप्पणियाँ|
---|---|---|
|4 |00010001 | प्रारूप पहचानकर्ता। 65537 का मान
|4 |अगले की शुरुआत | पहले हेडर के स्थान को समाप्त करने के बाद ऑफसेट। हेडर जानकारी का एक नया क्रम शुरू करता है|
|4 |लंबाई| पहले हेडर की लंबाई|
|एन |फर्स्ट हेडर | सामग्री शीर्षलेख युक्त स्ट्रिंग। यह अगला क्रम शुरू करता है|
|2 |अज्ञात | हमेशा 1|
|2 |लंबाई | दूसरे हेडर की लंबाई|
|2 |पृष्ठ संख्या | पृष्ठों का प्रतिनिधित्व करने वाले दूसरे शीर्षलेख के बाद बाइट्स की कुल संख्या। इस कुल में बाइट शामिल हैं जिन्हें पेजमैप द्वारा अनदेखा किया जाता है।|
|2 |अज्ञात | हमेशा 32|
|एन |दूसरा हेडर | पेज मैपिंग हेडर युक्त स्ट्रिंग|
|4*N |पैडिंग | पेज मैपिंग हेडर में दिया गया पहला नंबर 0 बाइट्स की संख्या दर्शाता है
|4*N |पेज सूची ||

### कंटेंट हैडर

सामग्री शीर्षलेख में {} में संलग्न एक स्ट्रिंग होती है जिसमें कुंजी, मान जोड़े होते हैं:

|सामग्री| टिप्पणियाँ|
---|---|
|कंटेंटगाइड| गाइड.|
|असिन | पुस्तक के किंडल संस्करण के लिए अमेज़न पहचानकर्ता।|
|सीडी टाइप | MOBI सीडी टाइप। ebooks के लिए हमेशा EBOK होना चाहिए।|
|fileRevisionId | इस फ़ाइल का संशोधन।|

#### उदाहरण
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### पेज मैपिंग हैडर
पेज मैपिंग हेडर में एक स्ट्रिंग होती है जो {} में संलग्न होती है जिसमें कुंजी, मान जोड़े होते हैं।

|सामग्री | टिप्पणियाँ|
---|---|
|असिन | आईएसबीएन 10 पेपर बुक के लिए पेज जिसके अनुरूप हैं|
|पेजमैप| तीन मान टपल। ऐसा लगता है: "(एन, एन, एन) \
1) हेडर के बाद बाइट्स की संख्या जो पेज नंबरिंग सीक्वेंस शुरू करती है\
2) अज्ञात\
3) अज्ञात\|
#### उदाहरण
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### पृष्ठ सूची

पृष्ठ सूची कच्चे HTML में ऑफ़सेट का एक क्रम है। प्रत्येक
value एक नए पृष्ठ की शुरुआत है। प्रत्येक प्रविष्टि एक 4 बाइट बड़ा एंडियन है
इंट



## संदर्भ

* [अमेज़ॅन एपीएनएक्स फ़ाइल प्रारूप](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - MobileRead विकी द्वारा](https://wiki.mobileread.com/wiki/APNX)

