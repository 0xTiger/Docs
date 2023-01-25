{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ gif", "รูปแบบไฟล์ gif", "ไฟล์ gif คืออะไร", "ไฟล์", "ตัวอย่าง gif", "นามสกุลไฟล์ gif","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - รูปแบบไฟล์รูปภาพ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ GIF และ API ที่สามารถสร้างและเปิดไฟล์ GIF",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ GIF คืออะไร? ##

GIF หรือรูปแบบการแลกเปลี่ยนกราฟิกคือประเภทของภาพที่มีการบีบอัดสูง GIF ที่เป็นของ Unisys ใช้อัลกอริธึมการบีบอัด LZW ที่ไม่ทำให้คุณภาพของภาพลดลง สำหรับแต่ละภาพ GIF โดยทั่วไปจะอนุญาตให้มีได้สูงสุด 8 บิตต่อพิกเซล และอนุญาตให้ใช้สีได้สูงสุด 256 สีทั่วทั้งภาพ ตรงกันข้ามกับภาพ [JPEG](/th/image/jpeg/) ซึ่งสามารถแสดงสีได้มากถึง 16 ล้านสีและค่อนข้างจะเกินขีดจำกัดของสายตามนุษย์ ย้อนกลับไปเมื่ออินเทอร์เน็ตเกิดขึ้น GIF ยังคงเป็นตัวเลือกที่ดีที่สุดเนื่องจากต้องใช้แบนด์วิธต่ำและเข้ากันได้กับกราฟิกที่ใช้พื้นที่สีทึบ GIF แบบเคลื่อนไหวจะรวมภาพหรือเฟรมจำนวนมากไว้ในไฟล์เดียวและแสดงตามลำดับเพื่อสร้างคลิปภาพเคลื่อนไหวหรือวิดีโอสั้นๆ ข้อจำกัดของสีมีมากถึง 256 สำหรับแต่ละเฟรม และมีแนวโน้มว่าจะเหมาะสมน้อยที่สุดสำหรับการสร้างภาพและภาพถ่ายอื่นที่มีการไล่ระดับสี

## รูปแบบไฟล์ GIF ##

ตามแนวคิดแล้ว ไฟล์ GIF มีพื้นที่กราฟิกขนาดคงที่ซึ่งเต็มไปด้วยรูปภาพตั้งแต่ศูนย์ขึ้นไป ไฟล์ GIF บางไฟล์จะแบ่งพื้นที่กราฟิกขนาดคงที่หรือบล็อกเป็นภาพย่อยที่สามารถทำงานเป็นเฟรมภาพเคลื่อนไหวได้ในกรณีของ GIF แบบเคลื่อนไหว รูปแบบ GIF ใช้ความลึกของพิกเซลตั้งแต่ 1 ถึง 8 บิตเพื่อจัดเก็บข้อมูลบิตแมป โมเดลสี RGB และข้อมูลจานสีจะถูกใช้เพื่อเก็บภาพเสมอ ส่วนหัวที่มีความยาวคงที่ ("GIF87a" หรือ "GIF89a") กำหนดจุดเริ่มต้นของไฟล์ GIF ทั่วไป ทั้งนี้ขึ้นอยู่กับเวอร์ชัน

ปัจจุบัน GIF มี 2 เวอร์ชัน ได้แก่ 87a และ 89a รูปแบบแรกเป็นรูปแบบ GIF ดั้งเดิม ส่วนรูปแบบหลังเป็นรูปแบบ GIF ใหม่ ในรูปแบบไฟล์นี้ ลักษณะของบล็อกและขนาดพิกเซลจะกล่าวถึงใน Logical Screen Descriptor ที่มีความยาวคงที่ การมีอยู่และขนาดของ Global Color Table อาจระบุโดยคำอธิบายหน้าจอ ซึ่งจะติดตามรายละเอียดเพิ่มเติมหากมี ตัวอย่างคือไบต์สุดท้ายของไฟล์ที่มีเครื่องหมายอัฒภาค ASCII หนึ่งไบต์ รูปแบบไฟล์ GIF87a ทั่วไปมีดังนี้:

### หัวข้อ ###

ส่วนหัวมีหกไบต์และใช้เพื่อระบุประเภทของไฟล์เป็น GIF แม้ว่า Logical Screen Descriptor จะแยกออกจากส่วนหัวจริง แต่บางครั้งก็ถือว่าเป็นส่วนหัวที่สอง โครงสร้างเดียวกันซึ่งใช้ในการจัดเก็บส่วนหัวอาจจัดเก็บ Logical Screen Descriptor ไฟล์ GIF ทั้งหมดเริ่มต้นด้วยลายเซ็น 3 ไบต์และใช้อักขระ "GIF" เป็นตัวระบุ เวอร์ชันนี้ยังมีขนาดสามไบต์และประกาศเวอร์ชันของไฟล์ GIF

### คำอธิบายหน้าจอตรรกะ ###

Image Descriptor ที่มีความยาวคงที่จะระบุหน้าจอและข้อมูลสีที่จำเป็นในการสร้างภาพ GIF ฟิลด์ ความสูง และ ความกว้าง ล้อมรอบค่าที่น้อยที่สุดของความละเอียดหน้าจอ ซึ่งจำเป็นต้องแสดงข้อมูลรูปภาพ หากอุปกรณ์แสดงผลไม่สามารถแสดงความละเอียดที่ระบุได้ จำเป็นต้องปรับขนาดเพื่อให้แสดงภาพได้อย่างเหมาะสม หน้าจอและข้อมูลแผนที่สีแสดงโดยสี่ฟิลด์ย่อยของตารางด้านล่าง (ในขณะที่บิต 0 เป็นบิตที่มีนัยสำคัญน้อยที่สุด):


|บิต|ฟิลด์ย่อย
---|---|
|0-2|ขนาดของตาราง Global Color
|3|ค่าสถานะการเรียงตารางสี
|4-6|ความละเอียดของสี
|7|ธงตารางสีสากล

#### ตารางสีสากล ####

ตาราง Global Color ที่เป็นทางเลือกจะถูกวางไว้ต่อจาก Logical Screen Descriptor ตารางนี้แมปเพื่อจัดทำดัชนีข้อมูลสีของพิกเซลภายในข้อมูลภาพ ในกรณีที่ไม่มี Global Color Table แต่ละภาพในไฟล์ GIF จะใช้ Local Colour เป็นการดีกว่าที่จะจัดหาตารางสีเริ่มต้นหากไม่มีทั้ง Global และ Local Colour Table ชุดสามไบต์สามชุดประกอบด้วยองค์ประกอบของตารางสี แต่ละไบต์แสดงลักษณะของค่าสี RGB สีแดง เขียว และน้ำเงินถูกใช้เป็นค่าขององค์ประกอบตารางสีแต่ละรายการ รายการในตารางสีร่วมมีค่าสูงสุด 256 รายการและแสดงด้วยกำลังสองเสมอ

#### ข้อมูลรูปภาพ ####

ข้อมูลรูปภาพจัดเก็บสัญลักษณ์ที่ไม่ได้เข้ารหัสหนึ่งไบต์ ตามด้วยรายการลิงก์ย่อยพร้อมกับข้อมูลที่เข้ารหัส LZW

#### ตัวอย่าง ####

ตัวอย่างแสดงข้อมูลหนึ่งไบต์ที่เป็นอักขระตัวสุดท้ายในไฟล์ ค่าของไบต์นี้คือ 3Bh อย่างถาวรและระบุจุดสิ้นสุดของสตรีมข้อมูล ไฟล์ GIF ทุกไฟล์ต้องมีตัวอย่างในไฟล์สุดท้ายของแต่ละไฟล์

## อ้างอิง ##

* [รูปแบบไฟล์ GIF](https://en.wikipedia.org/wiki/GIF)
