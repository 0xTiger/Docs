{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ GCF และ API ที่สามารถสร้างและเปิดไฟล์ GCF",
  "title" : "ไฟล์ GCF - รูปแบบ Nadeo Game GCF",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-th",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## ไฟล์ GCF คืออะไร??

ไฟล์ .gcf เป็นไฟล์แคชเกมที่ใช้โดยแพลตฟอร์มเกม Steam ประกอบด้วยข้อมูลเกม เช่น พื้นผิว โมเดล และไฟล์อื่นๆ ที่เกมใช้ ไฟล์เหล่านี้จะถูกจัดเก็บไว้ในคอมพิวเตอร์ของผู้ใช้ และใช้เพื่อลดปริมาณข้อมูลที่จำเป็นต้องดาวน์โหลดเมื่ออัปเดตหรือติดตั้งเกม ไฟล์ .gcf ยังสามารถใช้เพื่อสร้างการสำรองข้อมูลการติดตั้งเกมหรือถ่ายโอนเกมระหว่างคอมพิวเตอร์

ไฟล์ GCF สามารถอ่านและเขียนได้โดยไลบรารีการเขียนโปรแกรม Open Source C++, **HLLib**

## รูปแบบไฟล์ GCF

ไฟล์ GCF จะถูกบันทึกลงแผ่นดิสก์เป็นไฟล์ไบนารี เดิมที GCF ถูกใช้เป็นตัวย่อสำหรับไฟล์แคชกริด (ชื่อรหัสแรกของ Steam คือกริด) แต่ต่อมาถูกนำไปใช้เป็นไฟล์แคชเกม ไฟล์ GCF เป็นไฟล์เก็บถาวรที่เก็บเกม Steam เนื้อหาอย่างเป็นทางการทั้งหมดจะถูกดาวน์โหลดเป็นไฟล์ GCF ไฟล์ GCF สามารถแชร์ระหว่างเกมได้

หมายเหตุ: GCF เป็นรุ่นก่อนของ [VPK file format](/game/vpk/)
## อ้างอิง

* [ซอฟต์แวร์วาล์ว](https://www.valvesoftware.com/en/)

* [รูปแบบไฟล์ GCF](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib - ไลบรารีการเขียนโปรแกรม C++ โอเพ่นซอร์สสำหรับการอ่านไฟล์ GCF](https://developer.valvesoftware.com/wiki/HLLib)

