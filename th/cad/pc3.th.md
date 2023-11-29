{
"วันที่": "2023-05-09",
  "keywords": [
"ไฟล์ pc3",
"ไฟล์ pc3 คืออะไร",
"วิธีสร้างไฟล์ pc3 ใน AutoCAD",
"ไฟล์ pc3 เป็นฟอร์แมตอะไร",
"ไฟล์ pc3 ประกอบด้วยอะไรบ้าง",
"ไฟล์",
"นามสกุลไฟล์ pc3",
"ส่วนขยาย"
],
  "author": {
"display_name": "ชาคีล ไฟซ์"
},
"draft": "false",
"toc": true,
"title": "รูปแบบไฟล์ PC3 - ไฟล์กำหนดค่าพล็อตเตอร์ AutoCAD",
  "description":"เรียนรู้เกี่ยวกับรูปแบบ PC3 และ API ที่สามารถสร้างและเปิดไฟล์ PC3",
"linktitle": "PC3",
  "menu": {
    "docs": {
      "identifier": "cad-pc3",
      "parent": "cad"
}
},
"lastmod": "2023-05-09"
}

## ไฟล์ PC3 คืออะไร?

ไฟล์ PC3 ใน AutoCAD เป็นไฟล์การกำหนดค่าพล็อตเตอร์ที่มีการตั้งค่าเครื่องพิมพ์หรือพล็อตเตอร์สำหรับใช้ในซอฟต์แวร์

เมื่อคุณสร้างการกำหนดค่าพล็อตเตอร์ใหม่ AutoCAD จะจัดเก็บข้อมูลที่จำเป็นทั้งหมดเกี่ยวกับเครื่องพิมพ์หรือพล็อตเตอร์ไว้ในไฟล์ PC3 ซึ่งรวมถึงสิ่งต่างๆ เช่น ขนาดกระดาษ ระยะขอบ ความละเอียด และการตั้งค่าอื่นๆ เฉพาะสำหรับเครื่องพิมพ์หรือพล็อตเตอร์ที่คุณใช้

คุณสามารถใช้ไฟล์ PC3 เพื่อตั้งค่าและกำหนดค่าเครื่องพิมพ์หรือพล็อตเตอร์ใน AutoCAD ได้อย่างง่ายดาย หากต้องการใช้ไฟล์ PC3 เพียงเลือกจากรายการการกำหนดค่าพล็อตเตอร์ที่มีอยู่ในกล่องโต้ตอบ Plot

คุณยังสามารถสร้างไฟล์ PC3 แบบกำหนดเองได้โดยแก้ไขการตั้งค่าของไฟล์ PC3 ที่มีอยู่ หรือโดยการสร้างไฟล์ PC3 ใหม่ตั้งแต่ต้นโดยใช้ Plotter Manager ใน AutoCAD

## จะสร้างไฟล์ PC3 ใน AutoCAD ได้อย่างไร?

หากต้องการสร้างไฟล์การกำหนดค่าพล็อตเตอร์ (PC3) ใน AutoCAD ให้ทำตามขั้นตอนเหล่านี้:

1. **เปิด Plotter Manager:** พิมพ์ "PLOTTERMANAGER" ในบรรทัดคำสั่งหรือไปที่แท็บ "Output" บน Ribbon และเลือก "Plotter Manager" จากแผง "Plot"
2. **คลิกที่ "Add-A-Plotter Wizard":** ซึ่งจะเปิดตัวช่วยสร้างที่จะแนะนำคุณตลอดกระบวนการสร้างไฟล์การกำหนดค่าพล็อตเตอร์ใหม่
3. **เลือกผู้ผลิตและรุ่นของพล็อตเตอร์:** ตัวช่วยสร้างจะแจ้งให้คุณเลือกผู้ผลิตและรุ่นของเครื่องพิมพ์หรือพล็อตเตอร์ของคุณจากรายการ หากไม่มีเครื่องพิมพ์หรือพล็อตเตอร์ของคุณอยู่ในรายการ คุณสามารถเลือก "My Computer" และเรียกดูไฟล์ไดรเวอร์ได้
4. **เลือกพอร์ต:** เลือกพอร์ตที่เครื่องพิมพ์หรือพล็อตเตอร์ของคุณเชื่อมต่ออยู่ หากคุณไม่แน่ใจ ให้ตรวจสอบเอกสารที่มาพร้อมกับเครื่องพิมพ์หรือพล็อตเตอร์ของคุณ
5. **ระบุการกำหนดค่าพล็อตเตอร์:** วิซาร์ดจะแจ้งให้คุณระบุการตั้งค่าต่างๆ สำหรับพล็อตเตอร์ของคุณ เช่น ขนาดกระดาษ ความละเอียด และความลึกของสี ตรวจสอบให้แน่ใจว่าได้ตั้งค่าตัวเลือกเหล่านี้อย่างถูกต้องสำหรับเครื่องพิมพ์หรือพล็อตเตอร์เฉพาะของคุณ
6. **บันทึกการกำหนดค่าพล็อตเตอร์:** เมื่อคุณระบุการตั้งค่าทั้งหมดแล้ว วิซาร์ดจะแจ้งให้คุณตั้งชื่อการกำหนดค่าพล็อตเตอร์ใหม่ สิ่งนี้จะสร้างไฟล์ PC3 ใหม่ในโฟลเดอร์ที่ระบุโดยวิซาร์ด
7. **ใช้การกำหนดค่าพล็อตเตอร์ใหม่:** หากต้องการใช้การกำหนดค่าพล็อตเตอร์ใหม่ใน AutoCAD ให้ไปที่กล่องโต้ตอบ "พล็อตเตอร์" เลือกการกำหนดค่าพล็อตเตอร์ใหม่ของคุณจากรายการการกำหนดค่าพล็อตเตอร์ที่มีอยู่ จากนั้นตั้งค่าพล็อตของคุณเป็น ตามปกติ.

