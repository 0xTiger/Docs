{
"วันที่": "2023-06-08",
  "keywords": [
"ไฟล์ hpp",
"ไฟล์ hpp คืออะไร",
"ไฟล์ hpp ประกอบด้วยอะไรบ้าง",
"ตัวอย่างไฟล์ hpp",
"ไฟล์ hpp เป็นรูปแบบอะไร",
"ไฟล์",
"นามสกุลไฟล์ hpp",
"ส่วนขยาย"
],
  "author": {
"display_name": "ชาคีล ไฟซ์"
},
"draft": "false",
"toc": true,
"title": "รูปแบบไฟล์ HPP - ไฟล์ส่วนหัว C++",
  "description":"เรียนรู้เกี่ยวกับรูปแบบ HPP และ API ที่สามารถสร้างและเปิดไฟล์ HPP",
"linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"lastmod": "2023-06-08"
}

## ไฟล์ HPP คืออะไร??

โดยทั่วไปรูปแบบไฟล์ ".hpp" จะใช้สำหรับไฟล์ส่วนหัวในภาษาการเขียนโปรแกรม C++ โดยทั่วไปไฟล์ส่วนหัวจะมีการประกาศและคำจำกัดความของฟังก์ชัน คลาส ตัวแปร และค่าคงที่ที่ใช้โดยไฟล์ซอร์สโค้ดอื่นในโครงการ C++

วัตถุประสงค์ของการใช้ไฟล์ส่วนหัวคือเพื่อให้มีวิธีแบ่งปันโค้ดทั่วไปในไฟล์ซอร์สโค้ดหลายไฟล์โดยไม่ต้องทำซ้ำโค้ด เมื่อไฟล์ต้นฉบับ C++ ต้องการเข้าถึงการประกาศหรือคำจำกัดความจากไฟล์ส่วนหัว ไฟล์นั้นจะรวมไฟล์ส่วนหัวโดยใช้คำสั่ง preprocessor `#include`

นามสกุลไฟล์ ".hpp" มักใช้เพื่อระบุว่าไฟล์นั้นเป็นไฟล์ส่วนหัว C++ ไม่จำเป็นต้องใช้ส่วนขยายเฉพาะนี้สำหรับไฟล์ส่วนหัว และคุณอาจพบไฟล์ส่วนหัวที่มี ".h" หรือส่วนขยายอื่น ๆ อีกด้วย การเลือกส่วนขยายส่วนใหญ่เป็นเรื่องของแบบแผนและความชอบส่วนบุคคล

เมื่อไฟล์ต้นฉบับ C++ รวมไฟล์ส่วนหัวโดยใช้ `#include` คอมไพลเลอร์จะรวมเนื้อหาของไฟล์ส่วนหัวเข้ากับไฟล์ต้นฉบับอย่างมีประสิทธิภาพก่อนที่จะคอมไพล์เป็นหน่วย ซึ่งช่วยให้ไฟล์ต้นฉบับสามารถเข้าถึงการประกาศและคำจำกัดความในไฟล์ส่วนหัว โดยให้ข้อมูลที่จำเป็นสำหรับคอมไพเลอร์ในการดำเนินการตรวจสอบประเภทและสร้างโค้ด

## ไฟล์ HPP ประกอบด้วยอะไรบ้าง

ต่อไปนี้เป็นเนื้อหาทั่วไปบางส่วนที่คุณอาจพบในไฟล์ ".hpp":

