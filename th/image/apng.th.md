{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ apng", "รูปแบบไฟล์ apng", "ไฟล์ apng คืออะไร", "ไฟล์", "ตัวอย่าง apng", "นามสกุลไฟล์ apng", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ APNG - ไฟล์กราฟิกเครือข่ายพกพาเคลื่อนไหว",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ APNG และ API ที่สามารถสร้างและเปิดไฟล์ APNG",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## ไฟล์ APNG คืออะไร??

ไฟล์ที่มีนามสกุล .apng (Animated Portable Network Graphics) เป็นรูปแบบกราฟิกแรสเตอร์และเป็นส่วนขยายที่ไม่เป็นทางการของ Portable Network Graphic ([PNG](/th/image/png/) ) ประกอบด้วยหลายเฟรม (แต่ละภาพ PNG) ที่แสดงถึงลำดับภาพเคลื่อนไหว ซึ่งให้การแสดงภาพที่คล้ายกับไฟล์ [GIF](/th/image/gif/) ไฟล์ APNG รองรับภาพ 24 บิตและความโปร่งใส 8 บิต APNG สามารถใช้งานร่วมกับไฟล์ GIF ที่ไม่ใช่ภาพเคลื่อนไหวย้อนหลังได้ ไฟล์ APNG ใช้นามสกุล .png เดียวกันและสามารถเปิดได้โดยแอปพลิเคชันต่างๆ เช่น Mozilla Firefox, Chrome ที่รองรับ APNG, แอป iMessage สำหรับ iOS 10

## ประวัติย่อ

* ข้อกำหนด APNG ถูกสร้างขึ้นในปี 2547 เพื่อรองรับภาพ PNG แบบเคลื่อนไหว
* ตัวถอดรหัส APNG ได้รับการพัฒนาให้มีขนาดเล็กลงมาก และใช้ด้านหลังของตัวถอดรหัส PNG
* หลังจากการพิจารณาอย่างต่อเนื่อง รูปภาพ/apng ประเภท MIME ใหม่ได้รับการกำหนดโดยที่ยังคงนามสกุลเดิมเป็น .png แทน .apng
* APNG ถูกปฏิเสธอย่างเป็นทางการโดยกลุ่ม PNG เมื่อวันที่ 20 เมษายน 2550 เนื่องจากมีความเหมือนกันกับภาพ PNG ในขณะเดียวกันก็มีข้อกำหนดที่แตกต่างกัน

## รูปแบบไฟล์ APNG

ไฟล์ APNG ถูกจัดเก็บเป็นไฟล์ไบนารีบนดิสก์ และใช้ข้อกำหนดเพิ่มเติมของ PNG สำหรับภาพเคลื่อนไหว เฟรมแรกของไฟล์ APNG คือสตรีม PNG ปกติที่ตัวถอดรหัส PNG สามารถอ่านได้เพื่อแสดง รูปแบบไฟล์ APNG เป็นไปตามข้อกำหนด PNG และข้อมูลจะถูกจัดเก็บไว้ในส่วนที่เรียกว่าก้อน อย่างไรก็ตาม APNG ได้แนะนำส่วนใหม่ต่อไปนี้:

`Animation Control Chunk (acTL)` - ระบุว่าไฟล์นี้เป็นไฟล์ PNG แบบเคลื่อนไหว แทนที่จะเป็นไฟล์ PNG ทั่วไป ทำหน้าที่เป็นเครื่องหมายและมาก่อน IDAT อัน นอกจากนี้ยังมีจำนวนเฟรมและข้อมูลเกี่ยวกับเวลาในการวนซ้ำภาพเคลื่อนไหว

`Frame Control Chunk` - เกิดขึ้นที่จุดเริ่มต้นของแต่ละรายการและข้อมูลเมตา เช่น มิติ ตำแหน่ง แอปพลิเคชันความโปร่งใส และข้อมูลการแทนที่โดยเฟรมก่อนหน้าหรือถัดไปเมื่อสิ้นสุด

`Frame Data Chunk` - จัดเก็บเนื้อหาของเฟรมและเริ่มต้นด้วยหมายเลขลำดับ หมายเลขลำดับนี้มีโครงสร้างเดียวกันกับ IDAT chunk ของรูปภาพเริ่มต้น

{{< figure src="../APNG.png" alt="PNG เคลื่อนไหว - รูปแบบไฟล์ APNG" >}}

APNG สามารถใช้งานร่วมกับ PNG แบบย้อนหลังได้เนื่องจากข้อกำหนดด้านข้างได้รับการออกแบบมาในลักษณะที่แอปพลิเคชันที่อ่านไฟล์ PNG ควรจะเพิกเฉยต่อชิ้นส่วนที่ไม่เข้าใจ ข้อมูลจำเพาะเกี่ยวกับความลึกของบิต ชนิดสี การบีบอัด ฟิลเตอร์ วิธีการอินเทอร์เลซ และข้อมูลจานสีจะใช้เหมือนกับรูปแบบ PNG เริ่มต้น

## APNG กับ GIF

เมื่อมี GIF อยู่แล้วและถูกใช้งานเป็นเวลานาน คุณอาจสงสัยว่า APNG แตกต่างจาก GIF อย่างไร ต่อไปนี้เป็นชุดการเปรียบเทียบระหว่าง APNG และ GIF ที่ให้แนวคิดโดยย่อเกี่ยวกับรูปแบบไฟล์ทั้งสอง

||APNG|GIF|
---|---|---|
|เผยแพร่|2547|2530|
|ความลึกของสี|24 บิต|8 บิต|
|อัตราเฟรม|ไม่จำกัด|10 เฟรมต่อวินาที|
|ความโปร่งใส|สมบูรณ์และบางส่วน|สมบูรณ์|
|การบีบอัด|ดีมาก|ดี|

## อ้างอิง

* [รูปแบบไฟล์ APNG](https://en.wikipedia.org/wiki/APNG)
* [ข้อกำหนดรูปแบบ PNG อย่างเป็นทางการ](https://www.w3.org/TR/PNG/)
