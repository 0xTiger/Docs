{
"วันที่": "2023-05-02",
  "keywords": [
"ไฟล์โอบี",
"ไฟล์โอบีคืออะไร",
"ไฟล์ obi เป็นรูปแบบอะไร",
"ไฟล์",
"นามสกุลไฟล์โอบี",
"ส่วนขยาย"
],
  "author": {
"display_name": "ชาคีล ไฟซ์"
},
"draft": "false",
"toc": true,
"title": "รูปแบบไฟล์ OBI - ไฟล์สมัครสมาชิก Outlook RSS",
  "description":"เรียนรู้เกี่ยวกับรูปแบบ OBI และ API ที่สามารถสร้างและเปิดไฟล์ OBI",
  "linktitle": "OBI",
  "menu": {
    "docs": {
      "identifier": "settings-obi",
      "parent": "settings"
}
},
"lastmod": "2023-05-02"
}

## ไฟล์ OBI คืออะไร??

ไฟล์ OBI เป็นไฟล์สมัครสมาชิก Outlook RSS ที่อนุญาตให้ผู้ใช้สมัครรับฟีด RSS ใน Microsoft Outlook RSS ย่อมาจาก Really Simple Syndication ซึ่งเป็นรูปแบบเว็บฟีดที่ใช้ในการเผยแพร่เนื้อหาที่อัปเดตบ่อยครั้ง เช่น บล็อกโพสต์ หัวข้อข่าว หรือพอดแคสต์

หากต้องการสมัครรับฟีด RSS ใน Outlook ผู้ใช้สามารถคลิกลิงก์ไปยังฟีด RSS บนเว็บไซต์หรือคัดลอก URL ของฟีด RSS และวางลงในกล่องโต้ตอบ "เพิ่มฟีด RSS ใหม่" ใน Outlook Outlook จะตรวจสอบฟีด RSS เป็นระยะเพื่อหาเนื้อหาใหม่ และแสดงในโฟลเดอร์ฟีด RSS ของผู้ใช้

ไฟล์การสมัครสมาชิก Outlook RSS มีนามสกุลไฟล์ ".rss" ไฟล์เหล่านี้มี URL ของฟีด RSS และสามารถใช้เพื่อแชร์การสมัครรับฟีด RSS กับผู้อื่น หรือเพื่อสำรองและกู้คืนการสมัครรับฟีด RSS

## รูปแบบไฟล์ OBI - ข้อมูลเพิ่มเติม

ไฟล์ OBI รู้จักกันในชื่อไฟล์ OPML (ภาษามาร์กอัปตัวประมวลผลโครงร่าง) และมีรายการ URL ฟีด RSS ที่สมัครเป็นสมาชิกใน Microsoft Outlook

เมื่อผู้ใช้ส่งออกฟีด RSS ไปยังไฟล์ OBI จะมีรายการฟีด RSS ทั้งหมดที่พวกเขาสมัครรับข้อมูล รวมถึงชื่อฟีดแต่ละรายการ URL ของฟีด และข้อมูลอื่น ๆ ที่เกี่ยวข้อง ช่วยให้ผู้ใช้สามารถถ่ายโอนการสมัครสมาชิกฟีด RSS ไปยังโปรแกรมอ่าน RSS อื่นหรือสำรองข้อมูลการสมัครสมาชิกเพื่อความปลอดภัยได้อย่างง่ายดาย

ไฟล์ OBI ยังสามารถใช้เพื่อนำเข้าการสมัครสมาชิกฟีด RSS ไปยัง Microsoft Outlook หรือโปรแกรมอ่าน RSS อื่น หากต้องการนำเข้าไฟล์ OBI ไปยัง Outlook ผู้ใช้สามารถคลิกที่ "ไฟล์"> "เปิดและส่งออก"> "นำเข้า/ส่งออก"> "นำเข้าจากโปรแกรมหรือไฟล์อื่น"> "ถัดไป" > "นำเข้า RSS Feeds จากไฟล์ OPML" และ จากนั้นเรียกดูตำแหน่งของไฟล์ OBI บนคอมพิวเตอร์

## ไฟล์ OBI อยู่ในรูปแบบใด

ไฟล์สมัครสมาชิก Outlook RSS หรือที่เรียกว่าไฟล์ OBI ใช้ XML (eXtensible Markup Language) เพื่อกำหนดโครงสร้างและเนื้อหาของไฟล์

ไฟล์ OBI ประกอบด้วยชุดขององค์ประกอบที่ซ้อนกัน แต่ละชุดมีคุณลักษณะและค่าของตัวเอง องค์ประกอบหลักในไฟล์ OBI คือองค์ประกอบ "โครงร่าง" ซึ่งมีข้อมูลเกี่ยวกับฟีด RSS รวมถึงชื่อของฟีด URL ของฟีด และข้อมูลอื่น ๆ ที่เกี่ยวข้อง

องค์ประกอบ "เค้าร่าง" แต่ละองค์ประกอบยังสามารถมีองค์ประกอบลูกซึ่งเป็นตัวแทนของโฟลเดอร์ย่อยหรือหมวดหมู่ย่อยภายในรายการฟีด RSS โครงสร้างของไฟล์ OBI ช่วยให้จัดระเบียบและจัดการการสมัครสมาชิกฟีด RSS ได้ง่าย และสามารถใช้เพื่อถ่ายโอนการสมัครสมาชิกระหว่างโปรแกรมอ่าน RSS ต่างๆ หรือสำรองและกู้คืนการสมัครสมาชิก

## อ้างอิง
* [ฟีด RSS คืออะไร](https://support.microsoft.com/en-us/office/what-are-rss-feeds-e8aaebc3-a0a7-40cd-9e10-88f9c1e74b97)

