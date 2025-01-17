{
  "date" : "2021-08-30",
  "keywords" :[ "ไฟล์ ipa", "รูปแบบไฟล์ ipa", "ไฟล์ ipa คืออะไร", "ไฟล์", "ตัวอย่าง ipa", "นามสกุลไฟล์ ipa","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ IPA และ API ที่สามารถสร้างและเปิดไฟล์ IPA",
  "title" :"IPA - ไฟล์แพ็คเกจแอปพลิเคชัน iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## ไฟล์ IPA คืออะไร??
ไฟล์ที่มีนามสกุล .ipa เป็นของ iOS และเรียกว่าไฟล์แพ็คเกจแอปพลิเคชัน นี่คือไฟล์เก็บถาวร (บีบอัดโดยใช้การบีบอัด [ZIP](/th/compression/zip/)) ซึ่งจัดเก็บแอปพลิเคชัน iOS แต่แอปพลิเคชันนั้นสามารถติดตั้งได้เฉพาะบนอุปกรณ์ MacOS ที่ใช้ iOS หรือ ARM เช่น iPad, iPhone หรือ ไอพอดทัช. โดยหลักแล้ว สามารถใช้ iTunes, Apple Configurator 2 หรือซอฟต์แวร์ของบริษัทอื่นเพื่อติดตั้งไฟล์ IPA ได้

## รูปแบบไฟล์ IPA
นักพัฒนา IOS ที่กำลังพัฒนาแอพโดยใช้ Apple Xcode นั้นคุ้นเคยกับไฟล์ IPA เป็นอย่างดี เพราะพวกเขาจำเป็นต้องรวมแพ็คเกจแอพที่พัฒนาแล้วเป็นไฟล์ IPA เพื่อทดสอบการใช้งานแอพสโตร์ แม้ว่าไฟล์ IPA จะติดตั้งเป็นแอป iOS แต่คุณก็สามารถขยายขนาดไฟล์เพื่อดูข้อมูลแอปที่มีอยู่ได้ เนื่องจากไฟล์ IPA มีเพียงหนึ่งไบนารีสำหรับสถาปัตยกรรม ARM ของโทรศัพท์มือถือ และไม่มีไบนารีสำหรับสถาปัตยกรรม x86 ไฟล์ .ipa จำนวนมากจึงไม่สามารถติดตั้งบน iPhone Simulator ได้
### โครงสร้างไฟล์ .ipa
ตัวอย่างต่อไปนี้แสดงโครงสร้างของ IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
ด้านบนเป็นโครงสร้างในตัวสำหรับ iTunes และ App Store ในการรับรู้ ตามโครงสร้างนี้:
- ไดเร็กทอรี Payload มีข้อมูลแอปทั้งหมด
- ไฟล์ iTunes Artwork เป็นภาพ PNG ขนาด 512×512 พิกเซล ซึ่งมีไอคอนของแอปสำหรับแสดงใน iTunes และแอป App Store บน iPad
- iTunesMetadata.plist ประกอบด้วยข้อมูลหลายส่วน ตั้งแต่ชื่อและ ID ของผู้พัฒนา ข้อมูลลิขสิทธิ์ ตัวระบุบันเดิล ชื่อของแอพ ประเภท วันที่วางจำหน่าย วันที่ซื้อ ฯลฯ
- โฟลเดอร์ META-INF มีเฉพาะข้อมูลเมตาเกี่ยวกับโปรแกรมที่ใช้สร้าง IPA


## อ้างอิง

* [.ipa - โดย Wikipedia](https://en.wikipedia.org/wiki/.ipa)


