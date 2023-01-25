{
  "date" : "2019-10-11",
  "keywords" :[ "XER", "P6XER", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "โครงการ", "การจัดการ", "Primavera", "P6"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"โครงการ XER - Primavera P6",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XER และ API ที่สามารถสร้างและเปิดไฟล์ XER",
  "linktitle" : "XER",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## ไฟล์ XER คืออะไร??

รูปแบบไฟล์ XER เป็นรูปแบบไฟล์โครงการที่เป็นกรรมสิทธิ์ซึ่งใช้โดยแอปพลิเคชันการวางแผนและการจัดการโครงการ Primavera P6 เช่นเดียวกับรูปแบบไฟล์ [MPP](/th/project-management/mpp/) รูปแบบไฟล์นี้จะเก็บข้อมูลที่เกี่ยวข้องกับการวางแผนโครงการ เช่น งาน ทรัพยากร ลำดับเวลา และวัสดุ Primavera ได้รับการพัฒนาโดย Oracle และให้บริการการวางแผนโครงการที่สมบูรณ์ และพบการใช้งานในสาขาต่างๆ ที่ใช้งานได้จริง เช่น น้ำมันและก๊าซ การก่อสร้าง การผลิต ฯลฯ ช่วยให้ผู้จัดการโครงการวางแผน กำหนดเวลา และควบคุมโปรแกรมขนาดใหญ่และแต่ละโครงการโดยการบูรณาการ ด้วยระบบการบริหารการเงินและการบริหารทุนมนุษย์ ซอฟต์แวร์และ API จำนวนมากสามารถอ่านและแปลงไฟล์ XER เป็นรูปแบบไฟล์โครงการยอดนิยมอื่นๆ เช่น XML และ MPP

## รูปแบบไฟล์ XER ##

ไฟล์ XER เป็นไฟล์ข้อความและสามารถเปิดได้อย่างง่ายดายด้วยโปรแกรมแก้ไขข้อความ การเปิดข้อมูลที่เกี่ยวข้องกับโครงการในโปรแกรมแก้ไขข้อความอาจมีประโยชน์ แต่การสร้างลิงก์ด้วยตนเองนั้นไม่ใช่เรื่องง่ายที่จะทำความเข้าใจ รูปแบบนี้เป็นรูปแบบที่ใช้มากที่สุดในการแลกเปลี่ยนข้อมูลกับฐานข้อมูล P6 อื่นๆ มีระดับการควบคุมข้อมูลที่นำเข้าจากรูปแบบอื่นค่อนข้างต่ำ ข้อได้เปรียบของ XER ในรูปแบบ XML ที่เทียบเท่า ได้แก่ ความสามารถในการย้ายรหัสส่วนกลางและปฏิทินไปยังระดับโครงการและรหัสแผนที่, UDF, ทรัพยากร และปฏิทินไปยังค่าที่มีอยู่


## ปัญหาในการเปิดไฟล์ XER? ##

ปัญหาทั่วไปบางประการที่อาจเกิดขึ้นและทำให้รูปแบบ XER ทำงานผิดพลาดมีดังนี้:

* ไม่มีซอฟต์แวร์สนับสนุน
* ไฟล์เสียหาย
* ไฟล์ติดไวรัสเนื่องจากไวรัส
* คำอธิบาย XER ถูกลบออกจากรีจิสทรีของ Windows โดยไม่ได้ตั้งใจ
* ไม่มีสิทธิ์ในระบบในการเปิดไฟล์
* ไดรฟ์ที่ล้าสมัยในระบบของคุณ
* นามสกุลของไฟล์ถูกเปลี่ยนชื่อ

## อ้างอิง ##
 

 * [Oracle - P6 XER](https://docs.oracle.com/cd/E90748_01/English/admin/p6_pro_importing_exporting/p6_pro_importing_exporting.pdf)