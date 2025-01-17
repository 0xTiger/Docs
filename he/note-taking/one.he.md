{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Microsoft OneNote Format File",
  "description":"למד על פורמט קובץ ONE וממשקי API שיכולים ליצור ולפתוח קבצי ONE.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ ONE? ##

קבצים המיוצגים על ידי סיומת ONE נוצרים על ידי יישום Microsoft OneNote. OneNote מאפשר לך לאסוף מידע באמצעות היישום כאילו אתה משתמש בפנקס הטיוטה שלך לרישום הערות. קבצי OneNote יכולים להכיל אלמנטים שונים שניתן למקם במקומות לא קבועים בדפי מסמכים. אלמנטים אלה עשויים להכיל טקסט, כתב יד דיגיטאלי ואובייקטים שהועתקו מיישומים אחרים, כולל תמונות, ציורים וקטעי מולטימדיה (אודיו/וידאו). מיקרוסופט מציעה כעת גרסה מקוונת של OneNote כחלק מ-Office365 שבה ניתן לשתף הערות עם משתמשי OneNote אחרים דרך האינטרנט.

## מפרטי פורמט קובץ .ONE ##

פורמט הקובץ OneNote מספק דרך יעילה לייצוג הערות דיגיטליות כקבוצות היררכיות של מקטעים ודפים. כל עמוד מכיל תוכן מוגדר על ידי משתמש במבנה ספציפי לייצוג על ידי פורמט הקובץ Document Object Model (DOM). מודל הנתונים של פורמט זה הוא כמתואר להלן.

### סקירת מבנה ###

כפי שמודגם במודל הנתונים עבור פורמט קובץ OneNote, מסמך OneNote מורכב מאלמנטים שונים.

#### סעיף ####

קטע הוא המיכל העליון ביותר בקובץ OneNote שמכיל עוד אלמנטים שונים כמו:

* דפים
* מטא נתונים
* נכסים

מטא נתונים ומאפיינים כוללים את שם המדור, זיהוי הדפים הכלולים במדור והסדר שבו מופיעים דפים אלו. המונח "מקטע" מתייחס לכל הדפים שנמצאים במקטע ולייצוג של נתונים אלה בקובץ מאגר גרסאות של OneNote®, בעל סיומת שם קובץ .one.

#### עמוד ####

תוכן מוגדר על ידי משתמש במסמך OneNote כלול בתוך עמוד. מידע העמוד כולל טקסט, רשימות, טבלאות, כותרות עמודים, תמונות ותגי הערות. עמוד מורכב מאובייקטי מתאר שאליהם מתווספים רוב האובייקטים הכלולים. לכל עמוד ניתן להקצות שם לייצוג משמעותי וניתן להוסיף אובייקטים ישירות לדפים גם כן. עמוד יכול להכיל עוד דפי משנה במערכת היררכית.

#### מאפיינים וערכות נכסים ####

תוכן OneNote מורכב ממאפיינים, מערכי מאפיינים ואובייקטי נתוני קבצים. ערכת מאפיינים היא אוסף של מאפיינים המייצגים סוג כלשהו של תוכן. אובייקט נתוני קובץ הוא בלוק של נתונים בינאריים המכיל תמונות, קבצים משובצים או תוכן אודיו/וידאו.

#### מחברת OneNote ####

מחברת היא אוסף של קבצי מקטעים המאוחסנים באותה ספרייה. אוסף של מאפיינים משמש לציון הגדרות כגון סדר הסעיפים בתוך המחברת וצבע המחברת.

### מבנה הקובץ ###

קובץ מאגר גרסאות חייב להתחיל במבנה **Header**. שאר הקובץ מחולק לקוביות של בתים, כאשר הגודל והמבנה של כל בלוק מוגדרים על ידי השדה שמפנה אליו. ניתן להגיע לבלוק אם הוא מופנה על ידי מבנה **Header**, או אם מפנה אליו שדה בבלוק אחר שניתן להגיע אליו. יש להתעלם מנתונים מחוץ למבנה **Header** וכל בלוקים שניתן להגיע אליהם.

כל המבנים מיושרים על גבולות של 1 בייט. כל המספרים השלמים חתומים אלא אם צוין אחרת. כל השדות הם [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) אלא אם צוין אחרת.

#### כותרת ####

הכותרת של קובץ ONE מורכבת מנתחים המכילים מזהים ושדות ייחודיים שונים לייצוג מידע קובץ כדלקמן:

`guidFileType (16 בתים):` GUID המציין את סוג קובץ מאגר הגרסאות. חייב להיות אחד מהערכים מהטבלה הבאה.


|פורמט קובץ|ערך
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 בתים):` GUID המציין את הזהות של קובץ מאגר גרסאות זה. צריך להיות ייחודי בעולם.

`guidLegacyFileVersion (16 בתים):` חייב להיות "{00000000-0000-0000-0000-0000000000000}" ויש להתעלם ממנו.

`guidFileFormat (16 בתים):` GUID המציין שהקובץ הוא קובץ מאגר גרסאות. חייב להיות "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 בתים):` מספר שלם ללא סימן. חייב להיות אחד מהערכים בטבלה הבאה, בהתאם לסוג הקובץ.

