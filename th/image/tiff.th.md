{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ tiff", "รูปแบบไฟล์ tiff", "ไฟล์ tiff คืออะไร", "ไฟล์", "ตัวอย่าง tiff", "นามสกุลไฟล์ tiff", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - รูปแบบไฟล์รูปภาพ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ TIFF และ API ที่สามารถสร้างและเปิดไฟล์ TIFF",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ TIFF คืออะไร??

TIFF หรือ TIF รูปแบบไฟล์รูปภาพที่ติดแท็ก แสดงถึงภาพแรสเตอร์ที่มีไว้สำหรับการใช้งานบนอุปกรณ์ต่างๆ ที่สอดคล้องกับมาตรฐานรูปแบบไฟล์นี้ สามารถอธิบายข้อมูลภาพสองระดับ ระดับสีเทา จานสี และสีเต็มในพื้นที่สีต่างๆ ได้ รองรับแผนการบีบอัดแบบ lossy และ lossless เพื่อเลือกระหว่างพื้นที่และเวลาสำหรับแอปพลิเคชันโดยใช้รูปแบบ รูปแบบไม่ขึ้นอยู่กับเครื่องและปราศจากขอบเขต เช่น โปรเซสเซอร์ ระบบปฏิบัติการ หรือระบบไฟล์

## ประวัติโดยย่อของรูปแบบไฟล์ TIFF

รูปแบบไฟล์ TIFF ถูกสร้างขึ้นครั้งแรกโดย Aldus Corporation ในฤดูใบไม้ร่วงปี 1986 หลังจากการประชุมหลายครั้งกับผู้ผลิตสแกนเนอร์และนักพัฒนาซอฟต์แวร์หลายราย วัตถุประสงค์หลักของรูปแบบไฟล์ TIFF คือเพื่อให้รูปแบบไฟล์ภาพที่สแกนทั่วไปสำหรับผู้จำหน่ายสแกนเนอร์เดสก์ท็อปทั้งหมด เริ่มต้นด้วยการสนับสนุนเฉพาะรูปแบบภาพไบนารี รูปแบบดังกล่าวได้พัฒนาเพื่อรองรับภาพโทนสีเทาและภาพสีเมื่อเวลาผ่านไป ข้อกำหนดรูปแบบไฟล์ TIFF เวอร์ชันเริ่มต้นสามารถระบุเป็น Reivision 3.0 ได้ เนื่องจากมีการเผยแพร่แบบร่างก่อนหน้านี้สองฉบับ Revision 5.0 ที่สำคัญได้รับการเผยแพร่ในปี 1988 ซึ่งเพิ่มการรองรับภาพสีจานสีและการบีบอัด LZW รูปแบบไฟล์ TIFF เวอร์ชันแก้ไข 6.0 ได้รับการเผยแพร่ในปี 1992 หลังจากนั้น ในปี พ.ศ. 2537 Adobe Systems ได้เข้าซื้อกิจการของ Aldus และตอนนี้ Adobe Systems สามารถเข้าถึงข้อมูลจำเพาะและดูแลรักษาได้

## ข้อมูลจำเพาะรูปแบบไฟล์ TIFF

รูปแบบไฟล์ TIFF สามารถขยายได้และผ่านการแก้ไขหลายครั้งซึ่งอนุญาตให้รวมข้อมูลส่วนตัวหรือข้อมูลเพื่อวัตถุประสงค์พิเศษได้ไม่จำกัดจำนวน ไฟล์ TIFF เริ่มต้นด้วยส่วนหัว 8 ไบต์ โดยที่ไบต์เป็นตัวเลขตั้งแต่ 0 ถึง N ไฟล์ TIFF ที่ใหญ่ที่สุดที่เป็นไปได้คือความยาว 2**32 ไบต์ ไฟล์เริ่มต้นด้วยส่วนหัวของไฟล์รูปภาพขนาด 8 ไบต์ที่ชี้ไปยังไฟล์รูปภาพโดยตรง (IFD) IFD มีข้อมูลเกี่ยวกับภาพรวมทั้งตัวชี้ไปยังข้อมูลภาพจริง

### ส่วนหัวของไฟล์ TIFF

ส่วนหัวของไฟล์ TIFF ขนาด 8 ไบต์ประกอบด้วยข้อมูลต่อไปนี้:

**ไบต์ 0-1:** ลำดับไบต์ที่ใช้ภายในไฟล์ ค่าทางกฎหมายคือ: “II”(4949.H)“MM” (4D4D.H)

ในรูปแบบ "II" ลำดับไบต์จะเรียงจากไบต์ที่มีนัยสำคัญน้อยที่สุดไปยังไบต์ที่มีนัยสำคัญที่สุดเสมอ สำหรับจำนวนเต็มทั้งแบบ 16 บิตและ 32 บิต ซึ่งเรียกว่าลำดับไบต์แบบ little-endian ในรูปแบบ "MM" ลำดับไบต์จะเรียงจากนัยสำคัญมากที่สุดไปยังนัยสำคัญน้อยที่สุดเสมอ สำหรับจำนวนเต็มทั้งแบบ 16 บิตและ 32 บิต สิ่งนี้เรียกว่าลำดับไบต์ขนาดใหญ่

**ไบต์ 2-3:** หมายเลขตามอำเภอใจแต่เลือกอย่างระมัดระวัง (42) ซึ่งจะระบุไฟล์เพิ่มเติมว่าเป็นไฟล์ TIFF ลำดับไบต์ขึ้นอยู่กับค่าของไบต์ 0-1

**ไบต์ 4-7:** ออฟเซ็ต (เป็นไบต์) ของ IFD แรก ไดเร็กทอรีอาจอยู่ที่ตำแหน่งใดก็ได้ในไฟล์หลังส่วนหัว แต่ต้องเริ่มต้นที่ขอบเขตของคำ โดยเฉพาะอย่างยิ่ง Image File Directory อาจเป็นไปตามข้อมูลรูปภาพที่อธิบายไว้ ผู้อ่านต้องปฏิบัติตามตัวชี้ไม่ว่าจะนำไปสู่ที่ใดก็ตาม คำว่า ออฟเซ็ต ไบต์ ใช้ในเอกสารนี้เสมอเพื่ออ้างถึงตำแหน่งในส่วนที่เกี่ยวกับจุดเริ่มต้นของไฟล์ TIFF ไบต์แรกของไฟล์มีออฟเซ็ตเป็น 0

### ไดเร็กทอรีไฟล์รูปภาพ

IFD มีข้อมูลเกี่ยวกับรูปภาพและตัวชี้ไปยังข้อมูลรูปภาพจริง ประกอบด้วยจำนวน 2 ไบต์ของจำนวนรายการไดเร็กทอรี (เช่น จำนวนฟิลด์) ตามด้วยลำดับของรายการฟิลด์ 12 ไบต์ ตามด้วยออฟเซ็ต 4 ไบต์ของ IFD ถัดไป (หรือ 0 ถ้าไม่มี) ต้องมีอย่างน้อย 1 IFD ในไฟล์ TIFF และแต่ละ IFD ต้องมีอย่างน้อยหนึ่งรายการ

#### รายการ IFD

รายการ IFD ขนาด 12 ไบต์แต่ละรายการอยู่ในรูปแบบต่อไปนี้


|ไบต์|คำอธิบาย
---|---|
|0-1|แท็กที่ระบุฟิลด์
|2-3|ประเภทฟิลด์
|4-7|จำนวนประเภทที่ระบุ
|8-11|การชดเชยค่า การชดเชยไฟล์ (เป็นไบต์) ของค่าสำหรับฟิลด์ ค่านี้คาดว่าจะเริ่มต้นที่ขอบเขตของคำ การชดเชยมูลค่าที่สอดคล้องกันจะเป็นเลขคู่ การชดเชยไฟล์นี้อาจชี้ไปที่ใดก็ได้ในไฟล์ แม้ว่าจะอยู่หลังข้อมูลรูปภาพก็ตาม

ฟิลด์ TIFF เป็นเอนทิตีเชิงตรรกะที่ประกอบด้วยแท็ก TIFF และค่าของแท็ก แนวคิดเชิงตรรกะนี้ถูกนำมาใช้เป็นรายการ IFD บวกกับค่าจริงหากไม่พอดีกับส่วนค่า/ออฟเซ็ต 4 ไบต์สุดท้ายของรายการ IFD ฟิลด์เงื่อนไข TIFF และรายการ IFD สามารถใช้แทนกันได้ในบริบทส่วนใหญ่

### พื้นฐาน TIFF ###

Baseline TIFF เป็นแกนหลักของ TIFF ซึ่งเป็นสิ่งจำเป็นที่นักพัฒนา TIFF กระแสหลักทุกคนควรสนับสนุนในผลิตภัณฑ์ของตน ความสอดคล้องกับรูปแบบ TIFF ขึ้นอยู่กับการปฏิบัติตามข้อกำหนด Baseline TIFF ข้อกำหนดเหล่านี้ได้รับการบันทึกไว้อย่างดีในเอกสารข้อกำหนด 6.0

#### หลายภาพต่อไฟล์ ####

อาจมี IFD มากกว่าหนึ่งรายการในไฟล์ TIFF แต่ละ IFD กำหนดไฟล์ย่อย การใช้ไฟล์ย่อยที่เป็นไปได้ประการหนึ่งคือการอธิบายรูปภาพที่เกี่ยวข้อง เช่น หน้าของการส่งโทรสาร ตัวอ่าน TIFF พื้นฐานไม่จำเป็นต้องอ่าน IFD ใดๆ นอกเหนือจากตัวแรก

#### ประเภทรูปภาพ ####

รูปภาพ TIFF พื้นฐานมีประเภทดังต่อไปนี้:

**Bilevel:** ภาพ Bilevel มีสองสี ได้แก่ ขาวดำ TIFF อนุญาตให้แอปพลิเคชันเขียนข้อมูลสองระดับในรูปแบบสีขาวเป็นศูนย์หรือสีดำเป็นศูนย์ ช่องที่บันทึกข้อมูลนี้เรียกว่า **PhotometricInterpretation**

* RGB สีเต็มรูปแบบ

ข้อมูลการตีความโฟโตเมตริกสำหรับภาพ Bilevel มีดังนี้:

แท็ก = 262 (106.H)
ประเภท = สั้น
**ค่า**

|ค่า|คำอธิบาย|
---|---|
|0|สำหรับภาพระดับสองระดับและระดับสีเทา: 0 เป็นภาพสีขาว ค่าสูงสุดจะถูกแสดงเป็นสีดำ นี่คือค่าปกติสำหรับ Compression#2|
|1|BlackIsZero. สำหรับภาพสองระดับและระดับสีเทา: 0 เป็นภาพสีดำ ค่าสูงสุดจะแสดงเป็นสีขาว หากระบุค่านี้สำหรับ Compression#2 รูปภาพควรแสดงและพิมพ์กลับด้าน|

**สเกลสีเทา:** รูปภาพสเกลสีเทาคือภาพรวมของรูปภาพสองระดับ ภาพสองระดับสามารถเก็บได้เฉพาะข้อมูลภาพขาวดำ แต่ภาพระดับสีเทาสามารถเก็บเฉดสีเทาได้เช่นกัน เพื่ออธิบายรูปภาพดังกล่าว คุณต้องเพิ่มหรือเปลี่ยนฟิลด์ต่อไปนี้ ฟิลด์บังคับอื่นๆ จะเหมือนกับฟิลด์ที่จำเป็นสำหรับภาพระดับสอง สำหรับรูปภาพระดับสีเทา การบีบอัด # 1 หรือ 32773 (PackBits) ใน Baseline TIFF รูปภาพระดับสีเทาสามารถจัดเก็บเป็นข้อมูลที่ไม่บีบอัดหรือบีบอัดด้วยอัลกอริทึม PackBits

ข้อมูล **BitsPerSample** สำหรับภาพระดับสีเทามีดังนี้:

แท็ก = 258 (102.H)
ประเภท = สั้น

จำนวนบิตต่อคอมโพเนนต์ค่าที่อนุญาตสำหรับรูปภาพระดับสีเทา TIFF พื้นฐานคือ 4 และ 8 ทำให้มีเฉดสีเทาที่แตกต่างกันอย่างใดอย่างหนึ่ง 16 หรือ 256 เฉด

**จานสี:** ภาพจานสีจะคล้ายกับภาพระดับสีเทา พวกเขายังคงมีหนึ่งองค์ประกอบต่อพิกเซล แต่ค่าองค์ประกอบจะถูกใช้เป็นดัชนีในตารางการค้นหา RGB แบบเต็ม หากต้องการอธิบายภาพดังกล่าว คุณต้องเพิ่มหรือเปลี่ยนฟิลด์ต่อไปนี้ ฟิลด์บังคับอื่นๆ จะเหมือนกับฟิลด์สำหรับภาพโทนสีเทา
ข้อมูลการตีความโฟโตเมตริกสำหรับภาพ Palette-Color มีดังนี้:

PhotometricInterpretation = 3 (สีจานสี)
ColorMapTag = 320 (140.H)
ประเภท = สั้น
N = 3 * (2 บิตต่อตัวอย่าง)

ฟิลด์นี้กำหนดแมปสีสีแดง-เขียว-น้ำเงิน (มักเรียกว่าตารางค้นหา) สำหรับภาพชุดสี ในภาพจานสี ค่าพิกเซลถูกใช้เพื่อจัดทำดัชนีลงในตารางการค้นหา RGB ตัวอย่างเช่น พิกเซลจานสีที่มีค่าเป็น 0 จะแสดงตามค่าสามสีแดง เขียว น้ำเงินตัวที่ 0 ใน TIFF ColorMap ค่าสีแดงทั้งหมดมาก่อน ตามด้วยค่าสีเขียว จากนั้นค่าสีน้ำเงิน ใน ColorMap สีดำแทนด้วย 0,0,0 และสีขาวแทนด้วย 65535, 65535, 65535

**RGB full-color:** ในภาพ RGB แต่ละพิกเซลประกอบด้วยสามองค์ประกอบ: สีแดง สีเขียว และสีน้ำเงิน ไม่มี ColorMap ในการอธิบายภาพ RGB คุณต้องเพิ่มหรือเปลี่ยนฟิลด์และค่าต่อไปนี้ ฟิลด์บังคับอื่นๆ จะเหมือนกับฟิลด์ที่จำเป็นสำหรับภาพจานสี

BitsPerSample = 8,8,8 แต่ละส่วนประกอบมีความลึก 8 บิตในรูปภาพ Baseline TIFF RGB

PhotometricInterpretation = 2 (RGB) และไม่มี ColorMap

แท็ก = 277 (115.H)
ประเภท = สั้น
จำนวนส่วนประกอบต่อพิกเซล หมายเลขนี้คือ 3 สำหรับภาพ RGB เว้นแต่จะมีตัวอย่างเพิ่มเติม

## อ้างอิง ##

* [รูปแบบไฟล์ TIFF - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

