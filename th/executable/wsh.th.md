{
  "date" : "2021-08-27",
  "keywords" :[ "ไฟล์ wsh", "รูปแบบไฟล์ wsh", "ไฟล์ wsh คืออะไร", "ไฟล์", "ตัวอย่าง wsh", "นามสกุลไฟล์ wsh", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ WSH และ API ที่สามารถสร้างและเปิดไฟล์ WSH",
  "title" :"WSH - ไฟล์สคริปต์ Windows",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## ไฟล์ WSH คืออะไร??
ไฟล์ที่มีนามสกุล .wsh มีคุณสมบัติและพารามิเตอร์สำหรับสคริปต์ภาษาโปรแกรมบางอย่าง เช่น VB หรือ VBS เป็นต้น ความต้องการที่แท้จริงของ WSH คือการใช้สิ่งเหล่านี้เพื่อปรับแต่งการทำงานของสคริปต์บางตัว จำเป็นต้องใช้ WScript หรือ CScript และทั้งสองอย่างนี้รวมอยู่ในระบบปฏิบัติการ Windows ไฟล์ WSH นั้นถูกจัดเตรียมไว้บน Windows 95 ในแผ่นดิสก์การติดตั้ง โดยเป็นตัวเลือกที่กำหนดค่าได้และติดตั้งได้สำหรับแผงควบคุม จากนั้นเป็นส่วนประกอบเริ่มต้นของ Windows 98

## รูปแบบไฟล์ WSH
WSH (Windows Script Host) อาจใช้เพื่อวัตถุประสงค์ต่างๆ รวมถึงการดูแลระบบ สคริปต์การเข้าสู่ระบบ และระบบอัตโนมัติทั่วไป WSH สร้างสภาพแวดล้อมสำหรับสคริปต์ที่จะรัน มันเรียกใช้เอ็นจิ้นสคริปต์ที่เหมาะสมและจัดสรรชุดบริการและออบเจกต์สำหรับสคริปต์ที่จะทำงานด้วย สคริปต์เหล่านี้สามารถเรียกใช้ในโหมด GUI จากวัตถุ COM หรือโหมดบรรทัดคำสั่ง ทำให้ผู้ใช้มีความยืดหยุ่นทั้งสคริปต์แบบโต้ตอบและไม่ใช่แบบโต้ตอบ

### ตัวอย่าง
นี่คือตัวอย่างง่ายๆ ที่แสดง VBScript บางตัวที่ใช้วัตถุ WSH COM รูท "WScript" เพื่อแสดงข้อความด้วยปุ่ม 'ตกลง' เมื่อสคริปต์นี้จะเปิดตัว เอ็นจิ้น CScript หรือ WScript จะถูกเรียกและสภาพแวดล้อมรันไทม์จะถูกสร้างขึ้น

```
WScript.Echo "Hello world"
WScript.Quit
```


## อ้างอิง

* [โฮสต์สคริปต์ Windows - โดย Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)


