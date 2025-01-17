{
  "date" : "2021-08-24",
  "keywords" :[ "קובץ trc", "פורמט קובץ trc", "מהו קובץ trc", "קובץ", "דוגמה ל-trc", "סיומת קובץ trc","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ TRC וממשקי API שיכולים ליצור ולפתוח קובצי TRC.",
  "title" :"TRC - SQL Server Trace File",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## מהו קובץ TRC?
קובץ עם סיומת .trc מכיל את תוצאות המעקב של הפעילות של מסד נתונים של שרת Miscrosoft SQL. קבצים אלה נוצרים על ידי תוכנת SQL Server Profiler; בדרך כלל ארוז עם תוכנת Microsoft SQL Server. מנהלי מסד הנתונים יכולים לנתח רצף של הצהרות מסד נתונים ויכולים לעיין ביומן המעקב אם יש חשד לסוג כלשהו של שגיאות או אזהרות. קבצים אלה ממוקמים בדרך כלל בתיקיית LOG הטיפוסית של MSSQL בתוך ספריית Program Files במערכת הפעלה Windows.

## פורמט קובץ TRC
פורמט הקובץ TRC משמש את SQL Server Profiler כדי ליצור באופן אוטומטי עקבות חדשה של ההצהרות שבוצעו לאחרונה על ידי שרת MS SQL. SQL Server Profiler משתמש בתבנית ברירת המחדל עבור כל מעקב חדש. עם זאת, התוכנה כוללת מספר תבניות מוגדרות מראש לניטור סוגים מסוימים של אירועים. כמו כן, ניתן להשתמש ב-SQL Server Profiler ליצירת תבניות שמגדירות את מחלקות האירועים ועמודות הנתונים שיש לכלול במעקבים.

### תבניות מוגדרות מראש
להלן רשימה של כמה תבניות מוגדרות מראש הכלולות ב-SQL Server Profiler:
- **SP_Counts**: לוכדת התנהגות ביצוע פרוצדורה מאוחסנת לאורך זמן.
- **סטנדרטי**: נקודת מוצא כללית ליצירת עקבות.
- **TSQL**: לוכדת את כל הצהרות Transact-SQL שנשלחות ל-SQL Server על ידי לקוחות ואת הזמן שהופק.
- **TSQL_Duration**: לוכד את כל הצהרות Transact-SQL שנשלחו ל-SQL Server על ידי לקוחות, זמן הביצוע שלהם, ומקבץ אותם לפי משך.
- **TSQL_Grouped**: השתמש כדי לחקור שאילתות מלקוח או משתמש מסוים.
- **TSQL_Locks**: השתמש לפתרון בעיות בקיפאון, נעילת פסק זמן ונעילה של אירועי הסלמה.
- **TSQL_Replay**: השתמש לביצוע כוונון איטרטיבי, כגון בדיקות בנצ'מרק.
- **TSQL_SPs**: השתמש כדי לנתח את השלבים המרכיבים של נהלים מאוחסנים.
- **כוונון**: השתמש להפקת פלט עקבות ש-Database Engine Tuning Advisor יכול להשתמש בו כעומס עבודה לכוונון מסדי נתונים.
### מתאם מעקב עם נתוני יומן הביצועים של Windows
ניתן להשתמש ב-SQL Server Profiler לפתיחת יומן ביצועים של Microsoft Windows, כדי לבחור את המונים שיתלוו ל-Trace, ולהציג את מוני הביצועים שנבחרו לצד ה-Trace בממשק המשתמש של MS SQL Server Profiler. כדי לציין את נתוני יומן הביצועים המתואמים עם אירוע המעקב שנבחר, פס אדום אנכי בחלונית חלון הנתונים של System Monitor של SQL Server Profiler.


## הפניות ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

