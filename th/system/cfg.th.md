{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "นามสกุล", "ไฟล์", "รูปแบบ", "ระบบ", "การกำหนดค่า", "การตั้งค่า", "โปรแกรม", "คอมพิวเตอร์", "แอปพลิเคชัน" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - รูปแบบไฟล์",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CFG และ API ที่สามารถสร้างและเปิดไฟล์ CFG",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## ไฟล์ CFG คืออะไร?? ##

ไฟล์ที่มีนามสกุล .cfg เป็นไฟล์ประเภท "การตั้งค่า" เป็นประเภทไฟล์ที่นิยมใช้และใช้เพื่อเก็บข้อมูลเกี่ยวกับการกำหนดค่าและการตั้งค่าสำหรับโปรแกรมคอมพิวเตอร์ ไฟล์ CFG ส่วนใหญ่จัดเก็บในรูปแบบข้อความและไม่ควรเปิดด้วยตนเอง แต่ควรเปิดโดยใช้โปรแกรมแก้ไขข้อความแทน อย่างไรก็ตาม มีไฟล์ CFG หลายประเภทที่แตกต่างกันในรูปแบบที่ใช้เก็บข้อมูล คุณสมบัติที่ไฟล์ CFG นำเสนอนั้นแตกต่างกันไปในแต่ละแอพพลิเคชั่น แอปพลิเคชั่นคอมพิวเตอร์บางตัวช่วยให้ผู้ใช้สามารถปรับเปลี่ยนหรือพัฒนาไวยากรณ์ไฟล์การกำหนดค่าโดยใช้การรบกวนทางกราฟิก ในขณะที่แอปพลิเคชั่นอื่น ๆ อนุญาตให้แก้ไขได้โดยใช้โปรแกรมแก้ไขข้อความเท่านั้น หลังจากแก้ไขไฟล์เหล่านี้แล้ว ผู้ใช้สามารถสั่งให้แอปพลิเคชันอ่านไฟล์เหล่านี้อีกครั้งและใช้การแก้ไขกับระบบ


## รูปแบบไฟล์ CFG ##

ไฟล์ CFG ได้รับการสนับสนุนโดยระบบปฏิบัติการต่างๆ เช่น ระบบปฏิบัติการ Unix และ Unix-like, MS-DOS, macOS, Microsoft Windows และ IBM OS/2 รูปแบบที่จัดเก็บไฟล์เหล่านี้และใช้ในแต่ละระบบปฏิบัติการจะแตกต่างกันไป ระบบส่วนใหญ่ใช้และจัดเก็บไฟล์เหล่านี้ในรูปแบบข้อความธรรมดาที่มนุษย์สามารถอ่านได้และแก้ไขได้ ขณะที่ระบบอื่นๆ จัดเก็บในรูปแบบที่ซับซ้อนมากขึ้น ทั้งนี้ขึ้นอยู่กับการใช้ไฟล์และความต้องการของระบบปฏิบัติการ

ในระบบปฏิบัติการ Unix และ Unix-like ไฟล์ CFG ส่วนใหญ่จะใช้สไตล์รูปแบบที่แตกต่างกันหลายรูปแบบสำหรับไฟล์ CFG อย่างไรก็ตาม รูปแบบที่พบมากที่สุดคือรูปแบบข้อความธรรมดาที่อ่านได้ง่าย และรูปแบบเกือบทั้งหมดอนุญาตให้แสดงความคิดเห็นและแก้ไขได้ นามสกุลไฟล์ที่พบบ่อยที่สุดสำหรับไฟล์ CFG ในระบบปฏิบัติการเหล่านี้คือ CNF, CONF, CF และ INI

ในระบบปฏิบัติการ MS-DOS เริ่มแรกมีรูปแบบไฟล์การกำหนดค่าเพียงรูปแบบเดียว ได้แก่ ข้อความธรรมดา อย่างไรก็ตาม MS-DOS 6 ได้นำรูปแบบไฟล์การกำหนดค่า INI มาใช้

macOS ใช้ไฟล์การกำหนดค่าสไตล์รูปแบบรายการคุณสมบัติมาตรฐาน

ใน Microsoft Windows ไฟล์การกำหนดค่าสไตล์ INI แบบข้อความล้วนเป็นแหล่งสำคัญในการจัดเก็บและแก้ไขข้อมูล อย่างไรก็ตาม ระบบฐานข้อมูลใหม่ถูกนำมาใช้ในปี 1993 ทำให้การใช้ไฟล์การกำหนดค่าใน Microsoft Windows ลดลงหลังปี 1993


## ตัวอย่าง CFG ##

ตัวอย่างไฟล์ CFG สามารถดูได้ด้านล่าง:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```
