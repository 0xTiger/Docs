{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ emf", "รูปแบบไฟล์ emf", "ไฟล์ emf คืออะไร", "ไฟล์", "ตัวอย่าง emf", "นามสกุลไฟล์ emf","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - รูปแบบ Metafile ที่ปรับปรุงแล้ว",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ EMF และ API ที่สามารถสร้างและเปิดไฟล์ EMF",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ EMF คืออะไร??

**รูปแบบไฟล์ metafile ที่ปรับปรุงแล้ว (EMF)** เก็บภาพกราฟิกโดยแยกจากอุปกรณ์ Metafiles ของ EMF ประกอบด้วยเร็กคอร์ดที่มีความยาวผันแปรได้ตามลำดับเวลาที่สามารถแสดงภาพที่เก็บไว้หลังจากแยกวิเคราะห์บนอุปกรณ์เอาต์พุตใดๆ บันทึกความยาวผันแปรเหล่านี้สามารถเป็นคำจำกัดความของวัตถุปิดล้อม คำสั่งสำหรับการวาดภาพ และคุณสมบัติกราฟิกที่สำคัญในการแสดงภาพได้อย่างถูกต้อง เมื่ออุปกรณ์เปิดไฟล์เมตา EMF โดยใช้สภาพแวดล้อมกราฟิกของตัวเอง สัดส่วน ขนาด สี และคุณสมบัติกราฟิกอื่นๆ ของภาพต้นฉบับจะยังคงเหมือนเดิมโดยไม่คำนึงถึงแพลตฟอร์มอุปกรณ์ที่เปิด

## ประวัติย่อ ##

ในปี 1990 Microsoft ได้ออกแบบรูปแบบไฟล์ภาพ Windows Metafile ([WMF](/th/image/wmf/)) สำหรับ Microsoft Windows ไฟล์ Metafile ของ Windows เป็นรูปแบบ 16 บิตที่อาจมีส่วนประกอบของบิตแมป WMF อาจประกอบด้วยกราฟิกแบบเวกเตอร์และมีจุดประสงค์เพื่อให้พกพาได้ระหว่างแอปพลิเคชันต่างๆ ในปี 1993 Win32/GDI ได้ประกาศ Enhanced Metafile (EMF) ซึ่งเป็นเวอร์ชันใหม่ที่เพิ่มความยืดหยุ่นและความสามารถในการปรับขนาด EMF ยังใช้เป็นคำสั่งภาษากราฟิกเพื่อเรียกใช้ไดรเวอร์เครื่องพิมพ์ ขณะนี้ Microsoft แนะนำให้ใช้รูปแบบ metafile ที่ปรับปรุงแล้ว (EMF) มากกว่ารูปแบบ Windows (WMF) เมื่อมีการเปิดตัว Windows XP รุ่น Enhanced Metafile Format Plus (EMF+) ได้รับการเผยแพร่ เวอร์ชันที่ใหม่กว่านี้ค้นหาวิธีโดยการทำให้การเรียก API ของ GDI+ เป็นอนุกรม เช่นเดียวกับการเรียกระเบียน WMF/EMF ไปยัง GDI มี EMF เวอร์ชันบีบอัด gzip ที่เรียกว่า EMZ อยู่

## รูปแบบไฟล์เมตา EMF ##

ต่อไปนี้เป็นองค์ประกอบสำคัญของรูปแบบ metafile ที่ปรับปรุงแล้ว:

* EMR_HEADER (รุ่น, ขนาด, ความละเอียดของภาพขณะสร้าง)
* ตารางสำหรับวัตถุ GDI
* จานสีที่สงวนไว้ (ไม่จำเป็น)
* บันทึก Metafile จัดเรียงในโครงสร้างอาร์เรย์ (การตั้งค่าคุณสมบัติ วัตถุที่กำหนด คำสั่งการวาด)
* บันทึก EMR_EOF (บันทึกล่าสุดในเมตาไฟล์ EMF)

## รุ่น EMF ##
* **ต้นฉบับ**: เวอร์ชันต้นฉบับระบุบันทึกที่จำเป็นในการเก็บภาพต้นฉบับและรักษาไว้โดยไม่ขึ้นกับอุปกรณ์ นอกจากนี้ยังสนับสนุนการบันทึกที่มีวัตถุกราฟิกและคำสั่งสำหรับการวาด
* **เวอร์ชัน 1**: EMF เวอร์ชันที่สองปรับปรุงความยืดหยุ่นและความเป็นอิสระของอุปกรณ์โดยเพิ่มบันทึกสำหรับรูปแบบพิกเซลและการจัดเตรียมเพื่อใช้คำสั่ง OpenGL
* **เวอร์ชัน 2**: เวอร์ชันที่สามปรับปรุงความแม่นยำโดยเพิ่มระบบเมตริกเพื่อวัดระยะห่างพื้นผิวของอุปกรณ์ ทำให้บันทึกปรับขนาดได้มากขึ้น

## บันทึก Metafile ที่ปรับปรุงแล้ว ##

บันทึก Metafile ถูกจัดเรียงในรูปแบบของอาร์เรย์ เร็กคอร์ดเหล่านี้มีโครงสร้าง ENHMETARECORD และความยาวผันแปร ENHMETARECORD ระบุข้อมูลที่กำหนดฟังก์ชัน GDI เพื่อสร้างรูปภาพโดยใช้รูปแบบ metafile ที่ปรับปรุงแล้ว โครงสร้าง **ENHMETAHEADER** เป็นระเบียนแรกในรูปแบบนี้เสมอ ส่วนหัว EMF นี้ประกอบด้วยข้อมูลต่อไปนี้

ทุกบันทึกของ metafile ที่ปรับปรุงแล้วมีสมาชิกสองตัวของ EMR (จัดเตรียมโครงสร้างพื้นฐาน) ในตอนเริ่มต้น สมาชิกตัวแรกรู้จักฟังก์ชัน GDI (ใช้พารามิเตอร์ในบันทึก) ซึ่งกำหนดประเภทของบันทึกและเรียกว่า iType สมาชิกอื่น nSize กำหนดขนาดของแต่ละระเบียน พารามิเตอร์ที่เหลือ (ถ้ามี) และข้อมูลเพิ่มเติมจัดเรียงด้านล่าง nSize ทันที ทันทีที่ต่อจากส่วนหัวอาจมีคำอธิบายข้อความเพิ่มเติม ชื่อภาพและผู้แต่งจะถูกบันทึกไว้ในคำอธิบายข้อความนั้น จานสีที่มีสถานะเป็นตัวเลือกจะระบุสีที่ใช้ในการสร้างไฟล์ metafile ที่ปรับปรุงแล้ว บันทึกอื่นใช้เพื่อระบุฟังก์ชัน GDI ซึ่งจำเป็นในการสร้างรูปภาพ

ควรมีระเบียน EMF อย่างน้อยหนึ่งรายการในแต่ละเมตาไฟล์ ข้อมูลการข้ามผ่านจากเรกคอร์ดหนึ่งไปยังอีกเรกคอร์ดหนึ่งขึ้นอยู่กับเรกคอร์ด EMF ดังนั้นจึงต้องจัดเรียงเรกคอร์ดเหล่านี้ให้อยู่ติดกัน ที่บันทึกใด ๆ ที่กำหนดใน metafile ยกเว้น EOF_record ความยาวของบันทึกนั้นกำหนดให้ย้ายไปยังบันทึกถัดไป

## การสร้าง Metafile ขั้นสูง ##

ฟังก์ชัน **CreateEnhMetaFile** ใช้เพื่อสร้างเมตาไฟล์ที่ปรับปรุงแล้ว อาร์กิวเมนต์ของฟังก์ชันนี้ใช้กับขนาดและการจัดเก็บรูปภาพบนดิสก์/หน่วยความจำ นอกจากนี้ ฟังก์ชันนี้ต้องการมิติของอุปกรณ์ที่รูปภาพปรากฏก่อน (อุปกรณ์อ้างอิง) และบริบทของอุปกรณ์อ้างอิง (DC) ดังนั้นอาร์กิวเมนต์เพื่อจัดการ DC นี้จึงต้องระบุเมื่อเรียกใช้ฟังก์ชัน **CreateEnhMetaFile** ไวยากรณ์ของฟังก์ชันมีดังนี้:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** จัดการกับอุปกรณ์อ้างอิง

**lptoFilename:** ตัวชี้ไปยังชื่อไฟล์

**lprc:** ตัวชี้ไปยังโครงสร้างวงรี ระบุขนาดภาพเป็น มม.

**lpDesc:** ตัวชี้ไปยังสตริงสำหรับชื่อเรื่องของรูปภาพและชื่อแอปพลิเคชันที่สร้างรูปภาพ

## ปรับปรุงการทำงานของ Metafile ##

ต่อไปนี้คืองานที่สามารถทำได้โดยใช้หมายเลขอ้างอิงกับเมตาไฟล์ที่ปรับปรุงแล้ว

* แสดงและแก้ไขภาพที่เก็บไว้
* ผลิตสำเนา metafile ที่ปรับปรุงแล้ว
* ดึงสำเนาของส่วนหัว EMF คำอธิบายเพิ่มเติม และเวอร์ชันไบนารีของ metafile ที่ปรับปรุงแล้ว
* สรุปสีในจานสี

## วัตถุกราฟิก ##

ในการดำเนินการวาดและลงสี วัตถุกราฟิกสามารถสร้างขึ้นโดยบันทึกการสร้างวัตถุและสามารถบันทึกเพื่อใช้ต่อไปได้ เรกคอร์ด `EMR_SELECTOBJECT` สามารถดึงวัตถุกราฟิกเหล่านี้โดยใช้บริบทของอุปกรณ์การเล่น ปากกา จานสี แปรง พื้นที่สี ฟอนต์ และวัตถุสต็อกเป็นวัตถุบางประเภทที่นำกลับมาใช้ใหม่ได้

## การจัดลำดับไบต์ ##

รูปแบบ Little-endian ใช้เพื่อจัดเก็บข้อมูลในบันทึกเมตาไฟล์

## การกำหนดเวอร์ชัน ##

รูปแบบไฟล์ EMF ได้รับการแก้ไขสองครั้ง เวอร์ชันที่เปลี่ยนแปลงคือต้นฉบับ ส่วนขยาย 1 และส่วนขยาย 2 เวอร์ชันเพิ่มเติมมีข้อกำหนดสำหรับบันทึก OpenGL และตัวอธิบายเพิ่มเติมสำหรับรูปแบบพิกเซลภายใน มีการเพิ่มสิ่งอำนวยความสะดวกในการวัดเป็นมิลลิลิตรสำหรับขนาดที่แสดง

## อ้างอิง ##

* [Metafiles รูปแบบที่ปรับปรุงแล้ว | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [รูปแบบและข้อมูลจำเพาะของ Metafile ที่ปรับปรุงแล้ว](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

