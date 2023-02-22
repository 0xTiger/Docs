{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "קובץ", "סיומת", "פורמט", "מהו פורמט קובץ m4a", "מוזיקה", "פורמט קובץ m4a", "M4A לעומת MP3", "מפרט פורמט קובץ m4a "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ M4A וממשקי API שיכולים ליצור, להמיר ולפתוח קבצי M4A.",
  "title" :"M4A - קובץ שמע MPEG-4",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## מהו קובץ M4A?

**פורמט הקובץ M4A** הוא קובץ שמע שנוצר באמצעות AAC (קידוד אודיו מתקדם) הידוע כדחיסה מאבדת. המילה M4A בקיצור MPEG 4 Audio. לקבצי אודיו אלה יש בדרך כלל סיומת קובץ .m4a. זה נכון במיוחד לגבי תוכן לא מוגן. הוא עשוי לאחסן סוגים שונים של תוכן אודיו, כגון ספרי שמע, שירים ופודקאסטים. M4A מתממש בדרך כלל כפורמט מתקדם יותר מ-MP3, שלא תוכנן בדרך כלל לשמע בלבד. זוהי רק שכבת שמע בקבצי וידאו MPEG 1 או 2.

פורמט M4A מוצפן על ידי FairPlay Digital Rights Management כפי שנמכרו דרך iTunes Store באמצעות סיומת .m4p. מכשירי האייפון של אפל משתמשים באודיו MPEG-4 עבור הרינגטונים שלהם, אך קבצי אודיו אלה משתמשים בסיומת .m4r.


## M4A לעומת MP3

גם M4A וגם [MP3](https://docs.fileformat.com/audio/mp3/) הם פורמטים של קבצים אודיו בלבד.

**M4A**: טוב יותר מ-MP3 מבחינת איכות וגדלים כאשר מקודדים באותו קצב סיביות. סיומת הקובץ .m4a כל כך נפוצה מכיוון שהם שימשו את אפל לשימוש בחנות המוזיקה של iTunes. ה-M4A הוא קובץ שמע אשר דחוס באמצעות טכנולוגיית MPEG-4; אלגוריתם לדחיסה מאבדת. זה בעצם קשור ל-"MPEG-4 Audio Layer", קבצים עם סיומת .m4a הם שכבת האודיו של סרטי MPEG-4. הוא נועד לעקוף את MP3 ולהפוך לסטנדרט החדש בדחיסת אודיו. הוא קרוב מאוד ל-MP3 במובנים רבים, אך הוצג כדי לקבל איכות טובה יותר באותו גודל קובץ או אפילו קטן יותר. פורמט M4A הוצג לראשונה על ידי אפל. סוג הפורמט מתממש גם כ-Applelessless Encoder (ALE).

לכן, כרגע ה-M4A לא הצליח להשיג את ההצלחה המיינסטרים של ה-MP3 מכיוון שפורמט האודיו עדיין לא ניתן להשמעה בדרך כלל. איכשהו זה מוגבל רק ל-MacOS, iPod ומוצרי אפל אחרים.

**Mp3**: פורמט האודיו הדיגיטלי המפורסם ביותר. זה היה גם אחד מפורמטי הדחיסה הראשונים בסצנה והפך לפופולרי מאוד בקרב חובבי מוזיקה. הצלחתו המיינסטרים היא כל כך מהירה עד שסוג הקובץ מסוגל להפעיל באופן אוניברסלי וכמעט עם כל דבר, חומרה או תוכנה. במובן כללי, ה-M4A יפיק איכות צליל טובה יותר, אבל רבים יטענו שבין אם זה נכון או לא, ההבדל בסאונד אינו ניתן להבחין, וזה יהיה בזבוז זמן לנסות להמיר קבצי MP3 לקבצי M4A. בסופו של דבר, ההמרה פשוט תגרום לך לאבד את איכות הצליל המקורית.

## מפרט פורמט קובץ M4A

קבצי M4A מורכבים מנתחים רצופים. לכל נתח יש כותרת בת 8 בתים ומחולקת כך:
- גודל נתח של 4 בתים (ביג-אנדיאן, בייט גבוה ראשון)
- סוג נתח של 4 בתים - אחת מהחתימות המוגדרות מראש: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

הנתח הראשון יהיה מסוג "ftype" ויש לו תת-סוג בהיסט 8. ה-M4A המוגדר לפי תת-סוג שחייב להיות "M4A_", עבור תת-סוג M4B חייב להיות "M4B_" ול-M4P תת-סוג חייב להיות להיות "M4P_".

איטרציה של נתחים, עד שיזוהה נתח מסוג לא ידוע, זה ירכיב קובץ M4A (MPEG-4 Audio).

## הפניות ##

* [MPEG-4 חלק 14 - מאת ויקיפדיה](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) דוגמה לפורמט ושחזור](https://www.file-recovery.com/m4a-signature-format.htm)
