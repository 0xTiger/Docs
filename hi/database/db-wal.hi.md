{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "DB-WAL फ़ाइल स्वरूप और API के बारे में जानें जो DB-WAL फ़ाइलें बना और खोल सकते हैं।",
  "title" : "DB-WAL फ़ाइल स्वरूप - SQLite डेटाबेस राइट-अहेड लॉग फ़ाइल",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-hi",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## DB-WAL फ़ाइल क्या है?

फ़ाइल एक्सटेंशन .db-wal SQLite से संबद्ध है, जो एक लोकप्रिय ओपन-सोर्स रिलेशनल डेटाबेस प्रबंधन प्रणाली है। WAL फ़ाइल स्वरूप (राइट-अहेड लॉग के लिए संक्षिप्त) SQLite द्वारा उपयोग किए जाने वाले पारंपरिक रोलबैक जर्नल का एक विकल्प है। यह अधिक समवर्ती नियंत्रण प्रदान करता है, जिससे कई प्रक्रियाओं को एक ही समय में डेटाबेस को पढ़ने की अनुमति मिलती है, जबकि अभी भी क्रैश-रिकवरी क्षमताएं प्रदान होती हैं। .db-wal फ़ाइल का उपयोग डेटाबेस में किए गए परिवर्तनों को संग्रहीत करने के लिए किया जाता है जो अभी तक मुख्य डेटाबेस फ़ाइल (.db एक्सटेंशन के साथ) के लिए प्रतिबद्ध नहीं हैं।

## सामान्य वाल प्रारूप

वाल (राइट-अहेड लॉग) फ़ाइल स्वरूप में, डेटाबेस में किए गए परिवर्तन मुख्य डेटाबेस फ़ाइल में प्रतिबद्ध होने से पहले वाल फ़ाइल में लिखे जाते हैं। यह डेटाबेस तक अधिक समवर्ती पहुंच की अनुमति देता है, क्योंकि परिवर्तन किए जाने के दौरान कई प्रक्रियाएं डेटाबेस से पढ़ सकती हैं। इसके अतिरिक्त, वाल फ़ाइल प्रारूप क्रैश-रिकवरी क्षमताएं प्रदान करता है, जिससे अप्रत्याशित शटडाउन की स्थिति में डेटाबेस को पिछली स्थिति में वापस लाया जा सकता है।

## डीबी-वाल और वाल प्रारूप के बीच अंतर

.db-wal और WAL फ़ाइल स्वरूप दोनों SQLite से संबद्ध हैं, जो एक लोकप्रिय ओपन-सोर्स रिलेशनल डेटाबेस प्रबंधन प्रणाली है। हालाँकि, दोनों के बीच एक सूक्ष्म अंतर है।

.db-wal फ़ाइल मूलतः एक WAL फ़ाइल है, लेकिन एक भिन्न फ़ाइल एक्सटेंशन के साथ। .db-wal फ़ाइल का उपयोग डेटाबेस में किए गए परिवर्तनों को संग्रहीत करने के लिए किया जाता है जो अभी तक मुख्य डेटाबेस फ़ाइल (.db एक्सटेंशन के साथ) के लिए प्रतिबद्ध नहीं हैं, जबकि WAL फ़ाइल प्रारूप का उपयोग डेटाबेस परिवर्तनों के राइट-फ़ॉरवर्ड लॉग को संग्रहीत करने के लिए किया जाता है। .

दूसरे शब्दों में, .db-wal फ़ाइल एक विशिष्ट प्रकार की WAL फ़ाइल है जिसका उपयोग SQLite डेटाबेस द्वारा डेटाबेस में किए गए परिवर्तनों को संग्रहीत करने के लिए किया जाता है जो अभी तक मुख्य डेटाबेस फ़ाइल के लिए प्रतिबद्ध नहीं हैं। वाल फ़ाइल स्वरूप इस प्रकार के फ़ाइल स्वरूप के लिए सामान्य शब्द है।

तो, वाल फ़ाइल प्रारूप के लिए सामान्य शब्द है, .db-wal SQLite डेटाबेस द्वारा उपयोग किए जाने वाले वाल फ़ाइल प्रारूप का एक विशिष्ट कार्यान्वयन है।

## संदर्भ
* [वाल-मोड फ़ाइल प्रारूप](https://www.sqlite.org/walformat.html)

* [राइट-अहेड लॉगिंग](https://www.sqlite.org/wal.html)

