{
  "date" : "2020-01-10",
  "keywords" :[ "ไฟล์ otg", "รูปแบบไฟล์ otg", "ไฟล์ otg คืออะไร", "ไฟล์", "ตัวอย่าง otg", "นามสกุลไฟล์ otg","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - รูปแบบไฟล์เทมเพลตการวาด OpenDocument",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ OTG และ API ที่สามารถสร้างและเปิดไฟล์ OTG",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## ไฟล์ OTG คืออะไร??

ไฟล์ OTG เป็นเทมเพลตการวาดที่สร้างขึ้นโดยใช้มาตรฐาน OpenDocument ซึ่งเป็นไปตาม OASIS Office Applications [ข้อกำหนด 1.0](http://www.oasis-open.org/ คณะกรรมการ/download.php/12572/OpenDocument-v1.0 -os.pdf). ซึ่งแสดงถึงการจัดระเบียบเริ่มต้นขององค์ประกอบการวาดสำหรับภาพเวกเตอร์ที่สามารถใช้เพื่อปรับปรุงเนื้อหาของไฟล์ให้ดียิ่งขึ้น ไฟล์ OTF นั้นเหมือนกับไฟล์รูปแบบ OpenDocument อื่นๆ ที่อิงตามรูปแบบ XML เพื่อแสดงเนื้อหาของเอกสาร สามารถดูไฟล์ OTF ได้โดยเปิดในโปรแกรมแก้ไขข้อความหรือ XML มาตรฐาน

## ข้อมูลจำเพาะรูปแบบไฟล์ OTG ##

รูปแบบไฟล์ OTG ขึ้นอยู่กับรูปแบบ OpenDocument XML ที่มีสคีมาที่ดี โครงสร้างของแต่ละคอมโพเนนต์ของรูปแบบ OpenDocument จะแสดงด้วยอิลิเมนต์ที่มีแอตทริบิวต์ที่เกี่ยวข้อง และเป็นเรื่องปกติสำหรับเอกสารทุกประเภท เช่น เอกสารข้อความ สเปรดชีต หรือไฟล์รูปวาด OTG ซึ่งเป็นเทมเพลตการวาดภาพใช้ข้อกำหนดเนื้อหากราฟิกอย่างกว้างขวางซึ่งรวมถึง:

* คุณสมบัติหน้าขั้นสูงสำหรับแอปพลิเคชันกราฟิก
* รูปร่างการวาด
* เฟรม
* รูปร่าง 3 มิติ
* รูปร่างที่กำหนดเอง
* รูปร่างการนำเสนอ
* ภาพเคลื่อนไหวการนำเสนอ
* ภาพเคลื่อนไหวการนำเสนอ SMIL
* เหตุการณ์การนำเสนอ
* นำเสนอฟิลด์ข้อความ
* เนื้อหาเอกสารการนำเสนอ

### คุณลักษณะของเพจที่ได้รับการปรับปรุงสำหรับแอปพลิเคชันกราฟิก ###
#### เอกสารแจกอาจารย์ ####

องค์ประกอบต้นแบบเอกสารประกอบคำบรรยายเป็นแม่แบบสำหรับสร้างหน้าเอกสารประกอบคำบรรยายโดยอัตโนมัติสำหรับแอปพลิเคชันที่รองรับการพิมพ์หน้าดังกล่าว
แอตทริบิวต์ที่อาจเชื่อมโยงกับ `<style:handout-master> ` องค์ประกอบคือ:

|เค้าโครง|แอตทริบิวต์|คำอธิบาย
---|---|---|
|เค้าโครงหน้าการนำเสนอ|การนำเสนอ:การนำเสนอ-หน้า-เค้าโครง-ชื่อ|ลิงก์ไปยัง `<style:presentation-page-layout> ` แอตทริบิวต์
|เค้าโครงหน้า|`สไตล์:ชื่อเค้าโครงหน้า` | ระบุเค้าโครงหน้าที่มีขนาด เส้นขอบ และการวางแนวของหน้าต้นแบบเอกสารประกอบคำบรรยาย
|สไตล์หน้า|`วาด:สไตล์-ชื่อ`|กำหนดแอตทริบิวต์การจัดรูปแบบเพิ่มเติมให้กับหน้าเอกสารประกอบคำบรรยายโดยกำหนดสไตล์หน้ารูปวาด|
|การประกาศส่วนหัว| `งานนำเสนอ:use-header-name`| ระบุชื่อของการประกาศฟิลด์ส่วนหัวที่ใช้สำหรับฟิลด์ส่วนหัวทั้งหมดที่แสดงในหน้าต้นแบบเอกสารประกอบคำบรรยาย
|การประกาศส่วนท้าย| งานนำเสนอ:ใช้ชื่อส่วนท้าย|ระบุชื่อของการประกาศฟิลด์ส่วนท้ายที่ใช้สำหรับฟิลด์ส่วนท้ายทั้งหมดที่แสดงบนหน้าต้นแบบเอกสารประกอบคำบรรยาย
|การประกาศวันที่และเวลา|ใช้ชื่อวันที่และเวลา|ระบุชื่อของการประกาศฟิลด์วันที่และเวลาที่ใช้สำหรับฟิลด์วันที่และเวลาทั้งหมดที่แสดงในหน้าต้นแบบเอกสารประกอบคำบรรยาย

### การวาดรูปร่าง ###
รูปแบบ OpenDocument รองรับรูปวาดหลายรูปแบบที่เอกสารประเภทใดก็ได้สามารถใช้ได้

|รูปร่าง|แอตทริบิวต์ที่เกี่ยวข้อง| องค์ประกอบ
---|---|---|
สี่เหลี่ยมผืนผ้า - `<draw:rect> `|ตำแหน่ง, ขนาด, ลักษณะ, เลเยอร์, ดัชนี Z, ID, รหัสคำบรรยาย, จุดยึดข้อความ, พื้นหลังตาราง, ตำแหน่งสิ้นสุดการวาด, มุมมน|ชื่อเรื่อง, คำอธิบายแบบยาว, Listener เหตุการณ์, จุดกาว, ข้อความ
บรรทัด `<draw:line> `|สไตล์, เลเยอร์, ดัชนี Z, ID, รหัสคำบรรยายและการแปลง, จุดยึดข้อความ, พื้นหลังตาราง, ตำแหน่งสิ้นสุดการวาด, จุดเริ่มต้น, จุดสิ้นสุด|ชื่อเรื่อง, คำอธิบายแบบยาว, Listener เหตุการณ์, จุดกาว, ข้อความ
โพลีไลน์ `<draw:polyline> `| ตำแหน่ง, ขนาด, กล่องมุมมอง, สไตล์, เลเยอร์, Z-Index, ID, Caption ID และการแปลง, สมอข้อความ, พื้นหลังตาราง, ตำแหน่งสิ้นสุดการวาด, จุด| ชื่อเรื่อง คำอธิบายแบบยาว ผู้ฟังเหตุการณ์ จุดกาว ข้อความ
รูปหลายเหลี่ยม `<draw:polygon> `|ตำแหน่ง, ขนาด, กล่องมุมมอง, สไตล์, เลเยอร์, ดัชนี Z, ID, ID คำบรรยายและการแปลง, สมอข้อความ, พื้นหลังตาราง, ตำแหน่งสิ้นสุดการวาด, จุด|ชื่อเรื่อง, คำอธิบายแบบยาว, Listener เหตุการณ์, จุดกาว, ข้อความ
|รูปหลายเหลี่ยมปกติ `<draw:regular-polygon> `|ตำแหน่ง, ขนาด, สไตล์, เลเยอร์, ดัชนี Z, ID, ID คำบรรยายและการแปลง, จุดยึดข้อความ, พื้นหลังตาราง, ตำแหน่งสิ้นสุดการวาด, ส่วนเว้า, มุม, ความคมชัด|ชื่อเรื่อง, คำอธิบายแบบยาว, Listener เหตุการณ์, จุดกาว, ข้อความ
|พาห์ท `<draw:path> `|ตำแหน่ง, ขนาด, กล่องมุมมอง, สไตล์, เลเยอร์, ดัชนี Z, ID, ID คำบรรยายและการแปลง, สมอข้อความ, พื้นหลังตาราง, ตำแหน่งสิ้นสุดการวาด, ข้อมูลพาธ| ชื่อเรื่อง คำอธิบายแบบยาว ผู้ฟังเหตุการณ์ จุดกาว ข้อความ

### กรอบ ###
กรอบในเอกสารรูปวาดคือภาชนะสี่เหลี่ยมที่มีกล่องข้อความ รูปภาพ หรือวัตถุ เฟรมรองรับคุณสมบัติเพิ่มเติม เช่น เส้นขอบ แผนที่รูปภาพ และไฮเปอร์ลิงก์ เฟรมอาจมีทั้งวัตถุและรูปภาพ ดังนั้นจึงทำให้มีการแสดงวัตถุได้หลายแบบ แอปพลิเคชันแสดงองค์ประกอบที่เกี่ยวข้องตามการสนับสนุนที่ดีที่สุด

เฟรมสามารถประกอบด้วย:
* กล่องข้อความ
* วัตถุที่แสดงในรูปแบบ OpenDocument หรือในรูปแบบไบนารีเฉพาะวัตถุ
* รูปภาพ
* แอปเพล็ต
* ปลั๊กอิน
* กรอบลอย

เฟรมอยู่ในเอกสารที่แสดงด้านล่าง

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>,
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## อ้างอิง ##
* [รูปแบบเอกสาร OASIS Open สำหรับแอปพลิเคชัน Office](https://www.oasis-open.org/ คณะกรรมการ/tc_home.php?wg_abbrev=office)
* [รูปแบบ OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
