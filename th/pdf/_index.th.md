{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "ปัจจัยพื้นฐาน" ],
  "description":"Portable Document Format (PDF) เป็นการแสดงมาตรฐานของเอกสารที่ไม่ขึ้นกับซอฟต์แวร์ ฮาร์ดแวร์ และระบบปฏิบัติการ มาตรฐาน PDF ได้แก่ PDF/A, PDF/E, PDF/UA, PDF/VT และ PDF/X",
  "title" :"รูปแบบไฟล์ PDF - ไฟล์ PDF คืออะไร",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) เป็นเอกสารประเภทหนึ่งที่สร้างขึ้นโดย Adobe ในช่วงปี 1990 จุดประสงค์ของรูปแบบไฟล์นี้คือเพื่อแนะนำมาตรฐานสำหรับการแสดงเอกสารและเอกสารอ้างอิงอื่นๆ ในรูปแบบที่ไม่ขึ้นกับแอพพลิเคชั่นซอฟต์แวร์ ฮาร์ดแวร์ และระบบปฏิบัติการ รูปแบบไฟล์ PDF มีความสามารถเต็มรูปแบบในการบรรจุข้อมูล เช่น ข้อความ รูปภาพ ไฮเปอร์ลิงก์ ช่องแบบฟอร์ม สื่อสมบูรณ์ ลายเซ็นดิจิทัล สิ่งที่แนบมา ข้อมูลเมตา คุณลักษณะเชิงพื้นที่ และวัตถุ 3 มิติ ซึ่งอาจกลายเป็นส่วนหนึ่งของเอกสารต้นฉบับได้

ในกรณีส่วนใหญ่ เอกสารที่มีอยู่จะถูกแปลงเป็น PDF แทนที่จะสร้าง PDF ใหม่ตั้งแต่ต้น แต่นั่นไม่ได้หมายความว่าไม่มีซอฟต์แวร์สำหรับสร้างหรือจัดการไฟล์ PDF

