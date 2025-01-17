{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XDELTA फ़ाइल - xdelta डिफरेंशियल फ़ाइल - .xdelta फ़ाइल क्या है और इसे कैसे खोलें?",
  "description" : "xdelta डिफरेंशियल फ़ाइल के बारे में जानें और इसे कैसे खोलें।",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta-hi",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## XDELTA फ़ाइल क्या है?

XDELTA फ़ाइल प्रारूप दो अन्य फ़ाइलों के बीच द्विआधारी अंतर रखता है और xdelta टूल द्वारा उत्पन्न होता है, जो डेल्टा एन्कोडिंग के लिए एक कमांड-लाइन उपयोगिता है, जिसमें दो फ़ाइलों के बीच अंतर की गणना करना और उन अंतरों को एक कॉम्पैक्ट प्रारूप में एन्कोड करना शामिल है। XDELTA फ़ाइलें मूल फ़ाइल और अद्यतन फ़ाइल के बीच परिवर्तन या अंतर का प्रतिनिधित्व करने वाले बाइनरी डेटा को संग्रहीत करती हैं। XDELTA फ़ाइल में बाइनरी डेटा एक फ़ाइल (मूल) को दूसरी फ़ाइल (अद्यतन या पैच किए गए संस्करण) में बदलने के लिए आवश्यक परिवर्तनों का प्रतिनिधित्व करता है।

वीडियो गेम के लिए संशोधन (मोड) वितरित करने के लिए गेमिंग समुदाय में XDELTA फ़ाइलों का अक्सर उपयोग किया जाता है। इन मॉड में कॉस्मेटिक बदलावों से लेकर गेमप्ले यांत्रिकी में महत्वपूर्ण बदलाव तक कुछ भी शामिल हो सकता है। XDELTA फ़ाइलें उपयोगकर्ताओं को XDELTA फ़ाइल में निर्दिष्ट परिवर्तनों के साथ मूल गेम फ़ाइलों को पैच करके इन संशोधनों को अपने गेम इंस्टॉलेशन में लागू करने की अनुमति देती हैं।

## xdelta

`xdelta` एक कमांड-लाइन उपयोगिता है जिसका उपयोग डेल्टा एन्कोडिंग और डिकोडिंग के लिए किया जाता है; इसका उपयोग मुख्य रूप से दो फ़ाइलों के बीच बाइनरी पैच बनाने और लागू करने के लिए किया जाता है, जिन्हें अक्सर डेल्टा पैच या एक्सडेल्टा पैच कहा जाता है; ये पैच मूल फ़ाइल और संशोधित या अद्यतन संस्करण के बीच अंतर दर्शाते हैं, जिससे अपडेट के कुशल वितरण की अनुमति मिलती है, खासकर उन परिदृश्यों में जहां बैंडविड्थ या भंडारण स्थान सीमित है।

यहां `xdelta` की मुख्य कार्यप्रणाली का संक्षिप्त विवरण दिया गया है:

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

`xdelta` का उपयोग आमतौर पर विभिन्न परिदृश्यों में किया जाता है, जैसे सॉफ़्टवेयर अपडेट वितरित करना, वीडियो गेम को पैच करना और एम्बेडेड डिवाइस या नेटवर्क उपकरणों में सिस्टम फ़ाइलों को अपडेट करना। यह बैंडविड्थ उपयोग और भंडारण आवश्यकताओं को कम करते हुए फ़ाइल अपडेट को प्रबंधित करने का एक लचीला और कुशल तरीका प्रदान करता है।

## xdeltaui

xdeltaui XDELTA पैच को प्रबंधित और लागू करने के लिए एक ग्राफिकल यूजर इंटरफ़ेस (GUI) एप्लिकेशन है। xdelta gui उपयोगकर्ताओं को XDELTA फ़ाइलों के साथ इंटरैक्ट करने और उन्हें संबंधित मूल फ़ाइलों पर लागू करने, उन्हें प्रभावी ढंग से पैच करने या अपडेट करने के लिए एक उपयोगकर्ता-अनुकूल इंटरफ़ेस प्रदान करता है।

xdelta के कमांड-लाइन संस्करण के विपरीत, जो टेक्स्ट-आधारित कमांड के माध्यम से संचालित होता है, xdeltaui XDELTA फ़ाइलों को संभालने का अधिक सहज तरीका प्रदान करता है, खासकर उन उपयोगकर्ताओं के लिए जो कमांड-लाइन इंटरफेस से परिचित नहीं हैं या ग्राफिकल टूल पसंद करते हैं।

xdeltaui के साथ, उपयोगकर्ता आमतौर पर मूल फ़ाइल का चयन करना, XDELTA पैच फ़ाइल का चयन करना और अद्यतन फ़ाइल उत्पन्न करने के लिए पैच लागू करना जैसे कार्य कर सकते हैं। यह वीडियो गेम या अन्य सॉफ़्टवेयर अनुप्रयोगों के लिए मॉड या अपडेट इंस्टॉल करने के लिए विशेष रूप से उपयोगी हो सकता है।

## एक्सडेल्टा डाउनलोड

लिनक्स सिस्टम पर, आप `xdelta` को स्थापित करने के लिए `apt`, `yum`, या `dnf` जैसे पैकेज प्रबंधकों का उपयोग कर सकते हैं। उदाहरण के लिए, उबंटू पर, आप निम्नलिखित कमांड का उपयोग कर सकते हैं:

```
sudo apt-get install xdelta3
```

## एक्सडेल्टा का उपयोग कैसे करें

`xdelta` का उपयोग करने के लिए, आपको आमतौर पर इन सामान्य चरणों का पालन करना होगा:

1.  **डाउनलोड और इंस्टॉल करें**: सबसे पहले, सुनिश्चित करें कि आपके सिस्टम पर `xdelta` इंस्टॉल है। आप इसे इसकी आधिकारिक वेबसाइट, पैकेज प्रबंधकों या अन्य विश्वसनीय स्रोतों से डाउनलोड कर सकते हैं।
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **एक पैच बनाना**:
    
- अपना कमांड-लाइन इंटरफ़ेस (टर्मिनल या कमांड प्रॉम्प्ट) खोलें।
- पैच बनाने के लिए उचित विकल्पों के साथ `xdelta` कमांड का उपयोग करें। मूल वाक्यविन्यास है:
               
```
एक्सडेल्टा डेल्टा<original_file><updated_file><patch_output_file>
```
        
बदलें `<original_file> ` मूल फ़ाइल के पथ के साथ, `<updated_file> ` अद्यतन फ़ाइल के पथ के साथ, और `<patch_output_file> ` पैच फ़ाइल के लिए वांछित नाम के साथ।
- उदाहरण:
               
```
xdelta delta मूल_फ़ाइल अपडेटेड_फ़ाइल पैच.xdelta
```
        
4.  **पैच लगाना**:
    
- सुनिश्चित करें कि आपके पास मूल फ़ाइल और पैच फ़ाइल उपलब्ध है।
- अपना कमांड-लाइन इंटरफ़ेस खोलें।
- पैच लागू करने के लिए उचित विकल्पों के साथ `xdelta` कमांड का उपयोग करें। मूल वाक्यविन्यास है:
        
      
```
एक्सडेल्टा पैच<original_file><patch_file><output_file>
```
        
बदलें `<original_file> ` मूल फ़ाइल के पथ के साथ, `<patch_file> ` पैच फ़ाइल के पथ के साथ, और `<output_file> `आउटपुट फ़ाइल के लिए वांछित नाम के साथ।
- उदाहरण:
                
```
xdelta पैच मूल_फ़ाइल पैच.xdelta अद्यतन_फ़ाइल
```
        
5.  **सहायता देखना**: यदि आपको विशिष्ट विकल्पों या आदेशों के साथ सहायता की आवश्यकता है, तो आप उपयोग की जानकारी और उपलब्ध विकल्पों को प्रदर्शित करने के लिए `-help` विकल्प के साथ `xdelta` कमांड का उपयोग कर सकते हैं।
    
## XDELTA फ़ाइल कैसे खोलें

XDELTA फ़ाइलें सीधे खोलने के लिए अभिप्रेत नहीं हैं। यदि आप किसी गेम या किसी अन्य फ़ाइल पर XDELTA पैच लागू करना चाहते हैं, तो आपके पास या तो xdelta का उपयोग करने का विकल्प है, जो कई प्लेटफार्मों पर संगत है, या xdelta UI, जो विशेष रूप से विंडोज उपयोगकर्ताओं के लिए डिज़ाइन किया गया है।

## संदर्भ
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)


