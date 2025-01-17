{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "למד על פורמט קבצי DSN וממשקי API שיכולים ליצור ולפתוח קובצי DSN.",
  "title" : "פורמט קובץ DSN - קובץ שמות מקור של מסד נתונים",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-he",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## מהו קובץ DSN?

DSN מייצג שם מקור נתונים והוא פורמט קובץ המשמש לאחסון מידע חיבור מסד נתונים. קבצי DSN משמשים בדרך כלל בשילוב עם ODBC (קישוריות מסד נתונים פתוחה) ומאפשרים גישה קלה למסד נתונים ספציפי על ידי אספקת המידע הדרוש לחיבור אליו, כגון שם השרת, שם המשתמש והסיסמה. הקובץ הוא בדרך כלל בטקסט רגיל וניתן ליצור ולערוך באמצעות עורך טקסט. ניתן להשתמש בו במערכות הפעלה שונות כמו Windows, Linux ו-Mac.

## איך יוצרים קובץ DSN?

השיטה ליצירת קובץ DSN עשויה להשתנות בהתאם למערכת ההפעלה ולכלים הזמינים. השלבים הבאים מספקים סקירה כללית של התהליך ליצירת קובץ DSN במערכת Windows.

1. פתח את מנהל מקורות הנתונים של ODBC על ידי חיפוש מקורות נתונים של ODBC בתפריט ההתחלה.
2. בחר בכרטיסייה מערכת DSN ולחץ על כפתור הוסף.
3. בחר את מנהל ההתקן המתאים למסד הנתונים שאליו ברצונך להתחבר ולחץ על סיום.
4. מלא את המידע הדרוש כדי להתחבר למסד הנתונים, כגון שם השרת, שם המשתמש והסיסמה.
5. לחץ על אישור כדי לשמור את קובץ ה-DSN.

לחלופין, תוכל ליצור קובץ DSN באופן ידני על ידי יצירת קובץ טקסט רגיל עם סיומת .dsn והזנת פרטי החיבור הדרושים בפורמט:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

לאחר מכן תוכל להשתמש בנתיב של קובץ זה בתור ה-DSN בקוד/סקריפט שלך כדי להתחבר למסד הנתונים.

## תוכניות שפותחות קובץ DSN

קובץ DSN הוא קובץ טקסט רגיל המאחסן מידע המשמש לחיבור למסד נתונים, כגון שם השרת, שם המשתמש והסיסמה. הוא משמש בדרך כלל בשילוב עם ODBC (קישוריות מסד נתונים פתוח) כדי לספק גישה קלה למסד נתונים ספציפי.

כדי לפתוח ולצפות בתוכן של קובץ DSN, ניתן להשתמש בכל עורך טקסט כגון Notepad, Sublime Text, Atom וכו'. תוכנות אלו יאפשרו לכם לפתוח את קובץ ה-DSN ולצפות במידע החיבור המאוחסן בתוכו.

עם זאת, כדי להשתמש בקובץ DSN כדי להתחבר למסד נתונים ולבצע פעולות כמו SELECT, INSERT, UPDATE, DELETE וכו', תוכנית עם תמיכה ב-ODBC, כגון שפת תכנות כמו Python, Java, C# או כלי ניהול מסד נתונים כמו Microsoft Access , נדרש סטודיו לניהול שרת SQL. תוכנות אלו יכולות להשתמש במידע בקובץ ה-DSN כדי להתחבר למסד הנתונים ולבצע את הפעולה הרצויה.

## הפניות

* [מהו DSN (שם מקור נתונים)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



