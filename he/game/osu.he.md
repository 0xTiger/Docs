{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ OSU וממשקי API שיכולים ליצור ולפתוח קובצי OSU.",
  "title" : "קובץ OSU - Osu! פורמט קובץ סקריפט",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-he",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## מהו קובץ OSU?

קובץ OSU הוא סקריפט משחק שנכתב עבור osu! משחק קצב. הוא מכיל מידע על מפת ביט המשמשת במשחק כמו רמת הקושי, השיר שיש לנגן, והתזמונים של אובייקטי הפגיעה אליהם השחקן צריך להסתנכרן עם המוזיקה. זה מאפשר לשחקני משחק קצב לפתח אתגרים מותאמים אישית ולשתף עם קהילת המשחקים.

**סוג MIME של פורמט קובץ OSR:** x-osu-beatmap

## פורמט קובץ OSU

קבצי OSU נשמרים כקובצי טקסט רגיל לדיסק והמבנה שלו מוגדר בצורה ברורה מאוד ב-[OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) של osu!.

### קטעים בקובץ OSU

לקובץ OSU טיפוסי יש את הסעיפים הבאים.

|קטע |תיאור |סוג תוכן|
---|---|---|
|[כללי]| מידע כללי על מפת הביט| מפתח: זוגות ערכים|
|[עורך]| הגדרות שמורות עבור עורך ה-beatmap| מפתח: זוגות ערכים|
|[Metadata] |מידע המשמש לזיהוי מפת הביט| מפתח:צמדי ערך|
|[קושי] |הגדרות קושי| מפתח:צמדי ערך|
|[אירועים]| אירועים גרפיים של Beatmap ו-storyboard| רשימות מופרדות בפסיק|
|[TimingPoints]| נקודות תזמון ובקרה| רשימות מופרדות בפסיק|
|[צבעים]| שילוב וצבעי עור| מפתח : זוגות ערכים|
|[HitObjects]| פגע באובייקטים| רשימות מופרדות בפסיק|

## הפניות

* [OSU! משחק קצב](https://osu.ppy.sh/home)

* [פורמט קובץ OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)

