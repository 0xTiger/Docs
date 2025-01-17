{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ mpx", "รูปแบบไฟล์ mpx", "ไฟล์ mpx คืออะไร", "ไฟล์", "ตัวอย่าง mpx", "นามสกุลไฟล์ mpx", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - รูปแบบไฟล์ Microsoft Project Exchange",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MPX และ API ที่สามารถสร้างและเปิดไฟล์ MPX",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## ไฟล์ MPX คืออะไร?? ##

ไฟล์ที่มีนามสกุล .mpx เป็นรูปแบบไฟล์ Microsoft Exchange รูปแบบไฟล์ MPX ได้รับการพัฒนาโดย Microsoft Project (MSP) เพื่ออำนวยความสะดวกในการแลกเปลี่ยนข้อมูลโครงการระหว่าง MSP และแอปพลิเคชันอื่นๆ ที่สนับสนุนรูปแบบไฟล์ MPX รวมถึง Primavera Project Planner, Sciforma และ Timerline Precision Estimating เมื่อใช้ไฟล์ MPX คุณสามารถถ่ายโอนข้อมูลทุกชนิดจากโครงการไปยังระบบอื่น เช่น ข้อมูลการกำหนดทรัพยากรโดยละเอียด ข้อมูลปฏิทิน หรือข้อมูลจากกล่องโต้ตอบข้อมูลโครงการ

Microsoft Project 4.0 แนะนำการสนับสนุนสำหรับการสร้างและการอ่านรูปแบบไฟล์ MPX ที่ยังคงใช้ผ่าน Microsoft Project 98 อย่างไรก็ตาม การสนับสนุนสำหรับการสร้างไฟล์ MPX ได้หยุดการเปิดตัว Microsoft Project 2000 และเวอร์ชันจนถึง Microsoft Project 2010 รองรับเฉพาะการอ่าน MPX รูปแบบไฟล์ MPX ไม่ได้รับการสนับสนุนในเวอร์ชันที่ใหม่กว่า MSP 2010

## รูปแบบไฟล์ MPX ##

ภาพรวมของข้อมูลจำเพาะของไฟล์ MPX ระบุไว้ในส่วนนี้ ดูข้อมูลจำเพาะทั้งหมดได้ใน [ฐานความรู้](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) บทความและสามารถอ้างอิงเพื่อดูรายละเอียด

### บันทึก ###

บันทึกของไฟล์ MPX ประกอบด้วยข้อมูลสำหรับโครงการ มีเรกคอร์ดหลายประเภทที่แต่ละเรกคอร์ดมีลำดับของตัวเอง แต่ละประเภทเรคคอร์ดจะถูกระบุด้วยหมายเลขเรคคอร์ด สำหรับไฟล์ MPX จำเป็นต้องมีประเภทเร็กคอร์ดการสร้างไฟล์ บันทึกประเภทอื่นๆ ไม่จำเป็น ตารางต่อไปนี้แสดงประเภทเรคคอร์ดทั้งหมด หมายเลขเรคคอร์ด และจำนวนเรคคอร์ดแต่ละประเภทอาจมีอยู่ในไฟล์ MPX การรวมเรกคอร์ดในไฟล์ MPX จะต้องเป็นไปตามลำดับของตาราง โดยใส่ความคิดเห็นไว้ที่ใดก็ได้

|ชื่อเรกคอร์ด|หมายเลขเรกคอร์ด|จำนวนเรกคอร์ดสูงสุด
---|---|---|
|การสร้างไฟล์ (จำเป็น)|ไม่มี|1
|การตั้งค่าสกุลเงิน|10|1
|การตั้งค่าเริ่มต้น|11|1
|การตั้งค่าวันที่และเวลา|12|1
|นิยามปฏิทินพื้นฐาน|20|250
|ฐานชั่วโมงปฏิทิน|25| 7 ต่อบันทึกคำจำกัดความของปฏิทินพื้นฐาน
|ข้อยกเว้นปฏิทินพื้นฐาน|26| 250 ต่อบันทึกข้อกำหนดปฏิทินพื้นฐาน
|ส่วนหัวโครงการ|30|1
|คำนิยามตารางทรัพยากรข้อความ|140|1- (หรือคุณสามารถใช้บันทึกคำนิยามตารางทรัพยากรที่เป็นตัวเลข)
|นิยามตารางทรัพยากรที่เป็นตัวเลข|41|1
|ทรัพยากร|50|9,999
|หมายเหตุทรัพยากร|51| 1 ต่อบันทึกทรัพยากร
|ข้อกำหนดปฏิทินทรัพยากร|55| 1 ต่อบันทึกทรัพยากร
|ชั่วโมงปฏิทินทรัพยากร|56| 7 ต่อปฏิทินทรัพยากร
|ข้อยกเว้นปฏิทินทรัพยากร| 57|250 ต่อปฏิทินทรัพยากร
|Text Task Table Definition|60|1 (หรือคุณสามารถใช้บันทึก Numeric Task Table Definition)
|นิยามตารางงานตัวเลข|61|1
|งาน|70|9
|บันทึกงาน|71| 1 ต่อบันทึกงาน
|งานประจำ|72| 1 ต่อบันทึกงาน
|การกำหนดทรัพยากร|75| 100 ต่อบันทึกงาน
|ฟิลด์เวิร์กกรุ๊ปการมอบหมาย|76| 1 ต่อบันทึกการมอบหมาย
|ชื่อโครงการ|80|500
|ลิงก์ไคลเอ็นต์ DDE และ OLE|81|500
|ความคิดเห็น|0|ไม่จำกัด

### โครงสร้างไฟล์ ###

ไฟล์ MPX ประกอบด้วยระเบียนที่กล่าวถึงข้างต้นซึ่งจัดเรียงไว้ล่วงหน้าภายในไฟล์ รายละเอียดเกี่ยวกับประเภทเรกคอร์ดเหล่านี้จะกล่าวถึงดังต่อไปนี้:

**บันทึกการสร้างไฟล์ (FCR):** นี่เป็นบันทึกบังคับที่มีวัตถุประสงค์เพื่อระบุ:

* รูปแบบไฟล์ (MPX)
* ตัวคั่นรายการที่ใช้ในไฟล์
* โปรแกรมและหมายเลขเวอร์ชันที่ใช้สร้างไฟล์
* หมายเลขเวอร์ชันของรูปแบบไฟล์ MPX ที่ใช้ในไฟล์
* หน้ารหัสที่ใช้ในการสร้างไฟล์

นี่ต้องเป็นบันทึกแรกในไฟล์ เมื่อส่งออกจาก Microsoft Project อักขระตัวคั่นรายการจะถูกระบุในรายการการตั้งค่าภูมิภาคในแผงควบคุม Windows บันทึก FCR ประกอบด้วยฟิลด์ต่อไปนี้:

* MPX ตามด้วยอักขระคั่นรายการทันที
* ชื่อโปรแกรม/ตัวระบุ
* หมายเลขเวอร์ชันของไฟล์
* หน้ารหัส (850, 437, MAC, ANSI)

ตัวอย่างเช่น บันทึกอาจมีข้อมูล **MPX, Microsoft Project, 3.0** ซึ่งระบุว่าใช้เครื่องหมายจุลภาคเป็นตัวคั่นรายการในไฟล์ MPX นี้ เวอร์ชันของรูปแบบ MPX ที่ใช้ในไฟล์จะถูกส่งออกจาก Microsoft Project เวอร์ชัน 3.0

**การตั้งค่าสกุลเงิน** เรกคอร์ดนี้มีเรกคอร์ดหมายเลข 10 ระบุการตั้งค่าสำหรับตัวเลือกสกุลเงินในกล่องโต้ตอบตัวเลือก ถ้าไม่มีบันทึกนี้ การตั้งค่าปัจจุบันในกล่องโต้ตอบตัวเลือกจะถูกใช้ ตัวคั่นหลักพันและทศนิยมระบุไว้ในรายการการตั้งค่าภูมิภาคในแผงควบคุมของ Windows
ฟิลด์ที่รวมอยู่ในบันทึกนี้คือ:

* สัญลักษณ์สกุลเงิน
* ตำแหน่งสัญลักษณ์ (0 # หลัง 1 # ก่อน 2 # หลังเว้นวรรค 3 # ก่อนเว้นวรรค)
* หลักสกุลเงิน (0,1,2)
* ตัวคั่นหลักพัน
* ตัวคั่นทศนิยม

**ตัวอย่าง:** 10,$,1,2,",",.
ตัวอย่างนี้ระบุว่าค่าสกุลเงินมีเครื่องหมายดอลลาร์ ($) อยู่ข้างหน้า ตัวเลขสองหลักถูกรวมไว้หลังจุดทศนิยม เครื่องหมายจุลภาคใช้เพื่อแยกหลักพัน และใช้จุดเป็นจุดทศนิยม เนื่องจากอักขระตัวคั่นรายการรวมอยู่ในฟิลด์ตัวคั่นหลักพัน ฟิลด์จึงล้อมรอบด้วยเครื่องหมายคำพูด

**การตั้งค่าเริ่มต้น:** เรกคอร์ดนี้มีเรกคอร์ดหมายเลข 11 ระบุการตั้งค่าสำหรับตัวเลือกเริ่มต้นในกล่องโต้ตอบตัวเลือก หากไม่ได้ระบุระยะเวลา จำเป็นต้องตั้งค่าหน่วยระยะเวลาเริ่มต้นสำหรับการคำนวณหน่วยระยะเวลาที่ถูกต้อง ถ้าไม่มีบันทึกนี้ การตั้งค่าปัจจุบันในกล่องโต้ตอบตัวเลือกจะถูกใช้
ฟิลด์ที่รวมอยู่ในบันทึกนี้คือ:

* หน่วยระยะเวลาเริ่มต้น (0 # นาที 1 # ชั่วโมง 2 # วัน 3 # สัปดาห์)
* ประเภทระยะเวลาเริ่มต้น (0 # ไม่คงที่, 1 # คงที่)
* หน่วยงานเริ่มต้น (0 # นาที 1 # ชั่วโมง 2 # วัน 3 # สัปดาห์)
* ชั่วโมงเริ่มต้น / วัน
* ชั่วโมงเริ่มต้น / สัปดาห์
* อัตรามาตรฐานเริ่มต้น
* อัตราการทำงานล่วงเวลาเริ่มต้น
* การอัปเดตสถานะงาน อัปเดตสถานะทรัพยากร (0 # ไม่, 1 # ใช่)
* แยกงานที่กำลังดำเนินการ (0 # ไม่, 1 # ใช่)

**การตั้งค่าวันที่และเวลา:** บันทึกนี้มีหมายเลขบันทึก 12 ระบุการตั้งค่าสำหรับตัวเลือกวันที่และเวลาในกล่องโต้ตอบตัวเลือก และตัวเลือกรูปแบบวันที่ของข้อความแท่งในกล่องโต้ตอบเค้าโครง ถ้าไม่มีบันทึกนี้ การตั้งค่าปัจจุบันในกล่องโต้ตอบตัวเลือกจะถูกใช้
\\ฟิลด์ที่รวมอยู่ในบันทึกนี้คือ:

* วันที่สั่งซื้อ (0 # เดือน/วัน/ปี, 1 # วัน/เดือน/ปี, 2 # ปี/เดือน/วัน)
* รูปแบบเวลา (0 # 12 ชั่วโมง, 1 # 24 ชั่วโมง)
* เวลาเริ่มต้น (จำนวนนาทีหลังเที่ยงคืน)
* ตัวคั่นวันที่
* ตัวคั่นเวลา
* 00:00 ถึง 11:59 ข้อความ
* 12:00 น. ถึง 23:59 น. ข้อความ
* รูปแบบวันที่ (0 -14)*
* รูปแบบวันที่ข้อความแถบ (0 -194)*

**คำจำกัดความของปฏิทินพื้นฐาน:** บันทึกเหล่านี้ซึ่งมีบันทึกหมายเลข 20 กำหนดปฏิทินพื้นฐานและวันที่ทำงานและไม่ทำงานของสัปดาห์ จะใช้การตั้งค่าเริ่มต้นหากไม่มีรายการในหนึ่งวัน การตั้งค่าเริ่มต้นคือวันจันทร์ถึงวันศุกร์สำหรับวันทำงาน และวันเสาร์และวันอาทิตย์สำหรับวันที่ไม่ทำงาน ในบันทึกนี้ จำเป็นต้องระบุฟิลด์ชื่อ สำหรับแต่ละวัน ค่า 0 ระบุว่าวันนั้นเป็นวันที่ไม่มีการทำงาน และค่า 1 ระบุว่าวันนั้นเป็นวันทำงาน
ฟิลด์ที่รวมอยู่ในบันทึกนี้คือ:

* ชื่อ
* วันอาทิตย์
* วันจันทร์
* วันอังคาร
* วันพุธ
* วันพฤหัสบดี
* วันศุกร์
* วันเสาร์

**ชั่วโมงปฏิทินพื้นฐาน:** บันทึกเหล่านี้ซึ่งมีหมายเลขบันทึก 25 ระบุชั่วโมงทำงานสำหรับวันในสัปดาห์หากแตกต่างจากการตั้งค่าเริ่มต้น ชั่วโมงทำงานเริ่มต้นคือ 8:00 น. ถึง 12:00 น. และ 13:00 น. ถึง 17:00 น. แต่ละบันทึกชั่วโมงปฏิทินพื้นฐานอ้างอิงถึงบันทึกข้อกำหนดปฏิทินฐานก่อนหน้า เรกคอร์ดเหล่านี้สามารถติดตามเรกคอร์ดข้อกำหนดปฏิทินพื้นฐานได้สูงสุดเจ็ดเรกคอร์ด

* วันในสัปดาห์ (1 - 7 โดยที่ 1 # อาทิตย์ และ 7 # วันเสาร์)
* ตั้งแต่เวลา 1
* ถึงเวลา 1
* ตั้งแต่เวลา 2
* ถึงเวลา 2
* ตั้งแต่เวลา 3
* ถึงเวลา 3

**ข้อยกเว้นปฏิทินพื้นฐาน:** บันทึกเหล่านี้ซึ่งมีหมายเลขบันทึก 26 กำหนดข้อยกเว้นสำหรับวันและชั่วโมงที่ระบุในประเภทบันทึกสองรายการก่อนหน้านี้ เรคคอร์ดเหล่านี้มากถึง 250 เรคคอร์ดสามารถติดตามแต่ละเรคคอร์ดข้อกำหนดปฏิทินพื้นฐาน บันทึกเหล่านี้จะต้องแสดงรายการตามลำดับเวลา หากมีข้อยกเว้นหนึ่งวัน คุณสามารถเว้นช่องวันที่ถึงวันที่ว่างไว้ได้ หากไม่ได้ระบุเวลา ระบบจะใช้เวลาเริ่มต้นเป็น 8:00 น. ถึง 12:00 น. และ 13:00 น. ถึง 17:00 น.
ฟิลด์ที่รวมอยู่ในบันทึกนี้คือ:

* จากวันที่
* ถึงวันที่
* ไม่ทำงาน/ทำงาน (0 # ไม่ทำงาน, 1 # ทำงาน)
* ตั้งแต่เวลา 1
* ถึงเวลา 1
* ตั้งแต่เวลา 2
* ถึงเวลา 2
* ตั้งแต่เวลา 3
* ถึงเวลา 3

**ส่วนหัวของโครงการ:** เรกคอร์ดนี้ซึ่งมีค่าเรกคอร์ด 30 ตั้งค่าฟิลด์โปรเจ็กต์ส่วนกลาง เช่น วันที่เริ่มต้นโปรเจ็กต์และวันที่สิ้นสุดโปรเจ็กต์ เขตข้อมูลในเรกคอร์ดนี้ตรงกับข้อมูลในกล่องโต้ตอบข้อมูลโครงการและสถิติ
เขตข้อมูลและแท็บที่รวมอยู่ในระเบียนนี้คือ:

* แท็บโครงการ
* บริษัท
* ผู้จัดการ
* ปฏิทิน (มาตรฐานใช้หากไม่มีรายการ)
* วันที่เริ่มต้น (ฟิลด์นี้หรือฟิลด์ถัดไปจะถูกคำนวณสำหรับไฟล์ที่นำเข้า ขึ้นอยู่กับการตั้งค่ากำหนดการจาก)
* วันที่เสร็จสิ้น
* กำหนดการจาก (0 # start, 1 # Finish)
* วันที่ปัจจุบัน*
* ความคิดเห็น
* ค่าใช้จ่าย
* ต้นทุนพื้นฐาน
* ต้นทุนที่แท้จริง
* ทำงาน
* งานพื้นฐาน
* งานจริง
* ทำงาน
* ระยะเวลา*
* ระยะเวลาพื้นฐาน *
* ระยะเวลาจริง
* เปอร์เซ็นต์เสร็จสมบูรณ์
* เริ่มต้นพื้นฐาน
* เสร็จสิ้นพื้นฐาน
* เริ่มต้นจริง
* เสร็จสิ้นจริง
* เริ่มความแปรปรวน
* เสร็จสิ้นความแปรปรวน
* เรื่อง
* ผู้เขียน
* คำหลัก

**คำนิยามตารางทรัพยากรข้อความ**: บันทึกนี้แสดงรายการฟิลด์ทรัพยากรตามลำดับที่กำลังนำเข้าหรือส่งออก สำหรับไฟล์ที่นำเข้า ชื่อต้องตรงกับชื่อฟิลด์ที่ใช้ใน Microsoft Project สำหรับไฟล์ที่ส่งออก ระเบียนนี้มาจากตารางการส่งออกทรัพยากร ต้องใช้เรกคอร์ดนี้หรือเรกคอร์ดคำนิยามตารางทรัพยากรที่เป็นตัวเลข เมื่อส่งออกจาก Microsoft Project เรกคอร์ดทั้งสองนี้จะรวมอยู่ด้วย

**คำจำกัดความของตารางทรัพยากรที่เป็นตัวเลข:** การใช้ตัวเลขแทนชื่อ บันทึกนี้จะแสดงรายการฟิลด์ทรัพยากรตามลำดับที่กำลังนำเข้าหรือส่งออก นี่เป็นวิธีอื่นในการระบุฟิลด์ทรัพยากรที่รวมอยู่ในบันทึกทรัพยากรแต่ละรายการ และมีประโยชน์เมื่อกำหนดไฟล์ MPX ที่สร้างโดยผลิตภัณฑ์ภาษาต่างประเทศ

**แหล่งข้อมูล:** บันทึกเหล่านี้ประกอบด้วยข้อมูลสำหรับทรัพยากรแต่ละรายการที่นำเข้าหรือส่งออก ระเบียนทรัพยากรแต่ละรายการจะอธิบายทรัพยากรหนึ่งรายการ เมื่อคุณนำเข้าข้อมูล ฟิลด์ที่รวมจะถูกกำหนดโดยเรกคอร์ดคำนิยามตารางทรัพยากรข้อความหรือเรกคอร์ดคำนิยามตารางทรัพยากรที่เป็นตัวเลข เมื่อคุณส่งออกข้อมูล ฟิลด์ที่รวมไว้จะแสดงรายการในตารางส่งออกทรัพยากร

**หมายเหตุทรัพยากร:** บันทึกเหล่านี้ประกอบด้วยบันทึกเกี่ยวกับบันทึกทรัพยากรที่อยู่ก่อนหน้าทันที สำหรับการขึ้นบรรทัดใหม่ภายในโน้ต จะใช้อักขระ ASCII 127 ถ้าหมายเหตุมีอักขระคั่นรายการ ให้ใส่เครื่องหมายคำพูดในเครื่องหมายคำพูด

**ข้อกำหนดปฏิทินทรัพยากร:** บันทึกเหล่านี้กำหนดวันทำงานสำหรับทรัพยากรที่ระบุในบันทึกทรัพยากรก่อนหน้าทันที สำหรับไฟล์ที่นำเข้า หากไม่มีรายการสำหรับฟิลด์ Base Calendar Name จะใช้ Standard ไม่มีรายการสำหรับวันที่ระบุระบุว่าวันถูกตั้งค่าเป็นค่าเริ่มต้น (2) หากไม่มีเรกคอร์ดข้อกำหนดปฏิทินทรัพยากร ระบบจะใช้มาตรฐานเป็นปฏิทินฐานสำหรับทรัพยากร โดยค่าเริ่มต้นจะใช้สำหรับวัน สำหรับแต่ละวัน ค่า 0 ระบุว่าวันนั้นเป็นวันไม่ทำงาน 1 ระบุว่าวันนั้นเป็นวันทำงาน และ 2 ระบุว่าใช้ค่าดีฟอลต์

**ชั่วโมงปฏิทินของทรัพยากร:** บันทึกเหล่านี้กำหนดชั่วโมงทำงานของทรัพยากรที่แตกต่างจากปฏิทินพื้นฐานที่ทรัพยากรใช้ เรกคอร์ดเหล่านี้นำไปใช้กับเรกคอร์ดข้อกำหนดปฏิทินทรัพยากรก่อนหน้าเรกคอร์ดนี้ทันที เรกคอร์ดเหล่านี้สามารถติดตามเรกคอร์ดข้อกำหนดปฏิทินทรัพยากรได้สูงสุดเจ็ดเรกคอร์ด

**ข้อยกเว้นปฏิทินทรัพยากร:** บันทึกเหล่านี้กำหนดข้อยกเว้นสำหรับวันและชั่วโมงที่ระบุในบันทึกสองประเภทก่อนหน้า สูงสุด 250 เรกคอร์ดเหล่านี้สามารถติดตามเรกคอร์ดข้อกำหนดปฏิทินทรัพยากรแต่ละรายการ บันทึกเหล่านี้จะต้องแสดงรายการตามลำดับเวลา หากข้อยกเว้นเป็นเพียงหนึ่งวัน คุณสามารถเว้นฟิลด์วันที่ถึงวันที่ว่างไว้ได้ หากไม่ได้ระบุเวลา ระบบจะใช้เวลาเริ่มต้น 8:00 น. ถึง 12:00 น. และ 13:00 น. ถึง 17:00 น.

**Text Task Table Definition:** บันทึกนี้แสดงรายการฟิลด์งานตามลำดับที่กำลังนำเข้าหรือส่งออก สำหรับไฟล์ที่นำเข้า ชื่อต้องตรงกับชื่อฟิลด์ที่ใช้ใน Microsoft Project หากกำลังส่งออกไฟล์ บันทึกนี้จะมาจากตารางงานส่งออก เมื่อส่งออกจาก Microsoft Project เรกคอร์ดทั้งสองนี้จะรวมอยู่ด้วย ฟิลด์ที่คำนวณโดย Microsoft Project เช่น การเริ่มต้นตามกำหนดการและการสิ้นสุดตามกำหนดการ จะถูกละเว้นหากนำเข้า หากคุณมีวันที่เริ่มต้นหรือวันที่สิ้นสุดของงานที่แน่นอน ให้ใช้ช่องประเภทข้อจำกัดและวันที่จำกัด

**คำจำกัดความของตารางงานที่เป็นตัวเลข:** การใช้ตัวเลขแทนชื่อ บันทึกนี้จะแสดงรายการฟิลด์งานตามลำดับที่กำลังนำเข้าหรือส่งออก นี่เป็นวิธีอื่นในการระบุฟิลด์งานที่รวมอยู่ในเรกคอร์ดงานแต่ละรายการ และมีประโยชน์เมื่อกำหนดไฟล์ MPX ที่สร้างโดยผลิตภัณฑ์ภาษาต่างประเทศ

**งาน:** บันทึกเหล่านี้ประกอบด้วยข้อมูลสำหรับแต่ละงานที่กำลังนำเข้าหรือส่งออก บันทึกงานแต่ละรายการจะอธิบายงานหนึ่งงาน เมื่อคุณนำเข้าข้อมูล ฟิลด์ที่รวมไว้จะถูกกำหนดโดยเรกคอร์ดคำนิยามตารางงานข้อความหรือเรกคอร์ดคำนิยามตารางงานที่เป็นตัวเลข เมื่อคุณส่งออกข้อมูล ฟิลด์ที่รวมไว้จะแสดงในรายการงานส่งออกตาราง

**บันทึกงาน:** บันทึกเหล่านี้มีบันทึกเกี่ยวกับบันทึกงานก่อนหน้าทันที ใช้อักขระ ASCII 127 เพื่อระบุบรรทัดใหม่ภายในบันทึกย่อ ถ้าหมายเหตุมีอักขระคั่นรายการ ให้ใส่เครื่องหมายคำพูดในเครื่องหมายคำพูด

**การกำหนดทรัพยากร**: เรกคอร์ดเหล่านี้แสดงรายการข้อมูลเกี่ยวกับทรัพยากรที่กำหนดให้กับงานที่กำหนดไว้ในเรกคอร์ดงานก่อนหน้า หากคุณกำลังผสานไฟล์และต้องการเก็บรักษาข้อมูลการกำหนดทรัพยากร คุณต้องรวมข้อมูลไว้ในไฟล์ MPX หากคุณผสาน การมอบหมายงานที่มีอยู่ทั้งหมดในงานที่ผสานจะถูกลบ หากคุณกำลังรวมไฟล์ตาม ID ที่ไม่ซ้ำ ทรัพยากรจะถูกกำหนดโดยใช้ ID ที่ไม่ซ้ำของทรัพยากร แทนที่จะเป็น ID

**ฟิลด์เวิร์กกรุ๊ปการมอบหมายทรัพยากร:** เรกคอร์ดเหล่านี้แสดงรายการข้อมูลที่จัดเก็บพร้อมกับการมอบหมายแต่ละรายการสำหรับคุณลักษณะเวิร์กกรุ๊ปของ Microsoft Project 4.0 และ 4.1 หากคุณใช้ฟีเจอร์ Workgroup คุณต้องรวมบันทึกนี้เพื่อให้แน่ใจว่าไม่มีข้อมูลใดสูญหาย

**ชื่อโครงการ:** ระเบียนเหล่านี้แสดงรายการชื่อลิงก์ DDE ทั้งหมดที่จัดเก็บไว้ในโครงการ

**ลิงก์ไคลเอนต์ DDE และ OLE:** เรกคอร์ดเหล่านี้แสดงรายการลิงก์ DDE ในโครงการ

**ความคิดเห็น:** บันทึกเหล่านี้สามารถใช้เพื่อเพิ่มความคิดเห็นในไฟล์และสามารถปรากฏในตำแหน่งใดก็ได้ในไฟล์ บันทึกความคิดเห็นแต่ละรายการต้องขึ้นต้นด้วย "0"

## ปัญหาในการเปิดไฟล์ MPX ##

ต่อไปนี้เป็นรายการปัญหาทั่วไปที่อาจเกิดขึ้นและทำให้รูปแบบ MPX ทำงานผิดพลาด:

* ไม่มีซอฟต์แวร์สนับสนุน
* ไฟล์เสียหาย
* ไฟล์ติดไวรัสเนื่องจากไวรัส
* ไม่มีสิทธิ์ในระบบในการเปิดไฟล์
* ไดรฟ์ที่ล้าสมัยในระบบของคุณ
* นามสกุลของไฟล์ถูกเปลี่ยนชื่อ

## อ้างอิง ##

* [MPX - ฐานความรู้ของ Microsoft](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

