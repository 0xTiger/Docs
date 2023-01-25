{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ txt", "รูปแบบไฟล์ txt", "ไฟล์ txt คืออะไร", "ไฟล์", "ตัวอย่าง txt", "นามสกุลไฟล์ txt","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TXT - ไฟล์เอกสารข้อความ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ TXT และ API ที่สามารถสร้างและเปิดไฟล์ TXT",
  "linktitle" : "TXT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ TXT คืออะไร??

ไฟล์ที่มีนามสกุล .TXT แสดงถึงเอกสารข้อความที่มีข้อความธรรมดาในรูปแบบของบรรทัด ย่อหน้าในเอกสารข้อความจะรับรู้โดยการขึ้นบรรทัดใหม่และใช้เพื่อการจัดเรียงเนื้อหาไฟล์ที่ดีขึ้น เอกสารข้อความมาตรฐานสามารถเปิดได้ในโปรแกรมแก้ไขข้อความหรือโปรแกรมประมวลผลคำบนระบบปฏิบัติการที่แตกต่างกัน ข้อความทั้งหมดที่อยู่ในไฟล์ดังกล่าวอยู่ในรูปแบบที่มนุษย์อ่านได้และแสดงตามลำดับอักขระ

ไฟล์ข้อความสามารถเก็บข้อมูลจำนวนมากได้เนื่องจากไม่มีข้อจำกัดเกี่ยวกับขนาดของเนื้อหา อย่างไรก็ตาม โปรแกรมแก้ไขข้อความที่เปิดไฟล์ขนาดใหญ่เช่นนี้จำเป็นต้องฉลาดในการโหลดและแสดงไฟล์เหล่านี้ ระบบปฏิบัติการเกือบทั้งหมดมาพร้อมกับโปรแกรมแก้ไขข้อความที่ให้คุณสร้างและแก้ไขไฟล์ข้อความ ตัวอย่างเช่น ระบบปฏิบัติการ Windows มาพร้อมกับ Notepad และ Wordpad เพื่อจุดประสงค์นี้ ในทำนองเดียวกัน MacOS มาพร้อมกับ TextEdit สำหรับสร้างและแก้ไขเอกสารข้อความ อย่างไรก็ตาม มีโปรแกรมแก้ไขข้อความฟรีอื่น ๆ ที่พร้อมใช้งานบนอินเทอร์เน็ตซึ่งให้ความสามารถในการทำงานกับเอกสารข้อความเช่น Notepad ++ ซึ่งมีฟังก์ชันการทำงานขั้นสูงกว่ามาก

## ข้อมูลจำเพาะของรูปแบบไฟล์ ##

รูปแบบไฟล์ข้อความไม่มีข้อกำหนดรูปแบบไฟล์พิเศษ ไฟล์ข้อความมีประเภท MIME "ข้อความ/ธรรมดา" และมีการจัดรูปแบบเพียงเล็กน้อยหรือไม่มีเลย สิ่งนี้ทำให้โปรแกรมแก้ไขข้อความสามารถเปิดไฟล์ดังกล่าวได้โดยไม่มีข้อกำหนดอื่นใด ชุดอักขระเริ่มต้นของไฟล์ข้อความคือ ASCII ที่ใช้สำหรับสร้างและแสดงเนื้อหาของไฟล์ข้อความ อักขระถูกเข้ารหัสโดยใช้ชุดอักขระ ASCII แต่สิ่งนี้กำหนดข้อจำกัดของการใช้อักขระ เช่น เครื่องหมายปอนด์ เครื่องหมายดอลลาร์ และยูโร ที่ไม่สามารถแสดงโดยใช้ชุดอักขระ ASCII ดังนั้น ไฟล์ข้อความยังสามารถบันทึกในรูปแบบ Unicode โดยส่วนใหญ่จะใช้ UTF-8

### รูปแบบไฟล์ข้อความ Windows ###

ไฟล์ข้อความบน Windows OS ประกอบด้วยหลายบรรทัดซึ่งแต่ละบรรทัดประกอบด้วยอักขระตามลำดับ บรรทัดโดยนัยของผู้ใช้แต่ละบรรทัดถูกกำหนดโดยการรวมกันของอักขระสองตัว ได้แก่ การขึ้นบรรทัดใหม่ (CR) และบรรทัดป้อน (LF) ไฟล์ข้อความ Windows สามารถเข้ารหัส ANSI, OEM, Unicode หรือ UTF-8 การเข้ารหัส UTF-16 ช่วยบันทึกข้อมูลในไฟล์ข้อความที่ต้องใช้สองไบต์ในการแสดงข้อมูล ไฟล์ดังกล่าวมักจะขึ้นต้นด้วย Byte Order Mark (BOM) ซึ่งสื่อถึงความสมบูรณ์ของเนื้อหาไฟล์ ควรสังเกตว่าแอปพลิเคชันอื่นบนระบบปฏิบัติการ Windows สามารถจัดเก็บข้อมูลในรูปแบบไฟล์ข้อความ แต่มีนามสกุลไฟล์ต่างกันเพื่อแสดงข้อความเฉพาะของแอปพลิเคชัน ตัวอย่างเช่น ภาษาโปรแกรมมักจะบันทึกโค้ดไว้ในไฟล์ข้อความแต่มีนามสกุลของมันเอง

### รูปแบบไฟล์ข้อความ Unix ###

ระบบดังกล่าวทั้งหมดปรับไฟล์ข้อความเป็นไฟล์ที่มีการจัดระเบียบอักขระเป็นศูนย์หรือมากกว่าบรรทัด แต่ละบรรทัดเป็นลำดับของอักขระที่ไม่ใช่การขึ้นบรรทัดใหม่ตั้งแต่ศูนย์หรือมากกว่า และอักขระการขึ้นบรรทัดใหม่ซึ่งสิ้นสุด โดยปกติจะเป็น LF

## อ้างอิง ##

* [รูปแบบไฟล์ TXT](https://en.wikipedia.org/wiki/Text_file)
