{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ wmf", "פורמט קובץ wmf", "מהו קובץ wmf", "קובץ", "דוגמה ל-wmf", "סיומת קובץ wmf","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows Metafile Format",
  "description":"למד על פורמט קובץ WMF וממשקי API שיכולים ליצור ולפתוח קובצי WMF.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ WMF?

קבצים עם סיומת WMF מייצגים את Microsoft Windows Metafile (WMF) לאחסון נתוני תמונות וקטורים כמו גם בפורמט סיביות. ליתר דיוק, WMF שייך לקטגוריית פורמט קבצים וקטור של פורמטים של קבצי גרפיקה שאינה תלויה במכשיר. ממשק התקן גרפי של Windows (GDI) משתמש בפונקציות המאוחסנות בקובץ WMF כדי להציג תמונה על המסך. מאוחר יותר פורסמה גרסה משופרת יותר של WMF, הידועה בשם Enhanced Meta Files (EMF), שהופכת את הפורמט לעשיר יותר בתכונות. למעשה, WMF דומים ל-SVG.

## מפרטי פורמט קובץ WMF ##

קובץ WMF התייחס לפורמט קובץ של 16 סיביות בזמן השקתו עם Windows 3.0. פורמט הקובץ מורכב מסדרה של רשומות באורך משתנה המכילות פקודות ציור גרפיות, הגדרות אובייקט ומאפיינים. מכיוון שקובצי WMF מבוססים על פקודות שניתנו ל-GDI לצורך ציור התמונה, היא ידועה גם כהקלטה דיגיטלית של התמונה שניתן להפעיל אותה כדי לשחזר את התמונה. מפרטי פורמט הקובץ המלאים של WMF זמינים באינטרנט ויש להפנות אותם לפיתוח יישומים לעבודה עם קבצי WMF. קובץ WMF מאורגן ל:

* שיא כותרת WMF
* רשומות WMF
* שיא סוף קובץ WMF

### שיא כותרת WMF ###

הרשומה **META_HEADER** מכילה מידע המגדיר את המאפיינים של המטא-קובץ, כולל:

* סוג המטא-קובץ
* הגרסה של המטא-קובץ
* גודל המטאפיל
* מספר האובייקטים המוגדרים במטא-קובץ
* גודל הרשומה הגדולה ביותר במטא-קובץ

### רשומת כותרת ניתנת להצבה של WMF ###

הרשומה **META_PLACEABLE** מכילה מידע מורחב בנוגע לתמונה, כולל:

* מלבן תוחם
* גודל יחידה לוגי, לשינוי קנה מידה
* סכום בדיקה, לאימות

### שיא WMF ###

לרשומות WMF יש פורמט גנרי, המצוין במסמך המפרטים. כל רשומת WMF מכילה את המידע הבא:

* גודל השיא
* פונקציית ההקלטה
* פרמטרים, אם יש, עבור פונקציית הרשומה

## הפניות ##

* [[MS-WMF]: פורמט Windows Metafile](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile - ויקיפדיה](https://en.wikipedia.org/wiki/Windows_Metafile)
