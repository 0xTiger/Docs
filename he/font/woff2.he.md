{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2 File - Web Open Font Format 2.0 File",
  "description": "למד על מהו קובץ WOFF2 וממשקי API שיכולים ליצור ולפתוח קובץ WOFF2.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-he2"
}
},
  "lastmod": "2023-01-10"
}

## מהו קובץ WOFF2?

WOFF2 הוא פורמט קובץ גופן שהוא גרסה דחוסה יותר של פורמט הגופן הפתוח באינטרנט (WOFF). זה פותח כדרך להקטין את גודל הקבצים של גופני אינטרנט, מה שמאפשר להם להיטען מהר יותר ולהשתמש פחות ברוחב פס. WOFF2 משתמש באלגוריתם דחיסה בשם Brotli כדי לדחוס את נתוני הגופן, מה שעלול לגרום לגדלי קבצים קטנים משמעותית מגופנים מקבילים של [WOFF](/font/woff/). פורמט זה נתמך על ידי רוב דפדפני האינטרנט המודרניים כולל Chrome, Firefox, Safari, Opera ו-Edge (גרסה 14 ואילך).

## פורמט קובץ WOFF2 - מידע נוסף

מבנה הקבצים הפנימי של קובץ גופן WOFF2 מורכב מכמה חלקים שונים, כולל כותרת, מטא נתונים, ספריית טבלה ונתוני הגופן עצמם.

 1. הכותרת מכילה מידע על הפורמט הכולל של הקובץ, כולל מספר הגרסה ומספר הטבלאות הקיימות בקובץ.

 1. קטע מטא נתונים מכיל מידע כגון שם גופן, זכויות יוצרים ומידע אחר הקשור לגופנים.

 1. ספריית הטבלאות מכילה מידע על הטבלאות השונות המרכיבות את הגופן, כולל מיקומן בקובץ ואורכן.

 1. נתוני הגופן עצמם מחולקים למספר טבלאות שונות, שכל אחת מהן מכילה מידע ספציפי על הגופן, כגון התווים שלו והגליפים המתאימים להם. טבלאות אלה עשויות לכלול:

 * הטבלה 'גליף' מכילה את קווי המתאר בפועל של הגופן, כולל הצורה והגודל של כל תו.
 * טבלת 'הראש' מכילה מידע כללי על הגופן, כגון מספר הגרסה שלו, גודל העיצוב וכדומה.
 * הטבלה 'hmtx' מכילה מידע על המדדים של הגופן, כולל הרוחב והמיקומים של התווים.
 * כל טבלה נדחסת ומאוחסנת בפורמט קובץ WOFF2 לאחר שהשלימה את תהליך הקידוד.

המבנה הכולל נועד לאפשר ניתוח ופענוח מהיר, כך שדפדפני אינטרנט יכולים לטעון ולהציג את הגופן במהירות וביעילות באתר.

### כותרת WOFF2
כותרת WOFF מורכבת מחתימה מזהה שמציינת את סוג הנתונים הכלולים בקובץ. כותרת WOFF יחד עם השדות שלה היא כדלקמן.

|הקלד|שם השדה|תיאור|
---|---|---|
|UInt32|חתימה |0x774F4632 'wOF2' |
|UInt32| flavor |גרסת sfnt של גופן הקלט.|
|UInt32| אורך |גודל כולל של קובץ WOFF.|
|UInt16| numTables |מספר ערכים בספריית טבלאות גופנים.|
|UInt16| שמור |שמורה; מוגדר לאפס.|
|UInt32| totalSfntSize |גודל כולל הדרוש לנתוני הגופן הלא דחוסים, כולל הכותרת, הספריה וטבלאות הגופנים sfnt (כולל ריפוד).|
|UInt32| totalCompressedSize האורך הכולל של בלוק הנתונים הדחוס.|
|UInt16| majorVersion |גרסה מרכזית של קובץ WOFF.|
|UInt16| minorVersion |גרסה מינורית של קובץ WOFF.|
|UInt32| metaOffset |היסט לבלוק מטא נתונים, מתחילת קובץ WOFF.|
|UInt32| metaLength |אורך של בלוק מטא נתונים דחוס.|
|UInt32| metaOrigLength |גודל לא דחוס של בלוק מטא נתונים.|
|UInt32| privOffset |היסט לבלוק נתונים פרטי, מתחילת קובץ WOFF.|
|UInt32| privLength |אורך של חסימת נתונים פרטית.|


## הפניות
 * [פורמט קובץ WOFF2 w3](https://www.w3.org/TR/WOFF2/)
