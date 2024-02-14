{
"תאריך":"2023-09-21",
   "keywords":[
"bps",
"קובץ bps",
"מהו קובץ bps",
"כיצד לפתוח קובץ bps",
"סיומת קובץ bps",
"סיומת",
"קוֹבֶץ"
],
   "author":{
"display_name":"שייק פאיז"
},
"draft": "false",
"toc":true,
"title": "פורמט קובץ BPS - קובץ תיקון BPS",
   "description":"למד על פורמט BPS וממשקי API שיכולים ליצור ולפתוח קובצי BPS.",
   "linktitle":"BPS",
   "menu":{
      "docs":{
         "identifier":"game-bps",
         "parent":"game"
}
},
"lastmod":"2023-09-21"
}

## מהו קובץ BPS?

סיומת קובץ ".bps" מתייחסת בדרך כלל לקובץ תיקון בינארי. קבצים אלה משמשים להחלת תיקונים או עדכונים על קבצים או תוכנות קיימים. להלן מידע נוסף על קבצי BPS:

1. **קבצי תיקון:** קובצי BPS מכילים נתונים בינאריים המייצגים את השינויים הדרושים לעדכון או שינוי של קובץ או תוכנית קיימים. במקום להחליף את הקובץ כולו, קבצי תיקון כוללים רק את ההבדלים בין הקובץ המקורי לגרסה המעודכנת.

2. **פריצת ROM:** קבצי BPS נמצאים בשימוש נפוץ בהקשר של פריצת ROM. האקרים של ROM משתמשים בקובצי BPS כדי להפיץ תיקונים שמשנים את קוד המשחק או את התוכן ב-ROM של משחקי וידאו קלאסיים. שחקנים יכולים להחיל תיקונים אלה על ROM המשחקים שלהם כדי לחוות שינויים ותרגומים שנעשו על ידי מעריצים.

3. **יישום תיקון:** כדי להחיל תיקון BPS, תזדקק לכלי תיקון. כלי עזר פופולריים לתיקון כמו "צף IPS" או "Beat" מאפשרים לך להחיל תיקוני BPS על קובץ ה-ROM המתאים, וליצור גרסה שונה של המשחק או התוכנה.

בסעיפים הבאים, נחקור את יישומי התוכנה המשויכים לקובצי BPS.

## IPS צף

Floating IPS (Flips) הוא כלי עזר פופולרי וידידותי למשתמש להחלת תיקונים על קבצי ROM בהקשר של פריצת ROM. הוא נמצא בשימוש נפוץ בקהילות אמולציה ותרגום מעריצים. מידע נוסף הקשור אליו ניתן להלן.

- **יישום תיקון:** IPS צף נועד להחיל קבצי תיקון, בדרך כלל בפורמט BPS, על קבצי ROM. תיקונים אלה מכילים נתונים בינאריים המייצגים שינויים ב-ROM המקורי, כגון תרגומים, תיקוני באגים או שינויים במשחק.

- **תיקון אוטומטי:** IPS צף מזהה אוטומטית את הכותרת של ROM היעד ומחיל את התיקון בהתאם, מה שמפשט את תהליך התיקון.

- **אימות Checksum:** הכלי כולל לעתים קרובות תכונת אימות Checksum כדי להבטיח את שלמות ה-ROM המתוקן, להפחית את הסיכון לשגיאות או שחיתות.

- **יצירת תיקונים:** בעוד ש-IPS צף משמש בעיקר להחלת תיקונים, ניתן להשתמש בו גם ליצירת קבצי תיקונים (פורמט BPS) מההבדלים בין שני ROM, מה שהופך אותו לשימושי עבור פריצת ROM ופרויקטי תרגום.

## MultiPatch

MultiPatch הוא כלי עזר נוסף הנפוץ בקהילת הפריצות ל-ROM, במיוחד להחלת תיקונים על קבצי ROM. זה דומה בתפקוד ל-IPS צף אבל מגיע עם תכונות וממשק משלו. מידע נוסף הקשור אליו ניתן להלן.

- **יישום תיקון:** MultiPatch נועד להחיל תיקונים על קבצי ROM, בדרך כלל בפורמטים כמו IPS, UPS או BPS. תיקונים אלה מכילים נתונים בינאריים המשנים את ה-ROM המקורי, לעתים קרובות למטרות כמו תרגומים, תיקוני באגים או התאמות אישיות.

- **תמיכה בפורמטים שונים של תיקון:** הוא תומך במגוון פורמטים של קבצי תיקון, כולל IPS (מערכת תיקון בינלאומית), UPS (פורמט תיקון אוניברסלי) ו-BPS (מערכת תיקון בינארית), מה שהופך אותו למגוון עבור סוגים שונים של טלאים.

- **תיקון אצווה:** ניתן להשתמש ב-MultiPatch להחלת תיקונים מרובים על קובץ ROM בודד או על קבצי ROM מרובים בו-זמנית, מה שמועיל לפריצות ROM מורכבות או פרויקטים הכוללים מספר תיקונים.

- **יצירת תיקון:** בדומה ל-IPS צף, ניתן להשתמש ב-MultiPatch גם ליצירת קבצי תיקון מההבדלים בין שני ROM, דבר שימושי עבור פריצת ROM ופרויקטי תרגום.

## איך פותחים קובץ BPS?

תוכניות הפותחות קבצי BPS כוללות

- IPS צף (חינם) עבור (MAC, Windows ולינוקס)
- MultiPatch (חינם) עבור (MAC)

## קבצי BPS אחרים

להלן סוגי קבצים אחרים המשתמשים בסיומת הקובץ **.bps**.

- [BPS - קובץ BPS Malware מ-SpywareCops](/he/misc/bps-malware/)
- [BPS - גיבוי מסמכי Microsoft Works](/he/misc/bps-works/)

## הפניות
* [IPS צף](https://www.gamebrew.org/wiki/Floating_IPS)
