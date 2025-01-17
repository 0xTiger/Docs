{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - פורמט קובץ מאגר מידע אישי של Outlook",
  "description":"למד על פורמט קובץ PST וממשקי API שיכולים ליצור ולפתוח קובצי PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ PST?

קבצים עם סיומת .pst מייצגים קבצי אחסון אישיים של Outlook (הנקראים גם טבלת אחסון אישית) המאחסנים מגוון מידע על המשתמש. פרטי המשתמש מאוחסנים בתיקיות מסוגים שונים הכוללות מיילים, פריטי לוח שנה, הערות, אנשי קשר ועוד מספר פורמטים של קבצים. קובצי PST משמשים לארכיון נתוני אימייל במצב לא מקוון שניתן לטעון ולהציג מאוחר יותר ביישומים שונים.

## מפרטי פורמט קובץ PST

פורמט קובץ PST [מפרטים](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) זמינים מ-Microsoft כרישוי פטנט בחינם ובלתי חוזר דרך הבטחת המפרט הפתוח .

### סוג פורמטי PST

פורמטים של קבצי PST מסווגים בשני סוגים על סמך הקידוד של סוג הקובץ. קובצי PST מקודדים ANSI הם פורמטי קבצים ישנים יותר ונתמכים על ידי Outlook 2002 וגרסאות קודמות בלבד. לקבצים כאלה יש מגבלת גודל מקסימלית של 2 GB (2^^31^^ Bytes) ואינם תומכים ב-Unicode. סוג פורמט קובץ מודרני יותר, המבוסס על קידוד Unicode, מסיר את מגבלת גודל הקובץ ויכול להגיע לגודל נתונים מקסימלי של 50GB.

### ארגון לוגי של פורמט קובץ PST

בבסיס פורמט קובץ PST נמצא B-Tree ששומר על מיון נתונים ומאפשר חיפושים, גישה רציפה, הוספות, מחיקות וכו' בזמן לוגריתמי. המבנה הכללי של קובץ PST מאורגן בשלוש שכבות.

![Logical layers of a PST file](/he/email/PST-1.png "Logical layers of a PST file")

`שכבת מסד נתונים של צומת (NDB)` - שכבת מסד נתונים של צומת נמצאת ברמה התחתונה של קובץ PST וכוללת מסד נתונים של צמתים. צמתים אלה למעשה מייצגים מתקני אחסון ברמה נמוכה יותר של פורמט קובץ PST. שכבת NDB כוללת מידע על כותרת, הקצאת קבצים, בלוקים ו-BTrees (צומת BTree ובלוק BTree) מנקודת מבט של אחסון. צמתים ובלוקים של שכבת NDB מקושרים באמצעות Data BID שהוא אחד מארבעת המאפיינים של הפניה לצומת, כלומר NID (מזהה צומת), NID אב, BID נתונים (BID BID) ו-SubNode BID.

שכבת `רשימות, טבלאות ומאפיינים -` שכבת LTP מספקת הבנה לוגית של מושגים ברמה גבוהה יותר על גבי NDB. מלבד אלמנטים אחרים, שכבת LTP מורכבת בעיקר מהקשר נכסים (PC) והקשר טבלה (TC). PC הוא אוסף של מאפיינים, בעוד ש-TC מייצג מטריצה דו מימדית של אוסף מאפיינים לעומת נוכחותם של אלה. יישום יעיל של מחשבי PC ו-TCs, שכבת ה-LTP משתמשת בשני סוגים של מבני נתונים על גבי צומת NDB:

* Heap On Node (HN) - מאפשר הקצאת משנה של זרם הנתונים של צומת למקטעים קטנים בגודל משתנה.
* BTree on Heap (BTH) - BTH מספק דרך נוחה ופרקטית לחיפוש דרך מחשבי נתונים, המתוארים לעיל, מיושמים כ-BTH וזו הסיבה שהוא מיושם על ידי בנייה בתוך מבנה HN.

`שכבת הודעות -` כללים ברמה גבוהה יותר והיגיון עסקי לעבודה עם קבצי PST מיושמים בשכבה זו. הפלט הלוגי של שכבה זו נובע כאובייקטי תיקיה, אובייקטי הודעה, אובייקטים מצורפים ומאפיינים אשר מתאפשר על ידי שילוב שכבות LTP ו-NDB. כללים ודרישות, שיש לפעול לפיהם בעת שינוי תוכן ה-PST, מוגדרים גם הם בשכבה זו.

### ארגון פיזי של פורמט קובץ PST

רמה גבוהה של ארגון הקבצים של קובץ PST היא כפי שמוצג באיור למטה. זוהי רק סקירה כללית של מושגים שונים מאלמנטים לוגיים של קובץ PST.

![Physical organization of the PST file format](/he/email/PST-2.png "Physical organization of the PST file format")


#### מידע על כותרת PST

מבנה HEADER של קובץ PST ממוקם ממש בתחילת הקובץ ב-0 offset. הוא מכיל מידע על מטא נתונים על קובץ ה-PST ומידע ROOT כדי לגשת למבני הנתונים של שכבת NDB שתוארו לעיל. מבנה HEADER שונה עבור גרסאות Unicode ו-ANSI של פורמט קובץ PST.

הכותרת מתחילה במילת קסם של 4 בתים **!BDN** המיוצגת על ידי בתים (0x21, 0x42, 0x44, 0x4E). מספר קסם נוסף של 2 בתים, **SM** (0x53, 0x4D), ממוקם בהיסט 8 מתחילת הקובץ. מידע הגרסה (ANSI או Unicode) נמצא בהיסט של 10 מתחילת הקובץ. ערך Hex (0x17) מציין קובץ Unicode PST בעוד 0x0E או 0x0F מייצגים פורמט קובץ ANSI.

|שדה|תיאור
---|---|
|dwMagic (4 בתים)|חייב להיות "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 בתים)|ערך CRC של 32 סיביות של 471 בתים של נתונים החל מ-wMagicClient (0ffset 0x0008)
|wMagicClient (2 בתים)|חייב להיות "{ 0x53, 0x4D }".
|wVer (2 בתים)|גרסת פורמט קובץ. ערך זה חייב להיות 14 או 15 אם הקובץ הוא קובץ ANSI PST, וחייב להיות 23 אם הקובץ הוא קובץ Unicode PST.
|wVerClient (2 בתים)|גרסת פורמט קובץ לקוח. הגרסה המתאימה לפורמט המתואר במסמך זה היא 19. יוצרים של קובץ PST חדש המבוסס על מסמך זה צריכים לאתחל ערך זה ל-19.
|bPlatformCreate (1 בייט)|ערך זה חייב להיות מוגדר ל-0x01.
|bPlatformAccess (1 בתים)|ערך זה חייב להיות מוגדר ל-0x01.
|dwReserved (8 בתים)|
|bidUnused (8 בתים Unicode בלבד)|ריפוד לא בשימוש נוסף כאשר פורמט קובץ ה-Unicode PST נוצר.
|bidNextP (Unicode: 8 בתים; ANSI: 4 בתים)| BID בעמוד הבא. לדפים יש מונה מיוחד להקצאת ערכי bidIndex. הערך של bidIndex עבור הצעות מחיר עבור דפים מוקצה ממונה זה.
|bidNextB (4 בתים ANSI בלבד): |BID הבא. ערך זה הוא המונה המונוטוני המציין את ה-BID שיש להקצות לבלוק המוקצה הבא. ערכי BID מתקדמים במרווחים של 4. לפרטים נוספים, ראה סעיף 2.2.2.2.
|dwUnique (4 בתים)|זהו ערך מונוטוני שעולה בשינוי בכל פעם שמבנה HEADER של קובץ ה-PST משתנה. תפקידו של ערך זה הוא לספק ערך ייחודי, ולהבטיח ש-HEADER CRCs שונים לאחר כל שינוי כותרת.
|rgnid[]   (128 בתים)|מערך קבוע של 32 NIDs, כל אחד מתאים לאחד מ-32 ה-NID_TYPEs האפשריים (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_MESSAGE)_ASS_MESSAGE)
|qwUnused (8 בתים)|שטח לא בשימוש; חייב להיות מוגדר לאפס. פורמט קובץ PST של Unicode בלבד.
|root (Unicode: 72 בתים; ANSI: 40 בתים)|מבנה ROOT (סעיף 2.2.2.5).
|dwAlign (4 בתים)|בתי יישור שאינם בשימוש; חייב להיות מוגדר לאפס. פורמט קובץ PST של Unicode בלבד.
|rgbFM (128 בתים)|FMap שהוצא משימוש. זה כבר לא בשימוש ויש למלא אותו ב-0xFF. הקוראים צריכים להתעלם מהערך של בתים אלה.
|rgbFP (128 בתים)|FPMap שהוצא משימוש. זה כבר לא בשימוש ויש למלא אותו ב-0xFF. הקוראים צריכים להתעלם מהערך של בתים אלה.
|bSentinel (1 בייט)|חייב להיות מוגדר ל-0x80.
|bCryptMethod (1 בתים)|מציין כיצד הנתונים בתוך קובץ ה-PST מקודדים. חייב להיות מוגדר לאחד מהערכים המוגדרים מראש (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserved (2 בתים)| שמורות; חייב להיות מוגדר לאפס.
|bidNextB (8 בתים)|מציין את ערך BID הזמין הבא. פורמט קובץ PST של Unicode בלבד.
|bidNextB (יוניקוד בלבד: 8 בתים)|הצעת מחיר הבאה. ערך זה הוא המונה המונוטוני המציין את ה-BID שיש להקצות לבלוק המוקצה הבא. ערכי BID מתקדמים במרווחים של 4. לפרטים נוספים, ראה סעיף 2.2.2.2.
|dwCRCFull (4 בתים)|ערך CRC של 32 סיביות של 516 בתים של נתונים החל מ-wMagicClient ועד bidNextB, כולל. פורמט קובץ PST של Unicode בלבד.
|ullReserved (8 בתים)|שמורה; חייב להיות מוגדר לאפס. פורמט קובץ ANSI PST בלבד.
|dwReserved (4 בתים)|שמורה; חייב להיות מוגדר לאפס. פורמט קובץ ANSI PST בלבד.
|rgbReserved2 (3 בתים)|
|bשמורה (1 בייט) |
|rgbReserved3 (32 בתים) |

### הגנת מידע ###

מטעמי אבטחה, קבצי PST יכולים להיות מוגנים באמצעות סיסמה, מה שמחייב את יישום הטעינה להחיל סיסמה לפני שניתן יהיה לצפות בהם. הסיסמה המוחלת על קובץ ה-PST מאוחסנת בחנות ההודעות. עם זאת, זה לא מספק הגנה חזקה על נתונים מכיוון שניתן להסיר את הסיסמה על ידי כלים זמינים. כמו כן, סיסמה שצוינה על ידי המשתמש אינה משמשת כחלק מהמפתח לקידוד ופענוח אלגוריתמי צופן. לפיכך, אין שום תועלת בהגנה על נתונים אליהם גורמים לא מורשים לגשת אליהם. אחסון של סיסמה כ- CRC-32 hash של המחרוזת המקורית גם הופך אותה לשיטה חלשה לאבטחת נתונים נגד גישת כוח גס.

## הפניות ##

* [פורמט קובץ של תיקיות אישיות של Outlook (.pst)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [מפרט פורמט קובץ תיקייה אישית](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

