{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ SHSH2 - รูปแบบไฟล์ iOS SHSH Blob",
  "description":"เรียนรู้ว่าไฟล์ SHSH2 คืออะไร",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## ไฟล์ SHSH2 คืออะไร??

ไฟล์ SHSH2 หรือที่เรียกว่า SHSH blob หรือ ECID SHSH เป็นลายเซ็นดิจิทัลที่ Apple ใช้เพื่อรับรองความถูกต้องและตรวจสอบการอัปเดตเฟิร์มแวร์สำหรับอุปกรณ์ iOS เช่น iPhone, iPad และ iPod ประกอบด้วยตัวระบุเฉพาะสำหรับอุปกรณ์ที่เรียกว่า ECID (รหัสชิปพิเศษ) นอกจากนี้ยังมีข้อมูลเกี่ยวกับเวอร์ชันเฟิร์มแวร์ที่ติดตั้งบนอุปกรณ์ด้วย

## รูปแบบไฟล์ SHSH2 - ข้อมูลเพิ่มเติม

ไฟล์ SHSH2 จะถูกบันทึกลงในแผ่นดิสก์ในรูปแบบไฟล์ไบนารีและรายละเอียดโครงสร้างไฟล์ภายในของรูปแบบไฟล์นี้ไม่เปิดเผยต่อสาธารณะ

เมื่อมีการติดตั้ง iOS เวอร์ชันใหม่บนอุปกรณ์ Apple เช่น iPhone, iPad หรือ Mac ไฟล์ SHSH2 จะถูกสร้างขึ้น ไฟล์ SHSH2 นี้ถูกส่งไปยังเซิร์ฟเวอร์ของ Apple ซึ่งจะอ่านและตรวจสอบไฟล์ลายเซ็นดิจิทัลนี้ ตามข้อมูลนี้ เซิร์ฟเวอร์อนุญาตหรือป้องกันการติดตั้ง

สิ่งเดียวกันนี้จะเกิดขึ้นเมื่อมีการร้องขอการอัปเดต เมื่อผู้ใช้ร้องขอการอัปเดตหรือกู้คืนอุปกรณ์ผ่าน iTunes หรือซอฟต์แวร์อื่น เซิร์ฟเวอร์ของ Apple จะตรวจสอบว่าไฟล์ SHSH2 ตรงกับ ECID และเวอร์ชันเฟิร์มแวร์ของอุปกรณ์ก่อนที่จะอนุญาตให้ดำเนินการอัปเดตต่อไป

## อ้างอิง

* [SHSH Blob - โดย Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)
