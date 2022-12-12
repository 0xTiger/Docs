{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ odp", "รูปแบบไฟล์ odp", "ไฟล์ odp คืออะไร", "ไฟล์", "ตัวอย่าง odp", "นามสกุลไฟล์ odp", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - รูปแบบไฟล์งานนำเสนอ OpenOffice",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ODP และ API ที่สามารถสร้างและเปิดไฟล์ ODP",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ ODP คืออะไร??

ไฟล์ที่มีนามสกุล .odp แสดงถึงรูปแบบไฟล์งานนำเสนอที่ OpenOffice.org ใช้ในมาตรฐาน OASISOpen ไฟล์งานนำเสนอคือชุดของสไลด์ ซึ่งแต่ละสไลด์สามารถประกอบด้วยข้อความ รูปภาพ การจัดรูปแบบ ภาพเคลื่อนไหว และสื่ออื่นๆ สไลด์เหล่านี้นำเสนอต่อผู้ชมในรูปแบบของสไลด์โชว์พร้อมการตั้งค่าการนำเสนอแบบกำหนดเอง ไฟล์ ODP สามารถเปิดได้โดยแอปพลิเคชันที่สอดคล้องกับรูปแบบ OpenDocument (เช่น OpenOffice หรือ StarOffice)

## ประวัติย่อ

ข้อกำหนดรูปแบบไฟล์ ODP เป็นไปตามมาตรฐานที่พัฒนาเป็นข้อกำหนด ODF ข้อกำหนดเหล่านี้ได้พัฒนามาในรูปแบบของสามเวอร์ชันที่พัฒนาและเผยแพร่โดย OASIS ดังนี้:

`2005` - เวอร์ชัน 1.0 เผยแพร่ในเดือนพฤษภาคม 2548
`2007` - เวอร์ชัน 1.1 เผยแพร่ในเดือนกุมภาพันธ์ 2550
`2011` - เวอร์ชัน 1.2 เผยแพร่ในเดือนกันยายน 2011

มีการเปลี่ยนแปลงเล็กน้อยในการเปลี่ยนจากเวอร์ชัน ODF 1.0 เป็น 1.1 [เวอร์ชัน ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) เป็นเวอร์ชันล่าสุดสำหรับข้อกำหนดเฉพาะของ ODF และควรปรึกษานักพัฒนาซอฟต์แวร์เกี่ยวกับการพัฒนาแอปพลิเคชันที่เกี่ยวข้องกับการอ่าน/เขียน ODS

## ข้อมูลจำเพาะรูปแบบไฟล์

รูปแบบ OpenDocument รองรับการแสดงเอกสารเป็นเอกสาร XML เดียว ตลอดจนการรวบรวมเอกสารย่อยหลายรายการภายในแพ็กเกจเป็นไฟล์เก็บถาวรแบบ [ZIP](https://docs.fileformat.com/Compression/ZIP/) ไฟล์แต่ละไฟล์จากไฟล์ ZIP เก็บส่วนหนึ่งของเอกสารฉบับสมบูรณ์ เอกสารย่อยแต่ละรายการจัดเก็บลักษณะเฉพาะของเอกสาร ตัวอย่างเช่น เอกสารย่อยหนึ่งประกอบด้วยข้อมูลลักษณะ และเอกสารย่อยอื่นประกอบด้วยเนื้อหาของเอกสาร เอกสาร ODF ทั่วไปมีองค์ประกอบดังต่อไปนี้:

* `content.xml` – เนื้อหาเอกสารและรูปแบบอัตโนมัติที่ใช้ในเนื้อหา
* `styles.xml` – สไตล์ที่ใช้ในเนื้อหาเอกสารและสไตล์อัตโนมัติที่ใช้ในสไตล์เอง
* `meta.xml` – ข้อมูลเมตาของเอกสาร เช่น ผู้เขียนหรือเวลาของการดำเนินการบันทึกครั้งล่าสุด
* `settings.xml` – การตั้งค่าเฉพาะแอปพลิเคชัน เช่น ขนาดหน้าต่างหรือข้อมูลเครื่องพิมพ์

นอกจากนี้ ในแพ็คเกจยังสามารถเป็นเอกสารย่อยอื่นๆ ได้อีกมากมาย เช่น ภาพขนาดย่อของเอกสาร รูปภาพ เป็นต้น

ไฟล์เอกสารสเปรดชีตเป็นส่วนย่อยของไฟล์ ODF ซึ่งเนื้อหา (แผ่นงาน) ถูกเก็บไว้ในเอกสารย่อย content.xml

## อ้างอิง

* [OpenDocument - โดย Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
