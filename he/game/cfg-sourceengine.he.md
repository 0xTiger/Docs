{
"date": "2023-09-27",
  "keywords": [
"cfg",
"קובץ cfg",
"קובץ תצורת מנוע מקור cfg",
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
"title": "פורמט קובץ CFG - קובץ תצורת מנוע מקור",
  "description":"למד על פורמט קובץ תצורת מנוע מקור CFG וממשקי API שיכולים ליצור ולפתוח קובצי CFG.",
  "linktitle": "CFG Source Engine",
  "menu": {
    "docs": {
      "identifier": "game-cfg-sourceengine",
      "parent": "game"
}
},
"lastmod": "2023-09-27"
}

## מהו קובץ CFG?

קובץ CFG בהקשר של **Valve's Source Engine**, כפי שניתן לראות במשחקים כמו Half-Life 2, משמש כקובץ תצורה. קבצים אלה משמשים לשינוי הגדרות שונות במשחק באמצעות רשימה של פקודות טקסט רגיל. פקודות אלה מסודרות בדרך כלל עם אחת בכל שורה ואחראיות להתאמה אישית של היבטים של המשחק.

לשחקנים ולמנהלי שרתים יש כמה אפשרויות להחלת שינויים שצוינו בקובץ `.cfg`:

1. **ביצוע ידני**: משתמשים יכולים לבצע פקודות באופן ידני בתוך קובץ CFG. המשמעות היא שהם מכניסים כל פקודה אחת לאחת בקונסולת המפתחים של המשחק. שיטה זו מאפשרת שליטה מדויקת על אילו הגדרות משתנות ומתי.
    





2. **ביצוע אוטומטי**: לחלופין, שחקנים יכולים לבחור בביצוע אוטומטי. זה כרוך בהצבת קובץ `.cfg` בספריית המשחק המתאימה. קבצי `.cfg` מסוימים, כמו `autoexec.cfg`, מופעלים אוטומטית עם תחילת המשחק. זה מבטיח שההגדרות שצוינו מיושמות מבלי לדרוש קלט ידני בכל פעם שהמשחק מופעל.

## מנוע מקור השסתום

מנוע מקור ה-Valve, המכונה לעתים קרובות בפשטות כ-**Source Engine**, הוא מנוע משחק רב תכליתי ונפוץ שפותח על ידי Valve Corporation. זה היווה בסיס למשחקי וידאו פופולריים רבים והניע כותרים מצליחים רבים. הנה כמה נקודות מפתח לגבי מנוע מקור שסתום:

1. **היסטוריה**: מנוע המקור הוצג לראשונה עם יציאת המשחק של Valve "Counter-Strike 1.6" בשנת 2004. מאז הוא עבר מספר עדכונים ותיקונים, כאשר הגרסה האחרונה ידועה בשם Source 2.0.
    





2. **משחקים בולטים**: מנוע המקור נוצל במגוון משחקים שזכו לשבחים, כולל אך לא מוגבל ל:
    





- "Half-Life 2" והפרקים שלו
- "פורטל" ו"פורטל 2"
- "טים פורטרס 2"
- "Left 4 Dead" ו-"Left 4 Dead 2"
- "Counter-Strike: Source" ו-"Counter-Strike: Global Offensive"
- "דוטה 2"
3. **תכונות**:
    





- **גמישות**: Source Engine ידועה בגמישותו המאפשרת למפתחים ליצור מגוון רחב של ז'אנרים של משחקים, החל ממשחקי יריות מגוף ראשון ועד למשחקי פאזל ועוד.
- **פיזיקה**: זה כולל מנוע פיזיקה חזק המאפשר אינטראקציות אובייקט מציאותיות והשפעות סביבתיות.
- **תמיכה במודינג**: למנוע יש תמיכת מודינג חזקה שהובילה ליצירת תוכן ומשחקים רבים שנוצרו על ידי משתמשים.
- **יכולות מרובה משתתפים**: מנוע המקור שימש לפיתוח משחקים לשחקן יחיד ומשחקים מרובי משתתפים, והוא מציע יכולות רשת נרחבות למשחק מקוון.
    





4. **גרפיקה**: במשך שנים קיבלה Source Engine עדכונים גרפיים כדי לעמוד בקצב של יכולות החומרה המתפתחות. הוא תומך בטכניקות עיבוד מתקדמות כמו תאורת HDR (High Dynamic Range) וצללים דינמיים.

## איך פותחים קובץ CFG?

יש לך אפשרות לפתוח ולשנות קובץ `.cfg` באמצעות עורכי טקסט כמו Microsoft Visual Studio Code או כל עורך טקסט אחר לבחירתך. עורכי טקסט אלו מספקים ממשק ידידותי למשתמש לצפייה ועריכה של פקודות טקסט רגיל בתוך קובץ `.cfg` המאפשר לך להתאים אישית הגדרות לפי הצורך.

תוכניות הפותחות או הפניות לקובצי CFG כוללות

- Microsoft Visual Studio Code
- פנקס רשימות
- עריכת טקסט
- כל עורך טקסט

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
* [מקור (מנוע משחק)](https://en.wikipedia.org/wiki/Source_(game_engine))
