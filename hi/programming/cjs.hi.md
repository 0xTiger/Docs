{
  "date" : "2023-10-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "सीजेएस फ़ाइल - कॉमनजेएस कोड फ़ाइल",
  "description":".cjs फ़ाइल क्या है और इसे कैसे खोलें?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-26"
}

## सीजेएस फ़ाइल क्या है?

कॉमनजेएस (सीजेएस) फ़ाइल एक फ़ाइल है जिसमें कॉमनजेएस सिंटैक्स में लिखा जावास्क्रिप्ट कोड होता है। कॉमनजेएस एक मॉड्यूल सिस्टम है जिसे फ्रंटएंड वेब ब्राउज़र से परे वातावरण में काम करने के लिए डिज़ाइन किया गया है, और इसे अक्सर नोड.जेएस जैसे सर्वर-साइड जावास्क्रिप्ट वातावरण में उपयोग किया जाता है।

## सीजेएस फ़ाइल प्रारूप - अधिक जानकारी

CJS फ़ाइलें CommonJS सिंटैक्स में लिखी जाती हैं और इन्हें Microsoft Notepad या Apple TextEdit जैसे किसी भी टेक्स्ट एडिटर में संपादित किया जा सकता है। कॉमनजेएस मॉड्यूल आमतौर पर अलग-अलग फाइलों में संग्रहीत होते हैं और बेहतर संगठन और रखरखाव के लिए कोड को इनकैप्सुलेट और मॉड्यूलराइज़ करने का इरादा रखते हैं। ये मॉड्यूल निर्भरताओं को आयात करने के लिए आवश्यक फ़ंक्शन का उपयोग करते हैं और कोड के अन्य भागों द्वारा उपयोग किए जा सकने वाले मूल्यों और कार्यों को उजागर करने के लिए मॉड्यूल.एक्सपोर्ट या एक्सपोर्ट ऑब्जेक्ट का उपयोग करते हैं।

## सीजेएस कोड उदाहरण

कॉमनजेएस मॉड्यूल में एक विशिष्ट वाक्यविन्यास और संरचना होती है जिसमें अन्य मॉड्यूल आयात करने के लिए आवश्यक फ़ंक्शन और मॉड्यूल से मूल्यों, कार्यों या वस्तुओं को निर्यात करने के लिए मॉड्यूल.निर्यात या निर्यात जैसी सुविधाएं शामिल होती हैं। इन मॉड्यूल का उपयोग कोड के टुकड़ों को एनकैप्सुलेट करने और अलग करने के लिए किया जाता है, जिससे बड़े जावास्क्रिप्ट कोडबेस को प्रबंधित करना और बनाए रखना आसान हो जाता है। यहां CommonJS मॉड्यूल का एक मूल उदाहरण दिया गया है:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## सन्दर्भ

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)