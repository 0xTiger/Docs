{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ mpx", "פורמט קובץ mpx", "מהו קובץ mpx", "קובץ", "דוגמה לmpx", "סיומת קובץ mpx","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Microsoft Project Exchange Format",
  "description":"למד על פורמט קובץ MPX וממשקי API שיכולים ליצור ולפתוח קובצי MPX.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## מהו קובץ MPX? ##

קובץ עם סיומת .mpx הוא פורמט קובץ של Microsoft Exchange. פורמט קובץ MPX פותח על ידי Microsoft Project (MSP) כדי להקל על חילופי מידע על הפרויקט בין MSP ליישומים אחרים התומכים בפורמט הקובץ MPX, כולל Primavera Project Planner, Sciforma ואומדן מדויק של Timerline. באמצעות קבצי MPX, תוכל להעביר כל מיני מידע מפרויקט למערכת אחרת, כגון מידע מפורט על הקצאת משאבים, מידע על לוח שנה או מידע מתיבת הדו-שיח 'מידע על פרויקט'.

Microsoft Project 4.0 הציגה תמיכה ביצירה וקריאה של פורמטים של קבצי MPX שהמשיכו להיות בשימוש באמצעות Microsoft Project 98. עם זאת, התמיכה ביצירת קבצי MPX הפסיקה את יציאתו של Microsoft Project 2000, והגירסאות עד Microsoft Project 2010 תומכות בקריאה של MPX בלבד. פורמט קובץ MPX אינו נתמך בגרסאות מאוחרות יותר מ-MSP 2010.

## פורמט קובץ MPX ##

סקירה כללית של מפרטי קבצי MPX ניתנת בסעיף זה. ניתן למצוא מפרטים מלאים ב-[מאגר הידע](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) זה מאמר וניתן להפנות לפרטים.

### רשומות ###

רישום של קובץ MPX מורכב ממידע עבור הפרויקט. ישנם סוגים שונים של רשומות כאשר לכל רשומה יש סדר משלה. כל סוג רשומה מזוהה לפי מספר הרשומה שלו. עבור קובץ MPX, יש צורך להכיל את סוג הרשומה של יצירת קבצים. סוגים אחרים של רשומות אינם חובה. הטבלה הבאה מציגה את כל סוגי הרשומות, מספרי הרשומות שלהם ומספר הרשומות שכל סוג עשוי להכיל בקובץ MPX. הכללת רשומות בקובץ MPX חייבת לפעול לפי סדר הטבלה, עם הערות מוכנסות בכל מקום.

|שם רשומה|מספר רשומות|מספר מקסימלי של רשומות
---|---|---|
|יצירת קובץ (חובה)|ללא|1
|הגדרות מטבע|10|1
|הגדרות ברירת מחדל|11|1
|הגדרות תאריך ושעה|12|1
|הגדרת לוח שנה בסיסית|20|250
|שעות לוח שנה בסיס|25| 7 לכל רשומת הגדרת לוח שנה בסיסית
|חריג יומן בסיס|26| 250 לכל רשומת הגדרת לוח שנה בסיסית
|כותרת פרויקט|30|1
|הגדרת טבלת משאב טקסט|140|1- (או שאתה יכול להשתמש ברשומת הגדרת טבלת משאבים נומרית)
|הגדרת טבלת משאבים מספרית|41|1
|משאב|50|9,999
|הערות משאבים|51| 1 לכל רשומת משאב
|הגדרת לוח השנה של משאבים|55| 1 לכל רשומת משאב
|שעות לוח שנה של משאבים|56| 7 לכל יומן משאבים
|חריג יומן משאבים| 57|250 לכל יומן משאבים
|הגדרת טבלת משימות טקסט|60|1 (או שאתה יכול להשתמש ברשומת הגדרת טבלת משימות נומרית)
|הגדרת טבלת משימות מספרית|61|1
|משימה|70|9
|הערות משימה|71| 1 לכל רשומת משימה
|משימה חוזרת|72| 1 לכל רשומת משימה
|הקצאת משאבים|75| 100 לכל רשומת משימה
|שדות קבוצת עבודה|76| 1 לכל רשומת מטלות
|שמות פרויקט|80|500
|קישורי לקוחות DDE ו-OLE|81|500
|הערות|0|ללא הגבלה

### מבנה הקובץ ###

קובץ MPX מורכב מרשומות שהוזכרו לעיל המסודרות בצורה מוגדרת מראש בתוך הקובץ. פרטים על סוגי רשומות אלה נדונים כדלקמן:

**רשומה ליצירת קבצים (FCR):** זוהי רשומה חובה שמטרתה לזהות את:

* פורמט קובץ (MPX)
* תו מפריד רשימה בשימוש בקובץ
* תוכנית ומספר גרסה המשמשים ליצירת הקובץ
* מספר גרסה של פורמט הקובץ MPX המשמש בקובץ
* דף קוד המשמש ליצירת הקובץ

זו חייבת להיות הרשומה הראשונה בקובץ. בעת ייצוא מ-Microsoft Project, תו מפריד הרשימה מצוין בפריט הגדרות אזוריות בלוח הבקרה של Windows. רשומת FCR כוללת את השדות הבאים:

* MPX ומיד אחריו תו מפריד הרשימה
* שם תוכנית/מזהה
* מספר גרסה של הקובץ
* עמוד קוד (850, 437, MAC, ANSI)

לדוגמה, הרשומה יכולה להכיל מידע **MPX, Microsoft Project, 3.0**, המציין שפסיק משמש בתור תו מפריד הרשימה בקובץ MPX זה. הגרסה של פורמט MPX המשמשת בקובץ מיוצאת מגרסה 3.0 של Microsoft Project.

**הגדרות מטבע** רשומה זו, בעלת רשומה מספר 10, מציינת הגדרות עבור אפשרויות המטבע בתיבת הדו-שיח 'אפשרויות'. אם רשומה זו אינה כלולה, נעשה שימוש בהגדרות הנוכחיות בתיבת הדו-שיח 'אפשרויות'. המפרידים האלפים והעשרוניים מצוינים בפריט הגדרות אזוריות בלוח הבקרה של Windows.
השדות הכלולים ברשומה זו הם:

* סמל המטבע
* מיקום סמל (0 # אחרי, 1 # לפני, 2 # אחרי עם רווח, 3 # לפני עם רווח)
* ספרות מטבע (0,1,2)
* מפריד אלפים
* מפריד עשרוני

**דוגמה:** 10,$,1,2,",",.
דוגמה זו מציינת שערכי מטבע כוללים סימן דולר ($) לפניהם, ששתי ספרות נכללות אחרי הנקודה העשרונית, שפסיק משמש להפרדה בין אלפים ושנקודה משמשת כנקודה העשרונית. מכיוון שתו מפריד הרשימה נכלל בשדה מפריד אלפים, השדה מוקף במרכאות.

**הגדרות ברירת מחדל:** רשומה זו, בעלת רשומה מספר 11, מציינת הגדרות עבור אפשרויות ברירת המחדל בתיבת הדו-שיח 'אפשרויות'. אם לא צוין משך זמן, יש להגדיר את יחידת משך ברירת המחדל לחישובים נכונים של יחידת משך. אם רשומה זו אינה כלולה, נעשה שימוש בהגדרות הנוכחיות בתיבת הדו-שיח 'אפשרויות'.
השדות הכלולים ברשומה זו הם:

* יחידות משך ברירת מחדל (0 # דקות, 1 # שעות, 2 # ימים, 3 # שבועות)
* סוג משך ברירת מחדל (0 # לא קבוע, 1 # קבוע)
* יחידות עבודה ברירת מחדל (0 # דקות, 1 # שעות, 2 # ימים, 3 # שבועות)
* שעות ברירת מחדל/יום
* ברירת מחדל שעות/שבוע
* תעריף סטנדרטי ברירת מחדל
* ברירת מחדל תעריף שעות נוספות
* עדכון סטטוס משימה עדכוני מצב משאב (0 # לא, 1 # כן)
* פיצול משימות בתהליך (0 # לא, 1 # כן)

**הגדרות תאריך ושעה:** רשומה זו, בעלת רשומה מספר 12, מציינת הגדרות עבור אפשרויות התאריך והשעה בתיבת הדו-שיח Options, ואת האפשרות Bar Text Date Format בתיבת הדו-שיח פריסה. אם רשומה זו אינה כלולה, נעשה שימוש בהגדרות הנוכחיות בתיבת הדו-שיח 'אפשרויות'.
\\השדות הכלולים ברשומה זו הם:

* סדר תאריך (0 # חודש/יום/שנה, 1 # יום/חודש/שנה, 2 # שנה/חודש/יום)
* פורמט זמן (0 # 12 שעות, 1 # 24 שעות)
* זמן ברירת מחדל (מספר דקות אחרי חצות)
* מפריד תאריכים
* מפריד זמן
* 0:00 עד 11:59 טקסט
* 12:00 עד 23:59 טקסט
* פורמט תאריך (0 -14)*
* פורמט תאריך של טקסט פס (0 -194)*

**הגדרת לוח שנה בסיסית:** רשומות אלה, בעלות רשומה מספר 20, מגדירות את לוחות השנה הבסיסיים ואת ימי העבודה והאי-עבודה שלהם בשבוע. הגדרות ברירת המחדל משמשות אם אין כניסה במשך יום אחד. הגדרות ברירת המחדל הן שני עד שישי עבור ימי עבודה ושבת וראשון עבור ימי עבודה שאינם. ברשומה זו, השדה שם נדרש. עבור כל אחד מהימים, ערך 0 מציין שהיום הוא יום שאינו יום עבודה, וערך 1 מציין שהיום הוא יום עבודה.
השדות הכלולים ברשומה זו הם:

*שם
* יום ראשון
*יום שני
* יום שלישי
* יום רביעי
* יום חמישי
*שישי
* יום שבת

**שעות בסיס לוח שנה:** רשומות אלה, בעלות רשומה מספר 25, מציינות את שעות העבודה עבור ימות השבוע אם הן שונות מהגדרות ברירת המחדל. ברירת המחדל של שעות העבודה היא 8:00 עד 12:00 ו-13:00 עד 17:00. כל רשומת שעות בסיס לוח שנה מתייחסת לרשומת הגדרת לוח השנה הבסיסית הקודמת. עד שבע מהרשומות הללו יכולות לעקוב אחר כל רשומת הגדרת לוח שנה בסיסית.

* יום בשבוע (1 - 7, כאשר 1 # יום ראשון ו-7 # שבת)
* מזמן 1
* לזמן 1
* מזמן 2
* לזמן 2
* מזמן 3
* לזמן 3

**חריג לוח שנה בסיסי:** רשומות אלה, בעלות רשומה מספר 26, מגדירות את החריגים לימים ולשעות שצוינו בשני סוגי הרשומות הקודמים. עד 250 מהרשומות הללו יכולות לעקוב אחר כל רשומת הגדרת לוח שנה בסיסית. יש לרשום רשומות אלו בסדר כרונולוגי. אם חריג הוא יום אחד, אתה יכול להשאיר את השדה עד תאריך ריק. אם לא מצוין שעות, נעשה שימוש בזמני ברירת המחדל של 8:00 עד 12:00 ו-13:00 עד 17:00.
השדות הכלולים ברשומה זו הם:

* מתאריך
* עד היום
* לא עובד/עובד (0 # לא עובד, 1 # עובד)
* מזמן 1
* לזמן 1
* מזמן 2
* לזמן 2
* מזמן 3
* לזמן 3

**כותרת פרויקט:** רשומה זו, בעלת ערך רשומה 30, מגדירה שדות פרויקט גלובליים, כגון תאריך תחילת הפרויקט ותאריך סיום הפרויקט. השדות ברשומה זו תואמים את המידע בתיבות הדו-שיח פרטי פרויקט וסטטיסטיקה.
השדות והכרטיסיות הכלולים ברשומה זו הם:

* לשונית פרויקט
* חברה
* מנהל
* לוח שנה (בשימוש רגיל אם אין כניסה)
* תאריך התחלה (השדה הזה או השדה הבא מחושב עבור קובץ מיובא, בהתאם להגדרת תזמון מאת)
* תאריך סיום
* לוח זמנים מ (0 # התחלה, 1 # סיום)
* דייט נוכחי*
* הערות
* עלות
* עלות בסיס
* עלות אמיתית
* עבודה
* עבודת בסיס
* עבודה בפועל
* עבודה
*משך*
*משך בסיס*
* משך בפועל
* אחוז השלמה
* התחלת בסיס
* גימור בסיס
* התחלה בפועל
* גימור בפועל
* שונות התחל
* שונות גימור
* נושא
* מחבר
* מילות מפתח

**הגדרת טבלת משאבי טקסט**: רשומה זו מפרטת את שדות המשאבים, לפי הסדר, המיובאים או מיוצאים. עבור קבצים מיובאים, השמות חייבים להתאים לשמות השדות המשמשים ב-Microsoft Project. עבור קבצים מיוצאים, רשומה זו מגיעה מטבלת ייצוא המשאבים. יש להשתמש ברשומה זו או ברשומת ההגדרה של טבלת משאבים נומרית. בעת ייצוא מ-Microsoft Project, שתי הרשומות הללו נכללות.

**הגדרת טבלת משאבים מספרית:** באמצעות מספרים במקום שמות, רשומה זו מפרטת את שדות המשאבים, לפי הסדר, שמיובאים או מיוצאים. זוהי שיטה חלופית לזיהוי שדות המשאבים הכלולים בכל רשומת משאב והיא שימושית בעת הגדרת קובץ MPX שנוצר על ידי מוצר בשפה זרה.

**משאב:** רשומות אלה מכילות את המידע עבור כל משאב המיובא או מיוצא. כל רשומת משאב מתארת משאב אחד. כאשר אתה מייבא מידע, השדות הכלולים מוגדרים על ידי רשומת הגדרת טבלת משאב טקסט או רשומת הגדרת טבלת משאבים נומרית. כאשר אתה מייצא מידע, השדות הכלולים הם אלה המפורטים בטבלת ייצוא המשאבים.

**הערות משאבים:** רשומות אלה מכילות הערות לגבי רשומת המשאבים הקודמת. עבור שורה חדשה בתוך ההערה, נעשה שימוש בתו ASCII 127. אם ההערה כוללת את תו מפריד הרשימה, הקף את ההערה במרכאות.

**הגדרת לוח השנה של משאבים:** רשומות אלה מגדירות את ימי העבודה עבור המשאב שצוין ברשומת המשאב הקודמת. עבור קבצים מיובאים, אם אין ערך עבור השדה Base Calendar Name, נעשה שימוש ב-Standard. שום ערך עבור היום הספציפי לא מציין שהיום מוגדר כברירת מחדל (2). אם אין רשומות הגדרת לוח שנה של משאב, Standard משמש כלוח השנה הבסיסי עבור המשאב, כאשר ברירת המחדל משמשת עבור הימים. עבור כל אחד מהימים, ערך 0 מציין שהיום הוא יום שאינו יום עבודה, 1 מציין שהיום הוא יום עבודה ו-2 מציין כי נעשה שימוש ברירת המחדל.

**שעות לוח שנה של משאב:** רשומות אלו מגדירות את שעות העבודה עבור המשאב השונות מלוח השנה הבסיסי בשימוש המשאב. רשומות אלה חלות על רשומת הגדרת לוח השנה של משאב הקודמת לרשומה זו. עד שבע מהרשומות הללו יכולות לעקוב אחר כל רשומת הגדרת לוח השנה של משאב.

**חריג יומן משאבים:** רשומות אלו מגדירות את החריגים לימים ולשעות שצוינו בשני סוגי הרשומות הקודמים. עד 250 מהרשומות הללו יכולות לעקוב אחר כל רשומת הגדרת לוח השנה של משאב. יש לרשום רשומות אלו בסדר כרונולוגי. אם החריגה היא רק יום אחד, אתה יכול להשאיר את השדה עד תאריך ריק. אם לא מצוין שעות, נעשה שימוש בזמני ברירת המחדל של 8:00 עד 12:00 ו-13:00 עד 17:00.

**הגדרת טבלת משימות טקסט:** רשומה זו מפרטת את שדות המשימות, לפי הסדר, המיובאים או מיוצאים. עבור קבצים מיובאים, השמות חייבים להתאים לשמות השדות המשמשים ב-Microsoft Project. אם הקובץ מיוצא, רשומה זו מגיעה מטבלת ייצוא המשימות. בעת ייצוא מ-Microsoft Project, שתי הרשומות הללו נכללות. שדות המחושבים על ידי Microsoft Project, כגון התחלה מתוזמנת וסיום מתוזמן, מתעלמים אם מיובאים. אם יש לך תאריכי התחלה או סיום של משימות קבועים, השתמש בשדות סוג אילוץ ותאריך אילוץ.

**הגדרת טבלת משימות מספרית:** באמצעות מספרים במקום שמות, רשומה זו מפרטת את שדות המשימות, לפי סדר, המיובאים או המיוצאים. זוהי שיטה חלופית לזיהוי שדות המשימות הכלולים בכל רשומת משימה והיא שימושית בעת הגדרת קובץ MPX שנוצר על ידי מוצר בשפה זרה.

**משימה:** רשומות אלה מכילות את המידע עבור כל משימה המיובאת או מיוצאת. כל רשומת משימה מתארת משימה אחת. כאשר אתה מייבא מידע, השדות הכלולים מוגדרים על ידי רשומת הגדרת טבלת משימות טקסט או רשומת הגדרת טבלת משימות נומרית. כאשר אתה מייצא מידע, השדות הכלולים הם אלה המפורטים בטבלת ייצוא המשימות.

**הערות משימה:** רשומות אלה מכילות הערות לגבי רשומת המשימה הקודמת. השתמש בתו ASCII 127 כדי לציין שורה חדשה בתוך ההערה. אם ההערה כוללת את תו מפריד הרשימה, הקף את ההערה במרכאות.

**הקצאת משאבים**: רשומות אלה מפרטות מידע על המשאבים שהוקצו למשימה שהוגדרה ברשומת המשימה הקודמת. אם אתה ממזג קבצים ואתה רוצה שיישמר מידע על הקצאת משאבים, עליך לכלול את המידע בקובץ MPX. אם תמזג, כל ההקצאות הקיימות במשימות ממוזגות יימחקו. אם אתה ממזג קבצים על סמך מזהים ייחודיים, משאבים מוקצים באמצעות מזהים ייחודיים של משאב ולא מזהים.

**שדות קבוצת עבודה של הקצאת משאבים:** רשומות אלה מפרטות את המידע המאוחסן עם כל הקצאה עבור תכונות קבוצת העבודה של Microsoft Project 4.0 ו-4.1. אם אתה משתמש בתכונות קבוצת העבודה, עליך לכלול את הרשומה הזו כדי להבטיח שאף אחד מהמידע לא יאבד.

**שמות פרויקטים:** רשומות אלה מפרטות את כל שמות קישורי ה-DDE המאוחסנים בפרויקט.

**קישורי לקוח DDE ו-OLE:** רשומות אלה מפרטות את קישורי ה-DDE לתוך הפרויקט.

**הערות:** ניתן להשתמש ברשומות אלו להוספת הערות לקובץ ויכולות להופיע בכל מיקום בקובץ. כל רשומת הערות חייבת להתחיל ב-"0".

## בעיות בפתיחת קובץ MPX ##

להלן רשימה של כמה בעיות נפוצות שעלולות להתעורר ולגרום לתפקוד שגוי של פורמט MPX:

* היעדר תוכנה תומכת
* קובץ פגום
* קובץ נגוע עקב וירוס
* אין זכות גישה במערכת לפתיחת הקבצים
* כונן מיושן במערכת שלך
* שם ההרחבה של הקובץ שונה

## הפניות ##

* [MPX - Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)
