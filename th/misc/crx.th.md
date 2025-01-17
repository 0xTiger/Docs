{
"วันที่": "2023-06-08",
  "keywords": [
"ไฟล์ crx",
"ไฟล์ crx คืออะไร",
"วิธีติดตั้งไฟล์ crx ใน Google Chrome",
"วิธีการเปิดไฟล์ crx",
"ไฟล์ crx ประกอบด้วยอะไรบ้าง",
"ไฟล์ crx เป็นรูปแบบอะไร",
"ไฟล์",
"นามสกุลไฟล์ crx",
"ส่วนขยาย"
],
  "author": {
"display_name": "ชาคีล ไฟซ์"
},
"draft": "false",
"toc": true,
"title": "รูปแบบไฟล์ CRX - ส่วนขยายของ Google Chrome",
  "description":"เรียนรู้เกี่ยวกับรูปแบบ CRX และ API ที่สามารถสร้างและเปิดไฟล์ CRX",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
      "parent": "misc"
}
},
"lastmod": "2023-06-08"
}

## ไฟล์ CRX คืออะไร??

รูปแบบไฟล์ CRX เชื่อมโยงกับส่วนขยายเบราว์เซอร์ Google Chrome ไฟล์ CRX นั้นเป็นแพ็คเกจบีบอัดที่มีไฟล์และข้อมูลเมตาที่จำเป็นสำหรับการติดตั้งและเรียกใช้ส่วนขยายใน Google Chrome ปรับปรุงการทำงานหรือรูปลักษณ์ของเว็บเบราว์เซอร์โดยมอบคุณสมบัติหรือธีมพิเศษ

เมื่อดาวน์โหลดและติดตั้งไฟล์ CRX ใน Google Chrome เบราว์เซอร์จะตรวจสอบความสมบูรณ์ของส่วนขยายโดยใช้รหัสสาธารณะและลายเซ็น หากการยืนยันสำเร็จ Chrome จะแยกเนื้อหาของไฟล์ CRX และติดตั้งส่วนขยายเพื่อให้สามารถใช้งานได้ ผู้ใช้สามารถจัดการส่วนขยายของตนผ่านทางหน้าส่วนขยายของ Chrome ซึ่งช่วยให้สามารถเปิด ปิด หรือลบส่วนขยายที่ติดตั้งได้

## จะติดตั้งไฟล์ CRX ใน Google Chrome ได้อย่างไร

หากต้องการติดตั้งไฟล์ CRX ใน Google Chrome คุณสามารถทำตามขั้นตอนเหล่านี้:

1. เปิดเบราว์เซอร์ Chrome
2. พิมพ์ `chrome://extensions` ในแถบที่อยู่แล้วกด Enter
3. เปิดใช้งานสวิตช์สลับ "โหมดนักพัฒนาซอฟต์แวร์" ซึ่งอยู่ที่มุมขวาบนของหน้าส่วนขยาย
4. คลิกที่ปุ่ม "โหลดแกะกล่อง"
5. ค้นหาและเลือกโฟลเดอร์ที่มีเนื้อหาที่แยกออกมาของไฟล์ CRX (หรือเพียงแค่เลือกไฟล์ CRX เอง)
6. คลิก "เปิด" เพื่อติดตั้งส่วนขยาย

## ไฟล์ CRX ประกอบด้วยอะไรบ้าง

ไฟล์ CRX ประกอบด้วยไฟล์และข้อมูลเมตาที่จำเป็นสำหรับส่วนขยายของ Google Chrome ต่อไปนี้คือรายละเอียดเนื้อหาทั่วไปที่พบในไฟล์ CRX:

