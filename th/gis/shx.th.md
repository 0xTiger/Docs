{
  "date" : "2021-07-29",
  "keywords" :[ "ไฟล์ shx", "รูปแบบไฟล์ shx", "ไฟล์ shx คืออะไร", "ไฟล์", "ตัวอย่าง shx", "นามสกุลไฟล์ shx", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - รูปแบบดัชนีรูปร่าง Shapefile",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ SHX และ API ที่สามารถสร้างและเปิดไฟล์ SHX",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## ไฟล์ SHX คืออะไร??
ไฟล์ SHX เป็นของรูปแบบดัชนีรูปร่างซึ่งเป็นดัชนีตำแหน่งของรูปทรงเรขาคณิตคุณลักษณะเพื่อให้สามารถค้นหาไปข้างหน้าและข้างหลังได้อย่างรวดเร็ว SHX เป็นไฟล์ออฟเซ็ตการเข้าถึงโดยตรง ไม่มีข้อมูลในไฟล์นี้ มีเพียงสำเนาซ้ำของร้อยไบต์แรก หมายเลขเร็กคอร์ด และออฟเซ็ตกับไบต์เริ่มต้นของเรคคอร์ดนั้นใน shp โปรดทราบว่าไฟล์ที่มีนามสกุล .shx ไม่ผูกกับ [SHP](/th/gis/shp/) และ [DBF](/th/database/dbf/)

## รูปแบบไฟล์ SHX
รูปแบบ SHX มีดัชนีตำแหน่งของรูปทรงเรขาคณิตคุณลักษณะและส่วนหัว 100 ไบต์คล้ายกับไฟล์ SHP ตามด้วยเร็กคอร์ดความยาวคงที่ 8 ไบต์จำนวนเท่าใดก็ได้ซึ่งมีสองฟิลด์ต่อไปนี้:
| ไบต์ | พิมพ์ | เอนเดียนเนส | การใช้งาน |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | ใหญ่ | บันทึกออฟเซ็ต (ในคำ 16 บิต) |
| 4–7 | int32 | ใหญ่ | ความยาวบันทึก (เป็นคำ 16 บิต) |

ดัชนีนี้ทำให้สามารถค้นหาย้อนหลังในไฟล์รูปร่างได้ โดยขั้นแรก ให้ค้นหาย้อนหลังในดัชนีรูปร่าง จากนั้นจึงอ่านค่าออฟเซ็ตของเรกคอร์ด สามารถใช้ออฟเซ็ตนั้นเพื่อค้นหาตำแหน่งที่ถูกต้องในไฟล์ SHP คุณยังสามารถแสวงหาไปข้างหน้า จำนวนระเบียนโดยพลการโดยใช้วิธีการเดียวกัน แม้ว่าจะสามารถสร้างดัชนีที่สมบูรณ์พร้อมกับไฟล์ SHP ได้ แต่ก็สามารถเพิ่มโอกาสที่จะทำให้ไฟล์ SHP เสียหายได้อย่างรวดเร็ว


## อ้างอิง

* [Shapefile - โดย Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)


