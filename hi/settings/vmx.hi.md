{
"तारीख": "2023-06-08",
  "keywords": [
"vmx फ़ाइल",
"वीएमएक्स फ़ाइल क्या है",
"vmx फ़ाइल उदाहरण",
"वीएमएक्स फ़ाइल कैसे खोलें",
"vmx फ़ाइल में क्या है",
"vmx फ़ाइल का प्रारूप क्या है",
"फ़ाइल",
"vmx फ़ाइल एक्सटेंशन",
"विस्तार"
],
  "author": {
"display_name": "शकील फ़ैज़"
},
"draft": "false",
"toc": true,
"title": "वीएमएक्स फ़ाइल प्रारूप - वीएमवेयर वर्चुअल मशीन कॉन्फ़िगरेशन फ़ाइल",
  "description":"वीएमएक्स प्रारूप और एपीआई के बारे में जानें जो वीएमएक्स फाइलें बना और खोल सकते हैं।",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent" : "settings"
}
},
"lastmod": "2023-06-08"
}

## वीएमएक्स फ़ाइल क्या है?

वीएमएक्स फ़ाइल, जिसे वर्चुअल मशीन कॉन्फ़िगरेशन फ़ाइल के रूप में भी जाना जाता है, एक सादा पाठ फ़ाइल है जिसका उपयोग वीएमवेयर वर्चुअलाइजेशन सॉफ़्टवेयर द्वारा वर्चुअल मशीन (वीएम) की सेटिंग्स और कॉन्फ़िगरेशन को परिभाषित करने के लिए किया जाता है। वीएमएक्स फाइलों में वीएम के हार्डवेयर कॉन्फ़िगरेशन, वर्चुअल डिस्क मैपिंग, नेटवर्क सेटिंग्स और अन्य पैरामीटर जैसी जानकारी होती है।

## वीएमएक्स फ़ाइल उदाहरण

यहां एक उदाहरण दिया गया है कि वीएमएक्स फ़ाइल कैसी दिख सकती है:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## वीएमएक्स फ़ाइल में क्या है?

VMX फ़ाइल में वर्चुअल मशीन (VM) के लिए विभिन्न कॉन्फ़िगरेशन सेटिंग्स होती हैं। यहां VMX फ़ाइल में आमतौर पर पाई जाने वाली कुछ सेटिंग्स दी गई हैं:

- `.एनकोडिंग:` फ़ाइल में प्रयुक्त वर्ण एन्कोडिंग निर्दिष्ट करता है।
- `config.version:` VMX फ़ाइल स्वरूप के संस्करण को इंगित करता है।
- `virtualHW.version:` VM के लिए वर्चुअल हार्डवेयर का संस्करण निर्दिष्ट करता है।
- `guestOS:` VM में स्थापित अतिथि ऑपरेटिंग सिस्टम को निर्दिष्ट करता है।
- `मेमसाइज:` वीएम को आवंटित मेमोरी की मात्रा को परिभाषित करता है।
- `डिस्प्लेनेम:` वीएम के लिए डिस्प्ले नाम या लेबल सेट करता है।
- `पावरटाइप:` विभिन्न परिचालनों (पावर ऑफ, पावर ऑन, रीसेट, सस्पेंड) के लिए पावर व्यवहार को परिभाषित करता है।
- `फ्लोपीएक्स:` फ्लॉपी ड्राइव से संबंधित कॉन्फ़िगरेशन सेटिंग्स, जैसे उपस्थिति और फ़ाइल मैपिंग।
- `numvcpus:` VM को निर्दिष्ट वर्चुअल सीपीयू की संख्या निर्दिष्ट करता है।
- `scsiX:` SCSI नियंत्रकों और उनसे संबंधित वर्चुअल डिस्क के लिए कॉन्फ़िगरेशन सेटिंग्स।
- `ईथरनेटएक्स:` वर्चुअल डिवाइस प्रकार, नेटवर्क नाम और पता प्रकार सहित नेटवर्क एडेप्टर के लिए कॉन्फ़िगरेशन सेटिंग्स।
- `ideX:` IDE नियंत्रकों और उनसे संबंधित वर्चुअल डिस्क के लिए कॉन्फ़िगरेशन सेटिंग्स।
- `usbX:` USB उपकरणों के लिए कॉन्फ़िगरेशन सेटिंग्स, जैसे उपस्थिति और कनेक्शन विवरण।
- `ध्वनि:` वर्चुअल ध्वनि एडाप्टर के लिए कॉन्फ़िगरेशन सेटिंग्स।
- `tools.syncTime:` इंगित करता है कि होस्ट सिस्टम के साथ समय सिंक्रनाइज़ेशन सक्षम है या नहीं।
- `uuid.bios:` VM का BIOS UUID निर्दिष्ट करता है।
- `uuid.location:` VM का स्थान UUID निर्दिष्ट करता है।

## वीएमएक्स फ़ाइल कैसे खोलें?

VMX फ़ाइल को मैन्युअल रूप से खोलने की अनुशंसा नहीं की जाती है। जब आप VMware फ़्यूज़न का उपयोग करके वर्चुअल मशीन चलाते हैं, तो सॉफ़्टवेयर स्वचालित रूप से VMX फ़ाइल से जानकारी लोड करता है।

हालाँकि, यदि आप वीएमएक्स फ़ाइल को मैन्युअल रूप से संपादित करना चाहते हैं, तो आप किसी भी टेक्स्ट एडिटर जैसे नोटपैड (विंडोज) या टेक्स्टएडिट (मैक) का उपयोग करके ऐसा कर सकते हैं।

## वीएमएक्स फ़ाइल का प्रारूप क्या है?

वीएमएक्स फ़ाइल विशिष्ट प्रारूप वाली एक सादा पाठ फ़ाइल है। प्रारूप एक कुंजी-मूल्य जोड़ी संरचना का अनुसरण करता है जहां प्रत्येक पंक्ति अलग कॉन्फ़िगरेशन विकल्प का प्रतिनिधित्व करती है।

VMX फ़ाइल का सामान्य प्रारूप इस प्रकार है:

```
key1 = value1
key2 = value2
key3 = value3
```

प्रत्येक पंक्ति में कुंजी के बाद समान चिह्न (=) और संगत मान होता है। कुंजी एक विशिष्ट कॉन्फ़िगरेशन सेटिंग का प्रतिनिधित्व करती है और मान उस सेटिंग को निर्दिष्ट मान का प्रतिनिधित्व करता है।

उदाहरण के लिए, VMX फ़ाइल में `memSize = "8192" निर्दिष्ट करता है कि वर्चुअल मशीन मेमोरी सीमा 8192MB RAM है।

वीएमएक्स फ़ाइल के प्रारूप में टिप्पणियाँ भी शामिल हो सकती हैं, जिन्हें पंक्ति की शुरुआत में पाउंड चिह्न (#) द्वारा दर्शाया जाता है, जिन्हें फ़ाइल को पार्स करते समय वीएमवेयर सॉफ़्टवेयर द्वारा अनदेखा कर दिया जाता है। टिप्पणियाँ अक्सर विशिष्ट सेटिंग्स के लिए अतिरिक्त जानकारी या स्पष्टीकरण प्रदान करने के लिए उपयोग की जाती हैं।

## संदर्भ
* [नमूना वीएमएक्स फ़ाइल](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




