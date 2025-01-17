{
"date": "2023-05-29",
  "keywords": [
"आरबी फ़ाइल",
"आरबी फ़ाइल क्या है",
"आरबी फ़ाइल में रूबी स्क्रिप्ट कैसे चलाएं",
"आरबी फ़ाइल में क्या है",
"आरबी फ़ाइल का प्रारूप क्या है",
"फ़ाइल",
"आरबी फ़ाइल एक्सटेंशन",
"विस्तार"
],
  "author": {
"display_name": "शकील फ़ैज़"
},
"draft": "false",
"toc": true,
"title": "आरबी फ़ाइल स्वरूप - रूबी स्रोत कोड फ़ाइल",
  "description":"आरबी प्रारूप और एपीआई के बारे में जानें जो आरबी फाइलें बना और खोल सकते हैं।",
"linktitle": "RB",
  "menu": {
    "docs": {
      "identifier": "programming-rb",
"parent" : "programming"
}
},
"lastmod": "2023-05-29"
}

## आरबी फाइल क्या है?

एक ".rb" फ़ाइल एक्सटेंशन आमतौर पर रूबी प्रोग्रामिंग भाषा फ़ाइलों से जुड़ा होता है। रूबी एक गतिशील, ऑब्जेक्ट-ओरिएंटेड प्रोग्रामिंग भाषा है जो अपनी सादगी और पठनीयता के लिए जानी जाती है।

".rb" फ़ाइल में रूबी स्रोत कोड होता है, जिसे रूबी दुभाषिया या रूबी विकास वातावरण द्वारा निष्पादित किया जा सकता है। इन फ़ाइलों में अक्सर कक्षाओं, विधियों, चर और अन्य रूबी कोड संरचनाओं की परिभाषाएँ होती हैं।

## आरबी फ़ाइल में रूबी स्क्रिप्ट कैसे चलाएं?

".rb" फ़ाइल में सहेजी गई रूबी स्क्रिप्ट को चलाने के लिए, आपको अपने सिस्टम पर रूबी दुभाषिया स्थापित करने की आवश्यकता होगी। यहां "example.rb" नामक फ़ाइल में सहेजी गई रूबी स्क्रिप्ट का एक मूल उदाहरण दिया गया है:

```
# example.rb

# Define a method to calculate the square of a number
def square(number)
  number * number
end

# Call the square method with an argument
result = square(5)

# Print the result
puts "The square of 5 is: #{result}"
```

इस स्क्रिप्ट को चलाने के लिए, आप अपनी कमांड लाइन या टर्मिनल खोल सकते हैं, उस निर्देशिका पर नेविगेट कर सकते हैं जहां "example.rb" फ़ाइल स्थित है और फिर रूबी दुभाषिया का उपयोग करें:

```
ruby example.rb
```

उपरोक्त आदेश निष्पादित करने से स्क्रिप्ट चलेगी और आउटपुट कंसोल में प्रदर्शित होगा:

```
The square of 5 is: 25
```

यह एक सरल उदाहरण है लेकिन ".rb" फ़ाइलों में कक्षाएं, मॉड्यूल और नियंत्रण संरचनाओं सहित अधिक जटिल कोड हो सकते हैं, जो आपको पूर्ण रूबी एप्लिकेशन बनाने की अनुमति देते हैं।

## आरबी फ़ाइल में क्या है?

".rb" फ़ाइल की विशिष्ट सामग्री इसके उद्देश्य और इसे लिखने वाले प्रोग्रामर के आधार पर भिन्न हो सकती है। हालाँकि, सामान्य तौर पर, ".rb" फ़ाइल में रूबी स्रोत कोड होता है, जिसमें निर्देशों की श्रृंखला होती है जिसे रूबी दुभाषिया समझ सकता है और निष्पादित कर सकता है।

यहां कुछ सामान्य तत्व दिए गए हैं जो आपको रूबी फ़ाइल में मिल सकते हैं:

- **टिप्पणियाँ:** रूबी सिंगल-लाइन और मल्टी-लाइन दोनों टिप्पणियों का समर्थन करती है। टिप्पणियों का उपयोग व्याख्यात्मक नोट्स जोड़ने या कोड की विशिष्ट पंक्तियों को निष्पादन से अक्षम करने के लिए किया जाता है। इन्हें # अक्षर से दर्शाया जाता है.

```
# This is a single-line comment

=begin
This is a
multi-line comment
=end
```

- **परिवर्तनीय घोषणाएँ:** रूबी एक गतिशील रूप से टाइप की गई भाषा है, इसलिए चर को स्पष्ट प्रकार की घोषणाओं की आवश्यकता नहीं है। आप असाइनमेंट ऑपरेटर (=) का उपयोग करके वेरिएबल्स को मान निर्दिष्ट कर सकते हैं।

- **तरीके:** रूबी तरीकों को परिभाषित करने के लिए `def` कीवर्ड का उपयोग करती है, जो कोड के पुन: प्रयोज्य ब्लॉक होते हैं जो विशिष्ट कार्य करते हैं।

- **कक्षाएँ और वस्तुएँ:** रूबी एक वस्तु-उन्मुख भाषा है, और कक्षाओं का उपयोग वस्तु ब्लूप्रिंट को परिभाषित करने के लिए किया जाता है। ऑब्जेक्ट कक्षाओं के उदाहरण हैं और उनमें विशेषताएँ (उदाहरण चर) और व्यवहार (उदाहरण विधियाँ) हो सकते हैं।

- **नियंत्रण संरचनाएं:** रूबी प्रोग्राम में निष्पादन के प्रवाह को नियंत्रित करने के लिए विभिन्न नियंत्रण संरचनाएं प्रदान करती है जैसे सशर्त विवरण (यदि, अन्यथा, elsif, जब तक), लूप (जबकि, जब तक, प्रत्येक के लिए), और अधिक।

```
if age >= 18
  puts "You are an adult."
else
  puts "You are a minor."
end

# Output: You are an adult.
```

## आरबी फ़ाइल का प्रारूप क्या है?

".rb" फ़ाइल का प्रारूप सादा पाठ है, जिसे आमतौर पर UTF-8 या ASCII एन्कोडिंग का उपयोग करके एन्कोड किया जाता है। यह रूबी प्रोग्रामिंग भाषा द्वारा परिभाषित एक विशिष्ट वाक्यविन्यास और संरचना का पालन करता है।

## RB फ़ाइल का MIME प्रकार क्या है?

- `एप्लिकेशन/एक्स-रूबी`

## संदर्भ
* [रूबी (प्रोग्रामिंग भाषा)](https://en.wikipedia.org/wiki/Ruby_(programming_language))

