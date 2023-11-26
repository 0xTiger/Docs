{
"तारीख": "2023-05-31",
  "keywords": [
"डेस्कटॉप फ़ाइल",
"डेस्कटॉप फ़ाइल क्या है",
"डेस्कटॉप फ़ाइल में क्या है",
"उदाहरण डेस्कटॉप फ़ाइल",
"डेस्कटॉप फ़ाइल कैसे खोलें",
"डेस्कटॉप फ़ाइल का प्रारूप क्या है",
"फ़ाइल",
"डेस्कटॉप फ़ाइल एक्सटेंशन",
"विस्तार"
],
  "author": {
"display_name": "शकील फ़ैज़"
},
"draft": "false",
"toc": true,
"title": "डेस्कटॉप फ़ाइल स्वरूप - डेस्कटॉप प्रविष्टि फ़ाइल",
  "description":"डेस्कटॉप प्रारूप और एपीआई के बारे में जानें जो डेस्कटॉप फाइलें बना और खोल सकते हैं।",
"linktitle": "डेस्कटॉप",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
"पैरेंट": "सेटिंग्स"
}
},
"lastmod": "2023-05-31"
}

## डेस्कटॉप फ़ाइल क्या है?

.डेस्कटॉप फ़ाइल एक कॉन्फ़िगरेशन फ़ाइल है जिसका उपयोग लिनक्स डेस्कटॉप वातावरण द्वारा एप्लिकेशन शॉर्टकट और लॉन्चर को परिभाषित करने के लिए किया जाता है। यह किसी एप्लिकेशन के बारे में मेटाडेटा प्रदान करता है जैसे उसका नाम, आइकन, निष्पादित करने का आदेश और अन्य गुण। इन फ़ाइलों का उपयोग आमतौर पर लिनक्स-आधारित सिस्टम में एप्लिकेशन मेनू, डेस्कटॉप लॉन्चर या पैनल में शॉर्टकट बनाने के लिए किया जाता है।

## डेस्कटॉप फ़ाइल में क्या है?

एक .desktop फ़ाइल विशिष्ट प्रारूप का अनुसरण करती है और इसमें कई प्रमुख फ़ील्ड शामिल होते हैं:

- **[डेस्कटॉप प्रविष्टि]:** यह .desktop फ़ाइल के लिए मुख्य अनुभाग शीर्षलेख है।
- **नाम:** आवेदन का नाम निर्दिष्ट करता है।
- **टिप्पणी:** आवेदन के बारे में संक्षिप्त विवरण या टिप्पणी प्रदान करता है।
- **निष्पादन:** एप्लिकेशन लॉन्च करते समय निष्पादित करने के लिए कमांड को परिभाषित करता है।
- **आइकन:** एप्लिकेशन से संबद्ध आइकन फ़ाइल का पथ निर्दिष्ट करता है।
- **टर्मिनल:** निर्दिष्ट करता है कि एप्लिकेशन को टर्मिनल विंडो में चलाया जाना चाहिए या नहीं।
- **प्रकार:** प्रविष्टि का प्रकार निर्दिष्ट करता है जैसे "एप्लिकेशन" या "लिंक।"
- **श्रेणियाँ:** श्रेणियाँ या समूह निर्दिष्ट करती हैं जिनके अंतर्गत एप्लिकेशन को मेनू में प्रदर्शित किया जाना चाहिए।
- **स्टार्टअपनोटिफ़ाई:** निर्दिष्ट करता है कि डेस्कटॉप वातावरण को एप्लिकेशन के लिए स्टार्टअप अधिसूचना दिखानी चाहिए या नहीं।
- **NoDisplay:** निर्दिष्ट करता है कि एप्लिकेशन को मेनू से छिपाया जाना चाहिए या नहीं।
- **क्रियाएँ:** अतिरिक्त क्रियाओं को परिभाषित करता है जो एप्लिकेशन पर की जा सकती हैं जैसे कि एक विशिष्ट फ़ाइल खोलना।

## उदाहरण डेस्कटॉप फ़ाइल

यहां "MyTextEditor" नामक काल्पनिक पाठ संपादक के लिए .desktop फ़ाइल का एक उदाहरण दिया गया है:

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

इस उदाहरण में, .desktop फ़ाइल अपने संबंधित गुणों के साथ एप्लिकेशन "MyTextEditor" को परिभाषित करती है। इसमें दो अतिरिक्त क्रियाएं भी शामिल हैं, "नई विंडो खोलें" और "मौजूदा फ़ाइल खोलें", जिसे एप्लिकेशन लॉन्चर के संदर्भ मेनू से एक्सेस किया जा सकता है।

