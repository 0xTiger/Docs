{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ obj", "รูปแบบไฟล์ obj", "ไฟล์ obj คืออะไร", "ไฟล์", "ตัวอย่าง obj", "นามสกุลไฟล์ obj", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ OBJ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ OBJ และ API ที่สามารถเปิดและสร้างไฟล์ OBJ",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ OBJ คืออะไร??

ไฟล์ **OBJ** ถูกใช้โดยแอปพลิเคชัน Advanced Visualizer ของ Wavefront เพื่อกำหนดและจัดเก็บวัตถุรูปทรงเรขาคณิต การส่งข้อมูลเรขาคณิตย้อนหลังและไปข้างหน้าสามารถทำได้ผ่านไฟล์ OBJ รูปแบบ OBJ รองรับทั้งรูปทรงหลายเหลี่ยม เช่น จุด เส้น จุดพื้นผิว ใบหน้า และรูปทรงอิสระ (เส้นโค้งและพื้นผิว) รูปแบบนี้ไม่รองรับภาพเคลื่อนไหวหรือข้อมูลเกี่ยวกับแสงและตำแหน่งของฉาก

ไฟล์ OBJ มักจะเป็นผลิตภัณฑ์สุดท้ายของกระบวนการสร้างแบบจำลอง 3 มิติที่สร้างโดย CAD (การออกแบบโดยใช้คอมพิวเตอร์ช่วย) ลำดับเริ่มต้นในการจัดเก็บจุดยอดคือทวนเข็มนาฬิกาเพื่อหลีกเลี่ยงการประกาศ face normals อย่างชัดเจน แม้ว่าไฟล์ OBJ จะประกาศข้อมูลมาตราส่วนในบรรทัดความคิดเห็น แต่ยังไม่มีการประกาศหน่วยสำหรับพิกัด OBJ

## ประวัติของรูปแบบ 3D OBJ

Wavefront Technologies สร้างรูปแบบไฟล์ OBJ สำหรับแอปพลิเคชัน Advanced Visualizer เพื่อจัดเก็บวัตถุทางเรขาคณิตและข้อมูล 3 มิติ เวอร์ชัน 2.11 ถูกแทนที่ด้วยเวอร์ชัน 3 ที่ได้รับการจัดทำเอกสารใหม่ รูปแบบไฟล์เป็นแบบเปิดและได้นำไปใช้โดยผู้จำหน่ายรายอื่นสำหรับแอปพลิเคชันกราฟิก 3 มิติของตน Wavefront Technologies เก็บรูปแบบไฟล์นี้ไว้เป็นโอเพ่นซอร์สและเป็นกลาง

## รูปแบบไฟล์ OBJ

ในวัตถุ 3 มิติ การเข้ารหัสรูปทรงเรขาคณิตพื้นผิวเป็นงานที่ท้าทายซึ่งรูปแบบไฟล์ OBJ ทำได้ดีมาก รูปแบบนี้ค่อนข้างหลากหลายเนื่องจากมีตัวเลือกมากมายในการเข้ารหัสรูปทรงเรขาคณิตของพื้นผิว ต่อไปนี้เป็นรูปแบบที่อนุญาตสามรูปแบบซึ่งมีข้อดีและข้อเสียในตัวเอง:

### Tessellation กับใบหน้าหลายเหลี่ยม

รูปแบบไฟล์ OBJ ช่วยให้ผู้ใช้สามารถทดสอบพื้นผิวแบบจำลอง 3 มิติโดยใช้รูปทรงเรขาคณิตที่เรียบง่ายหรือซับซ้อน สำหรับการเข้ารหัสรูปทรงเรขาคณิตพื้นผิวของแบบจำลอง ไฟล์จะจัดเก็บจุดยอดและค่าปกติสำหรับแต่ละรูปหลายเหลี่ยม แม้ว่าเทสเซลเลชันจะเพิ่มความหยาบให้กับโมเดล แต่ก็จำเป็นต้องค้นหาสมดุลที่ถูกต้องระหว่างขนาดของไฟล์และคุณภาพการพิมพ์

### เส้นโค้งรูปแบบอิสระ

รูปแบบไฟล์ OBJ อนุญาตให้ผู้ใช้กำหนดเส้นโค้งพื้นผิวรูปแบบอิสระเพื่อระบุรูปทรงเรขาคณิตพื้นผิวของแบบจำลอง เนื่องจากเส้นโค้งรูปแบบอิสระมีความซับซ้อนมากกว่าพื้นผิวหลายเหลี่ยม เนื่องจากด้วยพารามิเตอร์ทางคณิตศาสตร์เพียงเล็กน้อย เส้นโค้งจึงสามารถกำหนดได้ดีที่สุดโดยเส้นโค้งรูปแบบอิสระ ดังนั้น ด้วยข้อมูลที่น้อยกว่าเมื่อเทียบกับเทสเซลเลชันแบบหลายเหลี่ยม เส้นโค้งรูปแบบอิสระจึงใช้เพื่อสร้างการเข้ารหัสคุณภาพสูงของโมเดล 3 มิติใดๆ โดยไม่ต้องขยายขนาดไฟล์

### พื้นผิวรูปทรงอิสระ

รูปแบบไฟล์ OBJ ยังระบุการเรียงต่อกันของรูปทรงเรขาคณิตพื้นผิวด้วยแพตช์พื้นผิวรูปแบบอิสระ แผ่นแปะพื้นผิวรูปทรงอิสระ (NURBS) ชนิดนี้เหมาะมากสำหรับพื้นผิวที่ไม่มีมิติแนวรัศมีที่ตายตัว เช่น ตัวรถบรรทุก ปีกของเฮลิคอปเตอร์ หรือตัวเรือ การใช้พื้นผิวรูปทรงอิสระมีข้อได้เปรียบอย่างมาก เนื่องจากมีความแม่นยำมากขึ้นในการทำให้ขนาดไฟล์เล็กลงด้วยความแม่นยำสูง พื้นผิวเหล่านี้เป็นส่วนสำคัญของอุตสาหกรรมการบินและอวกาศและยานยนต์ซึ่งความแม่นยำต่ำเป็นสิ่งที่ไม่อาจคาดเดาได้

คำหลักต่อไปนี้จัดเรียงตามประเภทข้อมูลเพื่อกำหนดรูปทรงพื้นผิว


|องค์ประกอบ|ข้อความแสดงเส้นโค้งรูปแบบอิสระ/พื้นผิวของตัวเครื่อง|แอตทริบิวต์เส้นโค้งรูปแบบอิสระ/พื้นผิว
---|---|---|
|p|Point|parm|ค่าพารามิเตอร์|deg|Degree
|l|เส้น|ทริม|วงรอบการตัดแต่งภายนอก|bmat|เมทริกซ์พื้นฐาน
|f|ผิวหน้า|รู|วงเล็มด้านใน|ขั้นตอน|ขนาดขั้นบันได
|curv|Curve|scrv|เส้นโค้งพิเศษ|cstype|เส้นโค้งหรือพื้นผิว
|curv2|เส้นโค้ง 2 มิติ|sp|จุดพิเศษ|**การเชื่อมต่อและการจัดกลุ่มพื้นผิว**
|surf|Surface|end|End statement|con|connect
|**แสดง/แสดงแอตทริบิวต์**|g|ชื่อกลุ่ม
|bevel|การเอียงเอียง|shadow_obj|การหล่อเงา|s|กลุ่มการปรับให้เรียบ
|lod|ระดับรายละเอียด|trace_obj|Ray tracing|mg|Merging group
|d_interp|ละลายการแก้ไข|ctech|เทคนิคการประมาณเส้นโค้ง|o|ชื่อวัตถุ
|c_interp|การแก้ไขสี|stech|เทคนิคการประมาณพื้นผิว|
|usemtl|ชื่อวัสดุ|mtllib|ไลบรารีวัสดุ|
|**จุดยอดทางเรขาคณิต**|
|v|จุดยอดทางเรขาคณิต|vn|จุดยอดปกติ|
|vt|จุดยอดของพื้นผิว|vp|จุดยอดของพารามิเตอร์สเปซ|

### สีและพื้นผิว

ไฟล์ OBJ อนุญาตให้เก็บข้อมูลสีและพื้นผิวในรูปแบบไฟล์ที่เกี่ยวข้องซึ่งเรียกว่า Material Template Library (MTL) โมเดลเรขาคณิตหลายสีเรนเดอร์โดยใช้สองไฟล์นี้ร่วมกัน ไฟล์ MTL เป็นแบบ ASCII และอำนวยความสะดวกในการแสดงผลด้วยคอมพิวเตอร์โดยอธิบายคุณสมบัติการสะท้อนแสงของพื้นผิวโดยใช้แบบจำลองของการสะท้อนของฟอง มาตรฐานนี้ถูกนำมาใช้โดยผู้จำหน่ายซอฟต์แวร์จำนวนมากที่ใช้ประโยชน์จากการแลกเปลี่ยนวัสดุ รูปแบบ MTL ล้าสมัยเล็กน้อยเนื่องจากไม่รองรับเทคโนโลยีล่าสุด เช่น แผนที่สเปกกูลาร์และพารัลแลกซ์

## อ้างอิง

* [ไฟล์ Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

