{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "วิดีโอเสียงที่บีบอัด", "ไฟล์", "ส่วนขยาย", "รูปแบบไฟล์", "คอนเทนเนอร์มัลติมีเดีย", "XVid", "DivX", "Codecs", "รูปแบบไฟล์การแลกเปลี่ยนทรัพยากร", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ AVI - ไฟล์แทรกวิดีโอเสียง",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ AVI และ API ที่สามารถสร้างและเปิดไฟล์ AVI",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## ไฟล์ AVI คืออะไร?? ##

รูปแบบไฟล์ **AVI** เป็นรูปแบบไฟล์คอนเทนเนอร์มัลติมีเดีย Audio Video ที่ Microsoft นำมาใช้ โดยจะเก็บข้อมูลเสียงและวิดีโอที่สร้างและบีบอัดโดยใช้ตัวแปลงสัญญาณหลายตัว (ตัวเข้ารหัส/ตัวถอดรหัส) เช่น **XVid** และ **DivX** เนื่องจากสามารถใช้ตัวแปลงสัญญาณที่แตกต่างกันเพื่อเข้ารหัสเนื้อหา AVI ได้ แอปพลิเคชันที่ดึงข้อมูล เช่น เครื่องเล่น AVI จึงควรเปิดสิ่งเหล่านี้ได้ก็ต่อเมื่อมีตัวแปลงสัญญาณที่จำเป็นติดตั้งไว้ซึ่งเนื้อหา AVI ถูกสร้างขึ้น รูปแบบได้รับการสนับสนุนตามค่าเริ่มต้นบนแพลตฟอร์ม **Microsoft Windows** ทั้งหมด รวมทั้งบนแพลตฟอร์มหลักอื่นๆ เกือบทั้งหมด แอพพลิเคชั่นและ API หลายตัวให้ความสามารถในการสร้าง/บันทึก อ่าน และแปลง AVI เป็นรูปแบบยอดนิยมอื่นๆ เช่น MP4, MOV, WMV เป็นต้น

## รูปแบบไฟล์ AVI ##

ไฟล์ที่มีนามสกุล .avi คือไฟล์ AVI เป็นรูปแบบย่อยของ Resource Interchange File Format (RIFF) RIFF จัดระเบียบข้อมูลเป็นบล็อกหรือ "ก้อน" ที่ระบุด้วยแท็ก FourCC ไฟล์ AVI เป็นเพียง "ก้อน" เดียวในไฟล์ที่จัดรูปแบบ RIFF

ในกลุ่มย่อยแรก ส่วนหัวของไฟล์จะถูกระบุด้วยแท็ก "hdrl" เนื้อหาประกอบด้วยความกว้าง ความสูง และอัตราเฟรมของวิดีโอ ในส่วนย่อยที่สอง แท็กการเคลื่อนไหวแสดงถึงอัตราเฟรมของวิดีโอ วิดีโอ AVI ประกอบด้วยข้อมูลเสียง/ภาพจริงในกลุ่มนี้ นอกจากนี้ยังมีกลุ่มย่อยทางเลือกที่สามที่มีแท็ก "idx1" ซึ่งระบุตำแหน่งภายในไฟล์ของแต่ละกลุ่มข้อมูลที่เป็นของไฟล์

### ข้อจำกัด ###

* ข้อมูลอัตราส่วนภาพไม่สามารถเข้ารหัสในข้อกำหนด AVI ดั้งเดิมได้ แม้ว่าข้อกำหนด OpenDML ในภายหลัง (AVI 2.0) จะเสนอวิธีการที่เป็นมาตรฐาน
* แม้ว่าไฟล์ AVI จะถูกใช้กันอย่างแพร่หลายในขั้นตอนหลังการผลิตภาพยนตร์และรายการโทรทัศน์ แต่วิธีการต่างๆ ในการเพิ่มรหัสเวลาให้กับไฟล์เหล่านี้กำลังแข่งขันกัน ซึ่งส่งผลต่อความสามารถในการใช้งานของรูปแบบ
* ไฟล์วิดีโอที่เข้ารหัสใน AVI ไม่สามารถใช้เทคนิคการบีบอัดที่ต้องใช้ข้อมูลเฟรมในอนาคตนอกเหนือจากเฟรมที่ถูกเข้ารหัส (B-frame)
* เป็นปัญหาในการใช้ไฟล์ AVI ที่มีบิตเรตผันแปร (VBR) (เช่น เสียง MP3 ที่อัตราตัวอย่างต่ำกว่า 32 kHz)
* ไฟล์ AVI ที่เข้ารหัสภาพยนตร์สารคดีความละเอียดมาตรฐานตามที่ใช้ตามปกติ มีแนวโน้มที่จะมีค่าใช้จ่ายประมาณ 5 MB ต่อชั่วโมง ขึ้นอยู่กับวิธีการใช้ไฟล์
* คำบรรยายต้องฮาร์ดโค้ดลงในสตรีมวิดีโอหรือเผยแพร่ในไฟล์แยกต่างหาก ในกรณีที่ไฟล์ AVI ไม่รองรับไฟล์แนบ เช่น ฟอนต์และคำบรรยาย

## ประวัติย่อ ##

AVI ได้รับการแนะนำโดย Microsoft ในปี 1992 โดยมีจุดประสงค์เพื่อให้รูปแบบไฟล์เสียงและวิดีโอที่แข็งแกร่งและทันสมัยยิ่งขึ้น รูปแบบดังกล่าวได้รับความนิยมอย่างรวดเร็วจากการใช้อินเทอร์เน็ต ทำให้บุคคลสามารถแชร์ไฟล์วิดีโอได้โดยตรงและโดยอ้อมผ่านที่เก็บข้อมูลสื่อบนคลาวด์

## อ้างอิง ##

* [AVI - โดย Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

