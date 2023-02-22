{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ AML - ไฟล์ภาษาเครื่อง ACPI",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ACPI AML และ API ที่สามารถสร้างและเปิดไฟล์ AML",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## ไฟล์ AML คืออะไร??

ไฟล์ AML เป็นไฟล์ระบบที่สร้างขึ้นด้วยภาษา Advanced Configuration and Power Interface (ACPI) ที่ใช้สำหรับกำหนดค่าคุณสมบัติของฮาร์ดแวร์ ประกอบด้วยรหัสไบต์อิสระของเครื่องที่ใช้ในการกำหนดค่าฮาร์ดแวร์แม้สำหรับการดำเนินการง่ายๆ เช่น การปิดเครื่องคอมพิวเตอร์ ไฟล์ AML อาจมีคำแนะนำขึ้นอยู่กับวัตถุประสงค์ที่จะติดตั้งบนเครื่อง การดำเนินการตามมาตรฐาน ACPI ช่วยให้คุณปรับปรุงฟังก์ชันการจัดการพลังงานและอินเทอร์เฟซที่มีประสิทธิภาพสำหรับการกำหนดค่าอุปกรณ์เมนบอร์ด เช่น เมนบอร์ด P55

## รูปแบบไฟล์ ACPI AML

ไฟล์ AML จะถูกบันทึกเป็นไฟล์ไบนารี่ไปยังแผ่นดิสก์ที่มีเนื้อหาเขียนด้วยรหัสไบต์ ข้อกำหนดรูปแบบไฟล์ของมาตรฐาน ACPI มีอยู่ใน [uefi](https://uefi.org/node/735) ภาษานี้ได้รับการออกแบบมาเพื่อให้มีความเสถียรและความเข้ากันได้แบบย้อนหลัง ทำให้ไม่ต้องเขียนซ้ำหรือสร้างแอปพลิเคชันซ้ำใหม่

## ข้อมูลจำเพาะรูปแบบไฟล์ AML

ไฟล์ AML ประกอบด้วยตาราง DSDT และ SSDT รหัสไบต์ AML ถูกอ่านและแยกวิเคราะห์จากส่วนเริ่มต้นของแต่ละตารางเหล่านี้ ข้อมูลนี้ให้ข้อมูลเกี่ยวกับคำจำกัดความของอุปกรณ์และวัตถุในเนมสเปซ ACPI การใช้ข้อมูลนี้ ล่าม AML สามารถสร้างรายการอุปกรณ์ทั้งหมดที่มีอยู่ในระบบ รวมถึงคุณสมบัติและฟังก์ชันที่รองรับ

### ตัวอย่างรหัส ASL สำหรับ DSDT

ตัวอย่างของรหัส ASL สำหรับ DSDT มีดังต่อไปนี้

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## อ้างอิง

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)