- **ไฟล์ Manifest (manifest.json):** ไฟล์นี้เป็นไฟล์รูปแบบ JSON ที่มีข้อมูลเกี่ยวกับส่วนขยาย เช่น ชื่อ เวอร์ชัน คำอธิบาย สิทธิ์ และสคริปต์พื้นหลัง มันกำหนดโครงสร้างและพฤติกรรมของส่วนขยาย
- **ไฟล์ JavaScript:** ไฟล์เหล่านี้มีโค้ดที่กำหนดฟังก์ชันการทำงานของส่วนขยาย อาจมีสคริปต์สำหรับจัดการเหตุการณ์ การแก้ไขหน้าเว็บ หรือการโต้ตอบกับ API ของ Chrome
- **ไฟล์ HTML, CSS และรูปภาพ:** ส่วนขยายมักประกอบด้วยองค์ประกอบอินเทอร์เฟซผู้ใช้ เช่น หน้าต่างป๊อปอัปหรือหน้าตัวเลือก ไฟล์ HTML กำหนดโครงสร้างของอินเทอร์เฟซเหล่านี้ ในขณะที่ไฟล์ CSS ควบคุมลักษณะที่ปรากฏ ไฟล์รูปภาพใช้สำหรับไอคอนหรือเนื้อหากราฟิกอื่นๆ
- **ไฟล์ทรัพยากรเพิ่มเติม:** ส่วนขยายอาจมีแหล่งข้อมูลเพิ่มเติม เช่น ไฟล์การแปลเพื่อรองรับหลายภาษา ไฟล์เหล่านี้มีคำแปลข้อความที่ใช้ในอินเทอร์เฟซผู้ใช้ของส่วนขยาย
- **สคริปต์พื้นหลัง:** หากส่วนขยายมีกระบวนการพื้นหลังหรือสคริปต์ที่ทำงานโดยไม่ขึ้นอยู่กับหน้าเว็บที่ใช้งานอยู่ สคริปต์เหล่านี้จะรวมอยู่ในไฟล์ CRX
- **สคริปต์เนื้อหา:** สคริปต์เนื้อหาคือสคริปต์ที่สามารถแทรกลงในหน้าเว็บเพื่อแก้ไขพฤติกรรมหรือโต้ตอบกับเนื้อหาได้ หากส่วนขยายใช้สคริปต์เนื้อหา ไฟล์ที่จำเป็นสำหรับสคริปต์เหล่านั้นจะปรากฏในไฟล์ CRX
- **เนื้อหาอื่นๆ:** อาจมีไฟล์เพิ่มเติม เช่น ไฟล์เสียงหรือวิดีโอ แบบอักษร หรือไฟล์ข้อมูล ทั้งนี้ขึ้นอยู่กับข้อกำหนดเฉพาะของส่วนขยาย

รูปแบบไฟล์ CRX นั้นเป็นแพ็คเกจบีบอัดที่มีไฟล์และโฟลเดอร์เหล่านี้ทั้งหมดในลักษณะที่มีโครงสร้าง เมื่อติดตั้งไฟล์ CRX ใน Google Chrome เบราว์เซอร์จะแยกเนื้อหาและวางไว้ในตำแหน่งที่เหมาะสม ทำให้สามารถโหลดและเรียกใช้ส่วนขยายภายในเบราว์เซอร์ได้

## ไฟล์ CRX อยู่ในรูปแบบใด

รูปแบบไฟล์ CRX เป็นรูปแบบเฉพาะสำหรับการบรรจุและการเผยแพร่ส่วนขยายของ Google Chrome โดยพื้นฐานแล้วมันเป็นไฟล์ ZIP ที่ถูกบีบอัดซึ่งมีนามสกุลไฟล์ต่างกัน โครงสร้างพื้นฐานของไฟล์ CRX มีดังนี้:

- **ลายเซ็นไฟล์:** ไฟล์ 4 ไบต์แรกมีหมายเลขมหัศจรรย์ "Cr24" (เลขฐานสิบหก: 43 72 32 34) ซึ่งทำหน้าที่เป็นลายเซ็นเพื่อระบุไฟล์เป็นไฟล์ CRX
- **หมายเลขเวอร์ชัน:** 4 ไบต์ถัดไปแสดงถึงหมายเลขเวอร์ชันของรูปแบบ CRX
- **ความยาวของคีย์สาธารณะ:** 4 ไบต์ต่อไปนี้ระบุความยาวของคีย์สาธารณะที่เข้ารหัสซึ่งใช้สำหรับการตรวจสอบลายเซ็นส่วนขยาย
- **ความยาวของลายเซ็น:** 4 ไบต์ต่อมาจะระบุความยาวของลายเซ็นของนามสกุล
- **รหัสสาธารณะ:** ส่วนนี้ประกอบด้วยรหัสสาธารณะที่เข้ารหัสซึ่งใช้ในการตรวจสอบความสมบูรณ์ของส่วนขยาย
- **ลายเซ็น:** ส่วนนี้ประกอบด้วยลายเซ็นของส่วนขยาย ซึ่งสร้างขึ้นโดยการลงนามในเนื้อหาของส่วนขยายโดยใช้คีย์ส่วนตัวที่สอดคล้องกับคีย์สาธารณะที่กล่าวถึงข้างต้น
- **ไฟล์ ZIP:** ไบต์ที่เหลือของไฟล์ CRX ประกอบด้วยไฟล์ ZIP ที่บีบอัด ไฟล์เก็บถาวรนี้ประกอบด้วยไฟล์และโฟลเดอร์ส่วนขยายที่จำเป็นทั้งหมด รวมถึงไฟล์รายการ ไฟล์ JavaScript ไฟล์ HTML ไฟล์ CSS รูปภาพ และทรัพยากรอื่น ๆ

## อ้างอิง
* [ข้อกำหนดรูปแบบ CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

