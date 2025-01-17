{
  "date" : "2020-03-16",
  "keywords" :[ "קובץ IGES", "פורמט קובץ", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קבצי IGES וממשקי API שיכולים ליצור ולפתוח קובצי IGES.",
  "title" :"פורמט קובץ IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## מהו קובץ IGES?

קובץ עם סיומת .iges משמש להחלפת מידע עיצובי בין יישומי עיצוב בעזרת מחשב (CAD). IGES ראשי תיבות של Initial Graphics Exchange Specifications. מידע שהוחלף באמצעות IGES כולל דיאגרמת מעגלים, מסגרת תיל, משטח חופשי או ייצוגי דוגמנות מוצקים. IGES מוצא את היישומים שלה בשרטוטים הנדסיים מסורתיים, ניתוח מודלים ופונקציות ייצור. הפורמט יכול להחליף מידע עיצובי 2D או 3D בין תוכניות CAD. ניתן לפתוח קבצי IGES עם מספר יישומי CAD כגון Autodesk ו-CADSoftTools ABViewer. ישנם גם מספר ממשקי API זמינים לפתיחה והמרת קבצי IGES באופן תכנותי.

## פורמט קובץ IGES

קבצי IGES הם בפורמט טקסט ASCII וניתן לפתוח אותם בכל עורך טקסט כדי להציג את תוכן הקובץ. מידע טקסטואלי בקובץ IGES מיוצג בפורמט "Hollerith". קובץ IGES נפוץ יכול להכיל אלפי שורות כדי לייצג את המידע הדו-ממדי או התלת-ממדי שניתן להחליף לפי פורמט זה. קובץ IGES מחולק לחמישה מקטעים, מסומנים באות גדולה ספציפית בעמודה ה-73. הקטעים האלה הם מקטעים 'התחל' (S), 'גלובל' (G), 'הזנת נתונים' (D), 'נתוני פרמטרים' (P), ו'סיום' (T). הסעיפים הזנת נתונים ונתוני פרמטר מקוצרים בדרך כלל DE ו-PD, בהתאמה.

### כותרת קובץ IGES

החלקים 'התחלה' ו'גלובליים' מכילים מידע בסיסי על:
* שם הקובץ ומקורו
* תוחמים למקטע נתוני פרמטרים
* מחבר הקובץ, ומידע כללי אחר.

קטעי התחלה וגלובליים מהמסמך לדוגמה בוויקיפדיה הם כדלקמן.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
כפי שניתן לראות, שדה ההתחלה מכיל תיאורים הניתנים לקריאה אנושית של הקובץ, ויש לי תווים כלשהם בעמודות 1-72, כשהשורה מסתיימת בכותרת הסעיף ובמספר שורה של הקטע. חייבת להיות שורה אחת לפחות בקטע ההתחלה. הקטע הגלובלי מכיל נתוני מעבד מראש. זה גם חייב להיות קיים בקובץ ולהסתיים בפורמט G000000#.

### סעיף הזנת נתונים (DE) ונתוני פרמטרים (PD).

#### מדור הזנת נתונים
קובץ IGES מורכב מכמה ישויות המכילות את המידע על הנתונים הבסיסיים של פורמט הקובץ IGES. ישות מכילה מידע על אלמנטים שונים של פורמט נתונים של IGES ומשמשת לציור. ישויות נפוצות יותר כוללות:
* קשת מעגלית
* עקומה מורכבת
* קשת חרוטית
*מטוס
* קו

אלה רק כמה ויש כ-150 ישויות שונות ב-IGES. כל ישות מזוהה על ידי מספר סוג כגון:
* קשת מעגלית (סוג 100)
* LINE (סוג 110)

##### מאפייני ישות

לכל ישות מוצהרת יש את המאפיינים הבאים.

|שם שדה|תיאור|
---|---|
|סוג ישות |זהו סוג הישות המתואר. לדוגמה, 116 מתאר ישות Point.|
|PD pointer | זה נותן את המיקום של נתוני הישויות האלה במקטע נתוני פרמטרים. מיקום זה הוא פשוט מספר השורה בתוך קטע PD הכולל את השורה הראשונה של נתוני הישות הזו.|
|מבנה |אפס או מצביע לישות הגדרה. לא רלוונטי עבור רוב הישויות|
|דפוס גופן קו| מספר או מצביע לישות דפוס גופן קו. מספר מסמל: * 0 לא צוין תבנית (ברירת מחדל) * 1 מוצק * 2 מקווקו * 3 פנטום * 4 קו מרכז * 5 מנוקד|
|רמה| מציין רמות שישויכו לישות זו. מאפשר לישות להופיע ביותר מרמה אחת|
|הצג| מציין אפשרויות צפייה. אלה הם: 0 מציין נראות ומאפיינים שווים בכל התצוגות. מצביע ברירת מחדל לישות התצוגה (סוג 410) שניתן לצפות בה מהפניה לישות אסוציאטיביות נראית לתצוגה (סוג 402, טופס 3)
|מצביע מטריצת שינוי| מפנה לישות מטריצת טרנספורמציה (סוג 124) או אפס כברירת מחדל (ללא טרנספורמציה)|
|אסוציאטיביות לתצוגה של תווית| מפנה ל-Label Display Associativity (סוג 402, טופס 5) המגדיר כיצד תווית הישות מופיעה.|
|מספר סטטוס| מכיל ארבעה חלקים של שני מספרים. 1-2: מצב ריק. או 00 לרגיל או 01 לריק. 3-4: מתג ישות כפופה: הוא 00 עבור עצמאי, 01 עבור תלות פיזית, 02 עבור תלות לוגית ו-03 עבור שניהם. 5-6: דגל שימוש בישות: הוא 00 עבור גיאומטריה, 01 עבור ביאור, 02 עבור הגדרה, 03 עבור אחר, 04 עבור לוגי, 05 עבור פרמטרים דו-ממדיים ו-06 עבור גיאומטריית בנייה. לבסוף, 7-8 היא ההיררכיה, כאשר 00 מציין גלובלי מלמעלה למטה (השתמש במאפיינים של ישות זו), 01 הוא דחייה גלובלית (אל תשתמש במאפיינים של ישות זו), ו-02 הוא מאפיין שימוש היררכי (השתמש בישות היררכיה (סוג 406, טופס) 10)כדי לקבוע מאפיינים של קיבוץ היררכי).|
|מספר רצף| צוין על ידי D#, כאשר # הוא מספר השורה עבור קטע זה (לא מהחלק העליון של הקובץ). זה משמש גם כדי להצביע על ישות זו של הזנת נתונים.|
|סוג ישות| הוא מצוין פעמיים לכל רישום ישות|
|מספר משקל קו| מציין עובי בעת הצגת ישות. הקטן ביותר הוא 1, 0 הוא ברירת מחדל|
|מספר צבע| מציין את צבע הישות. ערכי מספרים שלמים מותרים הם: 0 ללא צבע (ברירת מחדל) 1 שחור 2 אדום 3 ירוק 4 כחול 5 צהוב 6 מגנטה 7 ציאן 8 לבן|
|מספר שורה של פרמטרים| מציין את מספר השורות שהישות הזו תופסת במקטע נתוני פרמטר|
|מספר טופס| מציין את הטופס, או את הייצוג של ישות זו. משנה את האופן שבו נתוני הפרמטר מתפרשים. ברירת המחדל היא 0|
|שדה שמור| לא בשימוש|
|שדה שמור| לא בשימוש|
|תווית ישות| מזהה שצוין יישום- זכות מוצדק|
|מספר מנוי| מסמיך מספרי עבור תווית הישות. שניהם יחד יוצרים מזהה ייחודי עבור הישות|
|מספר רצף ראה למעלה. |זה יהיה D#+1, מכיוון שכל ישות מצוינת בשתי שורות.|

#### סעיף נתוני פרמטר
לאחר הסעיף הזנת נתונים, הקטע נתוני פרמטרים. הוא מפרט את הנתונים עבור כל ערך בהתאמה ומפרט פרמטרים עבור הישות בהתבסס על המפרידים שצוינו בסעיף הגלובלי (בדרך כלל פסיקים לפרמטרים נפרדים ונקודה פסיק לסיום הרישום).


## הפניות
* [IGES מאת WikiPedia](https://en.wikipedia.org/wiki/IGES)