- **การประกาศฟังก์ชัน:** ไฟล์ส่วนหัวมักจะมีการประกาศฟังก์ชันโดยไม่มีการใช้งานจริง การประกาศเหล่านี้ให้ข้อมูลเกี่ยวกับชื่อของฟังก์ชัน ประเภทการส่งคืน และพารามิเตอร์ ทำให้ไฟล์ซอร์สโค้ดอื่นๆ สามารถใช้ฟังก์ชันได้โดยไม่จำเป็นต้องทราบรายละเอียดการใช้งาน
- **การประกาศคลาส:** ไฟล์ส่วนหัวสามารถมีการประกาศคลาส รวมถึงชื่อคลาส ตัวแปรสมาชิก ฟังก์ชันสมาชิก และตัวระบุการเข้าถึง ด้วยการรวมการประกาศคลาสไว้ในไฟล์ส่วนหัว ไฟล์ซอร์สโค้ดอื่น ๆ จะสามารถสร้างอ็อบเจ็กต์ของคลาสนั้นและเข้าถึงสมาชิกของคลาสได้
- **การประกาศค่าคงที่:** ไฟล์ส่วนหัวสามารถกำหนดค่าคงที่ได้ เช่น ตัวแปรร่วมหรือค่าแจงนับที่มีไว้เพื่อใช้ร่วมกันในไฟล์ซอร์สโค้ดหลายไฟล์ ค่าคงที่เหล่านี้สามารถเข้าถึงได้โดยการรวมไฟล์ส่วนหัวไว้ในไฟล์ต้นฉบับอื่น ทำให้สามารถใช้ค่าคงที่ที่กำหนดไว้ได้
- **คำจำกัดความประเภท:** ไฟล์ส่วนหัวอาจมีคำจำกัดความประเภทโดยใช้คีย์เวิร์ด "typedef" หรือนามแฝงประเภทโดยใช้คีย์เวิร์ด "using" คำจำกัดความเหล่านี้สร้างชื่อใหม่สำหรับประเภทที่มีอยู่ ทำให้โค้ดสามารถอ่านและบำรุงรักษาได้มากขึ้น
- **คำจำกัดความฟังก์ชันอินไลน์:** ในบางกรณี ไฟล์ส่วนหัวอาจมีคำจำกัดความฟังก์ชันอินไลน์ ฟังก์ชันอินไลน์เป็นฟังก์ชันขนาดเล็กที่ขยายที่ไซต์การโทร แทนที่จะเรียกว่าเป็นฟังก์ชันแยกกัน การรวมคำจำกัดความฟังก์ชันอินไลน์ในไฟล์ส่วนหัวทำให้คอมไพเลอร์สามารถแทนที่การเรียกใช้ฟังก์ชันด้วยเนื้อหาของฟังก์ชันได้โดยตรง ซึ่งอาจช่วยปรับปรุงประสิทธิภาพได้

## ตัวอย่างไฟล์ HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## ไฟล์ HPP อยู่ในรูปแบบใด

HPP เป็นไฟล์ข้อความธรรมดา แต่เป็นไปตามกฎทั่วไปและไวยากรณ์ของภาษาการเขียนโปรแกรม C++ ต่อไปนี้คือรายละเอียดรูปแบบและโครงสร้างทั่วไปของไฟล์ ".hpp":

- **ตัวป้องกันส่วนหัว:** โดยทั่วไป ไฟล์ ".hpp" จะขึ้นต้นด้วยตัวป้องกันส่วนหัวเพื่อป้องกันการรวมไฟล์เดียวกันหลายครั้ง ซึ่งทำได้โดยใช้คำสั่งตัวประมวลผลล่วงหน้า เช่น `#ifndef`, `#define` และ `#endif` การป้องกันส่วนหัวช่วยให้แน่ใจว่าเนื้อหาของไฟล์ถูกรวมเพียงครั้งเดียวในระหว่างกระบวนการคอมไพล์
- **รวมคำสั่ง:** หลังจากป้องกันส่วนหัว คุณสามารถรวมไฟล์ส่วนหัวอื่นๆ ที่จำเป็นได้โดยใช้คำสั่ง `#include` สิ่งเหล่านี้อาจรวมถึงส่วนหัวของไลบรารีมาตรฐานหรือส่วนหัวที่กำหนดเองอื่นๆ ที่จำเป็นสำหรับโค้ดของคุณ
- **การประกาศและคำจำกัดความ:** เนื้อหาหลักของไฟล์ ".hpp" คือการประกาศ และในบางกรณี เป็นคำจำกัดความของคลาส ฟังก์ชัน ค่าคงที่ ชื่อแทนประเภท และองค์ประกอบอื่นๆ ตัวอย่างเช่น คุณอาจประกาศคลาสโดยใช้คีย์เวิร์ด `class` ฟังก์ชันที่ใช้ประเภทการส่งคืน ชื่อ และรายการพารามิเตอร์ และค่าคงที่โดยใช้คีย์เวิร์ด 'const` ตามด้วยประเภทและชื่อ
- **คำจำกัดความฟังก์ชันอินไลน์:** ในบางกรณี คุณอาจรวมคำจำกัดความฟังก์ชันอินไลน์ไว้ในไฟล์ ".hpp" โดยตรง ฟังก์ชันอินไลน์มักจะถูกกำหนดไว้ภายในเนื้อหาของคลาส ซึ่งหมายความว่าคำจำกัดความของฟังก์ชันจะรวมอยู่เคียงข้างการประกาศ ซึ่งสามารถทำได้โดยใส่คำนำหน้านิยามฟังก์ชันด้วยคีย์เวิร์ด 'inline'
- **การประกาศเนมสเปซ:** หากคุณใช้เนมสเปซในโค้ด คุณสามารถประกาศได้ภายในไฟล์ ".hpp" ซึ่งทำได้โดยใช้คีย์เวิร์ด 'เนมสเปซ' ตามด้วยชื่อเนมสเปซ และปิดโค้ดที่เกี่ยวข้องภายในบล็อกเนมสเปซ

## อ้างอิง
* [ไฟล์ส่วนหัว (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
