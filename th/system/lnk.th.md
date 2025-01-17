{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "นามสกุล", "ไฟล์", "รูปแบบ", "ระบบ", "ไฟล์ LNK", "ลิงก์", "ไฟล์ LNK", "เอกสาร LNK", "แอปพลิเคชัน", "โปรแกรม" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - รูปแบบไฟล์ลิงค์",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ LNK และ API ที่สามารถสร้างและเปิดไฟล์ LNK",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## ไฟล์ LNK คืออะไร?? ##

ไฟล์ LNK ซึ่งคล้ายกับข้อมูลระบุตัวตนในระบบ Mac เป็นทางเลือกของ Windows หรือ "ลิงก์" ที่ทำหน้าที่เป็นตัวเชื่อมต่อกับโฟลเดอร์หรือโปรแกรมเอกสารภาพต้นฉบับ ประกอบด้วยประเภท ตำแหน่ง และชื่อไฟล์ของปลายทางทางลัด ตลอดจนแอปพลิเคชันที่เปิดเอกสารเป้าหมายและปุ่มทางลัดเพิ่มเติม

ใน Windows ให้ตรงไฟล์ โฟลเดอร์ หรือโปรแกรมที่เรียกใช้งานได้ แล้วเลือกสร้างทางลัด ตำแหน่งของรูปแบบไฟล์และไดเร็กทอรี "จุดเริ่มต้น" เป็นคุณสมบัติพื้นฐานสองประการของไฟล์ LNK รูปแบบไฟล์ของไฟล์ LNK ถูกปิดบัง และลูกศรโค้งแสดงว่าเป็นทางลัด

## รูปแบบไฟล์ LNK ##

รูปแบบไฟล์ LNK มักจะมีไอคอนเดียวกันกับไฟล์ปลายทาง แต่ด้วยการเพิ่มลูกศรโค้งเล็กน้อยเพื่อแสดงว่าไฟล์นั้นชี้ไปยังตำแหน่งอื่น เมื่อดับเบิ้ลคลิกช็อตคัท ช็อตคัทจะทำงานเหมือนกับว่าผู้ใช้ดับเบิลคลิกไฟล์จริง

ไฟล์ LNK ที่มีทางลัดแอปพลิเคชันอาจมีคุณสมบัติที่ส่งผลต่อการทำงานของโปรแกรม หากต้องการเปลี่ยนแอตทริบิวต์ ให้คลิกขวาที่ไฟล์ทางลัดแล้วเลือก **คุณสมบัติ** จากนั้นเปลี่ยนช่องเป้าหมาย

แทนที่จะเป็นนามสกุลไฟล์ ไฟล์ LNK เป็นนามสกุลของ Windows Explorer ในฐานะส่วนขยายเทอร์มินัล เอกสาร .lnk สามารถใช้ได้เฉพาะใน Windows Explorer เพื่อแทนที่ไฟล์ และเอกสารเหล่านี้มีวัตถุประสงค์อื่นใน Windows Explorer นอกเหนือจากการทำหน้าที่เป็นทางลัดไปยังเอกสารในเครื่อง ไฟล์เหล่านี้ขึ้นต้นด้วยตัวอักษร "L" เช่นกัน

แม้ว่าทางลัดจะลิงก์ไปยังไฟล์และไดเร็กทอรีเฉพาะเมื่อสร้างขึ้น แต่อาจใช้งานไม่ได้หากเปลี่ยนเป้าหมายไปยังตำแหน่งอื่น Explorer จะเริ่มซ่อมแซมโฟลเดอร์ทางลัดที่ชี้ไปยังเป้าหมายที่ตายแล้วเมื่อเปิดขึ้น


## ข้อมูลจำเพาะทางเทคนิค ##

เฉพาะเมื่อไม่ได้เลือกการตั้งค่าการดูโฟลเดอร์ "ซ่อนส่วนขยายสำหรับประเภทไฟล์ที่รู้จัก" Windows จะไม่แสดงส่วนขยายเอกสาร .lnk สำหรับทางลัดเอกสาร แม้จะไม่แนะนำ แต่คุณสามารถเปิดใช้งานนามสกุลไฟล์ที่จะแสดงได้โดยการลบคุณสมบัติ "NeverShowExt" ออกจากไฟล์ HKEY_CLASSES_ROOT\lnk รายการรีจิสทรีของ Windows

โดยทำตามขั้นตอนเหล่านี้:

* เปิด "Registration Editor" โดยป้อน "Regedit" ในช่องค้นหาแถบงานแล้วเลือกโปรแกรม
* ในแอปพลิเคชัน นำทางไปยังตำแหน่งไฟล์ Computer\HKEY HKEY_CLASSES_ROOT\lnk
* ทำการสำรองข้อมูลของรายการโดยคลิกขวาที่รายการนั้นแล้วเลือกส่งออก
* เลือกและลบแอตทริบิวต์ "NeverShowExt"
* ควรรีสตาร์ท Windows


## อ้างอิง ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
