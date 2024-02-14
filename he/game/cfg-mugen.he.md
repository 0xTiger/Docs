{
"date": "2023-09-27",
  "keywords": [
"cfg",
"קובץ cfg",
"קובץ תצורה של cfg mugen",
"מהו קובץ cfg",
"כיצד לפתוח קובץ cfg",
"קוֹבֶץ",
"סיומת קובץ cfg",
"סיומת"
],
  "author": {
"display_name": "שייק פאיז"
},
"draft": "false",
"toc": true,
"title": "פורמט קובץ CFG - קובץ תצורה של MUGEN",
  "description":"למד על פורמט קבצי תצורה של CFG MUGEN וממשקי API שיכולים ליצור ולפתוח קובצי CFG.",
  "linktitle": "CFG M.U.G.E.N",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen",
      "parent": "game"
}
},
"lastmod": "2023-09-27"
}

## מהו קובץ CFG?

קובץ CFG בהקשר של MUGEN מתייחס ל"קובץ תצורה של MUGEN." **MUGEN** הוא מנוע משחק לחימה דו-ממדי הניתן להתאמה אישית שפותח על ידי Elecbyte. משתמשים יכולים ליצור דמויות משלהם, שלבים ואפילו לשנות את ההתנהגות והחוקים של המשחק על ידי עריכת קבצי תצורה שונים כולל קובצי CFG.

הנה סקירה כללית בסיסית של מה שאתה עשוי למצוא בקובץ `.cfg` של MUGEN:

