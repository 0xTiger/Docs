{
  "date" : "2019-11-25",
  "keywords" :[ "קובץ jpeg", "פורמט קובץ jpeg", "מהו קובץ jpeg", "קובץ", "דוגמה לjpeg", "סיומת קובץ jpeg", "הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - פורמט קובץ תמונה",
  "description":"למד על פורמט קובץ JPEG וממשקי API שיכולים ליצור ולפתוח קובצי JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## מהו קובץ JPEG? ##

JPEG הוא סוג של פורמט תמונה שנשמר בשיטת הדחיסה המאבדת. תמונת הפלט, כתוצאה מדחיסה, היא פשרה בין גודל האחסון ואיכות התמונה. משתמשים יכולים להתאים את רמת הדחיסה כדי להשיג את רמת האיכות הרצויה ובו בזמן להקטין את גודל האחסון. איכות התמונה מושפעת באופן זניח אם מוחלת דחיסה של 10:1 על התמונה. ככל שערך הדחיסה גבוה יותר, כך הירידה באיכות התמונה גבוהה יותר.

## מפרטי פורמט קובץ ##

פורמט קובץ תמונה JPEG תוקן על ידי קבוצת המומחים לצילום, ומכאן השם JPEG. הפורמט היה הבחירה של אחסון והעברת תמונות צילום באינטרנט. כמעט לכל מערכות ההפעלה יש כעת צופים התומכים בהדמיה של תמונות JPEG, אשר מאוחסנות לרוב גם עם סיומת JPG. אפילו דפדפני האינטרנט תומכים בהדמיה של תמונות JPEG. לפני שנכנסים למפרטי פורמט קובץ JPEG, יש להזכיר את התהליך הכולל של השלבים הכרוכים ביצירת JPEG.

### שלבי דחיסת JPEG ###

**טרנספורמציה:** תמונות צבע עוברות טרנספורמציה מ-RGB לתמונת בהירות/כרומיננטיות (העין רגישה לבהירות, לא לכרומינציה, כך שחלק הכרומיננס יכול לאבד הרבה נתונים ולכן יכול להיות דחוס מאוד.

**דגימה למטה:** הדגימה למטה נעשית עבור רכיב צבעוני ולא עבור רכיב בהירות. הדגימה למטה נעשית ביחס של 2:1 אופקית ו-1:1 אנכית (2h 1 V). לפיכך התמונה מצטמצמת בגודלה מכיוון שלא נוגעים ברכיב 'y', אין אובדן ניכר באיכות התמונה.

**ארגון בקבוצות:** הפיקסלים של כל רכיב צבע מאורגנים בקבוצות של 8×2 פיקסלים הנקראות "יחידות נתונים" אם מספר השורות או העמודות אינו כפולה של 8, השורה התחתונה והעמודות הימנית ביותר משוכפלות.

**טרנספורמציה של קוסינוס דיסקרטית:** טרנספורמציה קוסינוס דיסקרטית (DCT) מוחלת לאחר מכן על כל יחידת נתונים כדי ליצור מפה של 8×8 של רכיבים שעברו טרנספורמציה.DCT כרוך באובדן מסוים של מידע עקב הדיוק המוגבל של אריתמטיקה ממוחשבת. זה אומר שגם בלי המפה יהיה אובדן מסוים באיכות התמונה אבל היא בדרך כלל קטנה.

**כימות:** כל אחד מ-64 הרכיבים שעברו טרנספורמציה ביחידת הנתונים מחולק במספר נפרד הנקרא 'מקדם קוואנטיזציה (QC)' שלו ולאחר מכן מעוגל למספר שלם. זה המקום שבו המידע אובד באופן בלתי הפיך, QC גדול גורם לאובדן רב יותר. באופן כללי, רוב יישומי JPEG מאפשרים שימוש בטבלאות QC המומלצות על ידי תקן JPEG.

**קידוד:** 64 המקדמים שעברו טרנספורמציה (שהם כעת מספרים שלמים) של כל יחידת נתונים מקודדים באמצעות שילוב של קידוד RLE ו-Huffman.

**הוספת כותרת:** השלב האחרון מוסיף כותרת וכל פרמטרי ה-JPEG המשמשים ומוציא את התוצאה.

מפענח ה-JPEG משתמש בשלבים הפוך כדי ליצור את התמונה המקורית מהתמונה הדחוסה.

### מבנה הקובץ ###

תמונת JPEG מיוצגת כרצף של קטעים כאשר כל קטע מתחיל בסמן. כל סמן מתחיל עם בתים 0xFF ואחריו דגל סמן כדי לייצג את סוג הסמן. המטען ואחריו הסמן שונה לפי סוג הסמן. סוגי סמני JPEG נפוצים הם כמפורט להלן:

|שם קצר|בתים|מטען|שם|הערות
---|---|---|---|---|
|SOI|0xFF, 0xD8|ללא|תחילת תמונה|
|S0F0|0xFF, 0xC0|גודל משתנה|תחילת המסגרת|
|S0F2|0xFF, 0xC2|גודל משתנה|התחל למסגרת|
|DHT|0xFF, 0xC4|גודל משתנה|הגדר טבלאות האפמן|
|DQT|0xFF, 0xDB|גודל משתנה|הגדר טבלאות קוונטיזציה|
|DRI|0xFF, 0xDD|4 בתים|הגדר מרווח הפעלה מחדש|
|SOS|0xFF, 0xDA|גודל משתנה|התחלת סריקה|
|RSTn|0xFF, 0xD//n//(/he//n//#0..7)|ללא|הפעל מחדש|
|APPn|0xFF, 0xE//n//|גודל משתנה|יישום ספציפי|
|COM|0xFF, 0xFE|גודל משתנה|הערה|
|EOI|0xFF, 0xD9|ללא|סוף תמונה|

בתוך הנתונים המקודדים באנטרופיה, לאחר כל בתים של 0xFF, מוכנס בתים של 0x00 על ידי המקודד לפני הביט הבא, כך שלא נראה שיש סמן שבו אף אחד לא מיועד, ומונע שגיאות מסגור. מפענחים חייבים לדלג על 0x00 בתים זה. טכניקה זו, הנקראת [סטuffing byte](https://en.wikipedia.org/wiki/Byte_stuffing) (ראה סעיף מפרט JPEG F.1.2.3), מיושמת רק על הנתונים המקודדים באנטרופיה, לא על נתוני מטען סמן . עם זאת, שימו לב שלנתונים המקודדים באנטרופיה יש כמה סמנים משלהם; במיוחד את סמני האיפוס (0xD0 עד 0xD7), המשמשים לבודד נתחים עצמאיים של נתונים מקודדים באנטרופיה כדי לאפשר פענוח מקביל, ומקודדים חופשיים להכניס את סמני האיפוס הללו במרווחים קבועים (אם כי לא כל המקודדים עושים זאת).
