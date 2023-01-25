{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"कुंजी फ़ाइल स्वरूप और API के बारे में जानें जो कुंजी फ़ाइलें बना और खोल सकते हैं।",
  "title" :"कुंजी फ़ाइल स्वरूप - गोपनीयता-संवर्धित मेल निजी कुंजी फ़ाइल",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## की फ़ाइल क्या है?

एक कुंजी फ़ाइल एक सुरक्षा तंत्र का निजी हिस्सा है जिसे गोपनीयता-संवर्धित मल (PEM) फ़ाइल स्वरूप में डिस्क में सहेजा जाता है। इसका उपयोग वेब ब्राउज़र और ब्राउज़िंग अनुरोधों को पूरा करने वाले वेब सर्वर के बीच आदान-प्रदान की गई जानकारी को डिक्रिप्ट करने के लिए किया जाता है। एक कुंजी फ़ाइल में एन्कोडेड तार होते हैं जो मानव आंखों के लिए बेकार हैं लेकिन वेब सर्वर पर एसएसएल प्रमाणपत्र के हिस्से के रूप में सूचना विनिमय को एन्क्रिप्ट/डिक्रिप्ट करने का सार हैं। कुंजी फ़ाइलें स्वचालित रूप से उत्पन्न होती हैं और क्लाइंट एंड पर स्थापित होती हैं।

आप किसी भी पाठ संपादक जैसे Microsoft Notepad (Windows), Apple TextEdit (Mac), या GitHub Atom (क्रॉस-प्लेटफ़ॉर्म) के साथ **कुंजी** फ़ाइलें खोल सकते हैं। कुंजी फ़ाइलें [CRT](/hi/web/crt/) और [CER](/hi/web/cer/) फ़ाइल स्वरूपों के समान हैं।

## कुंजी फ़ाइल स्वरूप - अधिक जानकारी

कुंजी फ़ाइलों को सादे पाठ फ़ाइलों के रूप में डिस्क में संग्रहीत किया जाता है, लेकिन एन्कोडेड स्ट्रिंग्स हैं जो पढ़ने के लिए मानव अनुकूल नहीं हैं। व्यावहारिक रूप से, टेक्स्ट एडिटर में खोले जाने पर उपयोगकर्ताओं को स्ट्रिंग्स की शून्य समझ होती है। निजी कुंजी प्रमाणपत्र गोपनीय है और इसे किसी के साथ साझा नहीं किया जाना चाहिए। इंटरनेट पर सूचनाओं के आदान-प्रदान को सुरक्षित करने की पूरी प्रक्रिया में शामिल हैं:

* **सार्वजनिक कुंजी** - ब्राउज़र और वेब सर्वर के बीच डेटा के आदान-प्रदान के लिए उपयोगकर्ता की जानकारी को एन्क्रिप्ट करने के लिए उपयोग किया जाता है
* **निजी कुंजी** - वेब सर्वर द्वारा प्राप्त जानकारी को डिक्रिप्ट करने के लिए उपयोग किया जाता है

SSL प्रमाणपत्र, जिसे X.509 प्रमाणपत्र के रूप में भी जाना जाता है, प्रत्येक वेबसाइट के लिए अद्वितीय होते हैं। निम्नलिखित सिंटैक्स का उपयोग करने वाली प्रमुख फाइलें:

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### कुंजी फ़ाइल उदाहरण

निम्नलिखित निजी कुंजी फ़ाइल का एक उदाहरण है।
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## संदर्भ

* [सार्वजनिक कुंजी, निजी कुंजी और प्रमाणपत्र](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)
