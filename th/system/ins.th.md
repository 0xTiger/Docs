{
  "date" : "2021-07-16",
  "keywords" :[ "ไฟล์ ins", "รูปแบบไฟล์ ins", "ไฟล์ ins คืออะไร", "ไฟล์", "ตัวอย่าง ins", "นามสกุลไฟล์ ins", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ INS และ API ที่สามารถสร้างและเปิดไฟล์ INS",
  "title" :"INS - ไฟล์การตั้งค่าอินเทอร์เน็ต",
  "linktitle" : "INS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-16"
}

## ไฟล์ INS คืออะไร??

Microsoft Windows จะใช้ไฟล์ที่มีนามสกุล .ins เพื่อตั้งค่าการเชื่อมต่อผ่านสายโทรศัพท์และอินเทอร์เน็ตบรอดแบนด์ ที่จริงแล้ว มันมีข้อมูลการตั้งค่าการเชื่อมต่อที่อนุญาตให้ Windows ตั้งค่าการเข้าถึงอินเทอร์เน็ตไปยัง ISP ไฟล์ INS มักใช้สำหรับตั้งค่าการเชื่อมต่อ LAN ของ Internet Explorer (IE) ไฟล์การตั้งค่าการเชื่อมต่อ IE บางครั้ง ISP และผู้ดูแลระบบจัดเตรียมให้กับผู้ใช้โดยมี URL ไปยังไฟล์ INS

## รูปแบบไฟล์ INS
คุณสามารถใช้ไฟล์การตั้งค่าอินเทอร์เน็ต (INS) ร่วมกับ Internet Explorer Administration Kit 11 (IEAK 11) เพื่อกำหนดค่าเบราว์เซอร์ที่กำหนดเองและส่วนประกอบต่างๆ คุณสามารถเขียนแพ็คเกจแบบกำหนดเองของคุณในเวอร์ชันต่างๆ ได้โดยปรับแต่งสำเนาของไฟล์ INS

### การตั้งค่า INS ที่เป็นไปได้
การตั้งค่า INS ที่เป็นไปได้มีให้ในตารางต่อไปนี้:

| การตั้งค่า | คำอธิบาย |
-----|---------|
| URL | จะใช้พร็อกซีเซิร์ฟเวอร์ที่กำหนดค่าอัตโนมัติหรือไม่ |
| การสร้างแบรนด์ | ปรับแต่งข้อมูลการสร้างแบรนด์และการตั้งค่าในแพ็คเกจเบราว์เซอร์ของคุณ |
| สื่อ | ประเภทของสื่อที่มีแพ็คเกจการติดตั้งแบบกำหนดเองของคุณ |
| แถบเครื่องมือเบราว์เซอร์ | ปรับแต่งรูปลักษณ์ของแถบเครื่องมือ IE |
| การลงนามรถแท็กซี่ | ข้อมูลลายเซ็นดิจิทัลสำหรับโปรแกรมของคุณ |
| ซ่อนกำหนดเอง | ซ่อนตัวระบุส่วนกลาง (GUID) สำหรับส่วนประกอบที่กำหนดเองแต่ละรายการหรือไม่ |
| การตั้งค่าการเชื่อมต่อ | ข้อมูลเกี่ยวกับการตั้งค่าการเชื่อมต่อเครือข่ายที่ใช้ในการติดตั้งแพ็คเกจแบบกำหนดเองของคุณ |
| การสร้างแบรนด์ที่กำหนดเอง | ตำแหน่ง URL ไปยังไฟล์ cabinet (.cab) ของแบรนด์ของคุณ |
| ExtRegInf | ชื่อของไฟล์ข้อมูลการตั้งค่า (.inf) ของคุณและโหมดการติดตั้งสำหรับคอมโพเนนต์ |
| รายการโปรดEx | เพิ่มเส้นทางไปยังไฟล์ไอคอนของคุณสำหรับรายการโปรด ตัดสินใจว่ารายการโปรดจะพร้อมใช้งานแบบออฟไลน์หรือไม่ และเพิ่ม URL ในแต่ละไซต์รายการโปรด |
| ISP_ความปลอดภัย | ใบรับรองหลักที่คุณกำลังเพิ่มในแพ็คเกจที่กำหนดเอง |
| หนังสือมอบฉันทะ | จะใช้พร็อกซีเซิร์ฟเวอร์หรือไม่ |
| นำเข้าความปลอดภัย | ว่าจะนำเข้าข้อมูลความปลอดภัยสำหรับแพ็คเกจที่คุณกำหนดเองหรือไม่ |




## อ้างอิง

* [การใช้ไฟล์การตั้งค่าอินเทอร์เน็ต (.INS) กับ IEAK 11](https://docs.microsoft.com/en-us/internet-explorer/ie11-ieak/using-internet-settings-ins-files)

