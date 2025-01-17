
{
  "date": "2023-01-05",
  "keywords": [
"ไฟล์ POV",
"รูปแบบไฟล์ POV",
"ไฟล์ pov คืออะไร",
"ไฟล์",
"ตัวอย่างมุมมอง",
"ไฟล์นามสกุล .pov",
"ส่วนขยาย",
"รูปแบบ"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "เรียนรู้เกี่ยวกับรูปแบบไฟล์ POV และ API ที่สามารถเปิดและสร้างไฟล์ POV",
  "title": "POV - ไฟล์การคงอยู่ของการมองเห็น",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-thv"
}
},
  "lastmod": "2023-01-05"
}

## ไฟล์ POV คืออะไร??

ไฟล์ POV เป็นไฟล์ข้อความธรรมดาที่มีคำแนะนำสำหรับซอฟต์แวร์ติดตามรังสี POV-Ray คำแนะนำเหล่านี้เขียนด้วยภาษาสคริปต์พิเศษเฉพาะสำหรับ POV-Ray โดยจะระบุฉากที่จะเรนเดอร์ รวมถึงวัตถุ 3 มิติ วัสดุ แสง และคุณสมบัติอื่นๆ ที่กำหนดลักษณะของฉาก ไฟล์ POV ใช้ภาษาสคริปต์พิเศษเฉพาะสำหรับ POV-Ray และสามารถใช้เพื่อสร้างฉาก 3 มิติที่ซับซ้อนและมีรายละเอียด นามสกุลไฟล์สำหรับไฟล์ POV โดยทั่วไปจะเป็น .pov หรือ .povray เมื่อคุณเปิดไฟล์ POV ใน POV-Ray ซอฟต์แวร์จะอ่านคำแนะนำในไฟล์และใช้เพื่อสร้างภาพที่เรนเดอร์ของฉาก

ศิลปินและนักออกแบบมักใช้ไฟล์ .pov เพื่อสร้างกราฟิกและแอนิเมชั่น 3 มิติสำหรับแอปพลิเคชันที่หลากหลาย รวมถึงภาพยนตร์ โทรทัศน์ วิดีโอเกม และสื่อทางการตลาด

## รูปแบบไฟล์ POV

โดยทั่วไปไฟล์ **.pov** จะเริ่มต้นด้วยชุดคำสั่ง **#include** ซึ่งใช้เพื่อรวมไลบรารีของสี พื้นผิว และทรัพยากรอื่นๆ ที่กำหนดไว้ล่วงหน้าที่สามารถนำมาใช้ในฉากได้ จากนั้น ไฟล์จะกำหนดวัตถุ วัสดุ และคุณสมบัติอื่นๆ ของฉากโดยใช้ชุดบล็อก มีออบเจ็กต์ วัสดุ และคุณสมบัติอื่นๆ อีกหลายประเภทที่คุณสามารถระบุในไฟล์ .pov และคุณสามารถใช้ลูปและคำสั่งแบบมีเงื่อนไขเพื่อสร้างฉากที่ซับซ้อนและมีรายละเอียดมากขึ้นได้

## แอพพลิเคชั่นซอฟต์แวร์สำหรับ POV

ซอฟต์แวร์ติดตามรังสี POV-Ray ใช้รูปแบบไฟล์ .pov ดังนั้นแอปพลิเคชันหลักสำหรับการเปิดไฟล์ .pov ก็คือซอฟต์แวร์ POV-Ray นั่นเอง คุณสามารถดาวน์โหลด POV-Ray เวอร์ชันล่าสุดได้จากเว็บไซต์อย่างเป็นทางการที่ https://www.povray.org/

นอกจาก POV-Ray แล้ว ยังมีแอปพลิเคชันอื่นๆ อีกจำนวนหนึ่งที่สามารถเปิดและแก้ไขไฟล์ .pov ได้ เช่น:

- BRL-CAD: ซอฟต์แวร์สร้างแบบจำลอง 3 มิติแบบโอเพ่นซอร์สที่สามารถนำเข้าและส่งออกไฟล์ .pov
- MeshLab: ซอฟต์แวร์ประมวลผล 3D mesh ที่สามารถนำเข้าและส่งออกไฟล์ .pov
- Blender: ซอฟต์แวร์กราฟิก 3D โอเพ่นซอร์สยอดนิยมที่สามารถนำเข้าและส่งออกไฟล์ .pov

อาจมีแอปพลิเคชันซอฟต์แวร์อื่นๆ ที่สามารถเปิดไฟล์ .pov ได้เช่นกัน ดังนั้นคุณอาจต้องการลองใช้โปรแกรมดูไฟล์หรือเครื่องมือแปลงไฟล์ หากคุณไม่สามารถเปิดไฟล์ .pov ด้วยแอปพลิเคชันข้างต้นได้

## ตัวอย่างมุมมอง

ตัวอย่างเช่น นี่คือตัวอย่างไฟล์ .pov ที่กำหนดฉากด้วยทรงกระบอกสีน้ำเงินอันเดียว:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

ในตัวอย่างนี้ บล็อกกล้องระบุตำแหน่งและทิศทางของกล้องในฉาก บล็อก `แหล่งกำเนิดแสง` ประกาศแหล่งกำเนิดแสงและระบุตำแหน่งและสี และบล็อก 'ทรงกระบอก' ประกาศวัตถุทรงกระบอกและระบุจุดสิ้นสุด รัศมีและคุณสมบัติของวัสดุ เมื่อคุณเปิดไฟล์ .pov นี้ในซอฟต์แวร์ POV-Ray มันจะเรนเดอร์รูปภาพของทรงกระบอกสีน้ำเงินอันเดียว

## อ้างอิง
 * [POV-Ray - วิกิพีเดีย](https://en.wikipedia.org/wiki/POV-Ray)
 * [เว็บไซต์เอกสาร POV-Ray](http://www.povray.org/documentation/)