|פורמט קובץ|ערך
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHaswrittenToThisFile (4 בתים):` מספר שלם ללא סימן. חייב להיות אחד מהערכים בטבלה הבאה, בהתאם לפורמט הקובץ של קובץ זה.


|פורמט קובץ|ערך
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 בתים):` מספר שלם ללא סימן. חייב להיות אחד מהערכים בטבלה הבאה, בהתאם לפורמט הקובץ של קובץ זה.

|פורמט קובץ|ערך
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 בתים):` מספר שלם ללא סימן. חייב להיות אחד מהערכים בטבלה הבאה, בהתאם לפורמט הקובץ של קובץ זה.

|פורמט קובץ|ערך
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 בתים):` מבנה **FileChunkReference32** שחייב להיות בעל ערך של "fcrZero".

`fcrLegacyTransactionLog (8 בתים):` מבנה **FileChunkReference32** שחייב להיות "fcrNil".

`cTransactionsInLog (4 בתים):` מספר שלם ללא סימן המציין את מספר העסקאות ביומן העסקאות. אסור להיות אפס.

`cbLegacyExpectedFileLength (4 בתים):` מספר שלם ללא סימן שחייב להיות אפס ויש להתעלם ממנו.

`rgbPlaceholder (8 בתים):` מספר שלם ללא סימן שחייב להיות אפס ויש להתעלם ממנו.

`fcrLegacyFileNodeListRoot (8 בתים):` מבנה **FileChunkReference32** שחייב להיות "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 בתים):` מספר שלם ללא סימן שחייב להיות אפס וחייב להתעלם ממנו.

`fNeedsDefrag (1 בייט):` יש להתעלם.

`fRepairedFile (1 בייט):` יש להתעלם.

`fNeedsGarbageCollect (1 בייט):` יש להתעלם.

`fHasNoEmbeddedFileObjects (1 בייט):` מספר שלם ללא סימן שחייב להיות אפס, ויש להתעלם ממנו.

`guidAncestor (16 בתים):` GUID המציין את השדה **Header.guidFile** של קובץ תוכן העניינים, שניתן על ידי הטבלה הבאה:


|פורמט תוכן קובץ|מיקום קובץ תוכן עניינים
--- | --- |
קובץ |Section File - .One|קובץ תוכן עניינים ממוקם באותה ספרייה של קובץ זה.
|קובץ תוכן עניינים - .onetoc2|קובץ תוכן העניינים ממוקם בספריית האב של קובץ זה.

אם ה-GUID הוא {00000000-0000-0000-0000-000000000000}, שדה זה אינו מפנה לקובץ תוכן עניינים.

