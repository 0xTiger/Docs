{
  "date" : "2021-07-30",
  "keywords" :[ "dlg फ़ाइल", "dlg फ़ाइल स्वरूप", "dlg फ़ाइल क्या है", "फ़ाइल", "dlg उदाहरण", "dlg फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - शेपफाइल शेप इंडेक्स फॉर्मेट",
  "description":"DLG फ़ाइल स्वरूप और API के बारे में जानें जो DLG फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## डीएलजी फाइल क्या है?
.dlg एक्सटेंशन वाली फ़ाइल में डिजिटल लाइन ग्राफ़ होता है जो कि एक कार्टोग्राफ़िक मानचित्र विशेषता है जिसे डिजिटल वेक्टर रूप में दिखाया जाता है जिसे यूएस जियोलॉजिकल सर्वे (USGS) द्वारा प्रशासित किया जाता है। DLG फाइलें दो अलग-अलग स्वरूपों में उपलब्ध हैं:
1. **वैकल्पिक प्रारूप**: उपयोग में आसान प्रारूप जिसमें 80-बाइट तार्किक रिकॉर्ड लंबाई, UTM ग्राउंड कोऑर्डिनेट सिस्टम, और लाइन, नोड और क्षेत्र तत्वों में निहित टोपोलॉजी लिंकेज शामिल हैं।
2. **स्थानिक डेटा स्थानांतरण मानक (एसडीटीएस) प्रारूप**: एक प्रारूप जो विभिन्न कंप्यूटर प्रणालियों के बीच स्थानिक डेटा के हस्तांतरण की सुविधा प्रदान करता है।

## डीएलजी फ़ाइल प्रारूप
DLG फ़ाइल स्वरूप USGS मानचित्रों के लिए डिज़ाइन किया गया है और नौ विभिन्न श्रेणियों की विशेषताओं के साथ बड़े, मध्यवर्ती और छोटे पैमाने पर प्रसारित किया जाता है। डीएलजी फाइलें वैकल्पिक और स्थानिक डेटा ट्रांसफर स्टैंडर्ड (एसडीटीएस) प्रारूपों में आती हैं, जो मैपिंग और जीआईएस अनुप्रयोगों में उपयोग के लिए टोपोलॉजिकल रूप से संरचित होती हैं।
### डीएलजी फ़ाइल प्रारूप के विनिर्देश
DLG फाइलें तीन अलग-अलग पैमानों पर वितरित की जाती हैं:

1. **बड़े पैमाने पर** - सामान्य रूप से इसके अनुरूप हैं:
- यूएसजीएस 7.5- 7.5 मिनट तक
- 1:24,000 और 1:25,000-पैमाने पर स्थलाकृतिक चतुर्भुज मानचित्र श्रृंखला
- अलास्का के लिए 1:63,360-पैमाने पर
- प्यूर्टो रिको के लिए 1:30,000-पैमाने पर
 

2. **इंटरमीडिएट स्केल** - यूएसजीएस से प्राप्त:

- 30- 60 मिनट तक

- 1:100,000-पैमाने पर नक्शा श्रृंखला
3. **छोटा पैमाना** - युनाइटेड स्टेट्स के राष्ट्रीय एटलस के यूएसजीएस 1:2,000,000-पैमाने के अनुभागीय मानचित्रों से व्युत्पन्न
### डेटा श्रेणियाँ
डीएलजी फाइलों में नौ विभिन्न श्रेणियों की परतें या विशेषताएं उपलब्ध हैं:
1. सार्वजनिक भूमि सर्वेक्षण प्रणाली (पीएलएसएस)
2. सीमाएं (बीडी)
3. परिवहन (टीआर)
4. हाइड्रोग्राफी (एचवाई)
5. हिप्सोग्राफी (एचपी)
6. गैर-वनस्पति विशेषताएं (एनवी)
7. सर्वेक्षण नियंत्रण और मार्कर (एसएम)

8. मानव निर्मित विशेषताएं (एमएस)

9. वनस्पति सतह कवर (एससी)

बड़े पैमाने पर DLG फाइलें सभी नौ परतों की पेशकश करती हैं, जबकि मध्यवर्ती स्तर PLSS, BD, TR, HY और HP की पांच परतों की पेशकश करती हैं। छोटे पैमाने के डीएलजी पीएलएसएस, बीडी, टीआर, एचवाई और एमएस की पांच परतों की पेशकश करते हैं।

## संदर्भ

* [डिजिटल लाइन ग्राफ - विकिपीडिया द्वारा)](https://en.wikipedia.org/wiki/Digital_line_graph)


