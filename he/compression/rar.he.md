{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ rar", "פורמט קובץ rar", "מהו קובץ rar", "קובץ", "דוגמה ל-rar", "סיומת קובץ rar", "הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"מהי סיומת קובץ RAR וממשקי API שיכולים ליצור ולפתוח קובצי RAR.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ RAR?

קבצים עם סיומת .rar הם קבצי ארכיון שנוצרים לאחסון מידע בצורה דחוסה או רגילה. RAR, ראשי תיבות של Roshal ARchive file format, הוא פורמט קובץ קנייני שנוצר על ידי יוג'ין רושל בשנת 1995 שהיה מהנדס תוכנה רוסי. הפורמט משמש לארכיון קבצים בשיטות שונות כולל טכניקות דחיסה שונות. קיימות מספר תוכנות יישומים זמינות עבור Windows, Linux ו- MacOS לחילוץ קבצי RAR. תוכנת WinRAR, מאת RARLab, היא כלי עזר לארכיון קבצים שיתופי (חינם למשך 40 יום) עבור פלטפורמת Microsoft Windows; התוכנה הועברה ללינוקס (כחולץ בלבד) על ידי אותו מחבר, יוג'ין רושל.

## היסטוריית גרסאות של פורמט קובץ RAR

* v1.3 (מקורי, אין לו חתימת "Rar!")
* v1.5
* v2.0 - שוחרר עם WinRAR 2.0 ו-Rar עבור MS-DOS 2.0
* v2.9 - שוחרר בגרסת WinRAR 3.00
* v5.0 - נתמך על ידי WinRAR 5.0 ואילך

## תכונות עיקריות של פורמט RAR

RAR נמצא בתחום כבר זמן רב והיה אחד מפורמטי קבצי הארכיון המועדפים. תכונות עיקריות לגבי פורמט RAR הן:

**`יחס דחיסה גבוה:`** מעולה בהשוואה ל-[ZIP](/he/compression/zip/), דומה לפורמט 7z ו-zipx.

**`הצפנת קבצים חזקה לפי עיצוב:`** ארכיוני RAR4 מוצפנים מסתמכים על הצפנה מבוססת AES-128 בעוד שארכיוני RAR5 מוצפנים מסתמכים על הצפנת AES-256 עם תזמון מפתח משופר

**`יכולות מתקדם של תיקון שגיאות ושחזור נתונים:`** רשומות שחזור אופציונליות במהלך יצירת ארכיון

**`גודל קובץ:`** מינימום 20 בייטים ומקסימום 2^63 בייטים בגודל (8 אקס-בייט מהגודל הכולל של הארכיון)

**`ארכיוני RAR מרובי נפחים:`** אפשרות לפצל ארכיונים גדולים למספר קבצים קטנים יותר כדי להקל על העברה דרך הרשת. במקרה כזה, סיומות הקובץ מוגדלות ב-1 כדי לייצג נפחים מפוצלים

## פורמט קובץ RAR

מפרטים מלאים של פורמט RAR אינם זמינים לציבור וזו הסיבה שלא ניתן לנסח פרטים על הפורמט בצורה תמציתית.

### פריסת ארכיון כללית

הפריסה הכללית של פורמט קובץ RAR שהוצג בגרסה 5.0 היא כדלקמן:

|פורמט קובץ
---|
|מודול לחילוץ עצמי (אופציונלי)
| חתימת RAR 5.0
|כותרת הצפנה לארכיון (אופציונלי)
|כותרת ראשית של הארכיון
|כותרת שירות הערות בארכיון (אופציונלי)
כותרת קובץ 1
|כותרות שירות (NTFS ACL, זרמים וכו') עבור הקובץ הקודם (אופציונלי)
|...
|כותרת קובץ N
|כותרות שירות (NTFS ACL, זרמים וכו') עבור הקובץ הקודם (אופציונלי)
|רשומה לשחזור (אופציונלי)
|סוף כותרת הארכיון

מידע על כל חלק בקובץ RAR שהוזכר לעיל ניתן למצוא במסמך [מפרטי פורמט הקובץ RAR 5.0](https://www.rarlab.com/technote.htm#arcstruct).

#### ארכיוני RAR לחילוץ עצמי

אם קובץ ה-RAR עצמו חילוץ עצמי, המידע לחילוץ עצמי כלול בתחילת הקובץ שלפני חתימת הארכיון. גודלו ותכולתו אינם מוגדרים.

#### חתימת RAR 5.0

חתימת ה-RAR היא כותרת בת 8 בתים המורכבת ממספר הקסם הבא:

0x 52 61 72 21 1A 07 00

איפה

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## הפניות

* [פורמט ארכיון RAR 5.0](https://www.rarlab.com/technote.htm)
* [RAR - מאת ויקיפדיה](https://en.wikipedia.org/wiki/RAR_(file_format))

