---
date: 2019-12-13
keywords: m3u, รูปแบบไฟล์ m3u, นามสกุล .m3u, รายการเล่นมัลติมีเดีย m3u, รูปแบบรายการเล่น m3u,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ M3U และ API ที่สามารถสร้างและเปิดไฟล์ M3U"
title: รูปแบบไฟล์ M3U,
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## ไฟล์ M3U คืออะไร?? ##

M3U (URL MP3) เป็นไฟล์รายการเล่นเสียงที่จัดเก็บด้วยนามสกุล .m3u M3U ไม่ใช่ไฟล์เสียงจริง แต่ชี้ไปที่ไฟล์เสียงและไฟล์วิดีโอในบางครั้ง M3U ได้รับการพัฒนาเพื่อใช้กับซอฟต์แวร์ Winplay3 โดย Fraunhofer นอกจากนี้ยังรองรับโดยเครื่องเล่นมีเดียและซอฟต์แวร์ต่างๆ

## รูปแบบไฟล์ M3U

ไม่มีข้อกำหนดอย่างเป็นทางการสำหรับรูปแบบไฟล์ M3U ซึ่งเป็นมาตรฐานจริง M3U เป็นไฟล์ข้อความล้วนที่ใช้นามสกุล .m3u หากข้อความเข้ารหัสในการเข้ารหัสที่ไม่ใช่ Unicode เริ่มต้นของระบบโลคัล หรือใช้นามสกุล .m3u8 หากข้อความเข้ารหัส UTF-8 แต่ละรายการในไฟล์ M3U สามารถเป็นหนึ่งในรายการต่อไปนี้:

- เส้นทางที่แน่นอนไปยังไฟล์
- เส้นทางไฟล์สัมพันธ์กับไฟล์ M3U
- URL

### ส่วนขยาย M3U ###

ใน M3U แบบขยาย จะมีการแนะนำคำสั่งเพิ่มเติมที่ขึ้นต้นด้วย "#" และลงท้ายด้วยเครื่องหมายทวิภาค (:) หากมีพารามิเตอร์ ด้านล่างนี้เป็นรายการคำสั่งสำหรับ M3U แบบขยาย

- **#EXTM3U** - เป็นส่วนหัวของไฟล์ที่ระบุ Extended M3U และต้องเป็นบรรทัดแรกของไฟล์
- **#EXTENC:** - การเข้ารหัสข้อความ ต้องเป็นบรรทัดที่ 2 ของไฟล์
- **#EXTINF:** - ใช้สำหรับข้อมูลแทร็กและคุณสมบัติเพิ่มเติมอื่นๆ
- **#PLAYLIST:** - ชื่อของเพลย์ลิสต์
- **#EXTGRP:** - เริ่มการจัดกลุ่มชื่อ
- **#EXTALB:** - ข้อมูลอัลบั้ม
- **#EXTART:** - ศิลปินในอัลบั้ม
- **#EXTGENRE** - ประเภทอัลบั้ม
- **#EXTM3A** - เพลย์ลิสต์ไฟล์เดียวสำหรับแทร็กหรือบทในอัลบั้ม
- **#EXTBYT:** - ขนาดไฟล์เป็นไบต์
- **#EXTBIN:** - ข้อมูลไบนารีตามมา
- **#EXTIMG:** - โลโก้ หน้าปก หรือรูปภาพอื่นๆ

### HLS M3U ###

HLS (HTTP Live Streaming) สร้างขึ้นโดย Apple เพื่อสตรีมเสียงและวิทยุไปยังอุปกรณ์ iOS มันขึ้นอยู่กับ M3U แบบขยายที่เข้ารหัส UTF-8 ได้รับมาตรฐานเป็น RFC 8216 ในปี 2560 โดย IETF แท็กสำหรับเพลย์ลิสต์ HLS ขึ้นต้นด้วย "#EXT-X-" ด้านล่างนี้เป็นรายการแท็กสำหรับ HLS

