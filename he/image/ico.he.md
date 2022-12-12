{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ ico", "פורמט קובץ ico", "מהו קובץ ico", "קובץ", "דוגמה ל-ico", "סיומת קובץ ico", "סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - פורמט קובץ תמונה",
  "description":"למד על פורמט קבצי ICO וממשקי API שיכולים ליצור ולפתוח קובצי ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ ICO?

קבצים עם סיומת ICO הם סוגי קבצי תמונה המשמשים כסמל לייצוג של יישום ב-[Microsoft Windows](https://www.microsoft.com/en-us/windows). אלה מגיעים בגדלים שונים, תמיכה בצבע וברזולוציה כדי להתאים לדרישות התצוגה. פורמט קובץ תמונה דומה נוסף ב-Microsoft Windows הוא [CUR](/he/image/cur/) עבור ייצוג הסמן ומגדיר נקודה חמה בכותרת התמונה. ב-MacOS, פורמטים של קבצי ICNS משרתים את אותה מטרה כמו קבצי ICO. מספר אתרים מקוונים כמו גם יישומים מספקים את התכונה של יצירת קבצים כאלה וממירים פורמטים אחרים של תמונה כגון [BMP](/he/image/bmp/), [PNG](/he/image/png/) וכו' לפורמט קובץ אייקונים. סוג המדיה הרשמי של IANA באינטרנט עבור קבצי ICO הוא image/vnd.microsoft.icon.

## היסטוריה קצרה ##

סמלים הוצגו עם השקת Microsoft Windows 1.0. אלה היו בגודל 32x32 והיו מונוכרום. עם ההגעה ל-win32, הוצגה תמיכה בתמונות אייקונים בצבע אמיתי עם מימד של עד 256x256 פיקסלים. Windows XP הייתה הראשונה שסיפקה תמיכה בתמונות של סמלים צבעוניים של 32 סיביות, המאפשרת להוסיף לסמל אזורים שקופים למחצה כמו צללים, אנטי-aliasing ואפקטים דמויי זכוכית. Microsoft המליצה רק על גדלים של סמלים של עד 48×48 פיקסלים עבור Windows XP. Windows Vista הוסיפה תצוגת סמל של 256×256 פיקסלים לסייר Windows, כמו גם תמיכה בפורמט דחוס [PNG](/he/image/png/). עם משתמשים שמשתמשים ברזולוציות גבוהות יותר ובמצבי DPI גבוהים, מומלצים פורמטים גדולים יותר של סמלים (כגון 256×256).

## פורמט קובץ ICO ##

קובץ ICO בודד מורכב מתמונה קטנה אחת או יותר בגדלים מרובים ובעומקי צבע. הנוכחות של תמונות בגדלים מרובים מיועדת לשינוי קנה מידה מתאים ברזולוציות מסך שונות. כל הערכים בקובצי ICO/CUR מיוצגים בסדר בתים [little-endian](https://en.wikipedia.org/wiki/Little-endian).

קובץ ה-ICO מורכב מכותרת אייקון, ספריית אייקונים,

|שדה|תיאור
---|---|
|Icon Header|מאחסן מידע כללי על קובץ ה-ICO.
|Directory[1..n]|מאחסן מידע כללי על כל תמונה בקובץ.
|אייקון #1|ה"נתונים" בפועל עבור התמונה הראשונה בפורמט AND/XOR DIB ישן או PNG חדש יותר
|...|
|אייקון #n|נתונים עבור תמונת הסמל האחרונה

### כותרת ###

|היסט|גודל (בבתים)|מטרה
---|---|---|
|0|2|שמור. חייב להיות תמיד 0.
|2|2|מציין סוג תמונה: 1 עבור תמונת סמל (.ICO), 2 עבור תמונת סמן (.CUR). ערכים אחרים אינם חוקיים.
|4|2|מציין את מספר התמונות בקובץ.

### ספרייה ###

הספרייה הכלולה בקובץ ICO, המיוצגת כמבנה ICONDIR, מכילה מבנה ICONDIRECTORY עבור כל תמונה בקובץ. אותו הדבר מלווה בלוק רציף של כל נתוני ה-bitmap של התמונה. זה כפי שמוצג להלן.

|היסט|גודל|תיאור
---|---|---|
|0 (0)|1|רוחב, צריך להיות 0 אם 256 פיקסלים
|1 (1)|1|גובה, צריך להיות 0 אם 256 פיקסלים
|2 (2)|1|ספירת צבעים, צריכה להיות 0 אם יותר מ-256 צבעים
|3 (3)|1|שמור, צריך להיות 0
|4 (4)|2|מישורי צבע בפורמט .ICO, צריכים להיות 0 או 1, או הנקודה חמה X בפורמט .CUR
|6 (6)|2|סיביות לפיקסל בפורמט .ICO, או נקודת Y בפורמט .CUR
|8 (8)|4|גודל נתוני מפת הסיביות בבתים.
|12 (C)|4|היסט בקובץ.

## הפניות ##

* [ICO - מאת ויקיפדיה](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)
