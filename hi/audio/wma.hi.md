{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "फ़ाइल", "एक्सटेंशन", "प्रारूप", "ऑडियो इंटरचेंज फ़ाइल स्वरूप", "संगीत"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WMA फ़ाइल स्वरूप और API के बारे में जानें जो WMA फ़ाइलें बना और खोल सकते हैं।",
  "title" :"WMA - विंडोज मीडिया ऑडियो फाइल",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## WMA फ़ाइल क्या है?

.wma एक्सटेंशन वाली फ़ाइल एक ऑडियो फ़ाइल का प्रतिनिधित्व करती है जो उन्नत सिस्टम प्रारूप (ASF) प्रारूप में सहेजी जाती है। एएसएफ माइक्रोसॉफ्ट का मालिकाना प्रारूप है जिसमें विंडोज मीडिया ऑडियो 9 द्वारा एन्कोड किए गए बिटस्ट्रीम शामिल हैं। ऑडियो सामग्री के अलावा, डब्लूएमए फ़ाइल में मेटाडेटा ऑब्जेक्ट्स जैसे शीर्षक, एल्बम, कलाकार और ट्रैक की शैली भी शामिल है। WMA फ़ाइलें मुख्य रूप से [.mp3](/hi/audio/mp3/) फ़ाइलों के समान वेब पर स्ट्रीमिंग के लिए उपयोग की जाती हैं।

## अर्थोपाय अग्रिम फ़ाइल स्वरूप

WMA फ़ाइल बाइनरी फ़ाइल स्वरूप है और ASF फ़ाइल स्वरूप में निहित है। यह MP3 फ़ाइलों द्वारा उपयोग किए जाने वाले ID3 टैग के समान फ़ाइल के बारे में मेटाडेटा के एन्कोडिंग को निर्दिष्ट करता है। WMA कोडेक 2008 से Microsoft द्वारा अपने संरक्षित इंटरऑपरेबल फ़ाइल फ़ॉर्मेट (PIFF) में उपयोग में है। हालाँकि, इसे संबंधित उद्योग मानकों जैसे DECE UltraViolet और MPEG-DASH द्वारा मानकीकृत ऑडियो कोडेक के रूप में घोषित नहीं किया गया है।

### अर्थोपाय अग्रिम प्रकार विशिष्ट डेटा

विंडोज मीडिया ऑडियो कोडेक के लिए टाइप-विशिष्ट जानकारी स्ट्रीम गुण ऑब्जेक्ट के प्रकार-विशिष्ट डेटा के भाग के रूप में निम्न स्वरूप में संग्रहीत की जाती है।

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## संदर्भ

* [एएसएफ अवलोकन - माइक्रोसॉफ्ट](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)
