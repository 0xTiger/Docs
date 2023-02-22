{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - สคริปต์ทรัพยากรที่คอมไพล์ด้วย C ++",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ RES พร้อมตัวอย่าง RES และ API ที่สามารถสร้างและเปิดไฟล์ RES",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## ไฟล์ RES คืออะไร??
ไฟล์ที่มีคำต่อท้ายหรือนามสกุล .res สามารถอยู่ในประเภทไฟล์หลายประเภท ที่นี่เรากำลังพูดถึงรูปแบบไฟล์ RES ซึ่งเป็นสคริปต์ทรัพยากรที่คอมไพล์ด้วย C ++; ไฟล์ไบนารีที่สร้างโดย Microsoft Resource Compiler (rc) ที่มีข้อมูลทรัพยากร ตามเนื้อหาของไฟล์คำจำกัดความของทรัพยากร เกี่ยวข้องกับโครงการซอฟต์แวร์หลัก ไฟล์ .res มักจะถูกฟอร์แมตใหม่เป็นไฟล์ออบเจกต์ทรัพยากรเพื่อลิงก์ไปยังไฟล์เรียกทำงานของแอปพลิเคชัน

## รูปแบบไฟล์ RES
รูปแบบไฟล์ RES เป็นของ Microsoft Resource Compiler (rc) คอมไพเลอร์ทรัพยากรเป็นเครื่องมือที่รวบรวมทรัพยากร เช่น เคอร์เซอร์ ไอคอน เมนู และกล่องโต้ตอบที่แอปพลิเคชันของคุณใช้ ไฟล์ทรัพยากรมักจะมีนามสกุล .res; มีทรัพยากร เช่น เคอร์เซอร์ รูปภาพ และข้อมูลเวอร์ชัน ไฟล์ RES อาจเป็นไฟล์ทรัพยากร 16 หรือ 32 บิต
## โครงสร้างไฟล์ทรัพยากร
ไฟล์รีซอร์สประกอบด้วยชุดของรีซอร์สต่างๆ แต่ละรายการประกอบด้วยส่วนหัวของทรัพยากรและข้อมูลที่เกี่ยวข้อง ส่วนหัวของทรัพยากรมักจะอยู่ในแนว DWORD ในไฟล์และประกอบด้วยสิ่งต่อไปนี้:

- **DWORD** เพื่อระบุขนาดของส่วนหัวทรัพยากร
- **DWORD** เพื่อระบุขนาดของข้อมูลทรัพยากร
- ประเภททรัพยากร
- ชื่อทรัพยากร
- ข้อมูลทรัพยากรเพิ่มเติม

โครงสร้างส่วนหัวของทรัพยากรกำหนดรูปแบบของไฟล์ RES ข้อมูลสำหรับทรัพยากรเป็นไปตามส่วนหัวของทรัพยากร ทรัพยากรบางอย่างยังเพิ่มรูปแบบส่วนหัวของกลุ่มเฉพาะทรัพยากรเพื่อให้ข้อมูลเกี่ยวกับกลุ่มของทรัพยากร ต่อไปนี้เป็นประเภทรายการทรัพยากรและคำอธิบาย:

### ทรัพยากรตารางตัวเร่งความเร็ว
ตารางส่วนเร่งเป็นรายการทรัพยากรในไฟล์ RES โดยไม่มีส่วนหัวของกลุ่ม รูปแบบ **ACCELTABLEENTRY** กำหนดแต่ละรายการในตารางส่วนเร่ง ไฟล์ RES อาจมีตารางตัวเร่งความเร็วหลายตัว

### ทรัพยากรเคอร์เซอร์และไอคอน
แม้ว่าระบบจะถือว่าแต่ละไอคอนและเคอร์เซอร์เป็นไฟล์เดียว แต่สิ่งเหล่านี้จะถูกจัดเก็บไว้ในไฟล์ RES เป็นกลุ่มของทรัพยากรไอคอนหรือกลุ่มของทรัพยากรเคอร์เซอร์ รูปแบบไฟล์ของทรัพยากรไอคอนและเคอร์เซอร์เหมือนกัน ส่วนหัวของกลุ่มรีซอร์สตามหลังไอคอนแต่ละรายการหรือคอมโพเนนต์กลุ่มเคอร์เซอร์ในไฟล์ .res

### ทรัพยากรกล่องโต้ตอบ
กล่องโต้ตอบยังรับรู้เป็นรายการทรัพยากรในไฟล์ RES ประกอบด้วยรูปแบบส่วนหัวของกล่องโต้ตอบ **DLGITEMTEMPLATE** หนึ่งรูปแบบ และรูปแบบ **DLGITEMTEMPLATE** หนึ่งรูปแบบสำหรับแต่ละตัวควบคุมเฉพาะในกล่องโต้ตอบ รูปแบบ **DLGTEMPLATEEX** และ **DLGITEMTEMPLATEEX** อธิบายถึงรูปแบบของทรัพยากรกล่องโต้ตอบแบบขยาย

### ทรัพยากรแบบอักษร
ทรัพยากรเมนูมีรูปแบบ **MENUHEADER** ตามมาด้วยรูปแบบ **NORMALMENUITEM** หรือ **POPUPMENUITEM** อย่างน้อยหนึ่งรูปแบบ สำหรับแต่ละรายการเมนูในเทมเพลตเมนู รูปแบบ **MENUEX_TEMPLATE_HEADER** และ **MENUEX_TEMPLATE_ITEM** อธิบายถึงรูปแบบของทรัพยากรเมนูเพิ่มเติม

### ทรัพยากรตารางข้อความ
ตารางข้อความประกอบด้วยข้อความที่จัดรูปแบบสำหรับแสดงเป็นข้อความแสดงข้อผิดพลาดหรือในกล่องข้อความ รูปแบบหลักในทรัพยากรตารางข้อความคือโครงสร้าง **MESSAGE_RESOURCE_DATA**

### ทรัพยากรเวอร์ชัน
รูปแบบหลักในทรัพยากรเวอร์ชันคือ **VS_FIXEDFILEINFO** รูปแบบเพิ่มเติม ได้แก่ **VarFileInfo** เพื่อจัดเก็บข้อมูลที่เกี่ยวข้องกับภาษา และ **StringFileInfo** สำหรับข้อมูลสตริงที่กำหนดเอง




## อ้างอิง

* [รูปแบบไฟล์ทรัพยากร](https://docs.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 


