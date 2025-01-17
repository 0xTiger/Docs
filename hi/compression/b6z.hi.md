{
  "date" : "2019-10-11",
  "keywords" :[ "b6z फ़ाइल", "b6z फ़ाइल स्वरूप", "b6z फ़ाइल क्या है", "फ़ाइल", "b6z उदाहरण", "b6z फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - B6ZIP संग्रह फ़ाइल स्वरूप",
  "description":"B6Z फ़ाइल स्वरूप और API के बारे में जानें जो B6Z फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## B6Z फ़ाइल क्या है?

.b6z एक्सटेंशन वाली फ़ाइल एक संपीड़ित संग्रह फ़ाइल है जिसे macOS सॉफ़्टवेयर एप्लिकेशन [B6Zip](http://b6zip.com) बनाया गया है जिसका उपयोग फ़ाइलों को संपीड़ित और विघटित करने के लिए किया जाता है। यह तुलनात्मक रूप से नया संग्रह प्रारूप है जो उच्च संपीड़न राशन की अनुमति देता है। B6Z में ओपन आर्किटेक्चर है और यह 900000 PB तक के फाइल साइज को सपोर्ट करता है। यह डेटा कम्प्रेशन, एरर रिकवरी और फाइल स्पैनिंग को सपोर्ट करता है। B6Zip उपयोगिता सॉफ्टवेयर, B6Z सहित विभिन्न प्रकार की संपीड़ित फ़ाइलों को खोलने के लिए MacOS पर मुफ्त में उपलब्ध है।

## B6Z फ़ाइल स्वरूप

B6Z फ़ाइल स्वरूप खुले आर्किटेक्चर पर आधारित है और AES-256 एन्क्रिप्शन एल्गोरिथम के साथ ठोस संपीड़न प्रदान करता है। यह LZMA2 को डिफ़ॉल्ट संपीड़न विधि के रूप में उपयोग करता है, लेकिन अनुसरण के रूप में अन्य संपीड़न विधियों का भी समर्थन करता है।

|विधि|विवरण|
---|---|
|LZMA |LZ77 एल्गोरिथम का अनुकूलित संस्करण|
|एलजेडएमए2| LZMA का बेहतर संस्करण|
|डिफ्लेट| नियमित LZ77 एल्गोरिथम|
|बीज़िप2| मानक बीडब्ल्यूटी एल्गोरिथम|
|पीपीएमडी| दिमित्री शकरीन की PPMdH|

B6Zip उपयोगिता इन सभी संपीड़न मानकों का समर्थन करती है और उच्च गति के परिणामस्वरूप अत्यधिक अनुकूलित है। यह [ZIP](/hi/compression/zip/), [TAR](/hi/compression/tar/) और [RAR](/hi/compression/rar/) फ़ाइल स्वरूपों के साथ काम करने का समर्थन करता है। B6Z फ़ाइलों में MIME प्रकार का अनुप्रयोग/x-b6z-संपीड़ित होता है।

## संदर्भ

* [बी6ज़िप](http://b6zip.com)

