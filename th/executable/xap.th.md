{
"วันที่": "2023-02-01",
  "keywords": [
"ไฟล์ xap",
"ไฟล์ xap คืออะไร",
"ไฟล์",
"วิธีการเปิดไฟล์ xap",
"นามสกุลไฟล์ xap",
"ส่วนขยาย"
],
  "author": {
"display_name": "ชาคีล ไฟซ์"
},
"draft": "false",
"toc": true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XAP และ API ที่สามารถสร้างและเปิดไฟล์ XAP",
"title": "รูปแบบไฟล์ XAP - แพ็คเกจแอปพลิเคชัน Silverlight",
  "linktitle": "XAP",
  "menu": {
    "docs": {
      "identifier": "executable-xap",
      "parent": "executable"
}
},
"lastmod": "2023-02-01"
}

## ไฟล์ XAP คืออะไร??

ไฟล์ .xap คือไฟล์แพ็คเกจแอปพลิเคชัน Silverlight ที่ใช้สำหรับปรับใช้แอปพลิเคชัน Silverlight บนเว็บ หากต้องการเปิดและเรียกใช้ไฟล์ .xap คุณจะต้องมีเว็บเบราว์เซอร์ที่รองรับ Silverlight (เช่น Internet Explorer หรือ Microsoft Edge) และติดตั้งปลั๊กอิน Silverlight เพียงนำทางไปยังเว็บไซต์ที่โฮสต์ไฟล์ .xap และแอปพลิเคชันควรจะทำงานในเบราว์เซอร์โดยอัตโนมัติ

## ไฟล์ XAP ถูกจัดเก็บอย่างไร?

ไฟล์ .xap จะถูกจัดเก็บเป็นไฟล์เก็บถาวรแบบบีบอัดของไฟล์ที่จำเป็นทั้งหมดสำหรับแอปพลิเคชัน Silverlight ไฟล์ .xap คือไฟล์เก็บถาวร .zip ที่มีไฟล์รายการ (AppManifest.xaml) และไฟล์ทั้งหมดที่จำเป็นสำหรับแอปพลิเคชันในการทำงาน เช่น ไฟล์ .dll, ไฟล์ .xaml, ไฟล์รูปภาพ และไฟล์มีเดีย โดยปกติแล้วไฟล์ .xap จะถูกใช้งานบนเว็บเซิร์ฟเวอร์ และไคลเอนต์สามารถดาวน์โหลดได้ และทำงานบนเว็บเบราว์เซอร์ที่เปิดใช้งาน Silverlight

## ความสัมพันธ์กับซิลเวอร์ไลท์

ไฟล์ .xap เกี่ยวข้องเป็นพิเศษกับ Microsoft Silverlight ซึ่งเป็นปลั๊กอินข้ามแพลตฟอร์มข้ามเบราว์เซอร์สำหรับมอบประสบการณ์มัลติมีเดียและแอปพลิเคชันเชิงโต้ตอบที่หลากหลายสำหรับเว็บ ไฟล์ .xap เป็นไฟล์แพ็กเกจประเภทหนึ่งที่ใช้สำหรับการปรับใช้แอปพลิเคชัน Silverlight บนเว็บ ประกอบด้วยไฟล์ที่จำเป็นทั้งหมดสำหรับแอปพลิเคชัน เช่น ไฟล์ .dll, .xaml, ไฟล์รูปภาพ และไฟล์มีเดีย ซึ่งรวมอยู่ในรูปแบบไฟล์เก็บถาวรที่บีบอัด เมื่อผู้ใช้นำทางไปยังเว็บไซต์ที่โฮสต์ไฟล์ .xap ปลั๊กอิน Silverlight จะดาวน์โหลดไฟล์ .xap ขยายขนาดไฟล์ และรันแอปพลิเคชัน Silverlight ที่อยู่ภายใน

## เปิดไฟล์ XAP ได้อย่างไร

หากต้องการเปิดไฟล์ .xap คุณจะต้องใช้เว็บเบราว์เซอร์ที่รองรับ Silverlight และติดตั้งปลั๊กอิน Silverlight แล้ว จากนั้น คุณสามารถนำทางไปยังเว็บไซต์ที่โฮสต์ไฟล์ .xap หรือเปิดไฟล์ในเครื่องได้ แอปพลิเคชัน Silverlight ที่อยู่ในไฟล์ .xap ควรทำงานในเบราว์เซอร์โดยอัตโนมัติ

หรือคุณสามารถแยกเนื้อหาของไฟล์ .xap ได้โดยเปลี่ยนชื่อเป็น .zip และขยายขนาดโดยใช้เครื่องมือบีบอัดไฟล์ เช่น WinZip หรือ 7-Zip ซึ่งจะช่วยให้คุณสามารถเข้าถึงแต่ละไฟล์ที่อยู่ในไฟล์เก็บถาวร .xap

## อ้างอิง
* [XAP - รูปแบบไฟล์](https://en.wikipedia.org/wiki/XAP_(file_format))

