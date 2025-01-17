{
  "date" : "2021-04-08",
  "keywords" :[ "ไฟล์ dar", "รูปแบบไฟล์ dar", "ไฟล์ dar คืออะไร", "ไฟล์", "ตัวอย่าง dar", "นามสกุลไฟล์ dar", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - รูปแบบไฟล์เก็บถาวรดิสก์",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DAR และ API ที่สามารถสร้างและเปิดไฟล์ DAR",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## ไฟล์ DAR คืออะไร??

ไฟล์ที่มีนามสกุล .dar เป็นไฟล์เก็บถาวรแบบบีบอัดที่สร้างขึ้นโดยใช้ไฟล์เก็บถาวร DAR Disk สามารถสร้างการสำรอง/เก็บถาวรสำหรับดิสก์เต็มหรือกลุ่มของไฟล์ สร้างขึ้นเพื่อแทนที่รูปแบบไฟล์ [TAR](/th/compression/tar/) บนระบบปฏิบัติการ UNIX และสามารถสร้างเป็นไฟล์เก็บถาวรแยกสำหรับไฟล์จำนวนมาก ไฟล์เก็บถาวร DAR รองรับตัวเลือกในการลบไฟล์ออกจากระบบซึ่งเชื่อมโยงกับไฟล์หลักในไฟล์เก็บถาวร ความสามารถในการสำรองส่วนต่าง ส่วนเพิ่ม และส่วนเพิ่ม ทำให้เหนือกว่าไฟล์ TAR

## รูปแบบไฟล์ DAR

ไฟล์ DAR เป็นไฟล์เก็บถาวรแบบบีบอัดที่สามารถใช้การบีบอัดต่อไฟล์ใดก็ได้ เช่น [gzip](/th/compression/gz/), [bzip2](/th/compression/bz2/), lzo, xz หรือ lzma รูปแบบไฟล์ที่แน่นอนของไฟล์ DAR ขึ้นอยู่กับประเภทของการจัดรูปแบบที่ใช้ในการบีบอัดเนื้อหาของไฟล์เก็บถาวร นอกจากนี้ยังอนุญาตให้ใช้การเข้ารหัส Blowfish, Twofish, AES, Serpent, Camellia และการเข้ารหัสคีย์สาธารณะและลายเซ็น (OpenPGP)

### คุณสมบัติ DAR

คุณลักษณะบางอย่างของรูปแบบไฟล์ DAR มีดังต่อไปนี้

* ดูแลไอโหนดทุกประเภท (ไดเร็กทอรี, ไฟล์ธรรมดา, ซิมลิงก์, อุปกรณ์พิเศษ, ไพพ์ที่มีชื่อ, ซ็อกเก็ต, ประตู, ...)
* ดูแล inodes ที่เชื่อมโยงอย่างหนัก (ไฟล์ธรรมดาที่เชื่อมโยงอย่างหนัก, อุปกรณ์ถ่าน, อุปกรณ์บล็อก, symlink ที่เชื่อมโยงอย่างหนัก)
* ดูแลไฟล์ที่กระจัดกระจาย
* ดูแลไฟล์ Linux Extended Attributes
* ดูแลไฟล์ Linux ACL
* ดูแลส้อมไฟล์ Mac OS X
* ดูแลแอตทริบิวต์เฉพาะของระบบไฟล์บางอย่าง เช่น วันเกิดของระบบไฟล์ HFS+ และแอตทริบิวต์ที่ไม่สามารถเปลี่ยนรูปได้ การทำเจอร์นัลข้อมูล การลบแบบปลอดภัย
* การบีบอัดต่อไฟล์ด้วย gzip, bzip2, lzo, xz หรือ lzma (ตรงข้ามกับการบีบอัดไฟล์เก็บถาวรทั้งหมด) แต่ละคนสามารถเลือกที่จะไม่บีบอัดไฟล์ที่บีบอัดแล้วตามคำต่อท้ายชื่อไฟล์
* แตกไฟล์อย่างรวดเร็วจากทุกที่ในไฟล์เก็บถาวร
* รายการเนื้อหาที่จัดเก็บอย่างรวดเร็วผ่านการบันทึกแคตตาล็อกของไฟล์ในที่จัดเก็บ
* การสำรองข้อมูลระบบไฟล์สด: ตรวจพบเมื่อไฟล์ได้รับการแก้ไขในขณะที่อ่านเพื่อสำรองข้อมูล และสามารถลองบันทึกซ้ำได้จนถึงจำนวนการลองใหม่สูงสุดที่กำหนด
* ไฟล์แฮช (MD5, SHA1 หรือ SHA-512) สร้างขึ้นทันทีสำหรับแต่ละสไลซ์ ไฟล์ผลลัพธ์เข้ากันได้กับ md5sum หรือ sha1sum เพื่อให้สามารถตรวจสอบความสมบูรณ์ของแต่ละสไลซ์ได้อย่างรวดเร็ว
* ระบบไฟล์ไม่ขึ้นกับระบบ: อาจใช้เพื่อกู้คืนระบบไปยังพาร์ติชันที่มีขนาดต่างกัน และ/หรือไปยังพาร์ติชันที่มีระบบไฟล์ต่างกัน[5]

## อ้างอิง

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

