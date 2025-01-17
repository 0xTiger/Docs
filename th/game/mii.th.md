{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MGX ของ Age of Empires 2 Expansion Replay และ API ที่สามารถสร้างและเปิดไฟล์ MGX ได้",
  "title" : "ไฟล์ MII - รูปแบบไฟล์ Avatar เสมือนของ Wii",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-th",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## ไฟล์ MII คืออะไร??

ไฟล์ MII เป็นรูปแบบไฟล์อวตารเสมือนที่ใช้จัดเก็บอวตารเสมือนบนคอนโซลเกม Nintendo Wii ไฟล์เหล่านี้ประกอบด้วยข้อมูลต่างๆ เช่น ลักษณะที่ปรากฏ การเคลื่อนไหว และภาพเคลื่อนไหว สามารถใช้ในเกม แอปพลิเคชันโซเชียลเน็ตเวิร์ก และซอฟต์แวร์อื่นๆ บน Wii ไฟล์ MII ยังมีคุณสมบัติอื่น ๆ เกี่ยวกับอวตาร เช่น เพศ สีผม สีผิว ลักษณะใบหน้า และประเภทดวงตา

คุณสามารถเปิดไฟล์ MII ได้โดยใช้ [My Avatar Editor](https://rc24.xyz/goodies/mii/)

## รูปแบบไฟล์ MII

รูปแบบไฟล์ MII มีการกำหนดรายละเอียดไว้บน [Wii Brew](https://wiibrew.org/wiki/Mii_data) สตริงในไฟล์ MII จะถูกจัดเก็บในรูปแบบ Unicode (UTF-16) ซึ่งเป็น big-endian

### MI บล็อก

ข้อมูลไฟล์ MII จะถูกจัดเก็บไว้ใน Wiimote ในสองช่วงตึก แต่ละบล็อกมีความยาว 750 ไบต์ โดยมี CRC 2 ไบต์ ทำให้มีทั้งหมด 752 ไบต์ แต่ละบล็อกเริ่มต้นด้วยค่า 4 ไบต์ ('RNCD') ซึ่งดูเหมือนจะเป็นตัวเลขมหัศจรรย์สำหรับรูปแบบไฟล์ MII

## จะสร้างไฟล์ MII ได้อย่างไร?

มีวิธีต่างๆ สองสามวิธีในการสร้างอวตารสำหรับ Nintendo Wii:

1. `การใช้ช่อง Mii ในตัวบน Wii:` ช่องนี้ช่วยให้คุณสร้างอวตารที่กำหนดเองโดยใช้เครื่องมือที่หลากหลาย รวมถึงลักษณะใบหน้า รูปร่าง และเสื้อผ้า เมื่อคุณสร้างอวาตาร์แล้ว คุณสามารถบันทึกเป็นไฟล์ Mii และใช้ในเกมและซอฟต์แวร์อื่นๆ บน Wii ได้

1. `การใช้แอป Mii Maker บน Nintendo 3DS:` แอป Mii Maker ช่วยให้คุณสร้างอวตารที่กำหนดเองได้โดยใช้หน้าจอสัมผัสและกล้องบน Nintendo 3DS ของคุณ เมื่อคุณสร้างอวาตาร์แล้ว คุณสามารถบันทึกเป็นไฟล์ Mii และโอนไปยัง Wii ของคุณผ่านการเชื่อมต่อไร้สาย

1. `การใช้ซอฟต์แวร์บุคคลที่สาม:` นักพัฒนาซอฟต์แวร์บางรายได้สร้างซอฟต์แวร์ที่ช่วยให้คุณสามารถสร้างอวตารที่กำหนดเองสำหรับ Wii ได้ โดยทั่วไปซอฟต์แวร์นี้ออกแบบมาเพื่อใช้กับคอมพิวเตอร์และอาจต้องมีขั้นตอนเพิ่มเติมในการถ่ายโอนอวตารไปยัง Wii ของคุณ

1. `การใช้รูปประจำตัวที่สร้างไว้ล่วงหน้า:` เกมบางเกมและซอฟต์แวร์อื่นๆ บน Wii อาจมาพร้อมกับรูปประจำตัวที่สร้างไว้ล่วงหน้าที่คุณสามารถใช้ได้

ในทุกกรณี คุณต้องมีบัญชี Nintendo เพื่อสร้างและบันทึกอวตารของคุณบน Wii

## อ้างอิง

* [โปรแกรมแก้ไขอวาตาร์ของฉัน](https://rc24.xyz/goodies/mii/)

* [Wii บริว](https://wiibrew.org/wiki/Mii_data)