**(ต้องการแชร์บางอย่างเกี่ยวกับรูปแบบไฟล์ PDF หรือไม่ คุณสามารถโพสต์สิ่งที่คุณค้นพบได้ในส่วน [ข่าวรูปแบบไฟล์ PDF](https://news.fileformat.com/t/PDF))**

## รูปแบบไฟล์ PDF - ประวัติย่อ

ไทม์ไลน์อย่างรวดเร็วเกี่ยวกับการสร้างไฟล์ PDF ในแง่ของไทม์ไลน์มีดังนี้:

**1993** - Adobe Systems ทำให้ข้อกำหนด PDF ใช้งานได้ฟรี

**2008** - PDF เปิดตัวเป็นมาตรฐานเปิดเมื่อวันที่ 1 กรกฎาคม 2008 และเผยแพร่โดย International Organization for Standardization ในชื่อ **ISO 32000-1:2008**

**2008** - Adobe เผยแพร่ใบอนุญาตสิทธิบัตรสาธารณะในรูปแบบ ISO 32000-1 สิทธิ์ปลอดค่าลิขสิทธิ์สำหรับสิทธิบัตรทั้งหมดที่ Adobe เป็นเจ้าของ ซึ่งจำเป็นต่อการสร้าง ใช้ ขาย และเผยแพร่การใช้งานที่สอดคล้องกับ PDF

PDF เวอร์ชันแรกกำหนดให้เป็น PDF 1.0 ซึ่งต่อมาได้ผ่านการแก้ไขเป็น PDF 1.7 PDF 1.7 ซึ่งกลายมาเป็น ISO 32000-1 รวมถึงเทคโนโลยีที่เป็นกรรมสิทธิ์ที่ไม่ได้มาตรฐานบางอย่าง เช่น Adobe XML Forms Architecture (XFA) และส่วนขยาย JavaScript สำหรับ Acrobat เมื่อวันที่ 28 กรกฎาคม 2017 เมื่อมีการเผยแพร่ PDF 2.0 หรือที่เรียกว่า ISO 32000-2:2017 ซึ่งไม่รวมถึงเทคโนโลยีที่ไม่ได้มาตรฐานใดๆ

## ข้อกำหนดรูปแบบไฟล์ PDF

ไฟล์ PDF คือชุดของไบต์ที่สามารถจัดกลุ่มเป็นโทเค็นตามกฎไวยากรณ์ที่กำหนดโดยข้อกำหนดเฉพาะของ PDF โทเค็นอย่างน้อยหนึ่งรายการจะรวมกันเพื่อสร้างเอนทิตีวากยสัมพันธ์ระดับสูงกว่า ซึ่งส่วนใหญ่เป็นวัตถุ ซึ่งเป็นค่าข้อมูลพื้นฐานที่ใช้สร้างเอกสาร PDF

### โครงสร้างไฟล์ของไฟล์ PDF

เนื้อหาไฟล์ PDF ถูกจัดเรียงตามลำดับต่อไปนี้ภายในไฟล์

|ส่วนหัว
|ร่างกาย
|ตารางอ้างอิงโยง
|ตัวอย่าง

#### ส่วนหัวของไฟล์ PDF ####

โดยไม่คำนึงถึงเวอร์ชัน PDF ไฟล์ PDF จะเริ่มต้นด้วยส่วนหัวที่มีตัวระบุเฉพาะสำหรับ PDF และเวอร์ชันของรูปแบบ เช่น %PDF-1.x โดยที่ x มีค่าตั้งแต่ 1-7

#### ตัวไฟล์ ####

เนื้อความของไฟล์ PDF ประกอบด้วยลำดับของอ็อบเจกต์ทางอ้อมที่แสดงถึงเนื้อหาของเอกสาร ออบเจกต์ตามที่อธิบายไว้ข้างต้น แสดงถึงส่วนประกอบต่างๆ ของเอกสาร เช่น ฟอนต์ หน้า และรูปภาพตัวอย่าง เริ่มต้นด้วย PDF 1.5 เนื้อหายังสามารถมีกระแสวัตถุ ซึ่งแต่ละรายการมีลำดับของวัตถุทางอ้อม

#### ตารางอ้างอิงโยง ####

ตารางอ้างอิงโยงมีข้อมูลที่อนุญาตให้เข้าถึงออบเจกต์ทางอ้อมภายในไฟล์โดยสุ่ม เพื่อให้ไม่ต้องอ่านทั้งไฟล์เพื่อหาออบเจกต์เฉพาะใดๆ ตารางจะต้องมีรายการหนึ่งบรรทัดสำหรับวัตถุทางอ้อมแต่ละรายการ โดยระบุการชดเชยไบต์ของวัตถุนั้นภายในเนื้อหาของไฟล์ (เริ่มต้นด้วย PDF 1.5 ข้อมูลอ้างอิงโยงบางส่วนหรือทั้งหมดอาจอยู่ในกระแสข้อมูลอ้างอิงโยง

#### ตัวอย่างไฟล์ ####

ตัวอย่างของไฟล์ PDF ช่วยให้ผู้อ่านที่สอดคล้องกันสามารถค้นหาตารางอ้างอิงโยงและวัตถุพิเศษบางอย่างได้อย่างรวดเร็ว ผู้อ่านที่เข้ากันได้ควรอ่านไฟล์ PDF จากส่วนท้ายของไฟล์ บรรทัดสุดท้ายของไฟล์ต้องมีเฉพาะเครื่องหมายสิ้นสุดไฟล์ %%EOF สองบรรทัดก่อนหน้าจะต้องมี หนึ่งบรรทัดต่อบรรทัดและตามลำดับ คำหลัก startxref และไบต์ออฟเซ็ตในสตรีมการถอดรหัสจากจุดเริ่มต้นของไฟล์ไปยังจุดเริ่มต้นของคำหลัก xref ในส่วนการอ้างอิงโยงล่าสุด

### วัตถุ PDF ###

ไฟล์ PDF มีอ็อบเจกต์ประเภทต่างๆ หลายประเภทดังต่อไปนี้

* ค่าบูลีน - แสดงเงื่อนไขจริงหรือเท็จ
* ตัวเลข - จำนวนเต็มและค่าจริง
* สตริง - มีอักขระอยู่ในวงเล็บ
* ชื่อ - ขึ้นต้นด้วยตัวข้างหน้า / เช่น /ASomewhatLongerName ผลลัพธ์ใน ASomewhatLongerName
* อาร์เรย์ - PDF รองรับอาร์เรย์หนึ่งมิติ อาร์เรย์ที่มีขนาดสูงกว่าสามารถสร้างได้โดยใช้อาร์เรย์เป็นองค์ประกอบที่ซ้อนกัน
* พจนานุกรม - ชุดของวัตถุเป็นคู่คีย์-ค่า สามารถมีรายการเป็นศูนย์
* Streams - แสดงถึงลำดับของไบต์ซึ่งสามารถมีความยาวได้ไม่จำกัดเช่นกัน
* Null Object - แสดงถึงค่า Null

อาจมีออบเจกต์อื่นๆ เช่น ความคิดเห็นที่มีเครื่องหมาย % และอาจมีอักขระ 8 บิต

### วัตถุทางอ้อม ###

วัตถุใดๆ ในไฟล์ PDF อาจถูกระบุว่าเป็นวัตถุทางอ้อม อ็อบเจ็กต์ทางอ้อมจะได้รับตัวระบุอ็อบเจ็กต์ที่ไม่ซ้ำใคร ซึ่งอ็อบเจ็กต์อื่นสามารถอ้างถึงได้ การอ้างอิงโยงไปยังสิ่งเหล่านี้จะถูกรักษาไว้ในตารางดัชนีและทำเครื่องหมายด้วยคีย์เวิร์ด xref ซึ่งตามหลังเนื้อหาหลัก และให้ค่าชดเชยไบต์ของแต่ละอ็อบเจ็กต์ทางอ้อมตั้งแต่เริ่มต้นไฟล์

### เค้าโครง PDF เชิงเส้นและไม่เป็นเชิงเส้น ###

เค้าโครง PDF ถูกจัดประเภทเป็น Lnear และ non-linear ขึ้นอยู่กับแอปพลิเคชันเป้าหมายและปัจจัยอื่นๆ

ไม่เป็นเชิงเส้น - ไฟล์ PDF ที่ไม่ใช่เชิงเส้นใช้พื้นที่ดิสก์น้อยกว่าเมื่อเทียบกับไฟล์ PDF เชิงเส้น หน้า PDF ของเอกสารอยู่ในรูปแบบกระจัดกระจายในไฟล์ PDF และนั่นคือสาเหตุที่ไฟล์ที่ไม่ใช่เชิงเส้นทำงานช้าลงเมื่อเทียบกับไฟล์เชิงเส้น

Linear PDF - การกำหนดเป้าหมายโปรแกรมดู PDF ออนไลน์ ไฟล์ PDF เชิงเส้นถูกสร้างขึ้นในลักษณะที่เขียนลงดิสก์ในลักษณะเชิงเส้น สิ่งนี้ไม่ต้องการปลั๊กอินของเบราว์เซอร์สำหรับการโหลดเอกสารทั้งหมดก่อนที่จะแสดง

### ภาพรวมวัตถุ ###

ดังที่กล่าวไว้ PDF body คือชุดของวัตถุที่กล่าวถึงข้างต้น PDF ส่วนใหญ่ใช้ PostScript โดยไม่มีคุณสมบัติการควบคุมของภาษาการเขียนโปรแกรม เช่น คำสั่ง if และ loop คำสั่งที่ออกโดยรหัส Postscript เพื่อสร้างเนื้อหากราฟิกจะถูกรวบรวมและแปลงเป็นโทเค็นนอกเหนือจากไฟล์ กราฟิก หรือแบบอักษรใดๆ ที่อ้างถึงโดยเอกสาร เนื้อหาทั้งหมดเหล่านี้ถูกรวบรวมเป็นไฟล์เดียว ส่งผลให้เอาต์พุต PostScript ประกอบด้วย

#### ข้อความ ####

ข้อความใน PDF แสดงด้วยองค์ประกอบข้อความซึ่งแสดงด้วยสัญลักษณ์จากแบบอักษร สัญลักษณ์เป็นรูปร่างกราฟิกและขึ้นอยู่กับการปรับแต่งกราฟิกทั้งหมด เช่น การแปลงพิกัด เนื่องจากความสำคัญของข้อความในคำอธิบายหน้าส่วนใหญ่ PDF จึงมีสิ่งอำนวยความสะดวกในระดับที่สูงขึ้นเพื่ออธิบาย เลือก และแสดงสัญลักษณ์อย่างสะดวกและมีประสิทธิภาพ

#### กราฟิก ####

ตัวดำเนินการกราฟิกที่ใช้ในสตรีมเนื้อหา PDF อธิบายลักษณะที่ปรากฏของหน้าที่จะทำซ้ำบนอุปกรณ์เอาต์พุตแรสเตอร์ สิ่งอำนวยความสะดวกนี้มีไว้สำหรับทั้งเครื่องพิมพ์และแอพพลิเคชั่นแสดงผล ตัวดำเนินการกราฟิกประกอบด้วยหกกลุ่มหลัก:

* ตัวดำเนินการสถานะกราฟิกจัดการโครงสร้างข้อมูลที่เรียกว่าสถานะกราฟิก ซึ่งเป็นเฟรมเวิร์กส่วนกลางที่ตัวดำเนินการกราฟิกอื่นดำเนินการ สถานะกราฟิกรวมถึงเมทริกซ์การแปลงปัจจุบัน (CTM) ซึ่งแมปพิกัดพื้นที่ของผู้ใช้ที่ใช้ภายในสตรีมเนื้อหา PDF เป็นพิกัดอุปกรณ์เอาต์พุต นอกจากนี้ยังรวมถึงสีปัจจุบัน เส้นทางการตัดปัจจุบัน และพารามิเตอร์อื่นๆ อีกมากมายที่เป็นตัวดำเนินการโดยปริยายของตัวดำเนินการวาดภาพ
* ตัวดำเนินการสร้างเส้นทางระบุเส้นทาง ซึ่งกำหนดรูปร่าง เส้นทางการเคลื่อนที่ของเส้น และขอบเขตของประเภทต่างๆ ซึ่งรวมถึงตัวดำเนินการสำหรับการเริ่มต้นเส้นทางใหม่ การเพิ่มส่วนของเส้นและเส้นโค้ง และปิดเส้นทาง
* ตัวดำเนินการระบายสีเส้นทางเติมเส้นทางด้วยสี วาดเส้นตามเส้นทาง หรือใช้เป็นขอบเขตการตัด
* ผู้ประกอบการวาดภาพอื่น ๆ วาดภาพวัตถุกราฟิกที่อธิบายตนเองบางอย่าง ซึ่งรวมถึงรูปภาพตัวอย่าง แรเงาที่กำหนดทางเรขาคณิต และสตรีมเนื้อหาทั้งหมดที่มีลำดับของตัวดำเนินการกราฟิก
* ตัวดำเนินการข้อความเลือกและแสดงสัญลักษณ์อักขระจากแบบอักษร (คำอธิบายของแบบอักษรสำหรับการแสดงอักขระข้อความ) เนื่องจาก PDF ถือว่าสัญลักษณ์เป็นรูปร่างกราฟิกทั่วไป ตัวดำเนินการข้อความจำนวนมากอาจถูกจัดกลุ่มด้วยสถานะกราฟิกหรือตัวดำเนินการระบายสี อย่างไรก็ตาม โครงสร้างข้อมูลและกลไกในการจัดการกับสัญลักษณ์และคำอธิบายแบบอักษรมีความเชี่ยวชาญเพียงพอ
* ตัวดำเนินการเนื้อหาที่ทำเครื่องหมายเชื่อมโยงข้อมูลเชิงตรรกะระดับสูงกับวัตถุในสตรีมเนื้อหา ข้อมูลนี้ไม่ส่งผลต่อลักษณะการแสดงผลของเนื้อหา มีประโยชน์สำหรับแอปพลิเคชันที่ใช้ PDF สำหรับการแลกเปลี่ยนเอกสาร

## อ้างอิง ##

* [รูปแบบไฟล์ PDF: โครงสร้างพื้นฐาน](https://resources.infosecinstitute.com/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [ข้อมูลอ้างอิง PDF - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
