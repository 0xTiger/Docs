{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "הרחבה", "פורמט", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ PML, Palm Markup Language וממשקי API שיכולים ליצור ולפתוח קובצי PML.",
  "title" :"PML - Palm Markup Language File",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## מהו קובץ PML?

Palm Inc הציגה את פורמט הקובץ PML שהוא ראשי תיבות של Palm Markup Language File. מטרתו היא ליצור מסמכים עבור eReader שהוא מכשיר קריאת ספר אלקטרוני הדומה למחשב הטאבלט. קובץ ה-PML נותן את הפריסה לקובץ [PDB](/he/ebook/pdb/) (המכיל קבצי נתונים שונים) להצגה ב-Palm Device.

## פרטים טכניים של קבצי PML

המבנה של קובצי PML מורכב מתגים ליצירת הגדרת ספר אלקטרוני, כולל פסקאות, כותרות, הזחות והפניות. זה גם מאפשר את תגי העיצוב כגון מודגש, אותיות קטנות וסופר-על. מפתחים יכולים גם להוסיף תמונות לספרים האלקטרוניים.

### Palm Markup Language
הטבלה הבאה מציינת את פקודות ה-PML:

|פקודה|תיאור|
---|---|
| \p | עמוד חדש |
| \x | פרק חדש; גם גורם למעבר עמוד חדש. הוסף את כותרת הפרק (וכל קודי סגנון) עם \x ו-\x |
| \Xn | פרק חדש, נסחף n רמות (n בין 0 ל-4 כולל) בתיבת הדו-שיח פרק; אינו גורם לשבירת עמוד. הוסף את כותרת הפרק (וכל קודי סגנון) עם \Xn ו-\Xn |
| \Cn="כותרת פרק" | הכנס "כותרת פרק" לרשימת הפרקים, עם רמה n (כמו \Xn). הטקסט אינו מוצג בעמוד ואינו מאלץ מעבר עמוד. זה יכול לפעמים להיות שימושי כדי להוסיף סימן פרק בתחילת הקדמה לפרק, למשל. |
| \c | מרכז את גוש הטקסט הזה; סגור עם \c בתחילת השורה |
| \r | ימינה יישר בלוק טקסט; סגור עם \r בתחילת השורה |
| \i | נטוי בלוק; לסגור עם \i |
| \u | בלוק קו תחתון; לסגור עם \u |
| \o | חסימת מכה יתרה; לסגור עם \o |
| \v | טקסט בלתי נראה; סגור עם \v (ניתן להשתמש בהערות) |
| \t | בלוק כניסה. התחל בתחילת שורה, סגור עם \t בסוף שורה |
| \T="50%" | מכניס את האחוז שצוין מרוחב המסך, 50% במקרה זה. אם מיקום הציור הנוכחי כבר עבר את מיקום המסך שצוין, התגית הזו תתעלם. |
| \w="50%" | הטמע כלל אופקי של רוחב אחוז נתון של המסך, במקרה זה 50%. תג זה גורם למעבר שורה לפניו ואחריו. הכלל מרוכז. סימן האחוזים הוא חובה. |
| \n | עבור לגופן "רגיל", אשר מצוין על ידי המשתמש |
| \s | עבור ל-stdFont; סגור עם \s כדי לחזור לגופן רגיל |
| \b | עבור לגופן מודגש; סגור עם \b כדי לחזור לגופן רגיל (הוצא משימוש; השתמש ב-\B במקום זאת) |
| \l | עבור ל- largeFont; סגור עם \l כדי לחזור לגופן רגיל |
| \B | סמן טקסט כמודגש. בניגוד לתג \b, \B לא משנה את הגופן, כך שתוכל לקבל טקסט מודגש גדול. אתה לא יכול לערבב את \b ו-\B באותו קובץ PML. |
| \Sp | סמן טקסט ככתב עילי. אין לערבב עם סגנונות אחרים כגון מודגש, נטוי וכו'. יש לצרף טקסט בכתב עילי עם \Sp. |
| \Sb | סמן טקסט כמנוי. אין לערבב עם סגנונות אחרים כגון מודגש, נטוי וכו'. יש לצרף טקסט מנוי עם \Sb. |
| \k | הפוך טקסט מצורף לכפות קטנות; לסגור עם \k. כל התווים הכלולים בתגי \k (כולל אלה עם הדגשות) נעשים באותיות רישיות ומוצגים בגודל נקודה קטן יותר מאשר תו רגיל. |
| \\ | מייצג קו נטוי בודד |
| \aXXX | הוסף תו שאינו ASCII שקוד Windows-1252 שלו הוא XXX עשרוני. עיין בטבלת התווים של PML לפרטים. |
| \UXXXX | הוסף תו שאינו ASCII שקוד Unicode שלו הוא הקסדצימלי XXXX. עיין בטבלת התווים המורחבת של PML לפרטים. |
| \m="imagename.png" | הכנס את התמונה בעלת השם. עיין בסעיף על תמונות למטה. |
| \q="#linkanchor"חלק מהטקסט\q | הפניה לעוגן קישור שנמצא במקום אחר במסמך. המחרוזת שאחרי מפרט העוגן ולפני ה-\q הנגרר מסומנת בקו תחתון או מוצגת בדרך אחרת כקישור בעת הצגת המסמך. |
| \Q="linkanchor" | ציין עוגן קישור במסמך. |
| \- | הכנס מקף רך. מקף רך מופיע רק אם יש צורך לשבור מילה על פני קו. |
| \Fn="footnote1"1\Fn | קשר את ה"1" להערת שוליים ששמה הוא הערת שוליים1, מתויגת בסוף מסמך PML. עיין בסעיף על הערות שוליים וסרגלי צד למטה. |
| \Sd="sidebar1"Sidebar\Sd | קשר את הטקסט "סרגל צד" לסרגל צד ששמו הוא sidebar1, מתויג בסוף מסמך PML. עיין בסעיף על הערות שוליים וסרגלי צד למטה. |
| \I | סמן כפריט אינדקס הפניה. צירוף פריט אינדקס (וכל קודי סגנון) עם \I ו-\I.|
 


## הפניות

* [שפת סימון דקלים - מאת MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - מאת MobileRead](https://en.wikipedia.org/wiki/E-reader)