विशिष्ट निर्देशिकाओं जैसे `/usr/share/applications` या `~/.local/share/applications` में .desktop फ़ाइल रखकर, डेस्कटॉप वातावरण इसे पहचान लेगा और मेनू में तदनुसार एप्लिकेशन प्रदर्शित करेगा या इसे लॉन्च करने की अनुमति देगा डेस्कटॉप।

## डेस्कटॉप फ़ाइल कैसे खोलें?

कई सॉफ़्टवेयर प्रोग्राम .desktop फ़ाइलें खोल और संभाल सकते हैं। ये प्रोग्राम आम तौर पर लिनक्स-आधारित सिस्टम पर फ़ाइल प्रबंधक या डेस्कटॉप वातावरण होते हैं। यहां कुछ उदाहरण दिए गए हैं:

- **नॉटिलस (फ़ाइलें):** गनोम डेस्कटॉप वातावरण के लिए डिफ़ॉल्ट फ़ाइल प्रबंधक।
- **निमो:** सिनेमन डेस्कटॉप वातावरण के लिए फ़ाइल प्रबंधक।
- **डॉल्फिन:** केडीई प्लाज्मा डेस्कटॉप वातावरण के लिए डिफ़ॉल्ट फ़ाइल प्रबंधक।
- **थुनर:** Xfce डेस्कटॉप वातावरण के लिए डिफ़ॉल्ट फ़ाइल प्रबंधक।
- **केडीई मेनू संपादक:** केडीई प्लाज्मा डेस्कटॉप वातावरण के लिए एक विशिष्ट उपकरण जो आपको .डेस्कटॉप फ़ाइलों को देखने और संपादित करने की अनुमति देता है।

ये फ़ाइल प्रबंधक और डेस्कटॉप वातावरण .desktop फ़ाइलों के प्रबंधन के लिए ग्राफिकल इंटरफ़ेस प्रदान करते हैं। वे आपको .desktop फ़ाइलों के गुणों को देखने और संपादित करने, एप्लिकेशन लॉन्चर बनाने और एप्लिकेशन मेनू या डेस्कटॉप पर शॉर्टकट व्यवस्थित करने की अनुमति देते हैं।

.डेस्कटॉप फ़ाइलें सादा पाठ फ़ाइलें हैं, इसलिए आप उन्हें अपनी पसंद के पाठ संपादक के साथ खोल और संपादित भी कर सकते हैं। बस .desktop फ़ाइल पर राइट-क्लिक करें और इंस्टॉल किए गए प्रोग्रामों की सूची से एक टेक्स्ट एडिटर चुनने के लिए "इसके साथ खोलें" या "किसी अन्य एप्लिकेशन के साथ खोलें" का चयन करें।

## DESKTOP फ़ाइल का प्रारूप क्या है?

.डेस्कटॉप फ़ाइल स्वरूप विशिष्ट संरचना और प्रारूप का अनुसरण करता है। यह एक सादा पाठ फ़ाइल है जिसमें अनुभागों में व्यवस्थित कुंजी-मूल्य जोड़े का एक सेट होता है। यहां प्रारूप का अवलोकन दिया गया है:

- **अनुभाग शीर्षलेख:** प्रत्येक अनुभाग वर्गाकार कोष्ठक ([]) में संलग्न शीर्षलेख से शुरू होता है। प्राथमिक अनुभाग को आमतौर पर [डेस्कटॉप एंट्री] नाम दिया जाता है, जिसमें एप्लिकेशन या लॉन्चर के लिए मुख्य मेटाडेटा होता है।
- **कुंजी-मूल्य जोड़े:** प्रत्येक अनुभाग के भीतर, आप कुंजी-मूल्य जोड़े का उपयोग करके गुणों को परिभाषित करते हैं। प्रारूप "कुंजी=मान" है। कुंजी संपत्ति की पहचान करती है और मूल्य संबंधित डेटा प्रदान करती है।
- **प्रॉपर्टी सिंटैक्स:** प्रॉपर्टी मान स्ट्रिंग्स, बूलियन मान, फ़ाइल पथ या सूचियों सहित विभिन्न प्रकार के हो सकते हैं। प्रत्येक संपत्ति के मूल्य का प्रारूप उसके प्रकार पर निर्भर करता है।
- **टिप्पणियाँ:** आप '#' प्रतीक का उपयोग करके .desktop फ़ाइल में टिप्पणियाँ शामिल कर सकते हैं। ऑनलाइन '#' का अनुसरण करने वाली किसी भी चीज़ को एक टिप्पणी माना जाता है और उसे अनदेखा कर दिया जाता है।

## संदर्भ
* [डेस्कटॉप एंट्री फ़ाइलें](https://www.baeldung.com/linux/desktop-entry-files)
