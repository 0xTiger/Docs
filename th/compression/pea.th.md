{
  "date" : "2021-04-21",
  "keywords" :[ "ไฟล์ถั่ว", "รูปแบบไฟล์ถั่ว", "ไฟล์ถั่วคืออะไร", "ไฟล์", "ตัวอย่างถั่ว", "นามสกุลไฟล์ถั่ว","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - รูปแบบไฟล์เก็บถาวร PeaZip",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PEA และ API ที่สามารถสร้างและเปิดไฟล์ PEA",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## ไฟล์ PEA คืออะไร??

ไฟล์ที่มีนามสกุล .pea ซึ่งเป็นตัวย่อของ Pack, Encrypt และ Authenticate เป็นไฟล์เก็บถาวรแบบ [zip](/th/compression/zip/) ที่สร้างขึ้นด้วยแอปพลิเคชันซอฟต์แวร์การเก็บถาวร [PeaZip](https://peazip.github.io/) มีการบีบอัดและเอาต์พุตหลายโวลุ่ม และเสนอรูปแบบการรักษาความปลอดภัยที่ยืดหยุ่นผ่านการเข้ารหัสและการเข้ารหัสที่รับรองความถูกต้อง สิ่งนี้ให้ทั้งความเป็นส่วนตัวและการรับรองความถูกต้องของข้อมูล ยูทิลิตี้ PeaZip มีให้ใช้งานในรูปแบบเครื่องมือโอเพ่นซอร์สที่สามารถคอมไพล์สำหรับระบบปฏิบัติการที่แตกต่างกันตามความต้องการ

## รูปแบบไฟล์ กฟภ

[ข้อกำหนดรูปแบบไฟล์ PEA](https://peazip.github.io/pea_help.pdf) เผยแพร่ต่อสาธารณะเพื่อเป็นข้อมูลอ้างอิงสำหรับนักพัฒนาซอฟต์แวร์ ไฟล์เก็บถาวรของ PEA เป็นไฟล์ไบนารีที่มีรูปแบบการรักษาความปลอดภัยที่ยืดหยุ่นและการตรวจสอบความสมบูรณ์ซ้ำซ้อนตั้งแต่การตรวจสอบไปจนถึงแฮชที่รัดกุมในการเข้ารหัส สิ่งนี้กำหนดระดับการสื่อสารที่แตกต่างกันสามระดับเพื่อควบคุม:

* Streams - สตรีมข้อมูลเอาต์พุตที่เกิดขึ้นจริงซึ่งเกิดจากไฟล์อินพุตหลายไฟล์และสามารถเขียนลงในไดรฟ์ข้อมูลเอาต์พุตหลายชุดได้
* วัตถุ - ไฟล์อินพุตและโฟลเดอร์ที่ส่งไปยังไฟล์เก็บถาวร .pea
* Volumes - ไฟล์เก็บถาวรเอาต์พุตที่สามารถขยายไปยังขนาดที่ผู้ใช้กำหนด

แต่ละรายการเหล่านี้เป็นทางเลือกและสามารถรวมเข้าด้วยกันได้ตามความต้องการของผู้ใช้ รูปแบบไฟล์ PEA สามารถจัดเก็บสตรีมเดียวที่มีวัตถุไม่จำกัด แต่ละสตรีมมีขนาดสูงสุด 2^64 ไบต์

ไฟล์ PEA เสนอการตรวจสอบความสมบูรณ์ที่เป็นทางเลือกและการเข้ารหัสรับรองความถูกต้องโดยใช้ AES ในโหมด EAX หรือ HMAC หรืออีกทางเลือกหนึ่งคือ Twofish และ Serpent ในโหมด EAX

### ส่วนหัวเอกสารสำคัญของกฟภ

ส่วนหัวของไฟล์เก็บถาวรคือ 10 ไบต์และมีโครงสร้างดังต่อไปนี้

|ไบต์|คำอธิบาย|
---|---|
|1 | ฟิลด์เมจิกไบต์สำหรับแก้ความกำกวมของรูปแบบไฟล์: $EA|
|1 | หมายเลขเวอร์ชัน|
|1 | หมายเลขการแก้ไข|
|1 | รูปแบบการควบคุมระดับเสียง|
|1 | การประกาศ OS ที่สร้างสตรีม|
|1 | ประกาศการเข้ารหัสวันที่และเวลาของระบบปฏิบัติการ|
|1 | ประกาศการเข้ารหัสอักขระชื่อวัตถุ|
|1 | การประกาศประเภท CPU (เข้ารหัสใน 7 บิต) และ endianness (ใน msb)|
|1 | สงวนไว้สำหรับใช้ในอนาคต|

## อ้างอิง

* [ข้อกำหนดรูปแบบไฟล์ PEA](https://peazip.github.io/pea_help.pdf)
* [รูปแบบไฟล์ PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

