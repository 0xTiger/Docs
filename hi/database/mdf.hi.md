{
  "date" : "2020-11-11",
  "keywords" :[ "एमडीएफ", "एक्सटेंशन", "फाइल", "फाइल फॉर्मेट", "डेटाबेस फाइल टाइप", "डेटाबेस फाइल फॉर्मेट", "डेटाबेस फाइल्स"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MDF फ़ाइल स्वरूप और API के बारे में जानें जो MDF फ़ाइलें बना और खोल सकते हैं।",
  "title" :"MDF फ़ाइल स्वरूप - SQL सर्वर मास्टर डेटाबेस फ़ाइल",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## एमडीएफ फाइल क्या है?

.mdf एक्सटेंशन वाली फ़ाइल एक मास्टर डेटाबेस फ़ाइल है जिसका उपयोग [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) द्वारा उपयोगकर्ता डेटा संग्रहीत करने के लिए किया जाता है। यह प्रमुख महत्व का है क्योंकि सभी डेटा इस फ़ाइल में संग्रहीत हैं। MDF फ़ाइल उपयोगकर्ता डेटा को संबंधपरक डेटाबेस में प्रपत्र कॉलम, पंक्तियों, फ़ील्ड, अनुक्रमणिका, दृश्य और तालिकाओं में संग्रहीत करती है। SQL सर्वर डेटाबेस के प्रदर्शन पर सकारात्मक प्रभाव डालने के लिए ऑटोग्रो और ऑटोश्रिंक सेटिंग्स को सेट करने की अनुमति देता है। एमडीएफ फाइलों को माइक्रोसॉफ्ट एसक्यूएल सर्वर का उपयोग करके डेटाबेस से लोड और संलग्न किया जा सकता है। एमडीएफ फाइलों में एप्लिकेशन/ऑक्टेट-स्ट्रीम माइम प्रकार होता है।

## एमडीएफ फ़ाइल प्रारूप

SQL सर्वर में डेटा संग्रहण की मूलभूत इकाई एक पृष्ठ है। एक डेटाबेस असाइन किया गया संग्रहण पृष्ठ 0 से n तक के तार्किक पृष्ठों में विभाजित है। एक सिंगल पेज 96 बाइट्स हेडर से शुरू होता है जिसमें पेज आईडी, पेज से संबंधित संरचना का प्रकार, पेज में रिकॉर्ड्स की संख्या और पिछले और अगले पेज के पॉइंटर्स शामिल होते हैं।

### फ़ाइल संरचना

MDF फ़ाइल में निम्न डेटा संरचना होती है।

* पेज 0: हैडर
* पेज 1: पहला पीएफएस
* पेज 2: पहला GAM
* पेज 3: पहला एसजीएएम
* पेज 4: अप्रयुक्त
* पेज 5: अप्रयुक्त
* पेज 6: पहला डीसीएम
* पेज 7: पहला बीसीएम

#### फाइल हैडर

सभी फाइलों के पेज नंबर 0 में एक हेडर होता है जो फाइल के बारे में मेटाडेटा को स्टोर करता है।

#### पेज फ्री स्पेस (PFS)
पीएफएस आवंटन स्थिति की पहचान करता है और खाली स्थान की मात्रा निर्धारित करता है।

* बिट 1: इंगित करता है कि पृष्ठ आवंटित किया गया है या नहीं।
* बिट 2: इंगित करता है कि पृष्ठ मिश्रित सीमा से है या नहीं।
* बिट 3: इंगित करता है कि यह पृष्ठ एक IAM पृष्ठ है।
* बिट 4: इंगित करता है कि इस पृष्ठ में भूत रिकॉर्ड हैं
* बिट्स 5 से 7: एक संयुक्त तीन-बिट मान, जो पृष्ठ की पूर्णता को निम्नानुसार दर्शाता है:
*0: पेज खाली है
* 1: पेज 1-50% भरा हुआ है
* 2: पेज 51-80% भरा हुआ है
* 3: पेज 81-95% भरा हुआ है
* 4: पेज 96-100% भरा हुआ है

## संदर्भ

* [डेटाबेस फ़ाइलें और फ़ाइल समूह](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [डेटाबेस डिटैच और अटैच - SQL सर्वर](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [एसक्यूएल सर्वर डेटा फ़ाइल एनाटॉमी का विश्लेषण](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

