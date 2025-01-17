{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ไฟล์ TSX - ไฟล์ React TypeScript - ไฟล์ .tsx คืออะไร และวิธีการเปิด?",
  "description":"เรียนรู้เกี่ยวกับไฟล์ TSX React TypeScript และวิธีการเปิด.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-th-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## ไฟล์ TSX คืออะไร

นามสกุลไฟล์ ".tsx" โดยทั่วไปจะเชื่อมโยงกับไฟล์ TypeScript ที่มีโค้ด **React** **TypeScript เป็นชุดย่อยของ JavaScript** ที่เพิ่มการพิมพ์แบบคงที่ให้กับภาษา และ **React เป็นไลบรารี JavaScript สำหรับสร้างอินเทอร์เฟซผู้ใช้** เมื่อทำงานร่วมกับ React และ TypeScript ร่วมกัน นักพัฒนามักใช้ส่วนขยาย ".tsx" สำหรับไฟล์ของตนเพื่อระบุว่ามีทั้ง TypeScript และ JSX (ส่วนขยายไวยากรณ์ของ React สำหรับ JavaScript)

## ตัวอย่างไฟล์ TSX

TypeScript ช่วยให้คุณสามารถกำหนดประเภทของตัวแปร พารามิเตอร์ฟังก์ชัน และอื่นๆ ได้ คุณมักจะเห็นโค้ด TypeScript ในไฟล์ ".tsx" ที่ระบุประเภทของอุปกรณ์ประกอบฉาก สถานะ และตัวแปรอื่นๆ ที่ใช้ในส่วนประกอบ React

```
// ตัวอย่าง: รหัส TypeScript ในส่วนประกอบ React
อินเทอร์เฟซ MyComponentProps {
   ชื่อ: สตริง;
   อายุ: หมายเลข;
}
const MyComponent: React.FC<MyComponentProps> = ({ ชื่อ อายุ }) => {
   // ตรรกะส่วนประกอบที่นี่
   return <div>{name} มีอายุ {age} ปี</div>;
};
```

## JSX (ส่วนขยายไวยากรณ์ตอบโต้)

JSX เป็นส่วนขยายไวยากรณ์สำหรับ JavaScript ที่แนะนำโดย React มีลักษณะคล้ายกับ XML/HTML และใช้เพื่ออธิบายว่า UI ควรมีลักษณะอย่างไร

```
// ตัวอย่าง: JSX ในองค์ประกอบ React
const MyComponent: React.FC<MyComponentProps> = ({ ชื่อ อายุ }) => {
   return <div>{name} มีอายุ {age} ปี</div>;
};
```

โดยทั่วไปไฟล์ ".tsx" จะมีคำจำกัดความของส่วนประกอบ React โดยใช้ส่วนประกอบที่ใช้งานได้หรือส่วนประกอบของคลาส

```
// ตัวอย่าง: ตอบสนองคำจำกัดความขององค์ประกอบในไฟล์ ".tsx"
const MyComponent: React.FC = () => {
   กลับ <div>สวัสดี โต้ตอบ!</div>;
};
```

คุณมักจะเห็นคำสั่งนำเข้าที่จุดเริ่มต้นของไฟล์ ซึ่งนำการขึ้นต่อกันและโมดูลที่จำเป็นเข้ามา

```
// ตัวอย่าง: นำเข้าคำสั่งในไฟล์ ".tsx"
นำเข้าปฏิกิริยาจาก 'ปฏิกิริยา';
```

## เปิดไฟล์ TSX ได้อย่างไร

ไฟล์ TSX เป็นไฟล์ข้อความธรรมดา ดังนั้นคุณจึงสามารถเปิดในโปรแกรมแก้ไขข้อความใดก็ได้ เช่น แผ่นจดบันทึก อย่างไรก็ตาม ไฟล์เหล่านี้เป็นไฟล์เข้ารหัสและมีไว้สำหรับเปิดโดย IDE เช่น รหัสวิชวลสตูดิโอ