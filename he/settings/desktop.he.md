{
"date": "2023-05-31",
  "keywords": [
"קובץ שולחן עבודה",
"מהו קובץ שולחן העבודה",
"מה מכיל קובץ שולחן העבודה",
"קובץ שולחן עבודה לדוגמה",
"כיצד לפתוח קובץ שולחן עבודה",
"מהו הפורמט של קובץ שולחן העבודה",
"קוֹבֶץ",
"סיומת קובץ שולחן העבודה",
"סיומת"
],
  "author": {
"display_name": "שייק פאיז"
},
"draft": "false",
"toc": true,
"title": "פורמט קובץ שולחן העבודה - קובץ כניסה לשולחן העבודה",
  "description":"למד על פורמט DESKTOP וממשקי API שיכולים ליצור ולפתוח קבצי DESKTOP.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
}
},
"lastmod": "2023-05-31"
}

## מהו קובץ DESKTOP?

קובץ .desktop הוא קובץ תצורה המשמש את סביבות שולחן העבודה של לינוקס כדי להגדיר קיצורי יישומים ומשגרים. הוא מספק מטא נתונים על יישום כגון השם, הסמל, הפקודה לביצוע ומאפיינים אחרים. קבצים אלה משמשים בדרך כלל ליצירת קיצורי דרך בתפריטי יישומים, מפעילי שולחן העבודה או פאנלים במערכות מבוססות לינוקס.

## מה מכיל קובץ DESKTOP?

קובץ .desktop עוקב אחר פורמט ספציפי ומכיל מספר שדות מפתח:

- **[כניסה לשולחן העבודה]:** זוהי כותרת הסעיף הראשית של קובץ ה-.desktop.
- **שם:** מציין את שם היישום.
- **הערה:** מספקת תיאור קצר או הערה לגבי היישום.
- **Exec:** מגדיר פקודה לביצוע בעת הפעלת יישום.
- **סמל:** מציין נתיב לקובץ סמל המשויך ליישום.
- **מסוף:** מציין אם יש להפעיל את היישום בחלון מסוף.
- **סוג:** מציין סוג ערך כגון "אפליקציה" או "קישור".
- **קטגוריות:** מציינת קטגוריות או קבוצות שבמסגרתן יש להציג את האפליקציה בתפריט.
- **StartupNotify:** מציין אם סביבת שולחן העבודה צריכה להציג הודעת הפעלה עבור יישום.
- **NoDisplay:** מציין אם יש להסתיר את היישום מתפריטים.
- **פעולות:** מגדיר פעולות נוספות שניתן לבצע באפליקציה כגון פתיחת קובץ ספציפי.

## קובץ DESKTOP לדוגמה

הנה דוגמה לקובץ .desktop עבור עורך טקסט פיקטיבי בשם "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

בדוגמה זו, קובץ ה-.desktop מגדיר את היישום "MyTextEditor" עם המאפיינים המשויכים לו. זה כולל גם שתי פעולות נוספות, "פתח חלון חדש" ו"פתח קובץ קיים", שאליהן ניתן לגשת מתפריט ההקשר של מפעיל היישומים.

על ידי הצבת קובץ .desktop בספריות ספציפיות כגון `/usr/share/applications` או `~/.local/share/applications`, סביבת שולחן העבודה תזהה אותו ותציג את היישום בהתאם בתפריטים או תאפשר את הפעלתו מ שולחן העבודה.

## איך פותחים קובץ DESKTOP?

מספר תוכנות יכולות לפתוח קובצי .desktop ולטפל בהם. תוכניות אלה הן בדרך כלל מנהלי קבצים או סביבות שולחן עבודה במערכות מבוססות לינוקס. הנה כמה דוגמאות:

- **Nautilus (קבצים):** מנהל הקבצים המוגדר כברירת מחדל עבור סביבת שולחן העבודה של GNOME.
- **Nemo:** מנהל הקבצים עבור סביבת שולחן העבודה של Cinnamon.
- **Dolphin:** מנהל הקבצים המוגדר כברירת מחדל עבור סביבת שולחן העבודה של KDE Plasma.
- **Thunar:** מנהל הקבצים המוגדר כברירת מחדל עבור סביבת שולחן העבודה של Xfce.
- **עורך תפריט KDE:** כלי ספציפי לסביבת שולחן העבודה של KDE Plasma המאפשר לך להציג ולערוך קבצי .desktop.

מנהלי קבצים וסביבות שולחן עבודה אלה מספקים ממשק גרפי לניהול קבצי .desktop. הם מאפשרים לך להציג ולערוך מאפיינים של קבצי .desktop, ליצור מפעילי יישומים ולארגן קיצורי דרך בתפריטי יישומים או בשולחן העבודה.

קבצי ה-.desktop הם קבצי טקסט רגיל, כך שתוכל גם לפתוח ולערוך אותם עם עורך טקסט לבחירתך. פשוט לחץ לחיצה ימנית על קובץ ה-.desktop ובחר "פתח עם" או "פתח עם יישום אחר" כדי לבחור עורך טקסט מרשימת התוכניות המותקנות.

## מהו הפורמט של קובץ DESKTOP?

פורמט הקובץ .desktop עוקב אחר מבנה ופורמט ספציפיים. זהו קובץ טקסט רגיל עם קבוצה של צמדי מפתח-ערך המאורגנים במקטעים. להלן סקירה כללית של הפורמט:

- **כותרות קטעים:** כל קטע מתחיל בכותרת מוקפת בסוגריים מרובעים ([]). הקטע הראשי נקרא בדרך כלל [כניסת שולחן עבודה], המכיל את המטא-נתונים העיקריים עבור יישום או מפעיל.
- **צמדי מפתח-ערך:** בתוך כל חלק, אתה מגדיר מאפיינים באמצעות זוגות מפתח-ערך. הפורמט הוא "מפתח=ערך". המפתח מזהה נכס וערך מספק נתונים מתאימים.
- **תחביר מאפיינים:** ערכי המאפיינים יכולים להיות מסוגים שונים כולל מחרוזות, ערכים בוליאניים, נתיבים או רשימות. הפורמט של כל ערך נכס תלוי בסוג שלו.
- **הערות:** ניתן לכלול הערות בקובץ .desktop באמצעות הסמל '#'. כל דבר שעוקב אחרי '#' בשורה נחשב כהערה ומתעלמים ממנו.

## הפניות
* [קבצי כניסה לשולחן העבודה](https://www.baeldung.com/linux/desktop-entry-files)
