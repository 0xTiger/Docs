{
  "date" : "2020-11-11",
  "keywords" :[ "एलडीएफ", "एक्सटेंशन", "फाइल", "फाइल फॉर्मेट", "डेटाबेस फाइल टाइप", "डेटाबेस फाइल फॉर्मेट", "डेटाबेस फाइल्स"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"एलडीएफ फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एलडीएफ फाइलें बना और खोल सकते हैं।",
  "title" :"LDF - SQL सर्वर मास्टर डेटाबेस फ़ाइल स्वरूप",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## एलडीएफ फाइल क्या है?

.ldf एक्सटेंशन वाली फ़ाइल Microsoft SQL सर्वर द्वारा अनुरक्षित एक लॉग फ़ाइल है जो एक रिलेशनल डेटाबेस मैनेजमेंट सिस्टम (RDBMS) है। प्राथमिक डेटाबेस फ़ाइलों ([MDF](/hi/database/mdf/)) (जैसे सम्मिलन, अद्यतन, विलोपन) पर किए गए सभी लेनदेन LDF फ़ाइल में दर्ज किए जाते हैं। एलडीएफ फाइलें किसी भी डेटाबेस के महत्वपूर्ण घटक हैं। सिस्टम की विफलता के मामले में, लॉग फ़ाइल का उपयोग डेटाबेस को एक सुसंगत स्थिति में पुनर्स्थापित करने के लिए किया जाता है। यदि लेन-देन पूरी तरह से प्रतिबद्ध नहीं हैं, तो लेन-देन लॉग फ़ाइल आकार में बढ़ सकती है। एलडीएफ फाइलें माइक्रोसॉफ्ट एसक्यूएल सर्वर सॉफ्टवेयर एप्लीकेशन के साथ खोली जा सकती हैं।

## एलडीएफ फाइल में रिकॉर्ड किए गए ऑपरेशन

एक SQL लॉग फ़ाइल निम्नलिखित कार्यों को रिकॉर्ड करती है:

* प्रत्येक लेनदेन की शुरुआत और अंत।

* प्रत्येक डेटा डेटा संशोधन (सम्मिलित करें, अपडेट करें या हटाएं)। इसमें सिस्टम टेबल सहित किसी भी टेबल में सिस्टम स्टोर्ड प्रोसीजर या डेटा डेफिनिशन लैंग्वेज (DDL) स्टेटमेंट द्वारा किए गए बदलाव भी शामिल हैं।

* हर हद और पेज आवंटन या डीललोकेशन।

* टेबल या इंडेक्स बनाना या छोड़ना।

## एलडीएफ फ़ाइल प्रारूप

LDF फ़ाइल में SQL सर्वर लेनदेन रिकॉर्ड होते हैं जो लॉग रिकॉर्ड की स्ट्रिंग के रूप में व्यवस्थित होते हैं। प्रत्येक लॉग रिकॉर्ड में एक लॉग अनुक्रम संख्या (LSN) होती है जो पिछले रिकॉर्ड के LSN से अधिक होती है। फ़ाइल में तार एक दूसरे के बाद संयोजित होते हैं। आधुनिक उच्च गति वाले कंप्यूटरों के कारण, जहां LSN2 LSN1 से पहले लॉग फ़ाइल में मौजूद है, वहां रिकॉर्ड डाले जा सकते हैं। चूंकि संचालन एक धारावाहिक में दर्ज किए जाते हैं, एलएसएन 2 द्वारा वर्णित परिवर्तन लॉग रिकॉर्ड एलएसएन 1 के बाद किया गया था। किसी विशेष लेन-देन के रिकॉर्ड को उपयोग किए जाने वाले पॉइंटर्स का उपयोग करके पीछे से जोड़ा जाता है और लेनदेन के रोलबैक को गति देता है।
 

## संदर्भ

* [डेटाबेस फ़ाइलें और फ़ाइल समूह](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [लेन-देन लॉग आर्किटेक्चर और प्रबंधन गाइड](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server-ver15)

