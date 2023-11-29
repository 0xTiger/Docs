{
"วันที่":"2023-11-01",
   "keywords":[
"ตบ",
"ไฟล์แพท",
"ไฟล์การติดตั้งตัวจัดการ pat diskstation",
"วิธีการเปิดไฟล์ pat",
"ไฟล์",
"นามสกุลไฟล์ pat",
"ส่วนขยาย",
"ไฟล์"
],
   "author":{
"display_name":"ชาคีล ไฟซ์"
},
"draft": "false",
"toc":true,
"title": "รูปแบบไฟล์ PAT - ไฟล์การติดตั้ง DiskStation Manager ",
   "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์การติดตั้ง PAT DiskStation Manager และ API ที่สามารถสร้างและเปิดไฟล์ PAT",
"linktitle": "PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation",
         "parent":"system"
}
},
"lastmod":"2023-11-01"
}

## ไฟล์ PAT คืออะไร??

โดยทั่วไปไฟล์ PAT จะเชื่อมโยงกับ **DiskStation Manager (DSM)** ซึ่งเป็นระบบปฏิบัติการที่ใช้โดยอุปกรณ์ Synology Network-Attached Storage (NAS) ไฟล์ PAT เป็นไฟล์การติดตั้งที่ใช้ในการอัปเดตหรือติดตั้ง DSM บน Synology NAS

## การใช้งานไฟล์ PAT

โดยทั่วไปแล้วคุณใช้ไฟล์ PAT เพื่อติดตั้งหรืออัปเดต DSM บน Synology NAS ดังต่อไปนี้:

1. ดาวน์โหลดไฟล์ PAT: คุณสามารถรับไฟล์ PAT ได้จากเว็บไซต์อย่างเป็นทางการของ Synology หรือแหล่งที่เชื่อถือได้อื่นๆ
    







2. เข้าสู่ระบบ NAS ของคุณ: เข้าถึงอินเทอร์เฟซผู้ใช้บนเว็บของ Synology NAS ของคุณโดยป้อนที่อยู่ IP ลงในเว็บเบราว์เซอร์ คุณจะต้องมีสิทธิ์ของผู้ดูแลระบบจึงจะดำเนินการนี้ได้
    







3. ไปที่ Package Center: ในเว็บอินเตอร์เฟส ให้ไปที่ "Package Center" ที่นี่คือที่ที่คุณจัดการและติดตั้งแอปพลิเคชันบน NAS ของคุณ
    







4. การติดตั้งด้วยตนเอง: ใน Package Center ควรมีตัวเลือกสำหรับ "การติดตั้งด้วยตนเอง" หรือ "ติดตั้ง/อัปเดต" ขึ้นอยู่กับเวอร์ชันของ DSM ที่คุณใช้ เลือกตัวเลือกนี้
    







5. เรียกดูไฟล์ PAT: คุณจะได้รับแจ้งให้เรียกดูไฟล์ในเครื่องของคุณและเลือกไฟล์ PAT ที่ดาวน์โหลด
    







6. ติดตั้งหรืออัปเดต: หลังจากเลือกไฟล์ PAT แล้ว ให้ปฏิบัติตามคำแนะนำบนหน้าจอเพื่อติดตั้ง DSM (หากเป็นการติดตั้งใหม่) หรืออัปเดต DSM (หากคุณกำลังอัปเกรดเป็นเวอร์ชันที่ใหม่กว่า)
    







7. รอจนเสร็จสิ้น: กระบวนการติดตั้งหรืออัปเดตอาจใช้เวลาสักครู่และ NAS ของคุณอาจรีบูตโดยเป็นส่วนหนึ่งของกระบวนการ อดทนและรอให้มันเสร็จสิ้น
    







8. การกำหนดค่าหลังการติดตั้ง: หลังจากการติดตั้งหรืออัปเดต คุณอาจต้องกำหนดการตั้งค่า NAS ของคุณตามความต้องการของคุณ

## ผู้จัดการดิสก์สเตชั่น

DiskStation Manager หรือที่เรียกโดยย่อว่า DSM เป็นระบบปฏิบัติการที่พัฒนาโดย Synology สำหรับอุปกรณ์ Network-Attached Storage (NAS) โดยทำหน้าที่เป็นอินเทอร์เฟซการจัดการและการควบคุมสำหรับเซิร์ฟเวอร์ Synology NAS DiskStation Manager มีอินเทอร์เฟซบนเว็บที่เป็นมิตรต่อผู้ใช้ ซึ่งช่วยให้ผู้ใช้สามารถกำหนดค่าและจัดการด้านต่างๆ ของ NAS ได้ เช่น การจัดเก็บข้อมูล การแชร์ไฟล์ โซลูชันการสำรองข้อมูล บริการมัลติมีเดีย และอื่นๆ

DSM ขึ้นชื่อในด้านความอเนกประสงค์และระบบนิเวศแพ็คเกจที่กว้างขวาง ซึ่งช่วยให้ผู้ใช้สามารถติดตั้งและเรียกใช้แอปพลิเคชันและบริการต่างๆ บน Synology NAS ของตนได้ โดยเปลี่ยนให้เป็นเซิร์ฟเวอร์อเนกประสงค์สำหรับการใช้งานทั้งที่บ้านและในธุรกิจ ฟังก์ชันการทำงานทั่วไปบางอย่างของ DiskStation Manager ได้แก่ การแชร์ไฟล์ การสำรองข้อมูลและการซิงโครไนซ์ การสตรีมสื่อ คุณลักษณะด้านความปลอดภัย และการสนับสนุนการจำลองเสมือน

Synology ออกการอัปเดตและ DSM เวอร์ชันใหม่เป็นประจำเพื่อปรับปรุงความปลอดภัย ประสิทธิภาพ และคุณสมบัติต่างๆ ผู้ใช้สามารถอัปเดต DSM ด้วยตนเองโดยใช้ไฟล์ PAT หรือกำหนดค่าการอัปเดตอัตโนมัติเพื่อให้แน่ใจว่า NAS ของตนใช้งาน DiskStation Manager เวอร์ชันล่าสุดและปลอดภัยที่สุด

## เปิดไฟล์ .PAT ได้อย่างไร

หากต้องการอัปเดต DiskStation Manager ด้วยตนเอง คุณสามารถใช้ไฟล์ PAT ที่คุณดาวน์โหลดจาก Synology Download Center โดยใช้ขั้นตอนต่อไปนี้:

1. เข้าถึงแผงควบคุม DiskStation Manager
2. ไปที่ส่วน "อัปเดตและกู้คืน" และเลือก "อัปเดต DSM"
3. จากนั้นเลือก "การอัปเดต DSM ด้วยตนเอง"
4. คลิกที่ปุ่ม "เรียกดู" จากนั้นค้นหาและเลือกไฟล์ PAT ที่คุณดาวน์โหลด
5. หากต้องการเริ่มการอัปเดต DiskStation Manager ให้คลิกที่ปุ่ม "นำไปใช้"

## อ้างอิง
* [Synology](https://en.wikipedia.org/wiki/Synology)