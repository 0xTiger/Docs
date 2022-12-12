{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ LOCK - ไฟล์ล็อคคืออะไร",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ LOCK และ ",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## ไฟล์ LOCK คืออะไร??

ไฟล์ **LOCK** เป็นไฟล์ที่เปลี่ยนชื่อซึ่งใช้โดยแอปพลิเคชันและระบบปฏิบัติการเพื่อทำเครื่องหมายไฟล์หรืออุปกรณ์บางอย่างว่าล็อก ซึ่งจะบอกแอปพลิเคชันอื่นๆ ว่าอย่าใช้ไฟล์ เว้นแต่ว่าไฟล์นั้นจะว่างจากแอปพลิเคชันที่กำลังใช้ไฟล์นั้นอยู่ ในกรณีส่วนใหญ่ ไฟล์ล็อคเหล่านี้จะว่างเปล่า แต่ในกรณีอื่นๆ ไฟล์เหล่านี้อาจมีข้อมูลที่เกี่ยวข้องกับการล็อค เช่น คุณสมบัติและการตั้งค่า

ในบางครั้ง .NET Framework ของ Microsoft จะใช้ไฟล์ .lock เพื่อสร้าง **lockeed** สำเนาของไฟล์ฐานข้อมูล ในกรณีเช่นนี้ สำเนาของไฟล์ฐานข้อมูลจะเปิดขึ้นพร้อมกับนามสกุล .lock สิ่งนี้ไม่อนุญาตให้ผู้ใช้ทำการเปลี่ยนแปลงไฟล์ในขณะที่ผู้ใช้รายอื่นใช้งานอยู่

## รูปแบบไฟล์ LOCK - ข้อมูลเพิ่มเติม

แต่ละแอปพลิเคชันสร้างไฟล์ LOCK และรูปแบบไฟล์นั้นเฉพาะสำหรับแอปพลิเคชัน ไฟล์ล็อคเหล่านี้สามารถบันทึกได้ทั้งในรูปแบบข้อความและไฟล์ไบนารี

การมีไฟล์ล็อคป้องกันการเข้าถึงทรัพยากรพร้อมกันหลายไฟล์ที่พยายามเข้าถึงทรัพยากรนั้น สำเนาของไฟล์ต้นฉบับถูกสร้างขึ้นโดยมีนามสกุล .lock ต่อท้ายชื่อ สิ่งนี้บอกให้แอปพลิเคชันอื่นเข้าถึงไฟล์แบบอ่านอย่างเดียว ตัวอย่างเช่น resource.dat จะกลายเป็น resource.data.lock

สำหรับภาษาโปรแกรม Ruby คุณอาจเจอไฟล์ **gemfile.lock** นี่คือที่ที่ Bundler เก็บบันทึกเวอร์ชันที่แน่นอนที่ติดตั้งไว้ ดังนั้น เมื่อโปรเจ็กต์/ไลบรารีถูกย้ายไปยังเครื่องอื่น การรันบันเดิลจะดูที่ Gemfile สำหรับเวอร์ชันที่เกี่ยวข้อง

## ล็อคไฟล์ใน Linux

Linux รองรับการล็อคไฟล์สองประเภท: ล็อคคำแนะนำและการล็อคบังคับ

* **Advisory Locks**: ประเภทของการล็อคที่ไม่ได้บังคับใช้ ในกรณีนี้ กระบวนการที่เข้าร่วมจะร่วมมือกันเพื่อให้ได้มาซึ่งล็อคอย่างชัดเจน หากไม่สามารถทำได้ การล็อกคำแนะนำจะถูกละเว้น

* **การล็อกแบบบังคับ**: ในกรณีของการล็อกแบบบังคับ ระบบปฏิบัติการจะบังคับใช้การล็อกไฟล์โดยป้องกันไม่ให้กระบวนการอื่นอ่านหรือเขียนไฟล์ สิ่งนี้ไม่ต้องการความร่วมมือระหว่างกระบวนการ

การล็อคแบบบังคับไม่ต้องการความร่วมมือใดๆ ระหว่างกระบวนการที่เข้าร่วม เมื่อเปิดใช้งานการล็อกที่จำเป็นบนไฟล์ ระบบปฏิบัติการจะป้องกันไม่ให้กระบวนการอื่นๆ อ่านหรือเขียนไฟล์

## อ้างอิง

* [GemFile และ Gemfile.lock ใน Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [การล็อกใน Linux](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)
