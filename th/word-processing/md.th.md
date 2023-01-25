{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ md", "รูปแบบไฟล์ md", "ไฟล์ md คืออะไร", "ไฟล์", "ตัวอย่าง md", "นามสกุลไฟล์ md","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - ไฟล์ภาษา MarkDown",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MD และ API ที่สามารถสร้างและเปิดไฟล์ MD",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ MD คืออะไร??

ไฟล์ข้อความที่สร้างด้วยภาษาถิ่นของ Markdown จะถูกบันทึกด้วยนามสกุลไฟล์ **.md** หรือ **.MARKDOWN** ไฟล์ MD ถูกบันทึกในรูปแบบข้อความล้วนที่ใช้ภาษา Markdown ซึ่งรวมถึงสัญลักษณ์ข้อความแบบอินไลน์ด้วย กำหนดวิธีจัดรูปแบบข้อความ เช่น การเยื้อง การจัดรูปแบบตาราง แบบอักษร และส่วนหัว ไฟล์ MD สามารถแปลงเป็น HTML ด้วยโปรแกรมที่ชื่อว่า Markdown ภาษา Markdown เผยแพร่โดย John Gruber

ไฟล์ MD ยังสามารถจัดประเภทเป็นไฟล์สำหรับนักพัฒนาซึ่งส่วนใหญ่ใช้โดย Markdown สำหรับการแปลงไฟล์ข้อความเป็นเวอร์ชัน HTML เพื่อให้ผู้ใช้สามารถสร้างไฟล์ที่อ่านและเขียนได้ง่าย ต่อไปนี้คือแอปพลิเคชันที่สามารถเปิดไฟล์ .md ได้:

* ไมโครซอฟต์ โน้ตแพด
* แผ่นจดบันทึก 2
* Apple TextEdit
* ไมโครซอฟต์ เวิร์ดแพด

คำเตือนคืออย่าเปลี่ยนชื่อนามสกุลของไฟล์ .md ในกรณีนี้จะไม่เปลี่ยนประเภทไฟล์เพราะมีซอฟต์แวร์แปลงพิเศษสำหรับเปลี่ยนไฟล์จากประเภทหนึ่งเป็นอีกประเภทหนึ่ง ตามที่กล่าวไว้ข้างต้น ไฟล์ .MD เป็นส่วนขยายของไฟล์ที่สร้างซอฟต์แวร์ภาษา Markdown **Markdown** เป็น [ภาษามาร์กอัปแบบ lightweight](https://en.wikipedia.org/wiki/Lightweight_markup_language) ที่มีไว้เพื่อจุดประสงค์เดียว เพื่อใช้ในการจัดรูปแบบข้อความบนเว็บด้วยไวยากรณ์การจัดรูปแบบข้อความล้วน โปรดทราบว่า Markdown ไม่ใช่สิ่งทดแทน HTML เนื่องจากไวยากรณ์มีขนาดเล็กมาก ซึ่งมีแท็ก HTML ชุดย่อยที่น้อยมาก เหตุผลเบื้องหลัง Markdown คือทำให้ง่ายต่อการอ่าน เขียน และแก้ไขร้อยแก้ว เราสามารถพูดได้ว่า HTML เป็นรูปแบบการเผยแพร่ ในขณะที่ Markdown เป็นรูปแบบการเขียน

ปัจจุบัน Markdown เป็นหนึ่งในภาษามาร์กอัปที่ได้รับความนิยมมากที่สุดในโลก ขณะใช้ Microsoft Word การจัดรูปแบบคำและวลีจะผ่านการคลิกปุ่ม และการเปลี่ยนแปลงจะมองเห็นได้ทันที แต่ Markdown ไม่ใช่แบบนั้น เมื่อสร้างไฟล์ที่จัดรูปแบบ Markdown ไวยากรณ์ของ Markdown จะถูกเพิ่มลงในข้อความเพื่อระบุว่าคำและวลีใดที่อาจดูแตกต่างออกไป ตัวอย่างเช่น ในการแสดงหัวเรื่อง จะมีการใส่เครื่องหมายตัวเลขนำหน้า (เช่น # หัวเรื่องหนึ่ง) สำหรับการสร้างประโยคที่เป็นตัวหนา ให้ใส่เครื่องหมายดอกจันสองตัวก่อนและหลัง (เช่น **ข้อความนี้เป็นตัวหนา**) ไวยากรณ์ Markdown สามารถมองเห็นได้หลังจากในข้อความ

## ประวัติย่อ

John Gruber และ Aaron Swartz ในปี 2004 ได้สร้างภาษา Markdown โดยมีแนวคิดในการทำให้ผู้คน “สามารถเขียนโดยใช้รูปแบบข้อความธรรมดาที่อ่านและเขียนได้ง่าย และมีตัวเลือกในการแปลงเป็น XHTML หรือ HTML เป้าหมายเบื้องหลังการออกแบบคืออ่านง่าย ภาษาสามารถอ่านได้เหมือนเดิม โดยไม่ต้องแท็กหรือเพิ่มคำแนะนำการจัดรูปแบบเหมือนที่ทำในภาษามาร์กอัป เช่น RTF หรือ HTML โดยที่แท็กและคำแนะนำการจัดรูปแบบจะชัดเจน แรงบันดาลใจพื้นฐานคือการใช้แบบแผนที่มีอยู่เพื่อทำเครื่องหมายข้อความธรรมดาในอีเมล

ตั้งแต่นั้นเป็นต้นมา Markdown ก็ถูกนำมาใช้อีกครั้งโดยคนอื่นๆ เช่นเดียวกับใน Perl [โมดูล](https://en.wikipedia.org/wiki/Modular_programming) ที่มีอยู่ใน [CPAN](https://en.wikipedia.org/ wiki/CPAN) และในภาษาโปรแกรมอื่น ๆ มีการแจกจ่ายภายใต้ [ใบอนุญาตรูปแบบ BSD](https://en.wikipedia.org/wiki/BSD_license) และรวมอยู่ในหรือพร้อมใช้งานเป็นปลั๊กอินสำหรับ [ระบบจัดการเนื้อหา](https:// th.wikipedia.org/wiki/Content_management_system)

## ข้อกำหนดทางเทคนิค

เมื่อบางสิ่งถูกเขียนใน Markdown ข้อความจะถูกจัดเก็บไว้ในไฟล์ข้อความล้วนที่มีนามสกุลเป็น .md หรือ .markdown ก่อน จากนั้นจึงใช้แอปพลิเคชัน markdown เช่น Dillinger สำหรับการประมวลผลไฟล์ Markdown เพื่อแปลงข้อความที่จัดรูปแบบ Markdown เป็น HTML เพื่อแสดงในเว็บ เบราว์เซอร์ แอปพลิเคชัน Markdown ใช้ // ตัวประมวลผล Markdown// (เรียกอีกอย่างว่า "ตัวแยกวิเคราะห์" หรือ "การนำไปใช้งาน") เพื่อรับข้อความที่จัดรูปแบบ Markdown และส่งออกเป็นรูปแบบ HTML แผนภาพการไหลของกระบวนการมีดังนี้:

โดยย่อเป็นกระบวนการสี่ขั้นตอนดังนี้

1. ขั้นแรก สร้างไฟล์ Markdown ด้วยโปรแกรมแก้ไขข้อความหรือแอปพลิเคชัน Markdown ที่มีนามสกุลเป็น .md หรือ .markdown
1. ไฟล์ Markdown จะเปิดขึ้นในแอปพลิเคชัน Markdown
1. แอปพลิเคชัน Markdown ใช้เพื่อแปลงไฟล์ Markdown เป็นเอกสาร HTML
1. จากนั้นไฟล์ HTML จะดูในเว็บเบราว์เซอร์หรือใช้แอปพลิเคชัน Markdown เพื่อแปลงเป็นรูปแบบไฟล์อื่น เช่น PDF

Markdown รวดเร็วและง่ายต่อการจดบันทึก, เขียนเนื้อหาสำหรับเว็บไซต์, ผลิตเอกสารพร้อมพิมพ์, สำหรับจัดพิมพ์หนังสือ, สร้างงานนำเสนอและจัดทำเอกสาร

บางเวอร์ชันในมาร์กดาวน์มีผลกระทบอย่างมากต่อเวอร์ชันอื่นๆ มากจนเรามักมองว่าเวอร์ชันดังกล่าวถูกยกมาเป็นส่วนหนึ่งของเวอร์ชันอื่นๆ เช่น ห้องสมุดกล่าวถึงการสนับสนุน CommonMark (GFM) มาดูสั้น ๆ กัน

### จีเอฟเอ็ม
Markdown เป็นที่นิยมมากในหมู่นักพัฒนาเนื่องจาก Github แพลตฟอร์มการแชร์แบบโอเพ่นซอร์สยอมรับและขยายภาษาด้วยเวอร์ชันที่เรียกว่า Github Flavoured Markup (GFM) ซึ่งรวมถึง codeblocks ที่ไม่เหมาะสม, การเชื่อมโยง URL อัตโนมัติ, การขีดฆ่า, ตารางและสร้างสิ่งที่ต้องทำ

### คอมมอนมาร์ค
เมื่อเร็ว ๆ นี้ นักพัฒนา Markdown พยายามสร้างมาตรฐานของ Markdown โดยร่วมกันสร้างเวอร์ชัน การทดสอบ และเอกสารประกอบสำหรับภาษาที่มีประสิทธิภาพมากกว่าและเรียกว่า CommonMark รูปแบบนี้ค่อนข้างใหม่และไม่รองรับฟีเจอร์มากมาย แต่เร็วๆ นี้ฟีเจอร์ MultiMarkdown มากมายจะถูกเพิ่มเข้ามา

### มัลติมาร์คดาวน์
Multi-Markdown เพิ่มคุณลักษณะต่างๆ ให้กับภาษาซึ่งเวอร์ชันอื่นรองรับ เดิมเขียนด้วยภาษา Perl แต่ภายหลังย้ายไปที่ C รองรับ codeblocks ที่ไม่เป็นระเบียบ, การเน้นไวยากรณ์, ตาราง, ข้อมูลเมตา, ลิงค์ส่วนย่อย / การอ้างอิงโยง, เชิงอรรถ, ขีดทับ, รายการคำจำกัดความ, คณิตศาสตร์

## อ้างอิง

* [มาร์กดาวน์ระดับมาสเตอร์](https://guides.github.com/features/mastering-markdown/)
