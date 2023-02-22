{
  "date" : "2020-11-11",
  "keywords" :[ "एनडीएफ", "एक्सटेंशन", "फाइल", "फाइल फॉर्मेट", "डेटाबेस फाइल टाइप", "डेटाबेस फाइल फॉर्मेट", "डेटाबेस फाइल्स"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MDF फ़ाइल स्वरूप और API के बारे में जानें जो NDF फ़ाइलें बना और खोल सकते हैं।",
  "title" :"NDF फ़ाइल स्वरूप - SQL सर्वर मास्टर डेटाबेस फ़ाइल",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## एनडीएफ फाइल क्या है?

.ndf एक्सटेंशन वाली फ़ाइल एक द्वितीयक डेटाबेस फ़ाइल है जिसका उपयोग [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) द्वारा उपयोगकर्ता डेटा संग्रहीत करने के लिए किया जाता है। NDF सेकेंडरी स्टोरेज फ़ाइल है क्योंकि SQL सर्वर उपयोगकर्ता द्वारा निर्दिष्ट डेटा को प्राथमिक स्टोरेज फ़ाइल में संग्रहीत करता है जिसे [MDF](/hi/database/mdf/) के रूप में जाना जाता है। NDF डेटा फ़ाइल वैकल्पिक है और प्राथमिक MDF फ़ाइल सभी आवंटित स्थान का उपयोग करने की स्थिति में डेटा संग्रहण को प्रबंधित करने के लिए उपयोगकर्ता-परिभाषित है। यह आमतौर पर अलग डिस्क पर संग्रहीत होता है और कई भंडारण उपकरणों में फैल सकता है। एनडीएफ फाइलें खोलने के लिए एमडीएफ फाइलों की मौजूदगी जरूरी है।

## एनडीएफ फ़ाइल प्रारूप

NDF फ़ाइल स्वरूप [MDF](/hi/database/mdf) से अलग नहीं है और डेटा संग्रहण की मूलभूत इकाई के रूप में पृष्ठों का उपयोग करता है। प्रत्येक पृष्ठ 96 बाइट्स हेडर से शुरू होता है जिसमें शामिल हैं:

*पेज आईडी
*संरचना का प्रकार
* पृष्ठों में रिकॉर्ड की संख्या
* पिछले और अगले पृष्ठों की ओर इशारा करता है

### एनडीएफ फ़ाइल संरचना

MDF फ़ाइल में निम्न डेटा संरचना होती है।

* पेज 0: हैडर
* पेज 1: पहला पीएफएस
* पेज 2: पहला GAM
* पेज 3: पहला एसजीएएम
* पेज 4: अप्रयुक्त
* पेज 5: अप्रयुक्त
* पेज 6: पहला डीसीएम
* पेज 7: पहला बीसीएम

#### एनडीएफ फाइल हैडर

सभी फाइलों के पेज नंबर 0 में एक हेडर होता है जो फाइल के बारे में मेटाडेटा को स्टोर करता है।

#### पेज फ्री स्पेस (PFS)
पीएफएस आवंटन स्थिति की पहचान करता है और खाली स्थान की मात्रा निर्धारित करता है।

* बिट 1: इंगित करता है कि पृष्ठ आवंटित किया गया है या नहीं।
* बिट 2: इंगित करता है कि पृष्ठ मिश्रित सीमा से है या नहीं।
* बिट 3: इंगित करता है कि यह पृष्ठ एक IAM पृष्ठ है।
* बिट 4: इंगित करता है कि इस पृष्ठ में घोस्ट रिकॉर्ड हैं
* बिट्स 5 से 7: एक संयुक्त तीन-बिट मान, जो पृष्ठ की पूर्णता को निम्नानुसार दर्शाता है:
*0: पेज खाली है
* 1: पेज 1-50% भरा हुआ है
* 2: पेज 51-80% भरा हुआ है
* 3: पेज 81-95% भरा हुआ है
* 4: पेज 96-100% भरा हुआ है

## डेटा फ़ाइल पृष्ठ

SQL सर्वर डेटा फ़ाइल में पृष्ठ शून्य (0) से शुरू होते हैं और क्रमिक रूप से बढ़ते हैं। प्रत्येक फ़ाइल को एक अद्वितीय फ़ाइल आईडी संख्या द्वारा पहचाना जाता है। फ़ाइल आईडी और पृष्ठ संख्या जोड़ी विशिष्ट रूप से एक डेटाबेस में एक पृष्ठ की पहचान करती है। एक डेटाबेस में पेज नंबर दिखाने वाला एक उदाहरण, निम्न छवि में है।

{{< figure src="../ndf.png" alt="NDF डेटाबेस फ़ाइल स्वरूप" >}}

यह उदाहरण एक डेटाबेस में पृष्ठ संख्या दिखाता है जिसमें 4-एमबी प्राथमिक डेटा फ़ाइल और 1-एमबी माध्यमिक डेटा फ़ाइल है।

## संदर्भ

* [डेटाबेस फ़ाइलें और फ़ाइल समूह](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [डेटाबेस डिटैच और अटैच - SQL सर्वर](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [एसक्यूएल सर्वर डेटा फ़ाइल एनाटॉमी का विश्लेषण](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)
