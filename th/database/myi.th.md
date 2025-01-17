---
date: 2020-11-11
keywords: myi, .myi, รูปแบบไฟล์ myi, วิธีเปิดไฟล์ myi, นามสกุล .myi, นามสกุล myi,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: รูปแบบไฟล์ MYI,
linktitle: MYI
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ MyI และ API ที่สามารถสร้างและเปิดไฟล์ MyI"
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## ไฟล์ MII คืออะไร?? ##

MyI เรียกอีกอย่างว่าไฟล์ดัชนี MySQL MyISAM ใช้สำหรับเก็บดัชนีสำหรับตาราง MyISAM โดย MySQL ดัชนีฐานข้อมูล MySQL กำหนดโครงสร้างของตารางและมีกลไกควบคุมเพื่อตรวจสอบความสมบูรณ์ของตาราง

## รูปแบบไฟล์ MYI ##

ไฟล์ MyI มีสองส่วน ส่วนหัวและค่าคีย์

### ส่วนหัวของ Myi ###

ส่วนหัวประกอบด้วยข้อมูลเกี่ยวกับตัวเลือก ขนาดไฟล์ และคีย์ คีย์ใน MySQL ถูกสร้างขึ้นด้วยคำสั่งเช่น

```sql
CREATE [UNIQUE] INDEX.
```

ไฟล์ที่อ่านและเขียนไฟล์ MyI อยู่ในไดเร็กทอรี ./myisam มีไฟล์ดังต่อไปนี้:

- mi_open.c: ไฟล์นี้มีรูทีนที่เขียนแต่ละส่วนของส่วนหัว
- mi_create.c: ไฟล์นี้มีรูทีนที่เรียกรูทีน mi_open.c
- myisamdef.h: ไฟล์นี้มีข้อกำหนดโครงสร้าง

ส่วนหัวมีส่วนต่อไปนี้:

- สถานะ: สถานะเขียนโดย mi_open.c, mi_state_info_write() โครงสร้างนี้เกิดขึ้นครั้งเดียวในไฟล์
- ฐาน: ฐานเขียนโดย mi_open.c, mi_base_info_write() MI_BASE_INFO เป็นโครงสร้างที่สอดคล้องกันสำหรับฐานใน myisamdef.h โครงสร้างนี้เกิดขึ้นครั้งเดียวในไฟล์
- keydef: keydef เขียนโดย mi_open.c, mi_keydef_write() MI_KEYDEF เป็นโครงสร้างที่สอดคล้องกันสำหรับ keydef ใน myisamdef.h เป็นโครงสร้างแบบหลายเหตุการณ์ที่ปรากฏสำหรับแต่ละดัชนี
- recinfo: recinfo เขียนโดย mi_open.c, mi_recinfo_write() MI_COLUMNDEF เป็นโครงสร้างที่สอดคล้องกันสำหรับ recinfo ใน myisamdef.h เป็นโครงสร้างการเกิดขึ้นหลายครั้งที่ปรากฏขึ้นหนึ่งครั้งในแต่ละฟิลด์ที่ปรากฏในคีย์

### ค่าคีย์ ###

หน้าใน MySQL เรียกว่าบล็อก ค่าคีย์อยู่ในบล็อก บล็อกประกอบด้วยข้อมูลจากดัชนีเดียวเท่านั้น แต่ละคีย์ประกอบด้วยเนื้อหาทั้งหมดของคอลัมน์ทั้งหมด ความยาวบล็อกปกติคือ 0x0400 (1024) ไบต์ ตัวชี้มีตัวเลขขนาดคงที่ (4 ไบต์) สำหรับตารางแถวคงที่ที่มีหมายเลขแถวลำดับ หากคีย์เป็น null ไบต์จะเป็น 0x00 บล็อกปกติเต็มอย่างน้อย 65% และโดยทั่วไปจะเต็ม 80%

ไฟล์ myisamdef.h มีข้อมูลต่อไปนี้ที่แสดงเป็นค่าคงที่ จำนวนคีย์สูงสุดคือ 32 (MI_MAX_KEY) และจำนวนเซกเมนต์สูงสุดในคีย์คือ 16 (MI_MAX_KEY_SEG) ความยาวสูงสุดของคีย์คือ 500 (MI_MAX_KEY_LENGTH) ความยาวสูงสุดของบล็อกคือ 16384 (MI_MAX_KEY_BLOCK_LENGTH)

## อ้างอิง ##

- [ไฟล์ .MYI](https://dev.mysql.com/doc/dev/mysql-server/latest/)