`crcName (4 בתים):` מספר שלם ללא סימן המציין את ערך ה-CRC של השם של קובץ מאגר גרסאות זה. השם הוא ייצוג Unicode של שם הקובץ עם הסיומת שלו ותו ריק נוסף בסוף. CRC זה מחושב תמיד באמצעות אלגוריתם CRC עבור קובץ .one, ללא קשר לפורמט הקובץ של חנות הגרסאות הזו.

`fcrHashedChunkList (12 בתים):` מבנה **FileChunkReference64x32** המציין הפניה ל-**FileNodeListFragment** הראשון ברשימת נתחים מגובבים. אם הערך של המבנה **FileChunkReference64x32** הוא "fcrZero" או "fcrNil", רשימת הגיבובים לא קיימת.

`fcrTransactionLog (12 בתים):` מבנה **FileChunkReference64x32** המציין הפניה למבנה **TransactionLogFragment** הראשון ביומן עסקאות. הערך של השדה **fcrTransactionLog** לא חייב להיות "fcrZero" ואסור להיות "fcrNil".

`fcrFileNodeListRoot (12 בתים):` מבנה **FileChunkReference64x32** המציין הפניה לרשימת צמתים של קובץ שורש. הערך של השדה **fcrFileNodeListRoot** לא חייב להיות "fcrZero" ואסור להיות "fcrNil".

`fcrFreeChunkList (12 בתים):` מבנה **FileChunkReference64x32** המציין הפניה למבנה **FreeChunkListFragment** הראשון. אם הערך של המבנה **FileChunkReference64x32** הוא "fcrZero" או "fcrNil", אז רשימת הנתחים החופשיים לא קיימת.

`cbExpectedFileLength (8 בתים):` מספר שלם ללא סימן המציין את הגודל, בבתים, של קובץ מאגר גרסאות זה.

`cbFreeSpaceInFreeChunkList (8 בתים):` מספר שלם ללא סימן שאמור לציין את הגודל, בבתים, של השטח הפנוי שצוין ברשימת הנתחים הפנויים.

`guidFileVersion (16 בתים):` GUID. כאשר הערך של השדה **cTransactionsInLog** או השדה **guidDenyReadFileVersion** משתנים, יש לשנות את **guidFileVersion** ל-GUID חדש.

`nFileVersionGeneration (8 בתים):` מספר שלם ללא סימן המציין את מספר הפעמים שהקובץ השתנה. יש להגדיל כאשר השדה **guidFileVersion** משתנה.

`guidDenyReadFileVersion (16 בתים):` GUID. כאשר התוכן הקיים של הקובץ משתנה, למעט מבנה **Header** של הקובץ ובלוקי אחסון שאינם בשימוש, יש לשנות את **guidDenyReadFileVersion** ל-GUID חדש.

`grfDebugLogFlags (4 בתים):` חייב להיות אפס. יש להתעלם.

`fcrDebugLog (12 בתים):` מבנה **FileChunkReference64x32** שחייב להיות בעל ערך "fcrZero". יש להתעלם.

`fcrAllocVerificationFreeChunkList (12 בתים):` מבנה **FileChunkReference64x32** שחייב להיות "fcrZero". יש להתעלם.

`bnCreated (4 בתים):` מספר שלם ללא סימן המציין את מספר ה-build של האפליקציה שיצרה קובץ מאגר גרסאות זה. יש להתעלם.

`bnLastWroteToThisFile (4 בתים):` מספר שלם ללא סימן המציין את מספר ה-build של האפליקציה שכתבה לאחרונה לקובץ מאגר גרסאות זה. יש להתעלם.

`bnOldestWritten (4 בתים):` מספר שלם ללא סימן המציין את מספר ה-build של היישום הישן ביותר שכתב לקובץ מאגר גרסאות זה. יש להתעלם.

`bnNewestWritten (4 בתים):` מספר שלם ללא סימן המציין את מספר ה-build של היישום החדש ביותר שכתב לקובץ מאגר גרסאות זה. יש להתעלם.

`rgbReserved (728 בתים):` חייב להיות אפס. יש להתעלם.

## הפניות ##

* [[MS-ONESTORE] - פורמט קובץ OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - ויקיפדיה](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

