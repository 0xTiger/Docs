---
date: 2019-12-13
keywords: ra, รูปแบบไฟล์ ra, นามสกุล .ra, รูปแบบไฟล์เสียงจริง, รูปแบบเสียง ra, รูปแบบไฟล์ RealAudio,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ RA และ API ที่สามารถสร้างและเปิดไฟล์ RA"
title: รูปแบบไฟล์ RA,
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## ไฟล์ RA คืออะไร??

RealAudio (RA) เป็นรูปแบบเสียงที่เป็นกรรมสิทธิ์ซึ่งพัฒนาโดย Real Networks, Inc. และเผยแพร่ในเดือนเมษายน พ.ศ. 2538 โดยใช้นามสกุล .ra สำหรับไฟล์ต่างๆ ใช้บิตเรตต่ำและตัวแปลงสัญญาณเสียงที่มีความเที่ยงตรงสูง RA ใช้สำหรับการสตรีมเสียงผ่านอินเทอร์เน็ตโดยสถานีวิทยุอินเทอร์เน็ตหลายแห่ง เว็บไซต์ BBC ใช้ RA อย่างหนักจนถึงปี 2009 แต่หยุดให้บริการในเดือนมีนาคม 2011

## นามสกุลไฟล์โดย RealNetworks ##

RealNetworks ใช้รูปแบบไฟล์ RA สำหรับเสียง RealNetworks เริ่มให้บริการรูปแบบวิดีโอ ([RealVideo](/th/video/rv/)) ในปี 1997 ด้วยนามสกุล .rv [RealMedia (RM)](/th/video/rm/) ใช้สำหรับรูปแบบเสียงและวิดีโอร่วมกัน ด้วย RealProduce รุ่นล่าสุด (ตัวเข้ารหัสของ Real) จะใช้รูปแบบ RV สำหรับไฟล์วิดีโอ และใช้รูปแบบ [RealMedia Variable Bitrate (RMVB)](/th/video/rmvb/) สำหรับไฟล์วิดีโอ VBR (Variable bitrate)

## สตรีมมิ่งเสียง ##

RA ได้รับการพัฒนาเป็นรูปแบบสื่อสตรีมมิ่งและสามารถสตรีมได้โดยใช้ HTTP ไฟล์เสียงจะเริ่มเล่นทันทีที่ได้รับส่วนแรกของไฟล์ และเล่นต่อไปเมื่อดาวน์โหลดไฟล์ส่วนที่เหลือ

RealAudio เวอร์ชันแรกใช้โปรโตคอล PNA หรือ PNM ที่เป็นกรรมสิทธิ์เพื่อสตรีมเสียง ต่อมาพวกเขาเปลี่ยนไปใช้ RTSP (Real Time Streaming Protocol) ที่ได้มาตรฐานของ IETF เพื่อจัดการการเชื่อมต่อ พวกเขาใช้โปรโตคอล RDT (Real Data Transfer) ในการส่งข้อมูล โปรโตคอลถูกเก็บเป็นความลับในตอนแรก แต่ต่อมาบางส่วนก็ถูกเปิดเผยต่อสาธารณะผ่านโครงการ Helix

ในการสตรีมไฟล์ RealAudio หน้าส่วนใหญ่จะลิงก์ไปยังไฟล์ RAM (Real Audio Metadata) หรือไฟล์ SMIL (Synchronized Multimedia Integration Language) ไฟล์นี้ใช้เพื่อโหลดเครื่องเล่นสื่อของผู้ใช้และสตรีมเสียงจาก URL ที่มีอยู่ในไฟล์

## ตัวแปลงสัญญาณเสียง RealAudio ##

ต่อไปนี้คือรายการตัวแปลงสัญญาณเสียงที่แต่ละตัวระบุด้วยรหัสอักขระสี่ตัวพร้อมกับเวอร์ชันของ RealAudio ที่แนะนำ

|ตัวแปลงสัญญาณ|เวอร์ชัน RealAudio|
|---|---|
|lpcJ และ 14_4|1|
|28_8|2|
|dnet|3|
|sipr|4/5|
|ทำอาหาร|6|
|atrc|8|
|แรค|9|
|racp|10|
|ราล์ฟ|10|

## อ้างอิง ##

- [RealAudio - Wikipedia](https://en.wikipedia.org/wiki/RealAudio)
