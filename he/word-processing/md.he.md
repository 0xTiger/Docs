{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ md", "פורמט קובץ md", "מהו קובץ md", "קובץ", "דוגמה ל-md", "סיומת קובץ md","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - MarkDown Language File",
  "description":"למד על פורמט קובץ MD וממשקי API שיכולים ליצור ולפתוח קבצי MD.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ MD?

קבצי טקסט שנוצרו עם דיאלקטים בשפת Markdown נשמרים עם סיומת הקובץ **.md** או **.MARKDOWN**. קבצי MD נשמרים בפורמט טקסט רגיל המשתמש בשפת Markdown הכוללת גם סמלי טקסט מוטבעים, המגדירים כיצד ניתן לעצב טקסט כגון הזחה, עיצוב טבלה, גופנים וכותרות. ניתן להמיר קבצי MD ל-HTML באמצעות תוכנה בשם Markdown. שפת Markdown שוחררה על ידי ג'ון גרובר.

קבצי MD יכולים גם להיות מסווגים כקבצי מפתחים המשמשים בעיקר את Markdown, להמרת קבצי טקסט לגרסאות HTML כך שמשתמשים יכולים ליצור קבצים שקל לקרוא ולכתוב. להלן היישומים שיכולים לפתוח קובץ .md:

* פנקס רשימות של מיקרוסופט
*פנקס רשימות2
* עריכת טקסט של אפל
* Microsoft WordPad

מילה של זהירות היא שלא תשנה את שם הסיומת של קבצי .md. אם כן זה לא ישנה את סוג הקובץ מכיוון שקיימות תוכנות המרה מיוחדות לשינוי קובץ מסוג אחד לאחר. כפי שנדון לעיל קבצי MD הם הסיומות של קבצים שנוצרו בתוכנת שפת Markdown. **Markdown** היא [שפת סימון קלה](https://en.wikipedia.org/wiki/Lightweight_markup_language) המיועדת למטרה אחת, לשמש לעיצוב טקסט באינטרנט עם תחביר עיצוב טקסט רגיל. שיהיה ברור ש-Markdown אינו תחליף ל-HTML מכיוון שהתחביר שלו קטן מאוד, מכיל תת-קבוצה קטנה מאוד של תגי HTML. הסיבה מאחורי ה-Markdown היא להקל על הקריאה, הכתיבה והעריכה של פרוזה. במילים אחרות אנו יכולים לומר ש-HTML הוא פורמט פרסום בעוד Markdown הוא פורמט כתיבה.

Markdown היא כעת אחת משפות הסימון הפופולריות בעולם. בזמן השימוש ב-Microsoft Word, עיצוב מילים וביטויים מתבצע באמצעות לחיצה על כפתורים והשינויים גלויים מיד. אבל Markdown הוא לא כזה. כאשר נוצר קובץ בפורמט Markdown, תחביר Markdown מתווסף לטקסט כדי לציין אילו מילים וביטויים עשויים להיראות שונים. לדוגמה, כדי להציג כותרת, נוסף סימן מספר לפניה (למשל # Heading One). ליצירת משפט מודגש, שתי כוכביות מתווספות לפניו ואחריו (למשל, **טקסט זה מודגש**). ניתן לראות תחביר Markdown לאחר זמן בטקסט.

## היסטוריה קצרה

ג'ון גרובר ואהרון שוורץ ב-2004 יצרו את שפת Markdown מתוך רעיון לאפשר לאנשים "לכתוב באמצעות פורמט קל לקריאה ולכתיבה של טקסט רגיל ועם אפשרות להמיר אותו ל-XHTML או HTML. המטרה מאחורי העיצוב שלו היא קריאה - השפה ניתנת לקריאה כפי שהיא, מבלי להיראות כאילו תויגה או נוספה עם הוראות עיצוב כפי שנעשה בשפות סימון כמו RTF או HTML שבהן תגיות והוראות עיצוב ברורות. ההשראה הבסיסית היא שימוש במוסכמות קיימות לסימון טקסט רגיל בדוא"ל.

מאז Markdown הוטמע מחדש על ידי אחרים, כמו גם ב-Perl [מודול](https://en.wikipedia.org/wiki/Modular_programming) הזמין ב-[CPAN](https://en.wikipedia.org/wiki/CPAN) ובשפות תכנות שונות אחרות. הוא מופץ תחת [רישיון בסגנון BSD](https://en.wikipedia.org/wiki/BSD_license) והוא כלול או זמין כפלאגין עבור מספר [מערכות ניהול תוכן](https://en.wikipedia.org/wiki/Content_management_system).

## מפרט טכני

כאשר משהו נכתב ב-Markdown, הטקסט מאוחסן תחילה בקובץ טקסט רגיל עם סיומת של .md או .markdown, ולאחר מכן יישום Markdown כגון Dillinger משמש לעיבוד קובץ Markdown כדי להמיר טקסט בפורמט Markdown ל-HTML לצורך הצגתו באינטרנט דפדפנים. יישומי Markdown משתמשים במעבד //Markdown// (המכונה גם "מנתח" או "יישום") כדי לקחת את הטקסט המעוצב ב-Markdown ולהוציא אותו לפורמט HTML. תרשים הזרימה של התהליך הוא כדלקמן:

בקיצור זה תהליך בן ארבעה שלבים כדלקמן:

1. ראשית, יצירת קבצי Markdown עם עורך טקסט או יישום Markdown עם סיומת .md או .markdown.
1. לאחר מכן קובץ Markdown נפתח ביישום Markdown.
1. אפליקציית Markdown משמשת להמרת קובץ Markdown למסמך HTML.
1. לאחר מכן מוצג קובץ HTML בדפדפן אינטרנט או ביישום Markdown משמש להמרתו לפורמט קובץ אחר, כמו PDF.

Markdown מהיר וקל לרשום הערות, כתיבת תוכן לאתר, הפקת מסמכים מוכנים להדפסה, להוצאת ספרים, הפקת מצגות והכנת מסמכים.

לחלק מהגרסאות ב-Markdown הייתה השפעה מהותית על גרסאות אחרות עד כדי כך שלעתים קרובות ניתן לראות אותן מצוטטות כחלק מגרסאות אחרות. לדוגמה, ספריות מזכירות תמיכה ב-CommonMark (GFM). בואו נסתכל בקצרה על אלה.

### GFM
Markdown כל כך פופולרי בקרב מפתחים מכיוון שפלטפורמת שיתוף הקוד הפתוח Github קיבלה והרחיבה את השפה עם גרסה בשם Github Flavored Markup (GFM) הכוללת חסימות קוד מגודרות, aultolinking של כתובות אתרים, קו חוצה, טבלאות ויצירת מטלות.

### CommonMark
מפתחי Markdown ניסו לאחרונה לתקן את Markdown, הם חברו יחד כדי ליצור גרסה, בדיקות ותיעוד לשפה שהיא חזקה יותר ונקראת CommonMark. פורמט זה מעט חדש ואינו תומך בהרבה תכונות, אך בקרוב יתווספו תכונות רבות של MultiMarkdown.

### ריבוי סימון
Multi-Markdown הוסיפה תכונות שונות לשפה הנתמכות על ידי גרסאות אחרות. במקור הוא נכתב ב-Perl, אך מאוחר יותר עבר ל-C. הוא תומך בחסימות קוד מגודרות, הדגשת תחביר, טבלאות, מטא נתונים, קישורי קטעים/הפניות צולבות, הערות שוליים, קו חוצה, רשימות הגדרות, מתמטיקה.

## הפניות

* [Mastering MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

