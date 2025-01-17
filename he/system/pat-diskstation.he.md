{
"תאריך":"2023-11-01",
   "keywords":[
"טְפִיחָה",
"קובץ pat",
"pat diskstation manager file",
"איך פותחים קובץ pat",
"קוֹבֶץ",
"סיומת קובץ pat",
"סיומת",
"קוֹבֶץ"
],
   "author":{
"display_name":"שייק פאיז"
},
"draft": "false",
"toc":true,
"title": "פורמט קובץ PAT - קובץ התקנת DiskStation Manager",
   "description":"למד על פורמט קובץ התקנת PAT DiskStation Manager וממשקי API שיכולים ליצור ולפתוח קובצי PAT.",
   "linktitle":"PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation",
         "parent":"system"
}
},
"lastmod":"2023-11-01"
}

## מהו קובץ PAT?

קובץ PAT משויך בדרך כלל ל-**DiskStation Manager (DSM)**, מערכת הפעלה המשמשת את התקני Synology Network-Attached Storage (NAS). קובץ PAT הוא קובץ התקנה המשמש לעדכון או התקנה של ה-DSM ב-Synology NAS.

## שימוש בקובץ PAT

כך אתה משתמש בדרך כלל בקובץ PAT כדי להתקין או לעדכן DSM ב-Synology NAS:

1. הורד קובץ PAT: אתה יכול להשיג קובץ PAT מאתר Synology הרשמי או ממקורות מהימנים אחרים.
    







2. היכנס ל-NAS שלך: גש לממשק המשתמש מבוסס האינטרנט של Synology NAS שלך על ידי הזנת כתובת ה-IP שלו בדפדפן אינטרנט. תזדקק להרשאות מנהל כדי לבצע פעולה זו.
    







3. עבור אל מרכז החבילות: בממשק האינטרנט, נווט אל "מרכז החבילות". זה המקום שבו אתה מנהל ומתקין יישומים ב-NAS שלך.
    







4. התקנה ידנית: ב-Package Center, צריכה להיות אפשרות ל"התקנה ידנית" או "התקנה/עדכון" בהתאם לגרסת ה-DSM שבה אתה משתמש. בחר באפשרות זו.
    







5. עיין בקובץ PAT: תתבקש לעיין בקבצים המקומיים שלך ולבחור בקובץ PAT שהורד.
    







6. התקנה או עדכון: לאחר בחירת קובץ PAT, עקוב אחר ההוראות שעל המסך כדי להתקין DSM (אם זו התקנה חדשה) או לעדכן DSM (אם אתה משדרג לגרסה חדשה יותר).
    







7. המתן להשלמה: תהליך ההתקנה או העדכון עשוי להימשך זמן מה וה-NAS שלך עשוי לאתחל מחדש כחלק מהתהליך. היו סבלניים וחכו שזה יסתיים.
    







8. תצורה לאחר ההתקנה: לאחר ההתקנה או העדכון, ייתכן שיהיה עליך להגדיר את הגדרות ה-NAS שלך בהתאם להעדפותיך.

## מנהל DiskStation

DiskStation Manager, המקוצר לעתים קרובות כ-DSM, היא מערכת הפעלה שפותחה על ידי Synology עבור התקני ה-Network-Attached Storage (NAS) שלהם. הוא משמש כממשק ניהול ובקרה עבור שרתי Synology NAS. DiskStation Manager מספק ממשק מבוסס אינטרנט ידידותי למשתמש המאפשר למשתמשים להגדיר ולנהל היבטים שונים של ה-NAS שלהם כגון אחסון נתונים, שיתוף קבצים, פתרונות גיבוי, שירותי מולטימדיה ועוד.

DSM ידוע בזכות הרבגוניות שלו ובמערכת האקולוגית הנרחבת שלו, המאפשרת למשתמשים להתקין ולהפעיל יישומים ושירותים שונים ב-Synology NAS שלהם והופכת אותו לשרת רב תכליתי לשימוש ביתי ועסקי כאחד. חלק מהפונקציות הנפוצות של DiskStation Manager כוללות שיתוף קבצים, גיבוי וסנכרון נתונים, הזרמת מדיה, תכונות אבטחה ותמיכה בווירטואליזציה.

Synology משחררת באופן קבוע עדכונים וגרסאות חדשות של DSM כדי לשפר את האבטחה, הביצועים והתכונות. משתמשים יכולים לעדכן את DSM באופן ידני באמצעות קובצי PAT או להגדיר עדכונים אוטומטיים כדי להבטיח שה-NAS שלהם מפעיל את הגרסה העדכנית והמאובטחת ביותר של DiskStation Manager.

## כיצד לפתוח קובץ PAT

כדי לעדכן את DiskStation Manager באופן ידני, אתה יכול להשתמש בקובץ PAT שהורדת ממרכז ההורדות של Synology באמצעות השלבים הבאים:

1. גש ללוח הבקרה של DiskStation Manager.
2. נווט אל הקטע "עדכון ושחזור" ובחר "עדכון DSM".
3. משם, בחר "עדכון DSM ידני".
4. לחץ על כפתור "עיון", ולאחר מכן אתר ובחר את קובץ ה-PAT שהורדת.
5. כדי להתחיל את העדכון של DiskStation Manager, לחץ על כפתור "החל".

## הפניות
* [Synology](https://en.wikipedia.org/wiki/Synology)
