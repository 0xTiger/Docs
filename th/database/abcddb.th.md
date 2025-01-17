{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "เรียนรู้เกี่ยวกับรูปแบบไฟล์ ABCDDB และ API ที่สามารถสร้างและเปิดไฟล์ ABCDDB",
  "title" : "รูปแบบไฟล์ ABCDDB - ไฟล์ฐานข้อมูลรายชื่อผู้ติดต่อสมุดที่อยู่ของ Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-th",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## ไฟล์ ABCDDB คืออะไร??

ไฟล์ที่มีนามสกุล **.ABCDDB** ย่อมาจาก Apple Address Book Contact List Database เป็นของแอปพลิเคชัน **สมุดที่อยู่** หรือที่เรียกกันทั่วไปว่า **ผู้ติดต่อ** เป็นแอปพลิเคชั่นในตัวและรวมอยู่ในระบบปฏิบัติการ iOS และ macOS แอปพลิเคชันผู้ติดต่อทำให้ผู้ใช้สามารถบันทึกและจัดระเบียบข้อมูลที่เกี่ยวข้องกับผู้ติดต่อของตน รวมถึงบุคคล ธุรกิจ และองค์กร แอพนี้ช่วยให้ผู้ใช้ติดตามรายละเอียด เช่น ชื่อ ที่อยู่ หมายเลขโทรศัพท์ และที่อยู่อีเมล รวมถึงจัดหมวดหมู่ผู้ติดต่อออกเป็นกลุ่ม

## ความสัมพันธ์กับ SQLite และเส้นทางทั่วไป

สมุดที่อยู่ของ Apple (หรือที่เรียกว่ารายชื่อติดต่อ) จะจัดเก็บข้อมูลรายชื่อเป็น vCard ไว้ในโฟลเดอร์ข้อมูลเมตา **ไฟล์ _ABCDDB_ จริงๆ แล้วคือ _SQLite 3 datafile_**

SQLite เป็นระบบจัดการฐานข้อมูลยอดนิยมที่ออกแบบมาให้มีน้ำหนักเบาและมีความสมบูรณ์ในตัวเอง มันถูกใช้ในซอฟต์แวร์และอุปกรณ์หลายประเภท SQLite เป็น RDBMS ประเภทหนึ่ง ซึ่งหมายความว่าจะเก็บข้อมูลในตารางที่เกี่ยวข้องกันผ่านคีย์ สามารถจัดการประเภทข้อมูลได้หลากหลาย รวมถึงจำนวนเต็ม ตัวเลขทศนิยม สตริง และข้อมูลไบนารี นอกจากนี้ SQLite ยังรองรับธุรกรรมซึ่งช่วยให้ผู้ใช้สามารถดำเนินการฐานข้อมูลหลายรายการพร้อมกันเป็นหน่วยงานเดียว

โดยทั่วไปไฟล์ที่มีนามสกุล ABCDDB จะถูกเก็บไว้ที่นี่

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## แก้ไขฐานข้อมูลผู้ติดต่อที่เสียหาย

โปรดสำรองข้อมูลก่อนที่จะพยายามดำเนินการนี้ จากนั้นกรุณานำทางไปยัง

`~/Library/Application Support/AddressBook`

ในไดเร็กทอรีนั้น คุณจะพบไฟล์สามไฟล์ รวมถึงไฟล์ที่มีนามสกุล .abcddb

- `สมุดที่อยู่-v22.abcddb`
- `สมุดที่อยู่-v22.abcddb-wal`
- `สมุดที่อยู่-v22.abcddb-shm`

ลบไฟล์เหล่านี้ทั้งหมดแล้วเปิดผู้ติดต่ออีกครั้ง ซึ่งจะเริ่มทำงานอีกครั้ง

## กู้คืนฐานข้อมูล AddressBook จากการสำรองข้อมูล

สมมติว่า ผู้ติดต่อในฐานข้อมูล AddressBook ของคุณถูกจัดเก็บไว้ใน `addressbook-v22.abcddb`

- ขั้นแรกให้สำรองข้อมูล AddressBook ของคุณแล้วออกจากแอปพลิเคชันทั้งหมด
- ย้ายไฟล์ฐานข้อมูลของคุณไปที่ไดเร็กทอรีย่อย `~/Library/Application Support/AddressBook`
- เปิดตัว **Address Book.app**

## ส่งออกข้อมูลไฟล์ ABCDDB ไปยัง Microsoft Access

เนื่องจากไฟล์นี้เป็นไฟล์ข้อมูล SQLite 3 คุณจึงสามารถส่งออกข้อมูลภายในไฟล์ abcddb ไปยัง Microsoft Access โดยใช้ตัวเชื่อมต่อ ODBC

ตัวเชื่อมต่อ SQLite ODBC คือไลบรารีซอฟต์แวร์และไดรเวอร์ที่ช่วยให้แอปพลิเคชันที่รองรับอินเทอร์เฟซ ODBC สามารถเชื่อมต่อกับฐานข้อมูล SQLite ประกอบด้วยไลบรารีที่กำหนดอินเทอร์เฟซ ODBC และไดรเวอร์ที่แปลอินเทอร์เฟซนี้เป็นการเรียกไปยัง SQLite API หากต้องการใช้ตัวเชื่อมต่อ SQLite ODBC คุณต้องติดตั้งก่อน จากนั้นจึงตั้งค่าแหล่งข้อมูล ODBC บนคอมพิวเตอร์ของคุณ หลังจากทำตามขั้นตอนเหล่านี้แล้ว แอปพลิเคชันใดๆ ที่รองรับ ODBC จะสามารถเชื่อมต่อกับแหล่งข้อมูลและดึงข้อมูลจากฐานข้อมูล SQLite ได้

## อ้างอิง
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [ติดต่อฐานข้อมูลสำหรับ Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [ฉันจะเปิดหรือส่งออกไฟล์ abcddb ใน Windows 7 Excel ได้อย่างไร](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

