{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ PDF/X",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PDF/X และ API ที่สามารถสร้างและเปิดไฟล์ PDF/X",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# ไฟล์ PDF/X คืออะไร #

PDF/X เป็นมาตรฐาน ISO 15930 ที่เผยแพร่ในปี 2544 โดยมีฟังก์ชันย่อยของ PDF มาตรฐานนี้กำหนดขึ้นและเผยแพร่ตามข้อกำหนดเฉพาะของอุตสาหกรรมการพิมพ์และสิ่งพิมพ์ ข้อกำหนดสำหรับมาตรฐานนี้ได้รับการออกแบบตามความต้องการที่หลากหลายของอุตสาหกรรมการพิมพ์และสิ่งพิมพ์ PDF/X กำหนดให้ไฟล์ที่สอดคล้องต้องสมบูรณ์ เช่น มีอยู่ในตัวเอง สิ่งนี้กำหนดให้องค์ประกอบต่างๆ เช่น แบบอักษรที่ใช้ในหน้าควรเป็นส่วนหนึ่งของเอกสาร เนื้อหาเช่น 3D หรือวิดีโอไม่สามารถเป็นส่วนหนึ่งของเอกสาร PDF/X ข้อมูลที่อยู่ในเอกสาร PDF/X จำเป็นต้องมีความถูกต้อง

## PDF/X มาตรฐานและการแก้ไข ##

กลุ่มมาตรฐาน PDF/X ประกอบด้วยหลายเวอร์ชัน ซึ่งแต่ละเวอร์ชันได้รับการออกแบบมาสำหรับผลลัพธ์เฉพาะทาง การพัฒนามาตรฐานเหล่านี้มีวัตถุประสงค์เพื่อตอบสนองความต้องการที่หลากหลายของอุตสาหกรรมการพิมพ์และสิ่งพิมพ์

* `PDF/X-1a` - หรือที่เรียกว่ามาตรฐานแรกของตระกูล PDF/X PDF/X-1a กำหนดให้เนื้อหาทั้งหมดเป็นส่วนหนึ่งของเอกสาร PDF เพื่อให้สามารถพิมพ์ได้ ไม่อนุญาตให้ใช้องค์ประกอบของเอกสาร เช่น แบบอักษร แบบฟอร์ม การป้องกันด้วยรหัสผ่าน และคำอธิบายประกอบที่มองเห็นได้ PDF/X-1a มีข้อกำหนดเฉพาะของตัวเอง เช่น ข้อกำหนดเกี่ยวกับความโปร่งใสและเลเยอร์ที่ได้รับอนุญาต สิ่งเหล่านี้ยังกำหนดให้องค์ประกอบการพิมพ์ใช้เฉพาะ CMYK, ระดับสีเทาหรือสีเฉพาะจุด ทำให้ไม่ต้องใช้ RGB หรือพื้นที่สีที่ไม่ขึ้นกับอุปกรณ์ มีไว้สำหรับการแลกเปลี่ยนซึ่งไฟล์ทั้งหมดจะถูกส่งเป็น CMYK (และ/หรือสีเฉพาะจุด) โดยไม่มี RGB หรือข้อมูลที่จัดการด้วยสี PDF/X-1a เรียกอีกอย่างว่า Complete Exchange เนื่องจากความครบถ้วนของข้อมูลที่จำเป็นโดย
* `PDF/X-3` - เปิดตัวในปี 2545 และยกเลิกข้อจำกัดหลายอย่างของ PDF/X-1a สิ่งนี้เปิดใช้งานกราฟิกใน PDF/X-3 เพื่อใช้พื้นที่สี CMYK, grescale, RGB, Lab และ ICC อิงตามมาตรฐาน PDF 1.3 ด้วย [โปรไฟล์ ICC](https://en.wikipedia.org/wiki/ICC_Profile) นอกจากนี้ยังเรียกว่าการจัดการสีเนื่องจากความยืดหยุ่นและกฎที่แนะนำเกี่ยวกับสีที่รวมอยู่ในเอกสาร PDF
* `PDF/X-4` - รองรับแผ่นใส ดังนั้น PDF-X/4 จึงมีข้อมูลทั้งหมดที่จำเป็นสำหรับเอาต์พุตโดยไม่ทำให้แบนราบ
* `PDF/X-5` - ใช้ PDF/X-4 เพิ่มการรองรับกราฟิกภายนอกผ่าน XObjects อ้างอิง เช่นเดียวกับโปรไฟล์ n-colorant ภายนอกสำหรับการแสดงเจตนา ใช้สำหรับแลกเปลี่ยนข้อมูลการพิมพ์บางส่วนโดยใช้ PDF เวอร์ชัน 1.6

## อ้างอิง ##

* [PDF/X - โดย Wikipedia](https://en.wikipedia.org/wiki/PDF/X)

