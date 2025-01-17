{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "ส่วนขยาย", "ไฟล์", "รูปแบบ", "ระบบ", "การเริ่มต้น", "ส่วนขยายไดเร็กทอรี", "โปรแกรม", "คอมพิวเตอร์", "แอปพลิเคชัน" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - รูปแบบไฟล์เริ่มต้น",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ INI และ API ที่สามารถสร้างและเปิดไฟล์ INI",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## ไฟล์ INI คืออะไร?? ##

ไฟล์ INI เป็นเอกสารการกำหนดค่าข้อความสำหรับโปรแกรมคอมพิวเตอร์ที่มีคีย์สาธารณะสำหรับลักษณะและส่วนที่จัดระเบียบแอตทริบิวต์ในเฟรมเวิร์กและไวยากรณ์ เอกสารการกำหนดค่ารูปแบบไฟล์ระบบเหล่านี้มีชื่อมาจากนามสกุลไดเรกทอรี INI ของระบบปฏิบัติการ MS-DOS ซึ่งหมายถึงการเริ่มต้น ทำให้การตั้งค่าซอฟต์แวร์รูปแบบนี้เป็นที่นิยม หลายโปรแกรมในแอปพลิเคชันซอฟต์แวร์อื่นๆ ใช้ชื่อไฟล์เพิ่มเติม เช่น CONF และ [CFG](/th/system/cfg/) แม้ว่ารูปแบบดังกล่าวจะสร้างมาตรฐานอย่างไม่เป็นทางการในหลายๆ สถานการณ์ของการกำหนดค่า

## ประวัติย่อของไฟล์ INI##

ในขั้นต้น เทคนิคการกำหนดค่าโปรแกรมหลักของ Windows เป็นรูปแบบไฟล์ข้อความที่ประกอบด้วยบรรทัดข้อความที่มีคู่สำคัญหนึ่งคู่ต่อบรรทัด โดยแบ่งออกเป็นส่วนต่างๆ ไดรเวอร์อุปกรณ์ แบบอักษร และตัวเรียกใช้เริ่มต้นถูกจัดเก็บไว้ในรูปแบบนี้ทั้งหมด การตั้งค่าส่วนบุคคลมักถูกเก็บไว้ในไฟล์ INI โดยแอพ
จนถึง Windows 3.1x รูปแบบได้รับการสนับสนุนบนแพลตฟอร์ม Microsoft Windows 16 บิต ตั้งแต่ Windows 95 เป็นต้นมา Microsoft เริ่มสนับสนุนให้นักพัฒนาใช้ Windows Registry แทนไฟล์ INI สำหรับการกำหนดค่า

## ไฟล์ INI - ข้อมูลจำเพาะรูปแบบไฟล์

### คีย์/คุณสมบัติ ###

คีย์/คุณสมบัติเป็นองค์ประกอบพื้นฐานที่สุดของไฟล์ INI สัญลักษณ์เท่ากับ (=) แยกชื่อและค่าของแต่ละคีย์ ทางด้านซ้ายของเครื่องหมายเท่ากับคือตำแหน่งที่แสดงชื่อ สัญลักษณ์เท่ากับและเครื่องหมายอัฒภาคเป็นตัวอักษรที่ไม่สุภาพในระบบ Windows ดังนั้นจึงไม่สามารถใช้ในคีย์ได้ สามารถใช้อักขระใดก็ได้ในค่า

```
name=value
```

### ส่วน ###

ความคิดเห็นของส่วนปรากฏในวงเล็บเหลี่ยม ([]) ในบรรทัดของตัวเอง หลังจากคำจำกัดความของส่วน คีย์ทั้งหมดจะเชื่อมโยงกับส่วนนั้น ส่วนจะสิ้นสุดที่การกำหนดส่วนถัดไปหรือจุดสิ้นสุดของเอกสาร ไม่มีตัวคั่น "ส่วนท้ายของส่วน" เฉพาะ ไม่สามารถซ้อนส่วนได้ สามารถตั้งชื่อได้เพียงครั้งเดียวและไม่จำเป็นต้องเชื่อมโยง

```
[section]
a=a
b=b
```

### การเปลี่ยนแปลงคุณสมบัติ ###

รูปแบบไฟล์ INI ไม่มีคำจำกัดความที่ยอมรับทั่วโลก แอปพลิเคชันคอมพิวเตอร์จำนวนมากมีฟังก์ชันนอกเหนือจากที่กล่าวถึงแล้ว รายการด้านล่างประกอบด้วยลักษณะทั่วไปบางอย่างที่อาจมีหรือไม่มีในแต่ละโปรแกรม

* ความคิดเห็น
* ตัวละครหนี
* ชื่อซ้ำกัน


## ตัวอย่าง INI ##

ไฟล์ INI ตัวอย่างมีลักษณะดังนี้:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## อ้างอิง ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

