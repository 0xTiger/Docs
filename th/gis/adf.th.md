{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - ESRI ArcInfo รูปแบบไบนารีกริด",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ADF และ API ที่สามารถสร้างและเปิดไฟล์ ADF",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## ไฟล์ ADF คืออะไร??

ไฟล์ที่มีนามสกุล .adf เป็นรูปแบบไฟล์ข้อมูลแรสเตอร์ที่ใช้โดยแอปพลิเคชันซอฟต์แวร์ ESRI เช่น ArcGIS, ArcView และ ArcInfo ข้อมูลเชิงพื้นที่ถูกจัดเก็บเป็นกริดไบนารีที่เป็นของ ESRI ตารางประกอบด้วยแถวและคอลัมน์ของเซลล์ที่สามารถเป็นจำนวนเต็มและทศนิยมได้ กริดจำนวนเต็มในไฟล์ ADF แสดงข้อมูลแยกและตารางทศนิยมแสดงข้อมูลต่อเนื่อง รูปแบบไฟล์ ESRI ที่ได้รับความนิยมอีกรูปแบบหนึ่งคือไฟล์ [SHP](/th/gis/shp/) ที่แสดงถึงข้อมูลเชิงพื้นที่ในรูปแบบของข้อมูลเวกเตอร์ที่จะใช้โดยแอปพลิเคชันระบบสารสนเทศภูมิศาสตร์ (GIS)

## รูปแบบไฟล์ ADF - ข้อมูลเพิ่มเติม

ไฟล์ ADF จะถูกบันทึกเป็นไฟล์ไบนารีไปยังแผ่นดิสก์ในตารางไบนารี กริดจำนวนเต็มมีแอตทริบิวต์ที่จัดเก็บไว้ในตารางแอตทริบิวต์มูลค่า (VAT) แต่ละค่าที่ไม่ซ้ำกันในกริดมีหนึ่งเรกคอร์ดใน VAT โดยที่เรกคอร์ดจะเก็บค่าที่ไม่ซ้ำและจำนวนเซลล์ในกริดจะแสดงด้วยค่านั้น

กริดทศนิยมไม่มีภาษีมูลค่าเพิ่ม

### โครงสร้างกริด

ภายในไฟล์ ADF มีการใช้กริดโดยใช้โครงสร้างข้อมูลแรสเตอร์แบบเรียงต่อกัน หน่วยพื้นฐานภายในโครงสร้างข้อมูลแรสเตอร์นี้เป็นบล็อกสี่เหลี่ยมของเซลล์ แต่ละบล็อกจะถูกจัดเก็บไว้ในดิสก์และบีบอัดในโครงสร้างไฟล์ที่มีความยาวผันแปรได้ ซึ่งเรียกว่าไทล์ แต่ละบล็อกจะถูกจัดเก็บเป็นหนึ่งเรกคอร์ดที่มีความยาวผันแปรได้

GRID rasters จะถูกจัดเก็บไว้ในพื้นที่ทำงาน ซึ่งพื้นที่ทำงานประกอบด้วยไดเร็กทอรีย่อยข้อมูลหนึ่งไดเร็กทอรีและไดเร็กทอรีย่อยสำหรับแต่ละ GRID มีหลายไฟล์ที่ตำแหน่งทางภูมิศาสตร์และข้อมูลแอตทริบิวต์สำหรับกริดที่สอดคล้องกัน ไดเร็กทอรีย่อยข้อมูลประกอบด้วยไฟล์หลายไฟล์ที่เก็บรักษาข้อมูลบางอย่างเกี่ยวกับ GRID และชุดข้อมูลอื่นๆ เช่น ความครอบคลุม ในพื้นที่ทำงาน

## อ้างอิง ##

* [รูปแบบตาราง ESRI](https://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t0000000w000000)
* [คำถามที่พบบ่อย: โครงสร้างไฟล์ของ Arc/INFO Grid คืออะไร](https://support.esri.com/en/technical-article/000008526)
