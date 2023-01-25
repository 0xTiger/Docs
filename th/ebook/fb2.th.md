{
  "date" : "2019-12-12",
  "keywords" :[ "FB2", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "eBook", "เปิด", "XML", "อ่าน" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ FB2 และ API ที่สามารถสร้างและเปิดไฟล์ FB2",
  "title" :"ไฟล์ FB2 คืออะไร",
  "linktitle" : "FB2",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-11-22"
}

## ไฟล์ FB2 คืออะไร??

ไฟล์ที่มีนามสกุล .fb2 เป็นไฟล์ eBook ของ FictionBook 2.0 ที่มีโครงสร้างของ eBook มันขึ้นอยู่กับรูปแบบ XML และมีแท็กพิเศษสำหรับอธิบายแต่ละองค์ประกอบของหนังสือ ได้รับการพัฒนาขึ้นสำหรับงานเขียนและวรรณกรรมที่แต่งขึ้นเป็นหลัก แต่ไม่จำกัดเฉพาะสิ่งเหล่านี้เท่านั้น รูปแบบรองรับข้อมูลเมตาทั้งหมดรวมถึงเนื้อหาในตัวเอง และช่วยให้มีความยืดหยุ่นสำหรับการดำเนินการหลายอย่าง เช่น การประมวลผลอัตโนมัติ การจัดทำดัชนี และการแปลงเป็นรูปแบบอื่น กล่าวโดยย่อคือเน้นที่การอธิบายโครงสร้างของไฟล์แทนที่จะระบุลักษณะที่ปรากฏ มีแอปพลิเคชันหลายตัวรวมถึง API สำหรับแปลง FB2 เป็นรูปแบบอื่นๆ บน Windows, MacOS และ Linux

## รูปแบบไฟล์ FB2

รูปแบบไฟล์ FictionBook 2.0 ได้รับการพัฒนาโดย Dmitry Gribov แห่ง FictionBook ในรัสเซีย ซึ่งแตกต่างจากรูปแบบไฟล์ Ebook ยอดนิยมอื่นๆ เช่น [EPUB](/th/ebook/epub/) ที่มีไฟล์ XML หลายไฟล์ โดยจะขึ้นอยู่กับไฟล์ XML เดียวที่มีข้อมูลครบถ้วนเกี่ยวกับเนื้อหา หากมีรูปภาพในไฟล์ เช่น [PNG](/th/image/png/) หรือ [JPG](/th/image/jpeg/) รูปภาพเหล่านี้จะถูกแปลงเป็น Base64 และฝังอยู่ภายในเอกสาร [ข้อกำหนดรูปแบบไฟล์](http://gribuser.ru/xml/fictionbook/index.html.en) สำหรับ FB2 มีข้อมูลสำหรับรูปแบบเวอร์ชัน 2.0

## อ้างอิง ##

* [FB2 - โดย Wikipedia](https://en.wikipedia.org/wiki/FictionBook)
* [ข้อมูลจำเพาะของหนังสือนิยาย](http://gribuser.ru/xml/fictionbook/index.html.en)