- **EXT-X-VERSION** - ระบุเวอร์ชันที่เข้ากันได้ของไฟล์ตามสื่อและเซิร์ฟเวอร์
- **#EXT-X-START:** - ระบุจุดเริ่มต้นที่ต้องการสำหรับเพลย์ลิสต์
- **#EXT-X-PLAYLIST-TYPE:** - ระบุประเภทของเพลย์ลิสต์ (EVENT หรือ VOD)
- **#EXT-X-TARGETDURATION:** - ระบุระยะเวลาสูงสุดของกลุ่ม
- **#EXT-X-MEDIA-SEQUENCE:** - ระบุหมายเลขลำดับสื่อ
- **#EXT-X-INDEPENDENT-SEGMENTS** - แสดงว่าตัวอย่างสื่อทั้งหมดเป็นอิสระต่อกันและสามารถถอดรหัสได้โดยไม่มีส่วนอื่น
- **#EXT-X-MEDIA:** - ใช้เพื่อเชื่อมโยงเพลย์ลิสต์สื่อที่มีการแสดงทางเลือกของเนื้อหาเดียวกัน
- **#EXT-X-STREAM-INF:** - ระบุ Variant Stream ที่เป็นส่วนหนึ่งของ Renditions
- **#EXT-X-BYTERANGE:** - ระบุว่า Media Segment เป็นช่วงย่อยของทรัพยากรที่ระบุโดย URI
- **#EXT-X-DISCONTINUITY** - ระบุความไม่ต่อเนื่องระหว่างกลุ่มสื่อก่อนหน้าและต่อไปนี้
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - ช่วยให้สามารถซิงโครไนซ์ระหว่างการแสดงที่แตกต่างกันของ Variant Stream เดียวกันหรือ Variant Stream ที่แตกต่างกัน
- **#EXT-X-KEY:** - ระบุวิธีถอดรหัส Media Segments
- **#EXT-X-MAP:** - ระบุวิธีรับส่วนการเตรียมใช้งานสื่อ จำเป็นต้องแยกวิเคราะห์กลุ่มสื่อที่เกี่ยวข้อง
- **#EXT-X-PROGRAM-DATE-TIME:** - เชื่อมโยงตัวอย่างแรกของ Media Segment กับวันที่และ/หรือเวลาที่แน่นอน
- **#EXT-X-DATERANGE:** - เชื่อมโยงช่วงข้อมูล
- **#EXT-XI-FRAMES-ONLY** - ระบุว่าแต่ละส่วนสื่อในเพลย์ลิสต์อธิบาย I-frame เดียว
- **EXT-XI-FRAME-STREAM-INF** - แสดงว่าไฟล์เพลย์ลิสต์มี I-frames ของงานนำเสนอมัลติมีเดีย
- **#EXT-X-SESSION-DATA:** - อนุญาตให้ใช้ข้อมูลเซสชันตามอำเภอใจ
ดำเนินการในรายการเล่นหลัก
- **#EXT-X-SESSION-KEY:** - อนุญาตให้ใช้คีย์เข้ารหัส ลูกค้าสามารถโหลดคีย์เหล่านี้ล่วงหน้าโดยไม่ต้องอ่านเพลย์ลิสต์ก่อน
- **#EXT-X-ENDLIST** - ระบุว่าจะไม่มีการเพิ่ม Media Segments ลงในไฟล์อีกต่อไป

ต่อไปนี้คือรายการประเภทสื่ออินเทอร์เน็ตที่ใช้โดย M3U:

- **application/vnd.apple.mpegurl**: เป็นสื่อประเภทเดียวที่ลงทะเบียนแล้ว (จดทะเบียนในปี 2009) สำหรับ M3U ที่ใช้เพื่ออ้างถึงเพลย์ลิสต์ในแอปพลิเคชัน HLS
- ประเภทสื่ออินเทอร์เน็ตต่อไปนี้ใช้โดยแอปพลิเคชันที่ไม่ใช่ HLS
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## ตัวอย่าง M3U ##

นี่คือตัวอย่างของไฟล์ M3U

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## อ้างอิง ##

- [M3U - วิกิพีเดีย](https://en.wikipedia.org/wiki/M3U)
- [สตรีมมิงแบบสด HTTP](https://tools.ietf.org/html/rfc8216)
