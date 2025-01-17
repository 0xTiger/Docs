{
"วันที่": "2023-05-09",
  "keywords": [
"ไฟล์ mlx",
"ไฟล์ mlx คืออะไร",
"ไฟล์ mlx เป็นรูปแบบอะไร",
"ไฟล์ mlx ประกอบด้วยอะไร",
"วิธีสร้างไฟล์ mlx ด้วย MATLAB",
"วิธีการเปิดไฟล์ mlx",
"ไฟล์",
"นามสกุลไฟล์ MLX",
"ส่วนขยาย"
],
  "author": {
"display_name": "ชาคีล ไฟซ์"
},
"draft": "false",
"toc": true,
"title": "รูปแบบไฟล์ MLX - ไฟล์โค้ด MATLAB Live",
  "description":"เรียนรู้เกี่ยวกับรูปแบบ MLX และ API ที่สามารถสร้างและเปิดไฟล์ MLX",
  "linktitle": "MLX",
  "menu": {
    "docs": {
      "identifier": "executable-mlx",
      "parent": "executable"
}
},
"lastmod": "2023-05-09"
}

## ไฟล์ MLX คืออะไร??

ไฟล์ MLX เป็นรูปแบบไฟล์ประเภทหนึ่งที่ใช้ใน MATLAB ซึ่งเป็นภาษาการเขียนโปรแกรมและสภาพแวดล้อมการประมวลผลสำหรับการคำนวณเชิงตัวเลขและการวิเคราะห์ข้อมูล รูปแบบไฟล์ MLX ใช้สำหรับ MATLAB Live Scripts ซึ่งรวมข้อความ โค้ด และการแสดงภาพไว้ในเอกสารโต้ตอบเดียว

MATLAB Live Scripts ช่วยให้ผู้ใช้สามารถสร้างเอกสารปฏิบัติการที่สามารถแชร์กับผู้อื่นได้ และมอบวิธีการเชิงโต้ตอบในการสำรวจข้อมูลและอัลกอริธึม มีความคล้ายคลึงกับ Jupyter Notebooks ตรงที่อนุญาตให้ผสมโค้ด ข้อความ และการแสดงภาพได้ แต่มีความเฉพาะเจาะจงกับ MATLAB

ไฟล์ MLX สามารถเปิดและแก้ไขได้โดยใช้ MATLAB หรือ MATLAB Online ซึ่งเป็นซอฟต์แวร์เวอร์ชันบนเว็บ นอกจากนี้ยังสามารถส่งออกไปยังรูปแบบไฟล์อื่นๆ เช่น PDF หรือ HTML เพื่อแชร์กับผู้อื่นที่อาจไม่สามารถเข้าถึง MATLAB

## ไฟล์ MLX อยู่ในรูปแบบใด

รูปแบบไฟล์ MLX เป็นรูปแบบไฟล์ที่เป็นกรรมสิทธิ์ซึ่ง MATLAB ใช้สำหรับเอกสาร Live Script ไฟล์ MLX นั้นเป็นไฟล์ข้อความธรรมดาที่มีนามสกุลไฟล์ .mlx ที่ประกอบด้วยข้อความที่จัดรูปแบบ รหัส MATLAB และเอาต์พุต MATLAB ผสมกัน

เนื้อหาของไฟล์ MLX ถูกจัดระเบียบเป็นเซลล์ซึ่งสามารถประกอบด้วยข้อความหรือรหัส MATLAB เซลล์ข้อความสามารถมีข้อความ รูปภาพ และไฮเปอร์ลิงก์ที่จัดรูปแบบได้ ในขณะที่เซลล์โค้ดสามารถมีโค้ด MATLAB และเอาต์พุตได้ รวมถึงการแสดงภาพ เช่น พล็อต แผนภูมิ และกราฟ

## ไฟล์ MLX ประกอบด้วยอะไรบ้าง

ไฟล์ MLX มีส่วนผสมของข้อความที่จัดรูปแบบ รหัส MATLAB และเอาต์พุต MATLAB เนื้อหาของไฟล์ MLX ถูกจัดระเบียบเป็นเซลล์โดยแต่ละเซลล์สามารถมีข้อความหรือรหัส MATLAB ได้

เซลล์ข้อความสามารถมีข้อความที่จัดรูปแบบได้ เช่น หัวเรื่อง ย่อหน้า รายการสัญลักษณ์แสดงหัวข้อย่อยหรือลำดับเลข และไฮเปอร์ลิงก์ นอกจากนี้ยังสามารถประกอบด้วยรูปภาพ สมการ และสื่ออื่นๆ ได้อีกด้วย

เซลล์โค้ดประกอบด้วยโค้ด MATLAB ที่สามารถดำเนินการภายในเอกสาร Live Script โค้ดอาจรวมถึงตัวแปร ฟังก์ชัน ลูป และคำสั่งแบบมีเงื่อนไข ผลลัพธ์ของการเรียกใช้โค้ดจะแสดงในพื้นที่เอาต์พุต ซึ่งอาจรวมถึงตาราง พล็อต แผนภูมิ และการแสดงภาพอื่นๆ

## วิธีสร้างไฟล์ MLX ด้วย MATLAB

หากต้องการสร้างไฟล์ MLX ด้วย MATLAB คุณสามารถทำตามขั้นตอนเหล่านี้:

- เปิด MATLAB แล้วคลิกที่ปุ่ม "New Live Script" บนแท็บหน้าแรกของ Ribbon MATLAB
- โปรแกรมแก้ไข Live Script จะเปิดขึ้นและคุณสามารถเริ่มพิมพ์ข้อความหรือรหัส MATLAB ลงในเซลล์แรกได้
- เขียนข้อความหรือโค้ด MATLAB ลงในเซลล์
- หากต้องการบันทึกไฟล์ MLX ให้เลือก "บันทึก" จากเมนูไฟล์ หรือใช้ปุ่ม "บันทึก" บน Ribbon

## เปิดไฟล์ .MLX ได้อย่างไร

คุณสามารถเปิดไฟล์ MLX โดยใช้ MATLAB หากต้องการเปิดไฟล์ MLX ให้เลือกเปิดจากเมนูแล้วเลือกไฟล์ MLX จากนั้นเลือกเปิด


