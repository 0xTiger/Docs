{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "นามสกุล", "ไฟล์", "รูปแบบไฟล์", "ประเภทไฟล์ฐานข้อมูล", "รูปแบบไฟล์ฐานข้อมูล", "ไฟล์ฐานข้อมูล" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DDL และ API ที่สามารถสร้างและเปิดไฟล์ DDL",
  "title" :"รูปแบบไฟล์ DDL - ไฟล์ภาษาคำจำกัดความของข้อมูล",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## ไฟล์ DDL คืออะไร??

ไฟล์ที่มีนามสกุล .ddl คือไฟล์ Data Definition Language ซึ่งใช้เพื่อกำหนดสคีมาของฐานข้อมูล ประกอบด้วยคำสั่ง/คำสั่งสำหรับการทำงานกับโครงสร้างฐานข้อมูล เช่น ตาราง คอลัมน์ ระเบียน และฟิลด์อื่นๆ คำสั่งในไฟล์ DDL เขียนด้วย [SQL](/th/database/sql/) และสามารถดำเนินการต่างๆ เช่น สร้างตารางในฐานข้อมูล วาง และอัปเดต สคีมาฐานข้อมูลเป็นเจ้าของโดยสร้างขึ้นและสามารถดำเนินการ CRUD ทั้งหมดได้ แอปพลิเคชั่นยอดนิยมที่สามารถสร้างและเปิดไฟล์ DDL ได้แก่ Windows Text Editor, Jetbrains Intellij Idea และ EclipseLink

## คำสั่ง DDL

ไฟล์ DDL ไฟล์เดียวสามารถมีคำสั่งต่างๆ ได้หลายคำสั่ง ซึ่งจะดำเนินการตามลำดับและทำการเปลี่ยนแปลงกับสคีมา เช่น การสร้างชุดอักขระและตาราง การทิ้งตาราง การเปลี่ยนชื่อและการแก้ไขตาราง คำสั่ง DDL ต่อไปนี้มักใช้ในขณะที่ทำงานกับสคีมาฐานข้อมูล

`CREATE` - ใช้เพื่อสร้างฐานข้อมูลหรือวัตถุ (เช่น ตาราง ดัชนี ฟังก์ชัน มุมมอง ขั้นตอนการจัดเก็บ และทริกเกอร์)

`DROP` – ใช้เพื่อลบวัตถุออกจากฐานข้อมูล

`ALTER` - ใช้เพื่อแก้ไขโครงสร้างของฐานข้อมูล

`TRUNCATE` – ใช้เพื่อลบระเบียนทั้งหมดออกจากตาราง รวมถึงพื้นที่ทั้งหมดที่จัดสรรไว้สำหรับระเบียนจะถูกลบออก

`COMMENT` – เพิ่มความคิดเห็นลงในพจนานุกรมข้อมูล

`เปลี่ยนชื่อ` – เปลี่ยนชื่อวัตถุที่มีอยู่ในฐานข้อมูล

## ตัวอย่าง DDL

ตัวอย่างต่อไปนี้แสดงคำสั่ง DDL สำหรับคำสั่ง CREATE ซึ่งสร้างตารางและกำหนดเขตข้อมูล

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## อ้างอิง ##

* [DDL โดย Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

