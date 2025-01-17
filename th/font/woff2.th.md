{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ไฟล์ WOFF2 - ไฟล์รูปแบบฟอนต์เปิดเว็บ 2.0",
  "description": "เรียนรู้เกี่ยวกับไฟล์ WOFF2 และ API ที่สามารถสร้างและเปิดไฟล์ WOFF2 คืออะไร",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-th2"
}
},
  "lastmod": "2023-01-10"
}

## ไฟล์ WOFF2 คืออะไร??

WOFF2 เป็นรูปแบบไฟล์ฟอนต์ที่เป็นเวอร์ชันบีบอัดมากกว่าของ Web Open Font Format (WOFF) ได้รับการพัฒนาเพื่อลดขนาดไฟล์ของแบบอักษรบนเว็บ ทำให้สามารถโหลดได้เร็วขึ้นและใช้แบนด์วิธน้อยลง WOFF2 ใช้อัลกอริธึมการบีบอัดที่เรียกว่า Brotli เพื่อบีบอัดข้อมูลแบบอักษร ซึ่งอาจส่งผลให้ขนาดไฟล์มีขนาดเล็กกว่าแบบอักษร [WOFF](/font/woff/) ที่เทียบเท่ากันอย่างมาก เว็บเบราว์เซอร์รุ่นใหม่ส่วนใหญ่รองรับรูปแบบนี้ เช่น Chrome, Firefox, Safari, Opera และ Edge (เวอร์ชัน 14 เป็นต้นไป)

## รูปแบบไฟล์ WOFF2 - ข้อมูลเพิ่มเติม

โครงสร้างไฟล์ภายในของไฟล์ฟอนต์ WOFF2 ประกอบด้วยส่วนต่างๆ มากมาย รวมถึงส่วนหัว ข้อมูลเมตา ไดเร็กทอรีตาราง และข้อมูลฟอนต์เอง

 1. ส่วนหัวประกอบด้วยข้อมูลเกี่ยวกับรูปแบบโดยรวมของไฟล์ รวมถึงหมายเลขเวอร์ชันและจำนวนตารางที่มีอยู่ในไฟล์

 1. ส่วนข้อมูลเมตาประกอบด้วยข้อมูลเช่นชื่อแบบอักษร ลิขสิทธิ์ และข้อมูลอื่น ๆ ที่เกี่ยวข้องกับแบบอักษร

 1. ไดเร็กทอรีตารางประกอบด้วยข้อมูลเกี่ยวกับตารางต่างๆ ที่ประกอบเป็นฟอนต์ รวมถึงตำแหน่งในไฟล์และความยาวของตาราง

 1. ข้อมูลแบบอักษรนั้นแบ่งออกเป็นตารางต่างๆ มากมาย ซึ่งแต่ละตารางจะมีข้อมูลเฉพาะเกี่ยวกับแบบอักษร เช่น อักขระและสัญลักษณ์ที่เกี่ยวข้อง ตารางเหล่านี้อาจรวมถึง:

 * ตาราง 'glyf' ประกอบด้วยโครงร่างแบบอักษรจริง รวมถึงรูปร่างและขนาดของอักขระแต่ละตัว
 * ตาราง 'หัว' มีข้อมูลทั่วไปเกี่ยวกับแบบอักษร เช่น หมายเลขเวอร์ชัน ขนาดการออกแบบ และอื่นๆ
 * ตาราง 'hmtx' มีข้อมูลเกี่ยวกับหน่วยเมตริกของแบบอักษร รวมถึงความกว้างและตำแหน่งของอักขระ
 * แต่ละตารางจะถูกบีบอัดและจัดเก็บในรูปแบบไฟล์ WOFF2 หลังจากเสร็จสิ้นกระบวนการเข้ารหัส

โครงสร้างโดยรวมได้รับการออกแบบเพื่อให้สามารถแยกวิเคราะห์และถอดรหัสได้อย่างรวดเร็ว เพื่อให้เว็บเบราว์เซอร์สามารถโหลดและแสดงแบบอักษรบนเว็บไซต์ได้อย่างรวดเร็วและมีประสิทธิภาพ

### ส่วนหัว WOFF2
ส่วนหัว WOFF ประกอบด้วยลายเซ็นระบุซึ่งระบุชนิดของข้อมูลที่รวมอยู่ในไฟล์ ส่วนหัว WOFF พร้อมด้วยฟิลด์มีดังต่อไปนี้

|ประเภท|ชื่อฟิลด์|คำอธิบาย|
---|---|---|
| UInt32 | ลายเซ็น | 0x774F4632 'wOF2' |
|UInt32| รส |The sfnt version ของแบบอักษรอินพุต|
|UInt32| length |ขนาดรวมของไฟล์ WOFF.|
|UInt16| numTables |จำนวนรายการในไดเร็กทอรีของตารางแบบอักษร|
|UInt16| สงวนไว้ | สงวนไว้; ตั้งเป็นศูนย์|
|UInt32| TotalSfntSize |ขนาดรวมที่จำเป็นสำหรับข้อมูลแบบอักษรที่ไม่มีการบีบอัด รวมถึงส่วนหัว sfnt ไดเร็กทอรี และตารางแบบอักษร (รวมช่องว่างภายใน)|
|UInt32| TotalCompressedSize ความยาวรวมของบล็อกข้อมูลที่บีบอัด|
|UInt16| majorVersion |เวอร์ชันหลักของไฟล์ WOFF.|
|UInt16| minorVersion | เวอร์ชันรองของไฟล์ WOFF.|
|UInt32| metaOffset |ออฟเซ็ตเป็นบล็อกข้อมูลเมตา จากจุดเริ่มต้นของไฟล์ WOFF.|
|UInt32| metaLength |ความยาวของบล็อกข้อมูลเมตาที่ถูกบีบอัด|
|UInt32| metaOrigLength |ขนาดที่ไม่บีบอัดของบล็อกข้อมูลเมตา|
|UInt32| privOffset |ออฟเซ็ตเป็นบล็อกข้อมูลส่วนตัว จากจุดเริ่มต้นของไฟล์ WOFF|
|UInt32| privLength |ความยาวของบล็อกข้อมูลส่วนตัว|


## อ้างอิง
 * [รูปแบบไฟล์ w3 WOFF2](https://www.w3.org/TR/WOFF2/)

