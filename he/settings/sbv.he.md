{
"date": "2023-03-22",
  "keywords": [
"קובץ sbv",
"מהו קובץ sbv",
"כיצד לפתוח קובץ sbv",
"קוֹבֶץ",
"סיומת קובץ sbv",
"סיומת"
],
  "author": {
"display_name": "שייק פאיז"
},
"draft": "false",
"toc": true,
"title": "פורמט קובץ SBV - קובץ כיתובים של YouTube",
  "description":"למד על פורמט SBV וממשקי API שיכולים ליצור ולפתוח קובצי SBV.",
  "linktitle": "SBV",
  "menu": {
    "docs": {
      "identifier": "settings-sbv",
      "parent": "settings"
}
},
"lastmod": "2023-03-22"
}

## מהו קובץ SBV?

קובץ עם סיומת הקובץ sbv הוא קובץ כתוביות של SubViewer. SubViewer הוא פורמט של כתוביות בשימוש עם קובצי וידאו שמקורם בתחילת שנות ה-2000. קובץ ה-.sbv מכיל את טקסט הכתוביות יחד עם מידע על התזמון מתי כל כתובית צריכה להיות מוצגת במהלך הפעלת הסרטון.

לעתים קרובות נעשה שימוש בקבצי SubViewer עם סרטוני YouTube, מכיוון ש-YouTube תומך בפורמט SubViewer עבור כתוביות הווידאו שלו. ניתן להשתמש בקבצי SubViewer גם עם נגני וידאו ותוכנות אחרות התומכות בפורמט.

כדי להשתמש בקובץ .sbv עם קובץ וידאו, גם קובץ הווידאו וגם קובץ ה-.sbv צריכים להיות ממוקמים באותה תיקיה ובעלי אותו שם קובץ (למעט סיומת הקובץ). נגני וידאו רבים יטענו אוטומטית את קובץ ה-.sbv בעת הפעלת הסרטון אם הקבצים נקראים בצורה זו. ישנם יישומים שונים לעריכת כתוביות התומכים בפורמט SubViewer אם אתה צריך ליצור או לערוך קובץ sbv. Aegisub, סדנת כתוביות ועריכת כתוביות הם חלק מהכלים המשמשים לעתים קרובות.

## פורמט קובץ SBV - מידע נוסף

פורמט הקובץ SBV הוא פורמט פשוט מבוסס טקסט המשמש לאחסון כתוביות לסרטונים. SBV מייצג "SubViewer" או "SubRip Video", בהתאם למקור הקובץ. קובצי SBV מכילים כתוביות המסונכרנות עם תוכן הווידאו. כל כתובית מורכבת מחותמת זמן המציינת את זמני ההתחלה והסיום של הכתובית, ואחריה את הטקסט של הכתובית. חותמת הזמן היא בדרך כלל בפורמט של "hh:mm:ss,mmm" כאשר "hh" מייצג שעות, "mm" מייצג דקות, "ss" מייצג שניות ו-"mmm" מייצג אלפיות שניות. הטקסט של הכתובית הוא בדרך כלל בפורמט טקסט רגיל.

להלן דוגמה כיצד עשוי להיראות קובץ SBV:

```
0:00:01.000,0:00:03.000
Hello, and welcome to our video!

0:00:04.000,0:00:06.000
In this video, we will be discussing the SBV file format.

0:00:07.000,0:00:10.000
The SBV format is commonly used for storing subtitles for videos.
```

ניתן ליצור ולערוך קבצי SBV עם מגוון תוכנות לעריכת כתוביות, כגון Subtitle Workshop, Aegisub או Subtitle Edit. לאחר השלמת הכתוביות, ניתן לייבא את קובץ ה-SBV לתוכנית עריכת וידאו כדי ליצור סרטון עם כתוביות. בסך הכל, פורמט הקובץ SBV הוא פורמט פשוט ונפוץ לאחסון כתוביות התואם לתוכניות ונגנים רבים לעריכת וידאו.

## איך פותחים קובץ SBV?

קבצי SBV הם קבצי טקסט כך שתוכל לפתוח אותם באמצעות כל עורך טקסט, למשל Notepad או Notepad++

## הפניות
* [SubViewer](https://wiki.videolan.org/SubViewer/)
