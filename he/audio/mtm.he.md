{
"date": "2023-02-15",
  "keywords": [
"קובץ mtm",
"מהו קובץ mtm",
"קוֹבֶץ",
"כיצד לפתוח קובץ mtm",
"סיומת קובץ mtm",
"סיומת"
],
  "author": {
"display_name": "שייק פאיז"
},
"draft": "false",
"toc": true,
"title": "פורמט קובץ MTM - מודול MultiTracker",
  "description":"למד על פורמט קובץ MTM וממשקי API שיכולים ליצור ולפתוח קובצי MTM.",
  "linktitle": "MTM",
  "menu": {
    "docs": {
      "identifier": "audio-mtm",
      "parent": "audio"
}
},
"lastmod": "2023-02-15"
}

## מהו קובץ MTM?

MTM היא סיומת קובץ המייצגת MultiTracker Module, שהיא סוג של פורמט קבצי אודיו המשמש להשמעת מוזיקה ביישומי מולטימדיה ומשחקי וידאו שונים. קבצי MTM מכילים קבוצה של רצועות מוזיקה, שכל אחת מהן ניתנת להשמעה באופן עצמאי או ביחד כהרכב שלם. הפורמט דומה לפורמטים אחרים של קבצי מודול, כגון MOD ו-S3M, אך עם כמה הבדלים באופן האחסון וההשמעה של הנתונים.

קובצי MTM היו פופולריים בשנות ה-90 ותחילת שנות ה-2000, במיוחד בקהילות המוזיקה של דמו-סצנה ומשחקי וידאו. כיום, הם פחות נפוץ, אבל עדיין יש כמה יישומי מולטימדיה ומשחקים התומכים בפורמט. כדי להפעיל קובץ MTM, תזדקק לנגן מדיה או תוכנה התומכת בפורמט, כגון Winamp או ModPlug Player.

## ערוצי אודיו של MTM

מספר הערוצים שבהם תומך קובץ MTM (MultiTracker Module) יכול להשתנות בהתאם לאופן יצירתו ולתוכנה הספציפית המשמשת להפעלתו. באופן כללי, קבצי MTM תומכים לכל היותר בארבעה ערוצי שמע, המחולקים בדרך כלל לשני ערוצי סטריאו. המשמעות היא שהקובץ יכול להכיל עד ארבעה כלי נגינה בודדים או רצועות דוגמה שניתן לנגן בו זמנית. כל רצועה מוקצה לערוץ מסוים וניתן להפנות אותו שמאלה או ימינה כדי לשלוט במיקומו בשדה הסטריאו.

קבצי MTM תוכננו במקור לשימוש במחשבים אישיים וקונסולות משחקים ישנים יותר, שהיו להם יכולות חומרה מוגבלות ויכלו להפעיל רק מספר מוגבל של ערוצים בבת אחת. מגבלת ארבעת הערוצים הייתה אפוא מגבלה מעשית המבוססת על הטכנולוגיה הזמינה באותה תקופה. עם זאת, כמה פלטפורמות תוכנה וחומרה חדשות יותר עשויות לתמוך בספירת ערוצים גבוהה יותר עבור קובצי מודול, בהתאם ליישום הספציפי.

## גודל קובץ קטן וקצבי סיביות נמוכים יותר

קצב הסיביות של קובץ שמע MTM (MultiTracker Module) יכול להשתנות בהתאם למימוש הספציפי ולתוכנה המשמשת ליצירתו. באופן כללי, לעומת זאת, קבצי MTM קטנים יחסית וקצב סיביות נמוך בהשוואה לפורמטים מודרניים של קבצי אודיו.

קבצי MTM משתמשים בסוג של דחיסת אודיו המכונה סינתזה מבוססת דגימות, אשר מייצרת אודיו באמצעות דגימות קטנות ומוקלטות מראש או צורות גל במקום נתוני אודיו דיגיטליים מלאים. זה מאפשר גדלי קבצים קטנים יחסית וקצבי סיביות נמוכים יותר, אך עלול לגרום לאיכות שמע נמוכה יותר ולטווח מוגבל של צליל.

קצב הסיביות של קובץ MTM מתבטא בדרך כלל בקילוביט לשנייה (kbps) ויכול לנוע בין 16 kbps ל-128 kbps ומעלה, בהתאם למימוש הספציפי ולמספר הערוצים שבהם נעשה שימוש. עם זאת, מכיוון שקובצי MTM משמשים בדרך כלל להשמעת מוזיקה ביישומי מולטימדיה ומשחקים ישנים יותר, הם בדרך כלל אינם מיועדים לשחזור אודיו בנאמנות גבוהה ונעשה בהם שימוש נפוץ יותר בשל ערכם הנוסטלגי.

## איך פותחים קובץ MTM?

כדי לפתוח קובץ MTM (MultiTracker Module), תזדקק לנגן מדיה או תוכנה התומכת בפורמט הקובץ MTM. הנה כמה אפשרויות:

1. ModPlug Player: ModPlug Player הוא נגן מדיה חינמי התומך במגוון רחב של פורמטים של קבצי מודול, כולל MTM. אתה יכול להוריד אותו מהאינטרנט ולהתקין אותו במחשב שלך. לאחר ההתקנה, תוכל לפתוח את קובץ ה- MTM שלך עם הנגן ולהתחיל לנגן את המוזיקה.
2. Winamp: Winamp הוא נגן מדיה נוסף התומך בקבצי MTM, כמו גם בפורמטים רבים אחרים של קבצי אודיו. אתה יכול להוריד ולהתקין את הנגן במחשב שלך ולאחר מכן להשתמש באפשרות "פתח" כדי לחפש ולפתוח את קובץ ה-MTM שלך.

## הפניות
* [קובץ מודול](https://en.wikipedia.org/wiki/Module_file)

