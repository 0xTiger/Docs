{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - פורמט קובץ תמונת דיסק",
  "description":"מהו קובץ ISO וממשקי API שיכולים ליצור ולפתוח קובצי ISO.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## מהו קובץ ISO?

קובץ עם סיומת .iso הוא קובץ תמונת דיסק ארכיון לא דחוס המייצג את התוכן של כל הנתונים בדיסק אופטי כגון CD או DVD. בהתבסס על תקן [ISO-9660](https://www.iso.org/standard/17505.html), פורמט קובץ התמונה ISO מכיל את נתוני הדיסק יחד עם מידע מערכת הקבצים המאוחסן בו. היכולת של קובצי ISO להכיל העתק מדויק של התוכן הופכת אותו לסוג הקובץ המושלם ליצירת עותקים של תקליטורים/DVD ומשמשים בעיקר לאחסון נתונים הניתנים לאתחול להתקנה. רוב הפעמים, קבצי ISO נצרבים ל-USB/CD/DVD כתוכן שניתן לאתחול לאתחול המכונה להתקנה. לקבצי ISO יש סוג MIME‏ application/x-iso9660-image.

## פורמט קובץ ISO

פורמט קובץ ISO אינו דומה לפורמטים אחרים של קבצי מיכל למרות שהוא שומר את תוכן הנתונים שצוין בארכיון. הארכיון נוצר כקובץ בינארי עם המבנה המדויק של התוכן ומידע מערכת הקבצים. פורמט קובץ ה-ISO מתואר על ידי [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) כדלקמן.

### מבנה ברמה העליונה של קובץ ISO

המבנה הכללי של הקובץ מורכב מ:

* `שטח מערכת` - 32,768 בתים ואינו בשימוש על ידי ISO_9660
* `אזור נתונים` - מורכב מערך מתאר נפח וטבלאות נתיב, ספריות וקבצים

### ערכת מתאר נפח

אזור הנתונים מתחיל עם קבוצת מתארי נפח, קבוצה של מתאר נפח אחד או יותר המסתיימת עם מסיים ערכת נפח. אלה פועלים ביחד ככותרת לאזור הנתונים, ומתארים את תוכנו (בדומה לבלוק הפרמטרים של ה-BIOS המשמש דיסקים מעוצבים של FAT, HPFS ו-NTFS).

ערכת מתאר נפח היא כפי שמוצג להלן.

|סט מתאר כרך|
---|
|מתאר כרך #1|
|...|
|מתאר כרך #N|
| מסיים קבוצת מתאר עוצמת הקול|

#### מתאר כרך

כל מתאר נפח הוא בגודל של 2048 בתים ובעל המבנה הבא:

|חלק |סוג |מזהה |גרסה |נתונים|
---|---|---|---|---|
|גודל |1 בתים |5 בתים (תמיד 'CD001') |1 בתים (תמיד 0x01) |2,041 בתים|

## הפניות

* [תמונת דיסק אופטי - ויקיפדיה](https://en.wikipedia.org/wiki/Optical_disc_image)
* [חתימות קובץ](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - ויקיפדיה](https://en.wikipedia.org/wiki/ISO_9660)

