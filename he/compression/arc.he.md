---
date: 2019-12-09
keywords: arc, .arc, פורמט קובץ arc, כיצד לפתוח קבצי arc, סיומת arc, סיומת arc
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ ARC
linktitle: ARC
description: "למד על פורמט קבצי ARC וממשקי API שיכולים ליצור ולפתוח קובצי ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## מהו קובץ ARC?

ARC הוא פורמט דחיסת נתונים וארכיון ללא אובדן שפותח על ידי System Enhancement Associates (SEA). פורמט הקובץ והאפליקציה שיוצרת אותו נקראים ARC. ARC היה פופולרי מאוד במהלך הימים הראשונים של ה-BBS החיוג מכיוון שהוא שילב את התכונות של דחיסה וארכיון של מספר קבצים באותו קובץ. מאוחר יותר הוחלף ARC ב-[ZIP](/he/compression/zip/) שהציע יחסי דחיסה טובים יותר.

סיומת הקובץ .arc משמשת על ידי מספר סוגי קבצי ארכיון אחרים שאינם קשורים, כמו פורמט ARC המשמש את ארכיון האינטרנט לאחסון משאבי אינטרנט מרובים, פורמט ARC שונה בשימוש על ידי FreeArc Archiver, פורמט אחר המשמש את נינטנדו למשאבים וכו' .

## היסטוריה קצרה של פורמט קובץ ARC

תוכנית ARC נכתבה על ידי Thom Henderson מ-System Enhancement Associates בשנת 1985. תוכנית זו קיבצה קבצים לקובץ ארכיון בודד וגם דחסה אותם. הקבצים שנוצרו על ידי תוכנית ARC השתמשו בסיומת .arc. SEA פרסמה את קוד המקור עבור ARC ב-1986 ו-ARC הועברה ל-Unix ו-Atari ST על ידי Howard Chu ב-1987.

פיל כץ פיתח את PKARC ו-PKXARC לארכיון וחילוץ קבצים. הקבצים עבדו עם פורמט הקובץ ARC והיו מהירים משמעותית. שלא כמו ARC, כץ חילק את פונקציות הדחיסה והארכיון בין שני קבצים שונים מה שהפחית את דרישת הזיכרון להפעלתם.

לאחר התביעה בין SEA לכץ, SEA פרשה משוק התוכנות השיתופיות ופיתחה את ARC+Plus עם ממשק משתמש במסך מלא. פורמט ARC אינו נפוץ יותר במחשב.

## פורמט קובץ ARC

קובץ ה-ARC מורכב מרצף של כותרת וקובץ של קובץ ואחריו סמן סוף הארכיון כפי שמוצג להלן.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### כותרת קובץ ARC ###

|היסט|תווית|סוג|ערך|תיאור|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|שיטה|
|02|ARCFNT|DS|12|שם קובץ|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|גודל דחוס|
|13|ARCDAT|DW|0000|תאריך קובץ (MSDOS)|
|15|ARCTIM|DW|0000|זמן קובץ (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|גודל לא דחוס|
|1D|ARCFIL|DS|ARCNSZ| |

### שיטות דחיסה ###

בייט שיטת הדחיסה מציין את שיטת הדחיסה שבה נעשה שימוש. להלן שיטות הדחיסה המשמשות עבור קובץ ARC.

|שיטה|שם|תיאור|
|---|---|---|
|0|מאוחסן|לא נעשה שימוש בדחיסה|
|1|ארוז|קידוד אורך ריצה חוזר (RLE)|
|2|סחוט|קידוד האפמן|
|3|Crunched|LZW עם מאגר 4K, קודים של 12 סיביות|
|4|Crunched|אריזה ראשונה, ואז מאגר LZW 4K עם 12 ביטים|
|5|Crunched|אריזה, LZW, מאגר 4K, אורך משתנה (9-12 סיביות)|
|6|מעוך|LZW, מאגר 8K, אורך משתנה (9-13 סיביות)|
|7|מעוך|אריזה, ואז מאגר LZW 8K, 2-13 סיביות (PAK 1.0)|
|8|זיקוק|האפמן דינמי עם חיץ 8K (PAK 2.0)|

## הפניות

- [ARC (פורמט קובץ) - ויקיפדיה](https://en.wikipedia.org/wiki/ARC_(file_format))

