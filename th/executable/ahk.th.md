{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ AHK และ API ที่สามารถสร้างและเปิดไฟล์ AHK",
  "title" :"รูปแบบไฟล์ AHK- ไฟล์สคริปต์ AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## ไฟล์ AHK คืออะไร??

ไฟล์ AHK เป็นไฟล์สคริปต์ที่สร้างด้วยแอปพลิเคชันซอฟต์แวร์ AutoHotkey ที่ใช้สำหรับการทำงานอัตโนมัติใน Microsoft Windows มันมีคำแนะนำสำหรับการทำงานอัตโนมัติโดยใช้ปุ่มลัดที่สามารถใช้เพื่อดำเนินการทันที ไฟล์นี้ดำเนินการโดย AutoHotkey และการดำเนินการทั้งหมดจะดำเนินการตามลำดับ ไฟล์ AHK นั้นทรงพลังพอที่จะทำงานที่ซับซ้อนโดยใช้ปุ่มลัดที่กำหนดโดยใช้ปุ่มลัด ไฟล์ AHK สามารถเปิดได้ด้วยโปรแกรมแก้ไขข้อความ เช่น Microsoft Notepad และ Notepad++

## รูปแบบไฟล์ AHK

ไฟล์ AHK จะถูกบันทึกลงดิสก์เป็นไฟล์ข้อความธรรมดาและมีบรรทัดของโค้ดที่ AutoHotkey เรียกใช้ได้ AutoHotkey เป็นภาษาสคริปต์แบบโอเพ่นซอร์สฟรี และอนุญาตให้ผู้ใช้สร้างสคริปต์แบบง่ายไปจนถึงแบบซับซ้อนเพื่อดำเนินการต่างๆ เช่น การกรอกแบบฟอร์ม การคลิกอัตโนมัติ การเรียกใช้งานมาโคร เป็นต้น ไฟล์ AHK อย่างน้อยที่สุดสามารถดำเนินการเพียงครั้งเดียวแล้วออก .

มีเครื่องมือที่สามารถใช้เพื่อแปลงไฟล์ AHK เป็น [Exe](/th/executable/exe/)

### ตัวอย่าง AHK

ตัวอย่างต่อไปนี้ใช้ปุ่ม Win+Z เพื่อเรียกใช้ Microsoft Notepad หรือนำปุ่มนี้ไปไว้ข้างหน้าหากมีการเรียกใช้อยู่แล้ว

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad"),
    WinActivate
else
    Run Notepad
return
```

## ฉันจะสร้างไฟล์ AHK ได้อย่างไร

สามารถใช้ขั้นตอนต่อไปนี้เพื่อสร้างไฟล์ AHK สิ่งเหล่านี้ถือว่ามีการติดตั้ง AutoHotkey ไว้ในเครื่องแล้ว

* คลิกขวาบนเดสก์ท็อปของคุณ
* ค้นหา "ใหม่" ในเมนู
* คลิก "AutoHotkey Script" ในเมนู "New"
* ตั้งชื่อสคริปต์ใหม่
* ค้นหาไฟล์ที่สร้างขึ้นใหม่บนเดสก์ท็อปแล้วคลิกขวา
* คลิก "แก้ไขสคริปต์"
* ควรมีหน้าต่างโผล่ขึ้นมา อาจเป็น Notepad
* บันทึกไฟล์

## อ้างอิง

* [AutoHotkey](https://www.autohotkey.com/)
* [ไฟล์แบทช์ - โดย Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

