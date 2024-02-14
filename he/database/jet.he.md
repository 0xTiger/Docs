{
"date": "2023-09-05",
  "keywords": [
"מטוס סילון",
"קובץ סילון",
"מהו קובץ סילון",
"קובץ מסד הנתונים של JET Microsoft Access",
"איך פותחים קובץ ג'ט",
"קוֹבֶץ",
"סיומת קובץ jet",
"סיומת"
],
  "author": {
"display_name": "שייק פאיז"
},
"draft": "false",
"toc": true,
"title": "פורמט קובץ JET - קובץ מסד הנתונים של Microsoft JET",
  "description":"למד על פורמט JET וממשקי API שיכולים ליצור ולפתוח קבצי JET.",
  "linktitle": "JET",
  "menu": {
    "docs": {
      "identifier": "database-jet",
      "parent": "database"
}
},
"lastmod": "2023-09-05"
}

## מהו קובץ JET?

קובץ מסד נתונים של JET, הידוע גם כקובץ מסד נתונים של Microsoft Access, הוא פורמט קובץ המשמש את Microsoft Access, מערכת ניהול מסד נתונים פופולרית (DBMS). JET מייצג Joint Engine Technology, שהיה השם המקורי של מנוע מסד הנתונים שבו השתמשה Microsoft Access. גרסאות מאוחרות יותר של Access השתמשו במנועי מסד נתונים שונים, אך המונח "בסיס נתונים JET" עדיין משמש בדרך כלל כדי להתייחס לבסיסי נתונים של Access.

הנה כמה נקודות מפתח לגבי קבצי מסד נתונים של JET:

- **הרחבת קבצים:** לקבצי מסד נתונים של JET יש בדרך כלל סיומת קובץ של ".mdb" עבור גרסאות ישנות יותר של Access (Access 2003 ומעלה) ו-".accdb" עבור גרסאות חדשות יותר (Access 2007 ואילך). קבצי ".mdb" משתמשים במנוע מסד הנתונים הישן יותר של JET, בעוד שקבצי ".accdb" משתמשים בטכנולוגיית ACE (Access Database Engine) החדשה יותר.

- **מסד נתונים יחסי:** מסדי נתונים של JET הם מסדי נתונים יחסיים, כלומר הם מאחסנים נתונים בטבלאות עם קשרים מוגדרים ביניהם. משתמשים יכולים ליצור, לשנות ולשאול נתונים באמצעות SQL (Structured Query Language) או דרך הממשק הגרפי של Access.

- **אחסון נתונים:** מסדי נתונים של JET יכולים לאחסן מגוון רחב של סוגי נתונים, כולל טקסט, מספרים, תאריכים, תמונות ועוד. הם יכולים גם להתמודד עם מבני נתונים מורכבים וקשרים בין טבלאות.

- **גישה מרובה משתמשים:** מסדי נתונים של JET תומכים בגישה מרובה משתמשים, ומאפשרים למספר משתמשים לעבוד עם מסד הנתונים בו זמנית, אם כי יכולות להיות מגבלות מבחינת מדרגיות וביצועים עבור יישומים בקנה מידה גדול.

- **שילוב:** ניתן לשלב מסדי נתונים של Access עם יישומי Microsoft Office אחרים כמו Excel ו-Outlook, מה שהופך אותו נוח למשתמשים להחליף נתונים בין תוכניות שונות.

## מידע על מאגרי מידע של JET

**היסטוריה של מנוע JET:**

מנוע מסד הנתונים JET (Joint Engine Technology) פותח במקור על ידי מיקרוסופט בתחילת שנות ה-90 לשימוש ב-Microsoft Access. המנוע תוכנן להיות פתרון מסד נתונים קל משקל, מונחה שולחני עבודה, שניתן לשלב במוצרים שונים של מיקרוסופט.

**רכיבים של מסד נתונים של JET**

- **טבלאות:** מסדי נתונים של JET מאחסנים נתונים בטבלאות, שהן אוספים של רשומות המאורגנות בשורות ובעמודות.
- **שאילתות:** משתמשים יכולים ליצור שאילתות כדי לחלץ, לסנן ולתפעל נתונים מטבלאות באמצעות SQL (שפת שאילתות מובנית).
- **טפסים:** Access מספק מעצב טפסים המאפשר למשתמשים ליצור קלט נתונים מותאמים אישית ולהציג טפסים.
- **דוחות:** משתמשים יכולים להפיק דוחות בעלי מראה מקצועי מהנתונים המאוחסנים במסד הנתונים.
- **פקודות מאקרו ו-VBA:** משתמשים יכולים להפוך משימות לאוטומטיות ולהוסיף פונקציונליות מותאמת אישית באמצעות פקודות מאקרו או על ידי כתיבת קוד VBA.

**סוגי מידע**

מסדי נתונים של JET תומכים במגוון סוגי נתונים, כולל:

- **טקסט:** לאחסון תווים אלפאנומריים.
- **מספר:** עבור ערכים מספריים.
- **תאריך/שעה:** לערכי תאריך ושעה.
- **תזכיר:** לטקסט או הערות ארוכים יותר.
- **היפר-קישור:** לקישורי אינטרנט וכתובות דוא"ל.
- **קובץ מצורף:** לאחסון קבצים וקבצים מצורפים.

## איך פותחים קובץ JET?

תוכניות הפותחות או מתייחסות לקבצי JET כוללות

- Microsoft Access 365 (גרסת ניסיון בחינם)

## קבצי JET אחרים

- [JET - The Jackbox Party Pack Settings](/he/settings/jet/)


## הפניות
* [Access Database Engine](https://en.wikipedia.org/wiki/Access_Database_Engine)
