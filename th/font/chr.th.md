{
"วันที่": "10-10-2023",
   "keywords":[
"ชร์",
"ไฟล์ chr",
"ไฟล์ชุดอักขระ chr borland",
"วิธีการเปิดไฟล์ ch",
"ไฟล์",
"นามสกุลไฟล์ chr",
"ส่วนขยาย",
"ไฟล์"
],
   "author":{
"display_name":"ชาคีล ไฟซ์"
},
"draft": "false",
"toc":true,
"title":"รูปแบบไฟล์ CHR - ชุดอักขระบอร์แลนด์",
   "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ชุดอักขระ CHR Borland และ API ที่สามารถสร้างและเปิดไฟล์ CHR",
   "linktitle":"CHR",
   "menu":{
      "docs":{
         "identifier":"font-chr",
         "parent":"font"
}
},
"lastmod":"2023-10-11"
}

## ไฟล์ CHR คืออะไร??

ไฟล์ CHR ยังสามารถใช้เป็นไฟล์กำหนดค่าแบบอักษรที่ใช้โดย Microsoft Windows ไฟล์ประเภทนี้เก็บข้อมูลสำคัญที่ใช้ในการปรับขนาดและรูปแบบของแบบอักษรภายในระบบปฏิบัติการ แอปพลิเคชันซอฟต์แวร์ที่โต้ตอบกับแบบอักษรของระบบสามารถใช้ไฟล์ ".chr" เหล่านี้เพื่อปรับแต่งลักษณะที่ปรากฏของแบบอักษรเหล่านี้บนหน้าจอได้

## ชุดตัวละครบอร์แลนด์

"ชุดอักขระ" หมายถึงชุดอักขระ สัญลักษณ์ หรือสัญลักษณ์ที่กำหนดไว้ล่วงหน้าซึ่งเกี่ยวข้องกับรหัสตัวเลขเฉพาะ อักขระแต่ละตัวภายในชุดจะได้รับการกำหนดรหัสหรือตัวระบุที่ไม่ซ้ำกัน ซึ่งมักแสดงเป็นค่าตัวเลข ชุดอักขระเป็นพื้นฐานในการเข้ารหัสและแสดงข้อความในคอมพิวเตอร์และระบบดิจิทัล

ต่อไปนี้เป็นประเด็นสำคัญบางประการเกี่ยวกับชุดอักขระ:

1. **ชุดอักขระ ASCII:** ชุดอักขระที่รู้จักกันดีที่สุดคือชุดอักขระ ASCII (American Standard Code for Information Interchange) ซึ่งประกอบด้วยอักขระ เช่น ตัวอักษร ตัวเลข เครื่องหมายวรรคตอน และอักขระควบคุม ASCII ใช้ 7 หรือ 8 บิตเพื่อแสดงอักขระแต่ละตัว
    





2. **Unicode:** Unicode คือชุดอักขระที่ใช้กันอย่างแพร่หลายซึ่งมีจุดมุ่งหมายเพื่อรวมอักขระจากระบบการเขียนทั้งหมดในโลก ใช้จุดโค้ดที่ไม่ซ้ำกัน (ค่าตัวเลข) สำหรับอักขระแต่ละตัว ทำให้สามารถแสดงอักขระจากภาษา สคริปต์ และสัญลักษณ์ต่างๆ ได้
    





3. **การเข้ารหัสอักขระ:** ชุดอักขระมักใช้ร่วมกับการเข้ารหัสอักขระ การเข้ารหัสอักขระคือการแมประหว่างรหัสอักขระและการแทนค่าไบนารี (โดยปกติจะเป็นไบต์) ที่สามารถจัดเก็บหรือส่งแบบดิจิทัล การเข้ารหัสอักขระทั่วไป ได้แก่ UTF-8 และ UTF-16 สำหรับ Unicode
    





4. **การรองรับภาษา:** ชุดอักขระอาจแตกต่างกันไปในแง่ของการรองรับภาษา ชุดอักขระบางชุดมีความเฉพาะเจาะจงสำหรับภาษาหรือสคริปต์บางภาษา ในขณะที่ชุดอักขระอื่นๆ จะครอบคลุมมากกว่าและรองรับหลายภาษา
    





5. **ชุดอักขระแบบเดิม:** ในอดีต ระบบคอมพิวเตอร์และภูมิภาคต่างๆ ใช้ชุดอักขระของตนเอง ซึ่งอาจทำให้เกิดปัญหาในการแบ่งปันข้อมูลระหว่างระบบ Unicode ได้แก้ไขปัญหาความเข้ากันได้เหล่านี้เป็นส่วนใหญ่
    





6. **HTML และเว็บ:** เมื่อทำงานกับการพัฒนาเว็บและ HTML ให้ระบุชุดอักขระในข้อมูลเมตาของเอกสาร (เช่น การใช้ `<meta> ` ที่มีแอตทริบิวต์ "charset") เป็นสิ่งสำคัญเพื่อให้แน่ใจว่ามีการแสดงข้อความที่เหมาะสม

## เปิดไฟล์ .CHR ได้อย่างไร

ไฟล์ CHR ไม่ได้มีไว้สำหรับการเปิดหรือแก้ไขด้วยตนเองโดยผู้ใช้ แต่จะทำหน้าที่เป็นไฟล์กำหนดค่าที่โปรแกรม Windows โดยเฉพาะที่โต้ตอบกับแบบอักษรของระบบสามารถเข้าถึงได้เมื่อจำเป็น โปรแกรมเหล่านี้โหลดไฟล์ CHR เพื่อดึงข้อมูลเกี่ยวกับวิธีแสดงแบบอักษรเฉพาะ รวมถึงรายละเอียดเกี่ยวกับขนาด สไตล์ และคุณลักษณะอื่นๆ โดยทั่วไปผู้ใช้ไม่จำเป็นต้องโต้ตอบกับไฟล์ CHR โดยตรง เนื่องจากการจัดการแบบอักษรได้รับการจัดการโดยระบบปฏิบัติการและแอปพลิเคชันซอฟต์แวร์

## ไฟล์ CHR อื่นๆ

ต่อไปนี้คือไฟล์ประเภทอื่นๆ ที่ใช้นามสกุลไฟล์ **.chr**

**สามมิติ**
- [CHR - ไฟล์ตัวละคร CryENGINE](/th/3d/chr-cryengine/)
- [CHR - ไฟล์ตัวละคร 3ds Max](/th/3d/chr-3ds/)

**แบบอักษรและเกม**
- [CHR - ชุดอักขระบอร์แลนด์](/th/font/chr/)
- [CHR - ชมรมวรรณกรรมโดกิ โดกิ! ไฟล์ตัวละคร](/th/game/chr-doki/)

## อ้างอิง
- [ตัวละคร (คอมพิวเตอร์)](https://en.wikipedia.org/wiki/Character_(computing))

