{
  "date" : "2019-10-11",
  "keywords" :[ "vdw","ไฟล์ vdw", "รูปแบบไฟล์ vdw", "ประเภทไฟล์ vdw", "ไฟล์", "ประเภท", "ไฟล์ vdw คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - รูปแบบไฟล์บริการกราฟิก Visio",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VDW และ API ที่สามารถสร้างและเปิดไฟล์ VDW",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## ไฟล์ VDW คืออะไร??

VDW เป็นรูปแบบไฟล์ Visio Graphics Service ที่ระบุสตรีมและที่เก็บข้อมูลที่จำเป็นสำหรับการแสดงภาพวาดบนเว็บ การวาดภาพบนเว็บคือคอลเลกชันของหน้ารูปวาด รูปร่าง ฟอนต์ รูปภาพ การเชื่อมต่อข้อมูล และข้อมูลการอัปเดตไดอะแกรมที่สามารถแสดงผลเป็นรูปวาดเวกเตอร์หรือแรสเตอร์ ไฟล์ VDW สามารถเปิดได้ใน Microsoft Visio เช่นกัน แต่จะถูกบันทึกไว้เพื่อใช้บนเว็บเป็นหลัก Microsoft Visio มีความสามารถในการแปลงไฟล์ Visio เป็นรูปแบบไฟล์ต่างๆ มากมาย รวมถึง [PNG](/th/image/png/), [BMP](/th/image/bmp/), [PDF](/th/pdf/) และอื่นๆ

## **VDW** รูปแบบไฟล์

ข้อกำหนดทางเทคนิคของรูปแบบไฟล์ VDW มีให้ทางออนไลน์โดย [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) และนักพัฒนาสามารถใช้อ้างอิงเพื่อสร้าง แอพพลิเคชั่น. เอกสารทางเทคนิคอธิบายข้อมูลที่อยู่ในไฟล์ผสมซึ่งมีที่เก็บข้อมูลและสตรีม การแสดง Web Drawing ทำได้ผ่านสตรีมชื่อ VisioServerData ผ่านไฟล์ ZIP ส่วน XML ของ ShapGraphic ในไฟล์เก็บถาวรจะอธิบายองค์ประกอบกราฟิกที่แสดงใน Web Drawing และแสดงเป็นภาษามาร์กอัปแอปพลิเคชัน Extensible (XAML) คอลเลกชันของส่วน XML ในไฟล์เก็บถาวร ZIP อธิบายการเชื่อมต่อข้อมูลของภาพวาดบนเว็บ ข้อมูลเกี่ยวกับรูปร่างและตรรกะการอัปเดตไดอะแกรม ส่วนเหล่านี้แสดงเป็น XML ส่วน DataGraphic XML อธิบายถึงคุณสมบัติที่คำนวณใหม่ซึ่งจะถูกประเมินหลังจากที่ข้อมูลใน Web drawing ถูกรีเฟรชจากแหล่งข้อมูล รายการเพิ่มเติมในไฟล์ ZIP ประกอบด้วยข้อมูลสำหรับแบบอักษรและรูปภาพที่ใช้ในการวาดบนเว็บ

|![การใช้งานไฟล์ที่เป็นไปได้](/th/web/vdw.png "การใช้งานไฟล์ที่เป็นไปได้")

## อ้างอิง

* [[MS-VGSFF]: รูปแบบไฟล์บริการกราฟิก Visio (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

