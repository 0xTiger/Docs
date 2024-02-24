{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AVL - ไฟล์ ArcView Legend",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ AVL และ API ที่สามารถสร้างและเปิดไฟล์ AVL",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl-th",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## ไฟล์ AVL คืออะไร??

ไฟล์ AVL เป็นไฟล์คำอธิบายแผนภูมิที่มีคีย์สำหรับแผนที่ที่สร้างด้วยซอฟต์แวร์ ESRI ArcView GIS (ระบบสารสนเทศภูมิศาสตร์) ประกอบด้วยข้อมูลสัญลักษณ์อ้างอิงที่ใช้ในแผนที่ที่เกี่ยวข้องสำหรับการเข้าถึง ไฟล์ AVL อาจมีข้อมูลเพิ่มเติม เช่น สัญลักษณ์วิทยา การตั้งค่าการแสดงผล เช่น ความโปร่งใส คุณสมบัติการแสดงผลขึ้นอยู่กับขนาด ตารางที่รวม/ข้อมูลตารางที่เกี่ยวข้อง การสอบถามคำจำกัดความ คุณสมบัติการติดป้ายกำกับสำหรับเลเยอร์คุณลักษณะ และคุณสมบัติการแสดงคำอธิบายประกอบสำหรับเลเยอร์คำอธิบายประกอบ ขึ้นอยู่กับประเภท ชนิดของชั้น

ไฟล์ AVL อาจอ้างอิงจากไฟล์โครงการ ArcView [.APR](/gis/apr/)

## รูปแบบไฟล์ AVL - ข้อมูลเพิ่มเติม

ไฟล์ AVL จะถูกบันทึกในรูปแบบไฟล์ข้อความล้วน หมายความว่าคุณสามารถเปิดไฟล์ AVL ในโปรแกรมแก้ไขข้อความใดก็ได้ เช่น Notepad, Notepad++ และ Apple TextEdit เมื่อเปิดแล้ว คุณไม่เพียงสามารถดูเนื้อหาของไฟล์เท่านั้น แต่ยังแก้ไขสิ่งเหล่านี้ได้อีกด้วย

### ความแตกต่างระหว่างไฟล์ .LYR และ .AVL

 * **ความแตกต่างของรูปแบบไฟล์** - .lyr เป็นไฟล์ไบนารี่ ส่วน .avl เป็นไฟล์ข้อความ
 * **ความแตกต่างของเนื้อหา** - ไฟล์ .lyr มีข้อมูลมากกว่าไฟล์ .avl ไฟล์ AVL จะเก็บข้อมูลสัญลักษณ์วิทยาเท่านั้น ในขณะที่ไฟล์ LYR จะเก็บข้อมูลทั้งหมดที่มีอยู่ในกล่องโต้ตอบคุณสมบัติของเลเยอร์ใน ArcMap

## อ้างอิง

* [ความแตกต่างระหว่างไฟล์ .lyr และ .avl](https://support.esri.com/en/technical-article/000005936)

