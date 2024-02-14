
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ רביעי - פורמט קובץ שפה רביעית",
  "description":"למד מה זה פורמט קובץ .4 עם דוגמה וממשקי API שיכולים ליצור ולפתוח קבצים רביעיים.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## מהו קובץ רביעי?

קובץ עם סיומת קובץ 4th הוא קובץ תכנות שנוצר עבור **שפת התכנות הרביעית**. הוא מכיל קוד מקור לתוכניות הכתובות בשפת התכנות Forth ומייצר את הפלט כאשר התוכנית מבוצעת. זה רק עוד קובץ שפת תכנות הדומה לקובץ המקור [C](/he/programming/c/) ו-[C++](/he/programming/cpp/).

## פורמט קובץ 4 - מידע נוסף


### דוגמה לקוד שפת תכנות רביעית

הנה דוגמה לתוכנית פשוטה שנכתבה ב-Forth שמחשבת את הפקטוריאלי של מספר נתון:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

בדוגמה זו, המילה הפקטוריאלית לוקחת ארגומנט יחיד n ומחזירה את הפקטוריאלי שלו. מילת ה-dup משכפלת את הערך על גבי הערימה, drop משליך את הערך על גבי הערימה, ו-* מכפיל את שני הערכים על גבי הערימה. הקונסטרוקציות אם והתחל/עד שולטים בזרימת התוכנית.

כדי להשתמש בתוכנית זו, תזין את ההגדרה לתוך המתורגמן Forth, ולאחר מכן תתקשר למילה הפקטוריאלית עם המספר שאתה רוצה למצוא את הפרקטיאלי של:

```
10 factorial .
```
זה יביא לפלט 3628800, שהוא הפקטוריאלי של 10.

## הפניות

* [שפת התכנות הרביעית](https://en.wikipedia.org/wiki/Forth_(programming_language))
