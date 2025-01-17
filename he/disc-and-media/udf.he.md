{
  "date" : "2021-08-17",
  "keywords" :[ "קובץ udf", "פורמט קובץ udf", "מהו קובץ udf", "קובץ", "דוגמה ל-udf", "סיומת קובץ udf","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"למד על פורמט קובץ UDF וממשקי API שיכולים ליצור ולפתוח קובצי UDF.",
  "title" :"UDF - קובץ פורמט דיסק אוניברסלי",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## מהו קובץ UDF?
הקובץ עם סיומת .udf הוא פורמט הדמיית דיסק המשמש בדרך כלל לשמירת קבצים במדיה אופטית; יכול לשמש לצריבת תקליטורי DVD, תקליטורים ומדיה אופטית אחרת; מאחסן אוסף של קבצים באמצעות מבנה הספריות המצוין בתקן UDF; מאפשר למחוק ולשנות קבצים בדיסק היעד גם לאחר כתיבתם. איגוד טכנולוגיות האחסון האופטי קבע את מערכת הקבצים UDF כסטנדרט ליצירת מערכת קבצים משותפת עבור כל המדיה האופטית כגון עבור מדיה אופטית הניתנת לכתיבה מחדש ומדיה לקריאה בלבד.

## פורמט קובץ UDF
פורמט הקובץ UDF הוא מערכת קבצים פתוחה ללא ספק לאחסון נתונים במחשב עבור מגוון רחב של מדיה. נעשה בו שימוש נפוץ עבור תקליטורי DVD ופורמטים חדשים יותר של דיסקים אופטיים. בדרך כלל, התוכנה שולטת במערכת קבצים UDF בתהליך אצווה וכותבת אותה למדיה אופטית במעבר אחד. עם זאת, כאשר הוא כותב מנות למדיה הניתנת לכתיבה מחדש, ה-UDF מאפשר ליצור, למחוק ולשנות קבצים בדיסק בדומה למערכת קבצים למטרות כלליות על מדיה נשלפת כמו כונני הבזק או תקליטונים.
### מפרטי UDF
תקן UDF מגדיר את שלוש הווריאציות הבאות של מערכת הקבצים:

- **בנייה רגילה**: זהו הפורמט המקורי הנתמך בכל גרסאות UDF. הוא הוצג בגרסה הראשונה של התקן, ניתן להשתמש בפורמט זה בכל סוג של דיסק המאפשר גישה אקראית לקריאה או כתיבה, כגון DVD+RW, דיסקים קשיחים ומדיה DVD-RAM.
- **בניית מע"מ**: משמש במיוחד לכתיבה ל-write-one media. המע"מ הוא מבנה נוסף בדיסק המאפשר כתיבת מנות; כלומר, מיפוי מחדש של בלוקים פיזיים כאשר קבצים או נתונים אחרים בדיסק משתנים או נמחקים. עבור מדיה של כתיבה פעם אחת, הדיסק כולו מוירטטאלי, מה שהופך את אופי הכתיבה פעם אחת לשקוף עבור המשתמש; ניתן להתייחס לדיסק באותו אופן שמתייחס לדיסק הניתן לכתיבה מחדש.
- **מבנה חסוך (RW)**: משמש במיוחד לכתיבה למדיה הניתנת לכתיבה. זה מוסיף טבלת חסך נוספת כדי לנהל את התקלות שיתרחשו בסופו של דבר בחלקים מהדיסק שנכתבו מחדש מספר פעמים. טבלה זו חוסכת מעקב אחר סקטורים שחוקים וממפה אותם מחדש למגזרים עובדים. ניהול הפגמים של UDF אינו חל על מערכות שכבר מיישמות צורה אחרת של ניהול פגמים, כגון Mount Rainier (MRW) עבור דיסקים אופטיים, או בקר דיסק עבור כונן קשיח.
 




## הפניות


* [פורמט הדמיה של Windows - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


