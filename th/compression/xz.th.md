{
  "date" : "2022-01-23",
  "keywords" :[ "ไฟล์ xz", "รูปแบบไฟล์", "ไฟล์ xz คืออะไร", "ไฟล์", "ตัวอย่าง xz", "นามสกุลไฟล์ xz", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ XZ - ไฟล์บีบอัด XZ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XZ และ API ที่สามารถสร้างและเปิดไฟล์ XZ",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## ไฟล์ XZ คืออะไร??

XZ เป็นรูปแบบไฟล์บีบอัดที่ใช้อัลกอริธึมการบีบอัด LZMA2 ได้รับการออกแบบมาแทนรูปแบบ gzip และ bzip2 ที่เป็นที่นิยม และมีข้อดีหลายประการเหนือมาตรฐานเก่าเหล่านี้ ไฟล์ XZ ได้รับการสนับสนุนเป็นอย่างดีในหลายๆ แพลตฟอร์ม และสามารถขยายขนาดได้อย่างรวดเร็วและง่ายดาย แม้ว่าจะไม่เหมือนกับไฟล์ [ZIP](/th/compression/zip/) หรือ [RAR](/th/compression/rar/) แต่ไฟล์เก็บถาวร XZ สามารถใช้เพื่อเก็บข้อมูลจำนวนมากโดยไม่ลดทอนคุณภาพการบีบอัด หากคุณต้องการบีบอัดหรือคลายไฟล์ขนาดใหญ่ นามสกุลไฟล์ XZ ก็คุ้มค่าที่จะพิจารณา

## รูปแบบไฟล์ XZ

ไฟล์ XZ ถูกสร้างขึ้นและบันทึกเป็นไฟล์ไบนารีลงดิสก์ ใช้อัลกอริทึม LZMA เพื่อบีบอัดข้อมูล และสามารถบรรลุอัตราส่วนการบีบอัดสูงถึง 50% โดยทั่วไปไฟล์ XZ จะใช้สำหรับการแจกจ่ายซอฟต์แวร์และไฟล์สำรองข้อมูล สามารถคลายการบีบอัดได้โดยใช้ยูทิลิตี XZ ซึ่งรวมอยู่ในลีนุกซ์ส่วนใหญ่

## แตกไฟล์ XZ บน Linux/Unix

ในการแตกไฟล์ XZ ให้ติดตั้งแพ็คเกจ `xz-utils` ก่อน:
```
$ sudo apt-get install xz-utils
```

ใช้คำสั่ง `unxz` เพื่อแตกไฟล์ .xz:
```
$ unxz compressed_xz_file.xz
```

หรือใช้กับ --decompress ตัวเลือกของ XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## อ้างอิง

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)

