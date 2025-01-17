{
  "date" : "2021-04-10",
  "keywords" :[ "TR3", "फाइल", "एक्सटेंशन", "फाइल फॉर्मेट", "ईबुक", "टोमराइडर", "याडाबाइट"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"TR3 फ़ाइल स्वरूप और API के बारे में जानें जो TR3 फ़ाइलें बना और खोल सकते हैं।",
  "title" :"TR3 - टोमरेडर 3 ईबुक फ़ाइल",
  "linktitle" : "TR3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-04-10"
}

## TR3 फ़ाइल क्या है? ##

TR3 फ़ाइल एक TomeRaider 3 eBook है जो तेज़ खोज और संपीड़न के लिए सहायता प्रदान करती है। यह TomeRaider संबंधित कार्यक्रम के माध्यम से ठीक से काम कर सकता है। Yadabyte इस सॉफ़्टवेयर का डेवलपर है, एक ब्रिटिश सॉफ़्टवेयर और यूके में स्थित वेब डेवलपमेंट कंपनी है। TomeRaider ईबुक रीडर एप्लिकेशन का उपयोग इन TR3 फाइलों की सामग्री के उचित कामकाज और प्रबंधन के लिए किया जा सकता है। यह संबंधित ईबुक रीडर माइक्रोसॉफ्ट विंडोज-आधारित सिस्टम और कई हस्तांतरणीय गैजेट्स पर चलने वाले कंप्यूटरों में स्थापित किया जा सकता है। TR3 फाइल ऑपरेटिंग सिस्टम जैसे विंडोज 10, विंडोज 7, विंडोज 8 / 8.1, विंडोज विस्टा, विंडोज एक्सपी में उपयोग की जाने वाली ईबुक फाइलों के समूह से संबंधित है।

TR3 विशिष्ट **HTML टैग** इस प्रकार हैं:

|टैग|विवरण|
---|---|
|\<new> |पाठ फ़ाइलों से TomeRaider फ़ाइलें बनाने के लिए, नया टैग वह सब है जिसकी आवश्यकता है।<new> टैग पृष्ठों की शुरुआत को परिभाषित करता है।|
|\<CATDEF> ... \</CATDEF> |श्रेणी के नाम को परिभाषित करता है|
|\<META> ... \</META> | एक टैग है जिसका उपयोग फ़ाइल प्रारूप में उपयोग किए गए सभी मेटाडेटा को परिभाषित करने के लिए किया जाता है। इस टैग में कई पैरामीटर शामिल हैं।|
|\<EXPMSG> |यह टैग उस संदेश को नियंत्रित करता है जो किसी फ़ाइल की समय सीमा समाप्त होने पर दिखाई देता है। जब भी कोई उपयोगकर्ता फ़ाइल की समय सीमा समाप्त होने के बाद किसी पृष्ठ को देखने का प्रयास करता है, तो वास्तविक पृष्ठ पाठ के बजाय समाप्ति संदेश दिखाई देता है
|\<DIEMSG> |यह टैग EXPMSG के समान है। फ़ाइल के मरने पर संदेश प्रदर्शित करने के लिए इसका उपयोग किया जाता है।|
|\<ENGMSG> |इस टैग का उपयोग उस संदेश को बनाने के लिए किया जाता है जो एन्क्रिप्टेड पृष्ठों के लिए प्रदर्शित होता है। यदि उपयोगकर्ता किसी एन्क्रिप्ट किए गए पृष्ठ को अनलॉक करने से पहले उसे खोलने का प्रयास करता है तो संदेश पृष्ठ पाठ के बजाय प्रकट होता है
|\<expmsg> ,\<diemsg> तथा \<encmsg> |पेज टेक्स्ट में अनदेखा किया गया। उन्हें पहले फ़ाइल हेडर सेक्शन में रखा जाना चाहिए<new> टैग।|
|\<SELECTION> . \</ SELECTION> |क्वेरी का समर्थन करने के लिए प्रयुक्त। यह टैग पहले . से पहले होना चाहिए<new> उपनाम। यह उपयोगकर्ता की क्वेरी के लिए चयन डेटा संकलित करता है।|
|\<catset> . \</catset> | प्रत्येक विषय के लिए श्रेणी नाम निर्दिष्ट करने के लिए उपयोग किया जाता है।|


## TR3 फ़ाइल खोलने में समस्याएँ ##

यहां कुछ सामान्य मुद्दों की सूची दी गई है जो उत्पन्न हो सकते हैं और फ़ाइल प्रारूप के गलत कार्य का कारण बन सकते हैं:

* बिगड़ी हुई फ़ाइल
* वायरस के कारण संक्रमित फाइल
* संग्रह अभिगम में TR3 फ़ाइल के अनुचित लिंक
* फाइल खोलने के लिए सिस्टम में कोई एक्सेस अधिकार नहीं
* आपके सिस्टम में पुरानी ड्राइव
* TR3 की रिपोर्ट को विंडोज आर्काइव से हटाना
* बेहतर आउटपुट के लिए डेवलपर से संपर्क करना एक बेहतर विकल्प हो सकता है

