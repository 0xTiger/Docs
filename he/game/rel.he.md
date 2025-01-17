{
  "date" : "2021-09-08",
  "keywords" :[ "קובץ rel", "פורמט קובץ rel", "מהו קובץ rel", "קובץ", "לדוגמה", "סיומת קובץ rel","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ REL וממשקי API שיכולים ליצור ולפתוח קובצי REL.",
  "title" :"REL - קובץ מודול ניתן למיקום מחדש",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## מהו קובץ REL?
קובץ עם סיומת rel יכול לשמש לכמה סוגים של מטרות. לכן, מבחינת סיווג המשחקים הוא ידוע כקובץ מודול הניתן למיקום המשמש חלק ממשחקי Nintendo Wii, כגון Brawl, Super Smash Bros ו-Mario Kart Wii. הוא כולל את נתוני המשחק, כולל דגמי דמויות ושלבים. קבצי REL פועלים באופן דומה לקבצי ה-.DLL המשמשים את Microsoft Windows.

## פורמט קובץ REL
בפורמט קובץ REL, הקובץ מחולק למספר חלקים, מקובצים לפי גישה כמו, למשל נתונים לקריאה בלבד בקטע אחד, כל קוד ההפעלה ממוקם באחר וכו'. הקובץ מתחיל בסעיף כותרת, ואחריו:
- טבלה המכילה מידע על סעיפים.
- נתוני המדור.
- מידע על רילוקיישן.

### כותרת הקובץ
הקובץ מתחיל עם כותרת של עד 0x4C בתים:
| קיזוז | גודל | שם שדה | תיאור |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | מספר זיהוי שרירותי. חייב להיות ייחודי בין כל RELs המשמשים משחק. לא חייב להיות 0. |
| 0x04 | 4 | הבא | מצביע למודול הבא, מלא בזמן הריצה. |
| 0x08 | 4 | הקודם | מצביע למודול הקודם, מולא בזמן הריצה. |
| 0x0c | 4 | numSections | מספר הקטעים בקובץ. |
| 0x10 | 4 | sectionInfoOffset | קיזוז לתחילת טבלת המקטעים. |
| 0x14 | 4 | nameOffset | היסט למחרוזת ASCII המכילה את שם המודול. יכול להיות NULL. יחסית לתחילת קובץ REL. |
| 0x18 | 4 | גודל שם | גודל שם המודול בבתים. |
| 0x1c | 4 | גרסה | מספר גרסה של פורמט הקובץ REL. |
| 0x20 | 4 | bssגודל | גודל הקטע '.bss'. |
| 0x24 | 4 | relOffset | קיזוז לטבלת הרילוקיישן. |
| 0x28 | 4 | impOffset | היסט לטבלת ההשפעה. |
| 0x2c | 4 | impSize | גודל טבלת imp בבתים. |
| 0x30 | 1 | prologSection | אינדקס לטבלת סעיפים שאליה פרולוג הוא יחסי. דלג אם שדה זה הוא 0. |
| 0x31 | 1 | epilogSection | אינדקס לטבלת מקטעים שאליה מתייחס האפילוג. דלג אם שדה זה הוא 0. |
| 0x32 | 1 | לא פתור סעיף | אינדקס לטבלת מקטעים אשר לא פתורה היא ביחס אליה. דלג אם שדה זה הוא 0. |
| 0x33 | 1 | bssSection | אינדקס לטבלת מקטעים אשר bss יחסית אליה. התמלא בזמן ריצה! |
| 0x34 | 4 | פרולוג | קיזוז לקטע שצוין של הפונקציה _prolog. |
| 0x38 | 4 | אפילוג | קיזוז לקטע שצוין של הפונקציה _epilog. |
| 0x3c | 4 | לא פתור | קיזוז לקטע שצוין של הפונקציה _unresolved. |
| 0x40 | 4 | יישר | גרסה ≥ 2 בלבד. אילוץ יישור על כל הסעיפים, מבוטא בחזקת 2. |
| 0x44 | 4 | bssAlign | גרסה ≥ 2 בלבד. אילוץ יישור על כל קטע '.bss', מבוטא בחזקת 2. |
| 0x48 | 4 | fixSize | גרסה ≥ 3 בלבד. אם REL מקושר עם OSLinkFixed (במקום OSLink), ניתן להשתמש ברווח שאחרי כתובת זו למטרות אחרות (כמו BSS). |

### טבלת מידע על סעיפים
טבלת המידע של החלקים מכילה ערכי **numSections** כל אחד באורך 0x8 בתים:
| קיזוז | גודל | תיאור |
-------|------------|-------------|
| 0x0 | 30 ביטים | היסט מתחילת ה-REL לקטע. אם זה אפס, הקטע הוא קטע לא מאותחל (כלומר .bss). |
| 0x3.6 | 1 סיביות | לא ידוע. |
| 0x3.7 | 1 סיביות | דגל בר הפעלה; אם זה 1, הסעיף ניתן להפעלה. |
| 0x4 | 4 | אורך בבתים של הקטע. אם זה אפס, ערך זה ידלג. |
| 0x8 | כניסה הבאה | כניסה הבאה |

### נתוני רילוקיישן
נתוני המעבר הם רשימה אחת או יותר של מבני בתים בגודל 0x8. סוף כל רשימה מסומן בקוד הסוג המיוחד 203:
| קיזוז | שם | גודל | תיאור |
-------|------------|------------|-----|
| 0x0 | קיזוז | 2 | קיזוז בבתים מהמעבר הקודם לזה. אם מדובר ברילוקיישן ראשון במדור, זה יחסית לתחילת המדור. |
| 0x2 | הקלד | 1 | סוג הרילוקיישן. מתואר להלן. |
| 0x3 | סעיף | 1 | הקטע של הסמל שכנגדו יש לעבור. עבור סוג הרילוקיישן המיוחד 202, זהו במקום זאת מספר הסעיף בקובץ זה שעליו חלים ערכי הרילוקיישן הבאים. |
| 0x4 | להוסיף | 4 | קיזוז בבתים של הסמל שיש להזיז מולו, ביחס לתחילת הקטע שלו. זוהי כתובת מוחלטת במקום עבור רילוקיישן נגד main.dol. |
| 0x8 | כניסה הבאה | כניסה הבאה | הכניסה הבאה |


 




## הפניות


* [פורמט מודול אובייקטים שניתן להעתיק](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


