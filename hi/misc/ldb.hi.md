{
"तारीख": "2023-04-20",
  "keywords": [
"एलडीबी फ़ाइल",
"एलडीबी फ़ाइल क्या है",
"एलडीबी में कौन सी जानकारी है",
"एलडीबी फ़ाइल का उद्देश्य क्या है",
"एलडीबी एक्सटेंशन",
"फ़ाइल",
"विस्तार"
],
  "author": {
"display_name": "शकील फ़ैज़"
},
"draft": "false",
"toc": true,
"title": "एलडीबी फ़ाइल स्वरूप - माइक्रोसॉफ्ट एक्सेस लॉक फ़ाइल",
  "description":"एलडीबी प्रारूप के बारे में जानें और इसमें क्या जानकारी है।",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
"parent" : "misc"
}
},
"lastmod": "2023-04-20"
}

## एलडीबी फ़ाइल क्या है?

LDB फ़ाइल एक लॉक फ़ाइल है जिसका उपयोग Microsoft Access द्वारा कई उपयोगकर्ताओं को एक ही डेटाबेस को एक साथ संपादित करने से रोकने के लिए किया जाता है। जब उपयोगकर्ता एक्सेस डेटाबेस खोलता है, तो एक्सेस डेटाबेस के समान निर्देशिका में संबंधित एलडीबी फ़ाइल बनाता है। इस फ़ाइल में यह जानकारी है कि वर्तमान में डेटाबेस का उपयोग कौन कर रहा है और वे कौन से रिकॉर्ड संपादित कर रहे हैं।

जब डेटाबेस खोला जाता है तो LDB फ़ाइल Microsoft Access द्वारा स्वचालित रूप से बनाई जाती है, और डेटाबेस बंद होने पर हटा दी जाती है। यह ध्यान रखना महत्वपूर्ण है कि एलडीबी फ़ाइल को कभी भी मैन्युअल रूप से हटाया नहीं जाना चाहिए क्योंकि इससे डेटाबेस में समस्याएँ पैदा हो सकती हैं।

यदि आप माइक्रोसॉफ्ट एक्सेस डेटाबेस के साथ समस्याओं का सामना करते हैं, तो एक संभावित समाधान उस डेटाबेस से जुड़ी एलडीबी फ़ाइल को हटाने का प्रयास करना है। यह किसी भी लॉक को हटा देगा जो आपको डेटाबेस तक पहुंचने से रोक सकता है। हालाँकि, यह प्रयास करने से पहले डेटाबेस का बैकअप अवश्य बना लें, क्योंकि गलत तरीके से किए जाने पर एलडीबी फ़ाइल को हटाने से डेटा हानि या भ्रष्टाचार हो सकता है।

## एलडीबी फ़ाइल स्वरूप - अधिक जानकारी

माइक्रोसॉफ्ट एक्सेस में एक एलडीबी फ़ाइल में उन उपयोगकर्ताओं के बारे में जानकारी होती है जो वर्तमान में डेटाबेस तक पहुंच रहे हैं जैसे कि उनका उपयोगकर्ता नाम, कंप्यूटर नाम और लॉगिन समय। एलडीबी फ़ाइल में डेटाबेस पर रखे गए किसी भी लॉक के बारे में जानकारी भी होती है, जैसे कि किस उपयोगकर्ता द्वारा कौन से रिकॉर्ड संपादित किए जा रहे हैं।

यहां एलडीबी फ़ाइल में पाई जा सकने वाली जानकारी के प्रकारों की अधिक विस्तृत सूची दी गई है:

- **उपयोगकर्ता नाम** - उस उपयोगकर्ता का नाम जो वर्तमान में डेटाबेस तक पहुंच रहा है
- **कंप्यूटर का नाम** - उस कंप्यूटर का नाम जहां से उपयोगकर्ता डेटाबेस तक पहुंच रहा है
- **लॉगिन समय** - वह समय जब उपयोगकर्ता ने पहली बार डेटाबेस खोला
- **रिकॉर्ड लॉक** - इस बारे में जानकारी कि कौन सा रिकॉर्ड वर्तमान में किस उपयोगकर्ता द्वारा संपादित किया जा रहा है
- **ऑब्जेक्ट लॉक** - इस बारे में जानकारी कि कौन से डेटाबेस ऑब्जेक्ट (जैसे टेबल, फॉर्म या रिपोर्ट) वर्तमान में किस उपयोगकर्ता द्वारा संपादित किए जा रहे हैं
- **कनेक्शन जानकारी** - उपयोगकर्ता डेटाबेस से कैसे जुड़ा है इसके बारे में जानकारी (उदाहरण के लिए, क्या वे स्थानीय या नेटवर्क कनेक्शन का उपयोग कर रहे हैं)

एलडीबी फ़ाइल की जानकारी का उपयोग माइक्रोसॉफ्ट एक्सेस द्वारा एक ही समय में एक ही डेटाबेस में परस्पर विरोधी परिवर्तन करने से कई उपयोगकर्ताओं को रोकने के लिए किया जाता है। जब उपयोगकर्ता किसी रिकॉर्ड या ऑब्जेक्ट को संपादित करने का प्रयास करता है जो पहले से ही किसी अन्य उपयोगकर्ता द्वारा लॉक किया गया है, तो Microsoft Access एक संदेश प्रदर्शित करेगा जो दर्शाता है कि ऑब्जेक्ट पहले से ही उपयोग में है। जैसे ही उपयोगकर्ता डेटाबेस खोलते और बंद करते हैं और लॉक किए गए ऑब्जेक्ट में परिवर्तन करते हैं, एलडीबी फ़ाइल अपडेट हो जाती है।

## संदर्भ
* [एलडीबी फ़ाइल क्या है?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

