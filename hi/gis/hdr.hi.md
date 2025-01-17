{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एचडीआर फ़ाइल- ईएसआरआई बीआईएल हेडर फ़ाइल प्रारूप",
  "description":"एचडीआर फ़ाइल क्या है?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## एचडीआर फ़ाइल क्या है?

एचडीआर फ़ाइल एक जीआईएस हेडर फ़ाइल है जिसमें बैंड इंटरलीव्ड बाय लाइन (.बीआईएल) फ़ाइल के लिए हेडर जानकारी होती है। यह छवि डेटा का वर्णन करता है और इसका नाम छवि फ़ाइल के समान ही है। एचडीआर फ़ाइल में प्रविष्टियों का एक सेट शामिल होता है, जिनमें से प्रत्येक छवि की एक विशेष विशेषता का वर्णन करता है। एचडीआर फ़ाइल एक अलग जियोरेफ़रेंसिंग फ़ाइल के संयोजन में वास्तविक दुनिया के समन्वय में अनुवाद के लिए बीआईएल फ़ाइल के लेआउट और स्वरूपण का वर्णन करती है।

## एचडीआर फ़ाइल स्वरूप

HDR फ़ाइलें ASCII टेक्स्ट फ़ाइल स्वरूप में सहेजी जाती हैं। इसमें प्रविष्टियों का एक सेट होता है जहां प्रत्येक प्रविष्टि छवि की एक विशेष विशेषता का वर्णन करती है। प्रत्येक एचडीआर फ़ाइल में निम्नलिखित प्रारूप होता है:

```
<keyword> <value>
```

`<keyword> ` - यह उस विशेष विशेषता को इंगित करता है जिसे सेट किया जा रहा है
`<value> ` - यह वह मान है जिस पर विशेषता सेट की जा रही है

शीर्षलेख में प्रविष्टियों के क्रम पर कोई सीमा नहीं है। हालाँकि, एचडीआर पाठकों द्वारा उपयोग की जाने वाली पार्सिंग विधि का अनुपालन करने के लिए प्रत्येक प्रविष्टि को लाइन की एक अलग पंक्ति पर होना चाहिए।

## एचडीआर फ़ाइल में प्रयुक्त कीवर्ड का सारांश

|कीवर्ड |स्वीकार्य मान |डिफ़ॉल्ट|
---|---|---|
|nrows |कोई भी पूर्णांक > 0| कोई नहीं
|एनसीओएल |कोई भी पूर्णांक > 0| कोई नहीं
|nbands |कोई भी पूर्णांक > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|बाइटऑर्डर| I = Intel;M = Motorola |होस्ट मशीन के समान|
|लेआउट| बिल, बीआईपी, बीएसक्यू| बिल|
|स्किपबाइट्स| कोई भी पूर्णांक ≥ 0| 0
|ulxmap |कोई भी वास्तविक संख्या| 0|
|ulymap |कोई भी वास्तविक संख्या |nrows - 1|
|xdim |कोई वास्तविक संख्या| 1
|ydim |कोई वास्तविक संख्या| 1
|बैंड्रोबाइट्स |कोई पूर्णांक > 0| सबसे छोटा पूर्णांक ≥ (ncols x nbits) / 8|
|कुलरोबाइट्स |कोई पूर्णांक > 0| बीआईएल के लिए: एनबैंड्स एक्स बैंड्रोबाइट्स; बीआईपी के लिए: सबसे छोटा पूर्णांक ≥ (एनसीओएलएस एक्स एनबैंड्स एक्स एनबिट्स) / 8|
|बैंडगैपबाइट्स |कोई पूर्णांक ≥ 0| 0|

## संदर्भ

* [एचआरडी फ़ाइल प्रारूप - आर्कजीआईएस](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

