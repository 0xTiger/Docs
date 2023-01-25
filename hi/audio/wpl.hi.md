{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl फ़ाइल", "एक्सटेंशन", "प्रारूप", "WPL फ़ाइल क्या है", "संगीत", "wpl फ़ाइल स्वरूप"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WPL फ़ाइल स्वरूप और API के बारे में जानें जो WPL फ़ाइलें बना, परिवर्तित और खोल सकते हैं।",
  "title" :"WPL - विंडोज मीडिया प्लेयर प्लेलिस्ट फाइल",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## WPL फ़ाइल क्या है?

.wpl एक्सटेंशन वाली फाइल में माइक्रोसॉफ्ट विंडोज मीडिया प्लेयर पर चलने वाले गानों की प्लेलिस्ट होती है। ये फ़ाइलें आमतौर पर उपयोगकर्ताओं द्वारा अपने वीडियो और ऑडियो संग्रह के लिए बनाई जाती हैं। WPL फ़ाइल में लिखी गई सामग्री, .wpl फ़ाइल के निर्माता द्वारा चुनी गई मल्टीमीडिया फ़ाइलों के लिए केवल निर्देशिका पथ या स्थान है, इसलिए मीडिया प्लेयर एप्लिकेशन अपने निर्देशिका स्थानों से मल्टीमीडिया सामग्री को तुरंत ढूंढ और चला सकता है।

## डब्ल्यूपीएल फ़ाइल प्रारूप

WPL (Windows Media Player Playlist) एक मालिकाना फ़ाइल स्वरूप है जिसका उपयोग Microsoft Windows Media Player संस्करण 9 या उससे अधिक में किया जाता है। यह एक कंप्यूटर फ़ाइल स्वरूप है जो मल्टीमीडिया प्लेलिस्ट को संग्रहीत करता है। डिफ़ॉल्ट रूप से, प्लेलिस्ट को .wpl (विंडोज मीडिया प्लेयर प्लेलिस्ट) एक्सटेंशन के साथ सहेजा जाता है। आप इसके बजाय [.m3u](/hi/audio/m3u) एक्सटेंशन का उपयोग कर सकते हैं, यदि आप अपने डेटा डिस्क को किसी ऐसे उपकरण में चलाना चाहते हैं जो इस एक्सटेंशन का समर्थन नहीं करता है। WPL फ़ाइल के तत्वों को XML प्रारूप में दर्शाया जाता है।

शीर्ष-स्तरीय तत्व "स्माइल" निर्दिष्ट करता है कि फ़ाइल के तत्व सिंक्रोनाइज़्ड मल्टीमीडिया इंटीग्रेशन लैंग्वेज (SMIL) संरचना का पालन करते हैं। फ़ाइल को .wpl एक्सटेंशन के साथ बनाया और सहेजा गया है और इसका MIME प्रकार application/vnd.ms-wpl है।

### डब्ल्यूपीएल उदाहरण

यहाँ एक wpl फ़ाइल का एक उदाहरण है:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## संदर्भ ##

* [MPEG-1 ऑडियो लेयर II - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)
