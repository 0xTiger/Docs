{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ผงชูรส - รูปแบบอีเมล Microsoft Outlook",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MSG และ API ที่สามารถสร้างและเปิดไฟล์ MSG",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ MSG คืออะไร??

MSG เป็นรูปแบบไฟล์ที่ใช้โดย [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) และ Exchange เพื่อจัดเก็บข้อความอีเมล ติดต่อนัดหมายหรืองานอื่นๆ ข้อความดังกล่าวอาจมีฟิลด์อีเมลตั้งแต่หนึ่งฟิลด์ขึ้นไป โดยมีผู้ส่ง ผู้รับ หัวเรื่อง วันที่ และเนื้อความของข้อความ หรือข้อมูลติดต่อ รายละเอียดการนัดหมาย และข้อกำหนดเฉพาะของงานอย่างน้อยหนึ่งรายการ คุณสมบัติที่ประกอบขึ้นเป็นอ็อบเจกต์ Message รวมถึงเป็นส่วนหนึ่งของไฟล์ MSG ไฟล์ MSG มีส่วนหัว เนื้อหาข้อความหลัก และไฮเปอร์ลิงก์เป็นข้อความ ASCII ธรรมดา ไฟล์ MSG ยังเหมาะกับโปรแกรมที่ต้องการ Messaging Applications Programming Interface (MAPI) ของ Microsoft

## โครงสร้างไฟล์ MSG

รูปแบบ CFB_3 เป็นฐานของไฟล์ MSG กระบวนทัศน์นี้อิงตามแนวคิดของสตอเรจและสตรีม ซึ่งค่อนข้างใกล้เคียงกับไดเร็กทอรีและไฟล์ ดังนั้นความแตกต่างที่สำคัญในอดีตคือลำดับชั้นทั้งหมด ซึ่งบรรจุเป็นไฟล์ที่แตกต่างกัน เรียกว่าไฟล์ผสม อ็อบเจกต์ประกอบด้วยไฟล์ข้อความและประกอบด้วยคุณสมบัติเดียวหรือคอลเล็กชัน ความสามารถนี้ช่วยให้แอปพลิเคชันสามารถจัดเก็บข้อมูลที่มีโครงสร้างซับซ้อนไว้ในไฟล์เดียว รูปแบบนี้ยังระบุที่เก็บข้อมูลหลายที่ ซึ่งแต่ละที่เก็บข้อมูลจะแทนออบเจกต์ข้อความเป็นองค์ประกอบหลัก ที่เก็บข้อมูลเหล่านี้มีจำนวนสตรีมที่แสดงคุณสมบัติของส่วนประกอบนั้น นอกจากนี้ยังสามารถซ้อนที่เก็บข้อมูลได้อีกด้วย

## คุณสมบัติของมะปี

ที่ระดับบนสุดของไฟล์ .msg ที่เก็บข้อมูลประกอบด้วยสตรีมที่เก็บคุณสมบัติไว้ในนั้น สามารถแบ่งประเภทคุณสมบัติได้ดังนี้

* คุณสมบัติความยาวคงที่
* คุณสมบัติความยาวตัวแปร
* คุณสมบัติหลายค่า

โดยไม่คำนึงถึงหมวดหมู่ พร็อพเพอร์ตี้อาจเป็นแท็กหรือชื่อก็ได้ อย่างไรก็ตาม ข้อมูลการแม็พที่เหมาะสมสำหรับคุณสมบัติที่มีชื่อตามที่ระบุโดยที่จัดเก็บการแม็พ

## ที่เก็บของ

ที่เก็บข้อมูลเป็นองค์ประกอบหลักของวัตถุข้อความ รูปแบบไฟล์ MSG ระบุที่เก็บข้อมูลต่อไปนี้:

## โครงสร้างระดับบนสุด

วัตถุข้อความแสดงถึงระดับบนสุดของรูปแบบไฟล์ MSG ขึ้นอยู่กับประเภท คุณสมบัติ จำนวนผู้รับและวัตถุแนบ วัตถุข้อความสามารถมีที่เก็บข้อมูลสตรีมที่แตกต่างกันในไฟล์ .MSG ที่สอดคล้องกัน

### ความสัมพันธ์กับโครงสร้างอื่น ๆ

รูปแบบไฟล์ Msg มีความสัมพันธ์ต่อไปนี้กับโครงสร้างอื่นๆ:

* ฐานของ .msg คือรูปแบบไฟล์ไบนารีของไฟล์ผสม
* คุณสมบัติที่ใช้โดย Message and Attachment Object Protocol ถูกใช้โดยรูปแบบนี้

## สถานการณ์เพื่อหลีกเลี่ยงรูปแบบผงชูรส

อ็อบเจ็กต์ข้อความสามารถแชร์ระหว่างไคลเอ็นต์หรือที่เก็บข้อความที่ใช้ระบบไฟล์ .msg มีบางสถานการณ์ที่การจัดเก็บวัตถุข้อความในรูปแบบไฟล์ .msg จะไม่เหมาะสม ตัวอย่างเช่น:

* ในกรณีของการเก็บถาวรแบบสแตนด์อโลนขนาดใหญ่ จะเป็นการดีกว่าหากใช้รูปแบบเต็มรูปแบบซึ่งสามารถแสดงมุมมองได้แม่นยำยิ่งขึ้น
* หากไม่รู้จักผู้รับ อาจเป็นไปได้ว่ารูปแบบนั้นไม่รองรับโดยปลายทางของผู้รับ และอาจมีการส่งแบบส่วนตัวหรือไม่เกี่ยวข้อง

## ตัวอย่างไฟล์ MSG

หากต้องการทราบว่าไฟล์ MSG มีลักษณะอย่างไร คุณสามารถดาวน์โหลด [ไฟล์ MSG ตัวอย่าง](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) แล้วเปิดบน คอมพิวเตอร์เพื่อดูเนื้อหา

## อ้างอิง

* [[MS-OXMSG]: รูปแบบไฟล์ Outlook MSG](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

