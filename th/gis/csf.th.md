{
  "date" : "2023-01-27",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ CSF - รูปแบบไฟล์ระบบพิกัด GeoMedia",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CSF และ API ที่สามารถสร้างและเปิดไฟล์ CSF",
  "linktitle" : "CSF",
  "menu" : {
    "docs" : {
      "identifier":"gis-csf",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-27"
}

## ไฟล์ CSF คืออะไร??

ไฟล์ CSF เป็นไฟล์ระบบพิกัดที่มีข้อมูลเกี่ยวกับระบบพิกัดของไฟล์ GIS มันถูกใช้โดยซอฟต์แวร์ GeoMedia ของ Intergraph เพื่อกำหนดพารามิเตอร์ของระบบพิกัดเฉพาะ ซึ่งรวมถึงพารามิเตอร์ข้อมูล เช่น Datum การฉายภาพ และหน่วยการวัด ข้อมูลนี้ใช้เพื่อสร้างแผนที่สำหรับข้อมูลเอาต์พุตที่ไม่มีระบบพิกัด GeoMedia ใช้ข้อมูลนี้เพื่อแสดงและจัดการข้อมูลทางภูมิศาสตร์อย่างถูกต้องในระบบพิกัดที่ถูกต้อง

## รูปแบบไฟล์ CSF

ไฟล์ CSF จะถูกจัดเก็บเป็นไฟล์ข้อความพร้อมรายละเอียดระบบพิกัดทางภูมิศาสตร์ GeoMedia อนุญาตให้นำเข้าไฟล์ข้อมูลทางภูมิศาสตร์จากข้อมูลที่ป้อนซึ่งไม่ได้กำหนดระบบพิกัดไว้ การใช้ระบบฉายภาพและพิกัด ระบบ GIS จะแสดงไฟล์แผนที่ด้วยค่าที่แน่นอน ไฟล์ CSF ถูกสร้างขึ้นในตำแหน่งเดียวกับไฟล์เอาต์พุต

## อ้างอิง

* [คุณแสดงหรือให้บริการข้อมูลเชปไฟล์ใน GeoMedia อย่างถูกต้องได้อย่างไร?](https://supportsi.hexagon.com/help/s/article/How-do-you-correctly-display-or-serve-shapefile-data-into?language=en_US)

