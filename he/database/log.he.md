{
  "date" : "2021-06-14",
  "keywords" :[ "LOG", "הרחבה", "קובץ יומן", "פורמט קובץ יומן", "סוג קובץ מסד נתונים", "פורמט קובץ מסד נתונים", "מהו קובץ יומן" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ LOG וממשקי API שיכולים ליצור ולפתוח קובצי LOG.",
  "title" :"LOG - פורמט קובץ יומן",
  "linktitle" : "LOG",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## מהו קובץ LOG?
קובץ עם סיומת .log מכיל את רשימת הטקסט הפשוט עם חותמת הזמן. בדרך כלל, פרטי פעילות מסוימים מתועדים על ידי התוכנות או מערכות ההפעלה כדי לעזור למפתחים או למשתמשים לעקוב אחר מה שהתרחש בפרק זמן מסוים. משתמשים יכולים לערוך קבצים אלה בקלות רבה באמצעות כל עורכי טקסט. בדרך כלל דוחות השגיאה או פעילויות ההתחברות נרשמות על ידי מערכות ההפעלה, אך תוכנות אחרות או שרתי אינטרנט מייצרים גם קובצי יומן למעקב אחר מבקרים וכדי לנטר את השימוש ברוחב הפס.

## פורמט קובץ LOG
פורמט הקובץ LOG מתעד את האירועים האופייניים המתרחשים במערכת הפעלה, הודעות בין משתמשים שונים של תוכנת תקשורת או כל תוכנה אחרת המופעלת. פשוט אנו יכולים לומר שהודעות מסוימות בחותמות זמן מסוימות נרשמות בקובץ LOG. כמה מונחים נפוצים לרישום הם:
### יומני אירועים
זה מתעד אירועים המתרחשים בביצוע מערכת על מנת לעקוב ולהבין את פעילות המערכת ולאבחן בעיות. הם חשובים כדי לזהות את הפעילויות של מערכות מורכבות, בדרך כלל במקרה של יישומים עם מעט מאוד אינטראקציה של משתמשים.
### יומני עסקאות
כמעט כל מערכות מסדי הנתונים מחזיקות את יומן העסקאות, אשר בדרך כלל אינם מיועדים לשביל ביקורת לניתוח מאוחר יותר, ואינן קריאות לאדם. יומנים אלה שומרים רק את רישום השינויים בנתונים הקיימים כדי לאפשר למסד הנתונים להתאושש מקריסות או שגיאות נתונים אחרות ולשמור על הנתונים במצב עקבי. לפיכך, למערכות מסדי נתונים יש בדרך כלל גם יומני אירועים כלליים וגם יומני טרנזקציות.
### יומני הודעות
התקשורת הטקסטואלית שנשמרת על ידי Internet Relay Chat (IRC), תוכניות הודעות מיידיות (IM), לקוחות שיתוף קבצים עמית לעמית עם פונקציות צ'אט ומשחקים מרובי משתתפים (במיוחד MMORPGs) נקראים יומני הודעות. יומנים אלה נשמרים בדרך כלל בקבצי טקסט רגיל, אך לקוחות IM ו-VoIP (למשל Skype) עשויים לשמור אותם בקובצי HTML כדי להקל על הקריאה או לאפשר הצפנה.
### יומני שרת
יומן שרת הוא למעשה קובץ יומן המכיל רשימה של פעילויות שבוצעו ויצרו או נשמרו באופן אוטומטי על ידי השרת עצמו. בדרך כלל קבצים אלו אינם נגישים למשתמשי אינטרנט כלליים, אלא רק למנהל האתר או לאדם מנהלי אחר של שירות אינטרנט.



## הפניות ##

* [קובץ יומן - ויקיפדיה](https://en.wikipedia.org/wiki/Log_file)