1. **תצורת מערכת**: קבצי CFG מכילים לעתים קרובות הגדרות הקשורות להתנהגות כללית של מנוע המשחק. זה כולל דברים כמו רזולוציית מסך, הגדרות צליל ותצורת קלט (מיפוי מקלדת, ג'ויסטיק או בקר).
    








2. **ברירת מחדל של תווים ושלבים**: ניתן להגדיר הגדרות ברירת מחדל עבור תווים ושלבים. לדוגמה, אתה יכול לציין אילו דמויות ושלבים נטענים כאשר המשחק מתחיל.
    








3. **אפשרויות משחק**: קבצי MUGEN `.cfg` יכולים גם לשלוט באפשרויות משחק שונות כגון מגבלות זמן עגולות, קנה מידה נזק ועוד.
    








4. **ניפוי באגים ופיתוח**: משתמשים מתקדמים עשויים להשתמש בקבצי `.cfg` למטרות איתור באגים ופיתוח. הגדרות אלה יכולות לשלוט באופן שבו מידע ניפוי באגים מוצג על המסך או להגדיר התנהגויות אחרות הקשורות לפיתוח.
    








5. **תצורת ערכת מסך**: ערכות מסך הן נושאים ויזואליים שמשנים את המראה והתחושה של המשחק. קבצי `.cfg` יכולים לציין באיזו screenpack נעשה שימוש ולהגדיר את הרכיבים השונים שלו.
    








6. **התנהגות AI**: MUGEN מאפשרת לך להגדיר כיצד דמויות נשלטות מחשב (AI) מתנהגות בקרבות. קבצי `.cfg` יכולים להכיל הגדרות הקשורות לקושי והתנהגות בינה מלאכותית.

## קובץ תצורה של MUGEN

קובץ MUGEN CFG (קונפיגורציה) הוא מרכיב חיוני ליוצרים בעולם של משחקי לחימה מותאמים אישית. זה נותן להם כוח לעצב את כללי המשחק שלהם. זה כולל גורמים כמו כמה זמן נמשך כל סיבוב, רמת האתגר שמציגים יריבים הנשלטים על ידי מחשב, קצב המשחק, המידה שבה שילובים משפיעים על הנזק ועוד הרבה יותר.

יתר על כן, קובץ CFG מאפשר ליוצרים לקבוע את הגדרות התצוגה של המשחק, כגון רזולוציית המסך ולהחליט אם MUGEN צריך לנגן אפקטים קוליים ומוזיקה במהלך המשחק. לאלו הבקיאים במורכבויות של MUGEN, הקובץ הזה מציע פוטנציאל לכוונן מערך של הגדרות אחרות הקשורות למשחק כדי ליצור חווית משחק ייחודית.

כברירת מחדל, קובץ ה-CFG הראשי של MUGEN, המכונה `mugen.cfg`, נמצא בתיקיית הנתונים של התוכנית. אמנם ניתן לערוך ישירות את הגדרות המשחק בתוך קובץ זה, אך בדרך כלל מומלץ ליצור עותק גיבוי תחילה. אמצעי זהירות זה מבטיח שתוכל להחזיר את MUGEN ללא מאמץ להגדרות המקוריות שלו במידת הצורך ולמנוע מכל שינוי לא מכוון לשבש את חווית המשחק שלך.

## MUGEN - מנוע משחק

MUGEN הוא מנוע משחקי לחימה דו מימדי רב תכליתי וניתן להתאמה אישית שפותח על ידי Elecbyte. השם "MUGEN" מייצג "Mugen Ultimate Game Engine". הוא שוחרר לראשונה ב-1999 ומאז זכה לקהילה ייעודית של משתמשים ויוצרים המשתמשים במנוע כדי לעצב ולפתח משחקי לחימה דו-ממדיים משלהם.

להלן כמה תכונות והיבטים מרכזיים של MUGEN:

1. **דמויות הניתנות להתאמה אישית:** MUGEN מאפשרת למשתמשים ליצור ולייבא דמויות משלהם (המכונה "לוחמים" או "ספרייטים") לתוך המשחק. יוצרים יכולים לעצב סטים ייחודיים, אנימציות והתקפות מיוחדות עבור הדמויות הללו, מה שמאפשר לכלול למעשה כל דמות ממגוון זיכיונות או יצירות מקוריות.
    








2. **שלבים:** בנוסף לדמויות, משתמשים יכולים גם ליצור ולהתאים אישית שלבים שבהם מתרחשים קרבות. בשלבים אלו יכולים להיות אלמנטים אינטראקטיביים ורקעים ייחודיים.
      









3. **חבילות מסך:** ערכות מסך הן נושאים חזותיים שמשנים את המראה הכללי של המשחק, כולל תפריטים, מסכי בחירת דמויות וסרגלי חיים. משתמשים יכולים ליצור ולשתף חבילות מסך משלהם כדי לתת למשחקים שלהם מראה ותחושה ייחודיים.
    








4. **סאונד ומוזיקה:** יוצרים יכולים להוסיף אפקטים קוליים ומוזיקת רקע למשחקים שלהם, ולשפר את חווית המשחק הכוללת.
    








5. **סקריפטים:** משתמשים מתקדמים יכולים להשתמש בשפת סקריפטים מובנית כדי ליצור התנהגויות מורכבות של דמויות, מכניקת משחק ייחודית ואפקטים מיוחדים.

## איך פותחים קובץ CFG?

קובצי MUGEN CFG הם מסמכי טקסט רגיל המאפשרים גישה אליהם באמצעות עורכי טקסט שונים. ב-Windows, אתה יכול להשתמש ב-Microsoft Notepad או WordPad, בעוד שמשתמשי macOS יכולים להשתמש ב-Apple TextEdit למטרה זו. עורכים אלה מאפשרים למשתמשים להציג ולשנות הגדרות תצורה בתוך קבצי CFG בקלות.

תוכניות הפותחות או הפניות לקבצי CFG

- Elecbyte MUGEN
- פנקס רשימות
- עריכת טקסט

## קבצי CFG אחרים

להלן סוגי קבצים אחרים המשתמשים בסיומת הקובץ **.cfg**.

**הגדרות**
- [CFG - קובץ תצורה של Celestia](/he/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/he/settings/cfg-citrix/)
- [CFG - קובץ תצורה של MAME](/he/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/he/settings/cfg-lightwave/)

**מִשְׂחָק**
- [CFG - Wesnoth Markup Language File](/he/game/cfg-wesnoth/)
- [CFG - קובץ תצורה של MUGEN](/he/game/cfg-mugen/)
- [CFG - קובץ תצורת מנוע מקור](/he/game/cfg-sourceengine/)

**מערכת ושונות**
- [CFG - קובץ CFG](/he/system/cfg/)
- [CFG - Cal3D Model Configuration File](/he/misc/cfg-cal3d/)

## הפניות
* [Mugen (מנוע משחק)](https://en.wikipedia.org/wiki/Mugen_(game_engine))
