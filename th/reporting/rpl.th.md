{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - เค้าโครงหน้ารายงาน",
  "keywords" :[ "rpl", "เค้าโครงหน้ารายงาน", "XSD", "SQL Server", "การรายงาน"],
  "description":"เรียนรู้เกี่ยวกับรูปแบบสตรีม RPL ซึ่งเป็นรูปแบบไบนารีภายในที่ใช้โดย Microsoft SQL Server Reporting Services เมื่อติดต่อกับตัวควบคุมการดู",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## ไฟล์ RPL คืออะไร?? ##

รูปแบบสตรีม RPL (เค้าโครงหน้ารายงาน) เป็นรูปแบบไบนารีภายในที่ใช้โดย MS SQL Server Reporting Services เมื่อติดต่อกับตัวควบคุมตัวแสดงเพื่อลดการแสดงผลบางส่วนจากเซิร์ฟเวอร์ไปยังตัวควบคุมตัวแสดงไคลเอ็นต์ นักพัฒนาสามารถสร้างตัวออกแบบรายงานแบบกำหนดเองได้โดยใช้ RPL ซึ่งจะสร้าง RPL เช่นเดียวกับตัวแสดงรายงานแบบกำหนดเองที่ประมวลผลและแสดงไฟล์ RPL เพื่อแสดงรายงาน

## โครงสร้าง RPL

สตรีม RPL ประกอบด้วยโครงสร้างสตรีม โครงสร้างรายงาน คุณสมบัติรายงาน และการแจงนับ ทุกโครงสร้างมีดังต่อไปนี้:

- คำจำกัดความของโครงสร้าง

- ไวยากรณ์แบบฟอร์ม Backus-Naur เสริม (ABNF) สำหรับโครงสร้าง

- ไดอะแกรมบิตของโครงสร้าง

- คำจำกัดความของฟิลด์ทั้งหมดที่มีอยู่ในโครงสร้าง

นี่คือหมายเหตุสั้น ๆ เกี่ยวกับโครงสร้าง RPL บางส่วน:

### โครงสร้างสตรีม
โครงสร้างสตรีมประกอบด้วยชุดของเรกคอร์ด เรกคอร์ดมีฟิลด์ที่มีโครงสร้างเป็นศูนย์หรือมากกว่าที่มีโครงร่างรายงาน

#### สตรีม RPL
สตรีม RPL ต้องมีบันทึกรายงานเพียงรายการเดียว และสตรีมต้องเป็นชุดของบันทึกไบนารีที่เก็บลำดับชั้นของรายงาน

#### บันทึก
บันทึกเป็นแบบเอกสารสำเร็จรูปพื้นฐานที่ใช้ในการเก็บข้อมูลเกี่ยวกับรายงาน เร็กคอร์ดประกอบด้วยลำดับไบต์ที่มีความยาวแตกต่างกัน บันทึกประกอบด้วยสององค์ประกอบ:
- ประเภทบันทึก
- ข้อมูลบันทึกที่เฉพาะเจาะจงสำหรับประเภทบันทึกนั้น
ประเภทของเรคคอร์ดคือหนึ่งไบต์ที่กำหนดประเภทของข้อมูลที่ระบุโดยเรคคอร์ดและการจัดลำดับและโครงสร้างโครงสร้างของข้อมูลเรคคอร์ดที่เกี่ยวข้องกับเรคคอร์ด ค่าของเรกคอร์ดจะขึ้นอยู่กับชนิดของข้อมูลเฉพาะสำหรับเรกคอร์ดนั้น

#### โครงสร้างประเภทข้อมูลอย่างง่าย

ตารางต่อไปนี้กำหนดประเภทข้อมูลในสตรีม RPL

|รายละเอียด| รูปแบบ|
---|---|
|Char|แทนค่าตัวเลข (ลำดับ) ขนาด 16 บิต (2 ไบต์)|
|ไบต์|แทนจำนวนเต็มที่ไม่มีเครื่องหมาย 8 บิต (1 ไบต์)|
|Int16|แสดงถึงจำนวนเต็ม 16 บิต (2 ไบต์) ที่ลงชื่อแล้ว|
|Single|แสดงถึงค่าทศนิยมความแม่นยำเดียวแบบ 32 บิต (4 ไบต์)|
|ทศนิยม|แสดงชนิดข้อมูล 128 บิต (16 ไบต์)|
|วันที่และเวลา|แสดงการเข้ารหัส 64 บิต (8 ไบต์) ของค่าวันที่และเวลา|
|Int64|แสดงจำนวนเต็มที่ลงนาม 64 บิต (8 ไบต์)|
|Int32|แสดงถึงจำนวนเต็ม 32 บิต (4 ไบต์) ที่ลงชื่อแล้ว|
|โฟลต|แสดงถึงค่าทศนิยมแบบความแม่นยำเดียวแบบ 32 บิต (4 ไบต์)|
|บูลีน|แสดงค่าประเภทบูลีนเชิงตรรกะ 8 บิต (1 ไบต์) ค่าที่ใช้ได้คือ จริง (1) และ เท็จ (0).|
|ยาว|แทนจำนวนเต็ม 64 บิต (8 ไบต์) ที่เซ็นชื่อแล้ว|
|String|ค่าสตริงทั้งหมดภายในโปรโตคอลต้องเป็น UNICODE UTF-16 ตามค่าเริ่มต้น ค่าสตริงทั้งหมดจะเริ่มต้นด้วยจำนวนเต็มที่กำหนดความยาวของสตริง ค่าสตริงจะแสดงในโปรโตคอลเป็นอาร์เรย์ของไบต์ จำนวนไบต์ต้องเท่ากับจำนวนอักขระในสตริงคูณด้วยสอง|

### โครงสร้างรายงาน
โครงสร้างรายงานประกอบด้วยคำจำกัดความและขนาดของโครงสร้างและองค์ประกอบที่เกี่ยวข้อง

รายการต่อไปนี้ระบุโครงสร้างรายงาน:

- รายงาน
- เวอร์ชั่น
- คุณสมบัติรายงาน
- องค์ประกอบอาร์เรย์ชดเชย
- เนื้อหาของหน้า
- หน้าหนังสือ
- คุณสมบัติของเพจ
- เค้าโครงหน้า
- ส่วน
- ส่วนง่าย
- ส่วนผสม
- คุณสมบัติส่วน
- องค์ประกอบพื้นที่ร่างกาย
- องค์ประกอบส่วนหัวของหน้า
- องค์ประกอบส่วนท้ายของหน้า
- องค์ประกอบของร่างกาย
- คุณสมบัติองค์ประกอบ
- คุณสมบัติองค์ประกอบที่ใช้ร่วมกัน
- ใช้คุณสมบัติองค์ประกอบที่ใช้ร่วมกัน
- InlineSharedElementProperties
- NonSharedElementProperties
- สไตล์
- SharedStyleProperties
- คุณสมบัติ NonSharedStyle
- แอคชั่นอินโฟ
- แอคชั่นอินโฟคอนเทนท์
- การกระทำ
- ActionImageMapAreas
- ActionInfoWithMaps
- ไดนามิกอิมเมจดาต้า
- ImageConsolidationOffsets
- รายการรายงาน
- เส้น
- ภาพ
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- คุณสมบัติ NonSharedImageData
- ข้อมูลรูปภาพ
- ImageMapAreas
- ImageMapArea
- แผนภูมิ
- แผงมาตรวัด
- แผนที่
- สี่เหลี่ยมผืนผ้า
- รายงานย่อย
- Rich TextBox
- ย่อหน้าเนื้อหา
- เรียกใช้ข้อความ
- ย่อหน้า
- โครงสร้าง RichTextBox
- แท็บลิกซ์
- เนื้อหา Tablix
- โครงสร้าง Tablix
- การวัด Tablix
- ความกว้างของคอลัมน์
- ข้อมูลคอลัมน์
- โรว์ไฮท์
- ข้อมูลแถว
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- การวัด
- การวัด
- ReportElementEnd

### คุณสมบัติ
ต่อไปนี้คือรายการคุณสมบัติที่สามารถใช้ใน RPL Stream:

- รหัส
- จำนวนคอลัมน์
- ระยะห่างระหว่างคอลัมน์
- ชื่อเฉพาะ
- ชื่อ
- ฉลาก
- ที่คั่นหนังสือ
- เคล็ดลับเครื่องมือ
- สลับรายการ
- คำอธิบาย
- ที่ตั้ง
- ConsumeContainerWhiteSpace (RPL 10.6)
- ภาษา
- เวลาดำเนินการ
- ผู้เขียน
- รีเฟรชอัตโนมัติ
- ชื่อรายงาน
- ความสูงของหน้า
- หน้ากว้าง
- MarginTop
- ระยะขอบซ้าย
- มาร์จิ้นไรท์
- ขอบล่าง
- คอลัมน์
- ชื่อหน้า (RPL 10.6)
- เอียง
- สามารถเติบโต
- หดได้
- ค่า
- สลับสถานะ
- สามารถจัดเรียง
- สถานะการจัดเรียง
- สูตร
- IsToggleParent
- รหัสประเภท
- ค่าเดิม
- เรียบง่าย
- เนื้อหาชดเชย
- ชื่อสตรีม
- การปรับขนาด
- ลิงค์ทูไชด์
- พิมพ์บนหน้าแรก
- พิมพ์ระหว่างส่วน (RPL 10.4)
- FormattedValueExpressionBased
- ประมวลผลด้วยข้อผิดพลาด
- ImageMIMEType
- ชื่อภาพ
- ความกว้าง
- ส่วนสูง
- ความละเอียดแนวนอน
- ความละเอียดแนวตั้ง
- รูปแบบดิบ
- การเชื่อมโยงหลายมิติ
- บุ๊คมาร์คลิงค์
- รหัสการเจาะลึก
-DrillthroughUrl
- สีขอบ
- BorderColorซ้าย
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- สไตล์เส้นขอบ
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- ความกว้างขอบ
- ความกว้างขอบด้านซ้าย
- BorderWidthRight
- เส้นขอบความกว้างด้านบน
- ความกว้างของเส้นขอบด้านล่าง
- แพดดิ้งซ้าย
- แพดดิงไรท์
- เบาะรองนั่ง
- เบาะรองนั่งด้านล่าง
- รูปแบบตัวอักษร
- ฟอนต์แฟมิลี่
- ขนาดตัวอักษร
- ตัวอักษรน้ำหนัก
- รูปแบบ
- การตกแต่งข้อความ
- TextAlign
- VerticalAlign
- สี
- ความสูงของเส้น
- ทิศทาง
- โหมดการเขียน
- ยูนิโคดบีดี
- ภาพพื้นหลัง
- สีพื้นหลัง
- ทำซ้ำพื้นหลัง
- ภาษาตัวเลข
- ตัวแปรตัวเลข
- ปฏิทิน
- แถวส่วนหัวของคอลัมน์
- แถวส่วนหัวคอลัมน์
- ColsBeforeRowHeader
- ทิศทางเค้าโครง
- คำจำกัดความเส้นทาง
- ระดับ
- ดัชนีเซลล์สมาชิก
- CellItemOffset
- คอลสแปน
- แถวช่วง
- DefIndex
- ดัชนีคอลัมน์
- ดัชนีแถว
- ป้ายกำกับกลุ่ม
- RecursiveToggleLevel
- สไตล์รายการ
- ระดับรายการ
- เลขย่อหน้า
- เยื้องขวา
- เยื้องซ้าย
- เยื้องแขวน
- SpaceBefore
- Space After
- เส้นแรก
- มาร์กอัป
- เนื้อหาด้านบน
- เนื้อหาซ้าย
- ความกว้างของเนื้อหา
- ความสูงของเนื้อหา
- สถานะ
- CellItemState
- สมาชิก DefState

### การแจงนับ
รายการต่อไปนี้แสดงการแจงนับที่สามารถใช้ในสตรีม RPL:

- ตัวเลือกการจัดเรียง
- ขนาด
- ประเภทรูปร่าง
- ImageRawFormat
- รูปแบบตัวอักษร
- แบบอักษรน้ำหนัก
- การตกแต่งข้อความ
- การจัดตำแหน่งข้อความ
- การจัดแนวแนวตั้ง
- ทิศทาง
- โหมดการเขียน
- UnicodeBiDiTypes
- ปฏิทิน
- สไตล์เส้นขอบ
- BackgroundRepeatTypes
- รูปแบบรายการ
- รูปแบบมาร์กอัป
- รหัสประเภท
- ค่าสถานะ
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPL ขนาด





## อ้างอิง ##

- [เค้าโครงหน้ารายงาน (RPL) รูปแบบไบนารีสตรีม](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

