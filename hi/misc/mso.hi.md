{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एमएसओ - माइक्रोसॉफ्ट ऑफिस मैक्रो रेफरेंस फाइल",
  "description":"MSO फ़ाइल और API के बारे में जानें जो MSO फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## एमएसओ फाइल क्या है?

एक MSO फ़ाइल एक डेटा कंटेनर फ़ाइल स्वरूप है जो तब बनाया जाता है जब Microsoft Outlook का उपयोग करके एक HTML संदेश भेजा जाता है। यह ज्यादातर Microsoft Office 2000 अनुप्रयोगों के साथ होता है। अधिकांश मामलों में, ईमेल संदेश नाम **Oledata.mso** फ़ाइल के साथ अटैच किया जाता है। ईमेल प्राप्तकर्ता, जब ऐसा ईमेल खोलता है, फ़ाइल को सही ढंग से देख सकता है, भले ही उनके पास समान सॉफ़्टवेयर स्थापित न हो। एमएसओ फाइलें [माइक्रोसॉफ्ट कंपाउंड डॉक्यूमेंट फाइल फॉर्मेट (एमसीडीएफ)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b) को संदर्भित करती हैं।

## माइक्रोसॉफ्ट एमएसओ फ़ाइल स्वरूप

MSO फाइलें Microsoft कंपाउंड डॉक्यूमेंट फाइल फॉर्मेट (MCDF) में सहेजी जाती हैं, जिसे ऑब्जेक्ट लिंकिंग एंड एंबेडिंग (OLE) या कंपोनेंट ऑब्जेक्ट मॉडल (COM) स्ट्रक्चर्ड स्टोरेज कंपाउंड फाइल कार्यान्वयन बाइनरी फाइल फॉर्मेट के रूप में भी जाना जाता है।

### MSO फ़ाइल स्वरूप संरचना

एमएसओ फ़ाइल प्रारूप की आंतरिक फ़ाइल प्रारूप संरचना [संरचना](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd) एमसीडीएफ प्रलेखन का खंड। फ़ाइल आवंटन तालिका (FAT) सेक्टर आवंटन और सेक्टर चेन का प्रबंधन करती है। इसमें 32-बिट सेक्टर नंबरों की एक सरणी होती है। सरणी में प्रत्येक सूचकांक एक सेक्टर संख्या का प्रतिनिधित्व करता है जबकि इसका मान श्रृंखला या एक विशेष मूल्य में अगले सेक्टर का प्रतिनिधित्व करता है।

## संदर्भ

* [COM स्ट्रक्चर्ड स्टोरेज](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [माइक्रोसॉफ्ट कंपाउंड डॉक्यूमेंट फाइल फॉर्मेट (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

