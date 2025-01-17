{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "פורמט קובץ", "CAD", "פתח", "צור" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ DWG וממשקי API שיכולים ליצור ולפתוח קובצי DWG.",
  "title" :"פורמט קובץ DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ DWG?

קבצים עם סיומת DWG מייצגים קבצים בינאריים קנייניים המשמשים להכיל נתוני עיצוב דו-ממדיים ותלת-ממדיים. כמו DXF, שהם קבצי ASCII, DWG מייצג את פורמט הקובץ הבינארי עבור שרטוטי CAD (Computer Aided Design). הוא מכיל תמונה וקטורית ומטא נתונים לייצוג התוכן של קבצי CAD. ישנם צופים חינמיים זמינים לצפייה בקובצי DWG במערכת ההפעלה Windows כגון DWG TrueView החינמי של Autodesk. יש גם יישומי צד שלישי אחרים התומכים בהגעה לקבצי DWG. קובצי DWG מכילים מידע שנוצר על ידי המשתמש וכוללים:

* עיצובים
* נתונים גיאומטריים
* מפות ותמונות

פורמט זה נמצא בשימוש נרחב על ידי אדריכלים, מהנדסים ומעצבים למטרות עיצוב שונות.

## היסטוריה קצרה ##

פורמט קובץ DWG התפתח עם הזמן מאז הצגתו הרשמית בשנת 1982. סקירה קצרה של אירועי העבר מנקודת מבט ההיסטוריה היא כדלקמן.

**1982:** Autodesk העניקה רישיון לפורמט הקובץ DWG , שפותח על ידי מייק רידל ב-1970, כבסיס ל-AutoCAD.

**1998:** עם שחרורו של AutoCAD R14.01, Autodesk הוסיפה אימות קבצים באמצעות פונקציה בשם DWGCHECK שהטמיעה סכום ביקורת מוצפן וקוד מוצר, הנקרא WaterMark על ידי Autodesk, לתוך קבצי DWG שנוצרו על ידי התוכנית.

**2006:** Autodesk שינה את AutoCAD 2007, כדי לכלול את "TrustedDWG technology" כדי להטמיע מחרוזת טקסט "Autodesk DWG. קובץ זה הוא Trusted DWG שנשמר לאחרונה על ידי יישום Autodesk או יישום מורשה Autodesk" בקבצי DWG. המטרה של זה הייתה לעזור למשתמשי תוכנת Autodesk להבטיח שקבצים אלה נוצרו על ידי יישום Autodesk או RealDWG, מה שבהחלט אמור לעזור בהפחתת הסיכון לאי תאימות.

## מבנה קובץ ##

DWG היה אחד מפורמטי הקבצים הנפוצים במגוון יישומים ויש לו מבנה קבצים חזק. מכיוון ש-DWG הוא פורמט קובץ בינארי, הוא אינו קריא לאדם כמו פורמט הקובץ ASCII [DXF](/he/cad/dxf/) הרגיל. קובצי DWG כוללים בדרך כלל מידע על קואורדינטות התמונה וכל מטא נתונים הקשורים אליה. [מפרטים](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) מלאים של פורמט קובץ DWG זמינים להורדה על ידי OpenDesign. מבנה הקובץ של פורמט קובץ DWG מתמצה כדלקמן.

**Header**: כותרת הקובץ מורכבת ממשתני DWG Header ומידע על Cyclic Redundancy Check (CRC) המשמש לזיהוי השגיאות. כל תת-סעיף הוא וקטור מיוחד שבו נעשה שימוש באורכים שונים של סיביות לייצוג תוויות שונות. לדוגמה, 6 הסיביות הראשונות של המשתנה DWG Header מייצגות את מחרוזת הגרסה.

**הגדרות מחלקות:** קובץ DWG עשוי להכיל מחלקות רבות בהתאם למטרה הספציפית של קובץ ה-dwg. מידע כגון גודל מטא-נתונים של כיתה של אזור נתוני כיתה, מספר כיתה ו-checksum בנוסף לאחרים.

**תבנית**: זה אופציונלי ועבור גרסאות R15 ו-R15, קטע זה נמצא מתחת לקטע אובייקט פנוי.

**ריפוד**: המטא נתונים מתווספים ומתוקנים עם מספר מסוים של בתים, מה שהופך את גרסאות תוכנת AutoCAD הישנות יותר להיות תואמות קדימה לפורמט הקובץ החדש של DWG.

**נתוני תמונה**: המטא נתונים עבור סעיף זה תלויים בסוג ה-.dwg הספציפי. עבור משתמשי R14 ו-R15, סעיף זה הוא אופציונלי.

**נתוני אובייקט**: נתוני האובייקט מורכבים מרשימה מלאה של ישויות טבלה, ערכי מילון וכו' התואמת לרשימת האובייקטים הקיימת.

**מפת אובייקט**: המיקום של כל אובייקט בקובץ מצוין בחלק זה של הקובץ. רוב המטא נתונים בסעיף זה הם נקודות אחיזה לקבצים שמשחקות תפקיד בזיהוי ובעיבוד מחדש של האובייקט.

**שטח פנוי באובייקט**: סעיף זה הוא אופציונלי עבור כל המשתמשים

**כותרת שניה**: שכפול של קטע כותרת הקובץ לקראת סוף קובץ ה-DWG

## הפניות ##

* [מפרט פורמט קובץ DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [מפרט קובץ DWG](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG - מאת ויקיפדיה](https://en.wikipedia.org/wiki/.dwg)

