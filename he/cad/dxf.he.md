{
  "date" : "2020-03-16",
  "keywords" :[ "קובץ DXF", "פורמט קובץ", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ DXF וממשקי API שיכולים ליצור ולפתוח קובצי DXF.",
  "title" :"פורמט קובץ DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ DXF?

DXF, Drawing Interchange Format, או Drawing Exchange Format, הוא ייצוג נתונים מתויג של קובץ ציור AutoCAD. לכל רכיב בקובץ יש קידומת מספר שלם הנקרא קוד קבוצה. קוד קבוצה זה מייצג למעשה את האלמנט שאחריו ומציין את המשמעות של אלמנט נתונים עבור סוג אובייקט נתון. DXF מאפשר לייצג כמעט את כל המידע שצוין על ידי המשתמש בקובץ ציור.

פורמט קובץ DXF פותח על ידי Autodesk כפורמט קבצי CAD עבור יכולת פעולה הדדית בין AutoCAD ליישומים אחרים. לפיכך, ניתן לייבא נתונים מפורמטים אחרים ל-DXF ל-AutoCAD בהתאם למפרטי יכולת הפעולה ההדדית של פורמט הקובץ DXF.

## היסטוריה קצרה ##


ההיסטוריה של פורמט קובץ DXF החל משנת 1982, כאשר הוא הוצג כחלק מ-AutoCAD 1.0. גרסאות ראשוניות של AutoCAD תומכות רק בפורמט קובץ ASCII של DXF. עם שחרור 10 של AutoCAD (ומעלה) בשנת 1988, הוצגה ב-AutoCAD תמיכה גם בפורמט ASCII וגם בפורמט DXF בינארי. בשלבים המוקדמים יותר, Autodesk לא שיתפה אף מפרטי פורמט קבצים ובשל כך, יבוא נכון של קבצי DXF לא היה קל. עם זאת, Autodesk מפרסמת כעת את מפרטי DXF וזמינה לציבור הרחב.

## מפרטי פורמט קובץ ##

פורמט קובץ DXF משתמש בזוגות הקוד והערכים של הקבוצה כדי לסדר את התוכן למקטעים. כל מקטע מורכב מרשומות כאשר כל רשומה מורכבת מקוד קבוצתי ופריט נתונים. כל קוד וערך קבוצה נמצאים בשורה משלהם בקובץ DXF. כל קטע מתחיל בקוד קבוצה 0 ואחריו המחרוזת, SECTION. לאחר מכן מופיע קוד קבוצה 2 ומחרוזת המציינת את שם הקטע (לדוגמה, SECTION1). כל חלק מורכב מקודים וערכים קבוצתיים המגדירים את המרכיבים שלו. קטע מסתיים ב-0 ואחריו המחרוזת ENDSEC.

פורמט קובץ DXF מחשיב אובייקטים שונים מיישויות. לאובייקטים אין ייצוג גרפי כאן אבל ישויות יש את זה. לפיכך, לערכים ב-DXF מתייחסים כאל אובייקטים גרפיים בעוד שאובייקטים מכונה אובייקטים לא גרפיים. הקטעים BLOCK ו-ENTITIES של קובץ DXF מכילים ישויות והשימוש בקודי קבוצה בשני הסעיפים הללו זהה. סוף ישות מסומן על ידי קבוצת 0 הבאה, שמתחילה את הישות הבאה או מציינת את סוף הקטע.

### מבנה הקובץ ###

מקטעים בקובץ DXF מסודרים בסדר הבא:

|מדור|תיאור בסיסי
---|---|
|Header|חלק זה מכיל מידע כללי על הציור. זה כמו פונקציונליות ההגדרות בטלפון שלך, המכילה את המשתנים השונים הקשורים לשרטוט והערכים המשויכים לו. לדוגמה, הסעיף Header יגדיר באיזו גרסת AutoCAD קובץ DXF משתמש (המשתנה $ACADVER) או היחידה המשמשת למדידת זוויות בקובץ (המשתנה $AUNITS)
|Classes|הקטע CLASSES מכיל את המידע עבור מחלקות המוגדרות ביישום שהמופעים שלהן מופיעים במקטעים BLOCKS, ENTITIES ו-OBJECTS של מסד הנתונים.
|טבלאות|חלק זה מכיל הגדרות למספר טבלאות שונות, שכל אחת מהן מכילה מספר ערכי סמלים שונים. לדוגמה [סוג השורה](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) מגדירה את תבנית המקפים, הנקודות, הטקסט והסמלים בקובץ DXF וכיצד הם מותאמים. להלן רשימה מלאה של טבלאות שנמצאות בסעיף זה:<ul style=";text-align:right;direction:rtl"><li style=";text-align:right;direction:rtl"> טבלת מזהה אפליקציה (APPID).</li><li style=";text-align:right;direction:rtl"> טבלת Block Record (BLOCK_RECORD).</li><li style=";text-align:right;direction:rtl"> טבלת מימד סגנון (DIMSTYPE).</li><li style=";text-align:right;direction:rtl"> טבלת שכבות (LAYER).</li><li style=";text-align:right;direction:rtl"> טבלה מסוג Linetype (LTYPE).</li><li style=";text-align:right;direction:rtl"> טבלה בסגנון טקסט (STYLE).</li><li style=";text-align:right;direction:rtl"> טבלת מערכת קואורדינטות משתמש (UCS).</li><li style=";text-align:right;direction:rtl"> הצג (VIEW) טבלה</li><li style=";text-align:right;direction:rtl"> טבלת תצורת Viewport (VPORT).</li></ul>
|בלוקים|קטע זה מכיל את האובייקטים הגרפיים ויישויות הציור המרכיבות כל התייחסות לבלוק בשרטוט.
|ישויות|חלק זה מכיל את נתוני האובייקט בפועל והישויות הגרפיות של הציור. זה יכול לכלול נתונים גולמיים - לדוגמה, ישות עיגול מוגדרת על ידי העובי שלה, נקודת המרכז, הרדיוס שלה וכיוון האקסטרוזיה שלה.
|Objects|כאן תמצא את החלקים הלא-גרפיים של הציור. לדוגמה, מילוני AutoCAD מאוחסנים כאן.

## הפניות ##

* [מפרט קובץ DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF מאת ויקיפדיה](https://en.wikipedia.org/wiki/AutoCAD_DXF)