แค่นั้นแหละ! ตอนนี้คุณได้สร้างไฟล์การกำหนดค่าพล็อตเตอร์ (PC3) ใหม่ใน AutoCAD ที่คุณสามารถใช้สำหรับการพิมพ์หรือการวางแผนภาพวาดของคุณ

## ไฟล์ PC3 อยู่ในรูปแบบใด

รูปแบบไฟล์ PC3 เป็นรูปแบบไฟล์ที่เป็นกรรมสิทธิ์ซึ่งใช้โดยซอฟต์แวร์ AutoCAD ของ Autodesk ประกอบด้วยการตั้งค่าสำหรับพล็อตเตอร์หรือเครื่องพิมพ์เฉพาะ รวมถึงขนาดกระดาษ ความลึกของสี ความละเอียด และตัวเลือกอื่นๆ

โดยทั่วไปไฟล์ PC3 จะถูกจัดเก็บไว้ในโฟลเดอร์ "Plotter Configuration" ในไดเร็กทอรีการติดตั้ง AutoCAD และสามารถแชร์ระหว่างผู้ใช้หรือคอมพิวเตอร์ได้อย่างง่ายดายเพื่อให้แน่ใจว่าการตั้งค่าการพิมพ์และการพล็อตมีความสม่ำเสมอ

ไฟล์ PC3 นั้นเป็นไฟล์ข้อความที่มีข้อมูล XML ซึ่งเป็นรูปแบบที่เครื่องอ่านได้สำหรับจัดเก็บและแลกเปลี่ยนข้อมูล คุณสามารถดูและแก้ไขเนื้อหาของไฟล์ PC3 ได้โดยใช้โปรแกรมแก้ไขข้อความหรือโปรแกรมแก้ไข XML แต่ขอแนะนำให้คุณใช้ Plotter Manager ใน AutoCAD เพื่อทำการเปลี่ยนแปลงการกำหนดค่าพล็อตเตอร์ เนื่องจากจะช่วยให้มั่นใจได้ว่าการตั้งค่ามีรูปแบบที่ถูกต้องและเข้ากันได้กับซอฟต์แวร์

## ไฟล์ PC3 ประกอบด้วยอะไรบ้าง

ไฟล์ PC3 ใน AutoCAD มีการตั้งค่าเครื่องพิมพ์หรือพล็อตเตอร์เฉพาะสำหรับอุปกรณ์หรือไดรเวอร์เฉพาะ การตั้งค่าเหล่านี้ถูกใช้โดย AutoCAD เพื่อพิมพ์หรือลงจุดภาพวาดของคุณอย่างถูกต้อง และเพื่อให้แน่ใจว่าภาพเหล่านั้นมีลักษณะตามที่คุณต้องการ

นี่คือการตั้งค่าบางส่วนที่สามารถจัดเก็บไว้ในไฟล์ PC3:

- **ขนาดกระดาษ:** เป็นการระบุขนาดของกระดาษที่จะใช้สำหรับการพิมพ์หรือการวางแผน เช่น A4, Letter หรือแบบกำหนดเอง
- **พื้นที่ลงจุด:** ส่วนนี้ระบุส่วนของภาพวาดที่จะลงจุด เช่น เค้าโครงทั้งหมดหรือเฉพาะหน้าต่างใดหน้าต่างหนึ่ง
- **มาตราส่วนพล็อต:** ระบุมาตราส่วนที่จะพิมพ์หรือลงจุดภาพวาด เช่น 1:100 หรือ 1/4"=1'-0"
- **น้ำหนักเส้น:** ค่านี้ระบุความหนาของเส้นในภาพวาด ซึ่งส่งผลต่อลักษณะที่ปรากฏเมื่อพิมพ์หรือลงจุด
- **ความลึกของสี:** ระบุจำนวนสีที่จะใช้ในการพิมพ์หรือลงจุด เช่น ขาวดำหรือเต็มสี
- **ความละเอียด:** ค่านี้เป็นการระบุความละเอียดที่จะพิมพ์หรือลงจุดภาพวาด ซึ่งส่งผลต่อความคมชัดและรายละเอียดที่จะดู
- **ตัวเลือกอื่นๆ:** มีตัวเลือกอื่นๆ มากมายที่สามารถตั้งค่าในไฟล์ PC3 ได้ เช่น คุณภาพการพิมพ์ การวางแนว ระยะขอบ การแรเงา และอื่นๆ

ด้วยการสร้างและใช้ไฟล์ PC3 ที่มีการตั้งค่าที่ถูกต้องสำหรับเครื่องพิมพ์หรือพล็อตเตอร์เฉพาะของคุณ คุณสามารถมั่นใจได้ว่าภาพวาดของคุณจะถูกพิมพ์หรือลงจุดอย่างถูกต้องและมีคุณภาพสม่ำเสมอ

## อ้างอิง
* [PC3 ใน AutoCAD](https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Creating-plotter-configuration-files-PC3.html)
