{
"วันที่": "11-10-2023",
   "keywords":[
"ชร์",
"ไฟล์ chr",
"ไฟล์อักขระ ch cryengine",
"วิธีการเปิดไฟล์ ch",
"ไฟล์",
"นามสกุลไฟล์ chr",
"ส่วนขยาย",
"ไฟล์"
],
   "author":{
"display_name":"ชาคีล ไฟซ์"
},
"draft": "false",
"toc":true,
"title": "รูปแบบไฟล์ CHR - ไฟล์อักขระ CryENGINE ",
   "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์อักขระ CHR CryENGINE และ API ที่สามารถสร้างและเปิดไฟล์ CHR",
"linktitle": "CHR CryENGINE ",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## ไฟล์ CHR คืออะไร??

ไฟล์ CHR ในบริบทของ CryENGINE อ้างถึง **ไฟล์อักขระ CryENGINE** CryENGINE เป็นเอ็นจิ้นเกมที่พัฒนาโดย Crytek และไฟล์เหล่านี้ใช้สำหรับจัดเก็บโมเดลตัวละครและข้อมูลที่เกี่ยวข้องเพื่อใช้ในวิดีโอเกมและแอปพลิเคชันเรียลไทม์อื่น ๆ

## ไฟล์อักขระ CryENGINE

โดยทั่วไปไฟล์อักขระ CryENGINE จะมีส่วนประกอบดังต่อไปนี้:

1. **โมเดลตัวละคร**: นี่คือโมเดล 3 มิติของตัวละคร รวมถึงรูปทรงเรขาคณิต พื้นผิว และแอนิเมชั่น โมเดลเหล่านี้มักสร้างขึ้นโดยใช้ซอฟต์แวร์เช่น Autodesk Maya หรือ Blender จากนั้นนำเข้าสู่ CryENGINE
    




















2. **ข้อมูลแอนิเมชั่น**: CryENGINE รองรับแอนิเมชั่นที่ซับซ้อนสำหรับตัวละคร ดังนั้นไฟล์ ".chr" จึงอาจมีแอนิเมชั่นต่างๆ เช่น การเดิน การวิ่ง การกระโดด และอื่นๆ โดยทั่วไปภาพเคลื่อนไหวเหล่านี้จะถูกจัดเก็บเป็นข้อมูลคีย์เฟรม
    




















3. **ข้อมูลการริกกิ้ง**: การริกกิ้งหมายถึงกระบวนการสร้างโครงสร้างโครงกระดูกสำหรับโมเดลตัวละคร ซึ่งช่วยให้สามารถนำแอนิเมชั่นไปใช้กับโมเดลได้ ไฟล์ ".chr" อาจมีข้อมูลเกี่ยวกับลำดับชั้นของกระดูกและวิธีเชื่อมต่อเมชของตัวละครกับโครงกระดูกนี้
    




















4. **ข้อมูลวัสดุและพื้นผิว**: ข้อมูลเกี่ยวกับวัสดุที่ใช้ในโมเดลตัวละครและแผนที่พื้นผิวที่เกี่ยวข้องอาจรวมอยู่ในไฟล์ ".chr" CryENGINE รองรับการเรนเดอร์ตามสภาพร่างกาย ดังนั้นวัสดุเหล่านี้จึงมีรายละเอียดค่อนข้างมาก
    




















5. **ข้อมูลฟิสิกส์**: หากตัวละครมีจุดประสงค์เพื่อโต้ตอบกับโลกของเกม ไฟล์ ".chr" อาจมีข้อมูลฟิสิกส์ เช่น รูปร่างการชนกัน หรือข้อจำกัดสำหรับฟิสิกส์แร็กดอลล์
    




















6. **การตั้งค่าการกำหนดค่า**: การตั้งค่าต่างๆ ที่เกี่ยวข้องกับพฤติกรรมของตัวละครในโลกของเกม เช่น พฤติกรรมของ AI หรือเหตุการณ์ที่มีสคริปต์ อาจเป็นส่วนหนึ่งของไฟล์ ".chr" ด้วย

## ร้องไห้ENGINE

CryENGINE คือเอ็นจิ้นเกมอันทรงพลังที่พัฒนาโดย Crytek บริษัทวิดีโอเกมสัญชาติเยอรมัน เป็นที่รู้จักในด้านความสามารถด้านกราฟิกที่ล้ำสมัยและถูกนำมาใช้เพื่อสร้างวิดีโอเกมที่มีภาพสวยงามและมีเทคโนโลยีขั้นสูง นี่คือคุณสมบัติและข้อมูลหลักบางประการเกี่ยวกับ CryENGINE:

1. **กราฟิกและการเรนเดอร์**: CryENGINE มีชื่อเสียงในด้านความสามารถด้านกราฟิกขั้นสูง รองรับคุณสมบัติต่างๆ เช่น การส่องสว่างทั่วโลกแบบเรียลไทม์ แสงและเงาไดนามิกคุณภาพสูง การเรนเดอร์ตามทางกายภาพ (PBR) และพื้นผิวที่มีความละเอียดสูง คุณสมบัติเหล่านี้มีส่วนช่วยในการสร้างโลกของเกมที่สวยงามและสมจริง
    




















2. **กลไกฟิสิกส์**: CryENGINE มีกลไกฟิสิกส์ในตัวที่ให้การโต้ตอบที่สมจริงระหว่างวัตถุในโลกของเกม รองรับฟีเจอร์ต่างๆ เช่น ฟิสิกส์ของวัตถุแข็ง ฟิสิกส์ของวัตถุอ่อน และฟิสิกส์ของแร็กดอล ทำให้เหมาะสำหรับการสร้างสภาพแวดล้อมแบบไดนามิกและสมจริง
    




















3. **ภูมิประเทศและพืชพรรณ**: CryENGINE มอบเครื่องมือสำหรับการสร้างสภาพแวดล้อมกลางแจ้งที่กว้างใหญ่และมีรายละเอียด รองรับการแก้ไขภูมิประเทศ การวางตำแหน่งพืชพรรณ และระบบสภาพอากาศแบบไดนามิก ช่วยให้นักพัฒนาสามารถสร้างฉากกลางแจ้งที่กว้างขวางและสมจริง
    




















4. **แอนิเมชั่นตัวละคร**: CryENGINE มีเครื่องมือที่มีประสิทธิภาพสำหรับแอนิเมชั่นตัวละคร รองรับการสร้างตัวละครที่ซับซ้อน แอนิเมชั่นบนใบหน้า และระบบผสมผสานต้นไม้ที่ช่วยให้นักพัฒนาสามารถสร้างการเคลื่อนไหวของตัวละครและแอนิเมชั่นที่เหมือนจริงได้
    




















5. **ระบบ AI**: เอ็นจิ้นมีระบบ AI ที่ช่วยให้สามารถสร้าง NPC อัจฉริยะ (ตัวละครที่ไม่ใช่ผู้เล่น) และ AI ของศัตรู นักพัฒนาสามารถเขียนสคริปต์พฤติกรรมและการโต้ตอบของ AI เพื่อสร้างประสบการณ์การเล่นเกมที่ท้าทายและดื่มด่ำ
       





















6. **การเขียนสคริปต์**: CryENGINE ใช้ภาษาสคริปต์ที่เรียกว่า "Schematyc" ซึ่งช่วยให้นักพัฒนาสามารถสร้างตรรกะในการเล่นเกมและการโต้ตอบได้ นอกจากนี้ยังรองรับ C++ สำหรับความต้องการด้านการเขียนโปรแกรมขั้นสูงอีกด้วย

## รูปแบบไฟล์ที่ใช้โดย CryENGINE

ต่อไปนี้เป็นไฟล์ประเภททั่วไปบางส่วนที่เกี่ยวข้องกับ CryENGINE:

1. **cryproj**: ไฟล์โครงการ CryENGINE ไฟล์เหล่านี้จัดเก็บการตั้งค่าและการกำหนดค่าเฉพาะโปรเจ็กต์สำหรับโปรเจ็กต์เกมเฉพาะ
    




















2. **.ระดับ**: ไฟล์ระดับประกอบด้วยข้อมูลโลกของเกม 3 มิติ รวมถึงภูมิประเทศ วัตถุ แสง และการตั้งค่าเฉพาะระดับอื่น ๆ ระดับเป็นองค์ประกอบพื้นฐานของการออกแบบเกมใน CryENGINE
    




















3. **.cgf**: รูปแบบเรขาคณิตของอักขระ ไฟล์เหล่านี้มีข้อมูลโมเดล 3 มิติสำหรับตัวละคร วัตถุ และเนื้อหาเกมอื่นๆ ไฟล์ CGF สามารถรวมข้อมูลเรขาคณิต พื้นผิว และภาพเคลื่อนไหวได้
    




















4. **.chrparams**: ไฟล์พารามิเตอร์อักขระ ไฟล์เหล่านี้จัดเก็บการตั้งค่าและการกำหนดค่าสำหรับโมเดลตัวละครและภาพเคลื่อนไหว
    




















5. **.dds**: รูปแบบพื้นผิว DirectX โดยทั่วไปแล้ว CryENGINE จะใช้ไฟล์ DDS เพื่อจัดเก็บพื้นผิว รวมถึงแผนที่แบบกระจาย แผนที่ปกติ และพื้นผิวประเภทอื่น ๆ
    




















6. **.cryshader**: ไฟล์ CryENGINE Shader ไฟล์เหล่านี้จะกำหนดวิธีการเรนเดอร์วัสดุและวัตถุในโลกของเกม โดยระบุเชเดอร์ คุณสมบัติของวัสดุ และอื่นๆ
    




















7. **.crytif**: ไฟล์ข้อมูลพื้นผิว ไฟล์เหล่านี้เก็บข้อมูลเพิ่มเติมเกี่ยวกับพื้นผิว เช่น การตั้งค่าการบีบอัด มิปแมป และรายละเอียดอื่นๆ ที่เกี่ยวข้องกับพื้นผิว
    




















8. **.cdf**: ไฟล์คำจำกัดความอักขระ ไฟล์ CDF ใช้เพื่อกำหนดเนื้อหาของตัวละครและคุณสมบัติ รวมถึงไฟล์แนบ สถานะภาพเคลื่อนไหว และการตั้งค่าที่เกี่ยวข้องกับตัวละคร
    




















9. **.dds**: CryENGINE ยังใช้ไฟล์ DDS (DirectDraw Surface) สำหรับแผนที่พื้นผิวต่างๆ เช่น แผนที่ปกติ แผนที่แบบพิเศษ และแผนที่แบบกระจาย
    




















10. **.anim**: ไฟล์แอนิเมชั่น ไฟล์เหล่านี้จัดเก็บข้อมูลภาพเคลื่อนไหวสำหรับตัวละครและวัตถุ รวมถึงคีย์เฟรม ตำแหน่งกระดูก และลำดับภาพเคลื่อนไหว
    




















11. **.xml**: ไฟล์ XML อาจใช้สำหรับการกำหนดค่าและคำจำกัดความข้อมูลต่างๆ ภายใน CryENGINE เช่น ตรรกะของเกม พฤติกรรม AI และอื่นๆ
    




















12. **.pak**: [ไฟล์ PAK](/th/game/pak/) เป็นไฟล์เก็บถาวรที่ใช้ในการจัดแพ็คเกจเนื้อหาและทรัพยากรของเกม ทำให้การเผยแพร่และการโหลดเกมมีประสิทธิภาพมากขึ้น

## เปิดไฟล์ CHR ได้อย่างไร

โปรแกรมที่เปิดไฟล์ CHR ได้แก่

- **Crytek CryENGINE SDK** (ทดลองใช้ฟรี) สำหรับ Windows

**ประเภทย่อย:** ไฟล์ภาพ 3 มิติ

## ไฟล์ CHR อื่นๆ

ต่อไปนี้คือไฟล์ประเภทอื่นๆ ที่ใช้นามสกุลไฟล์ **.chr**

**สามมิติ**
- [CHR - ไฟล์ตัวละคร CryENGINE](/th/3d/chr-cryengine/)
- [CHR - ไฟล์ตัวละคร 3ds Max](/th/3d/chr-3ds/)

**แบบอักษรและเกม**
- [CHR - ชุดอักขระบอร์แลนด์](/th/font/chr/)
- [CHR - ชมรมวรรณกรรมโดกิ โดกิ! ไฟล์ตัวละคร](/th/game/chr-doki/)

## อ้างอิง
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)
